# 🔐 Plano de Segurança da Informação

Plano pensado para o cenário em que o jogo (ou parte dele) seja **alocado em um
servidor/cliente** — por exemplo, uma versão web, downloads ou um backend de
placar/progresso. Hoje o jogo é offline, então boa parte é **preventiva**.

## 🧭 Framework norteador: OWASP + ISO/IEC 27001 + STRIDE

- **OWASP** (Top 10 / ASVS) — riscos e controles para aplicações web/API.
- **ISO/IEC 27001** — gestão de segurança (confidencialidade, integridade,
  disponibilidade — a tríade CIA).
- **STRIDE** — modelagem de ameaças (Spoofing, Tampering, Repudiation,
  Information disclosure, Denial of service, Elevation of privilege).

---

## 🎯 Princípio central: privacidade de menores
O público são **crianças**. Por **LGPD** e **ECA**, a diretriz é:
- **Não coletar dados pessoais** de menores (privacy by design / data minimization).
- Se houver placar/progresso, usar **apelido anônimo**, sem nome real, e-mail
  ou foto; **consentimento do responsável** quando aplicável.

---

## 🧨 Modelagem de ameaças (STRIDE) — cenário com servidor

| Ameaça | Exemplo | Mitigação |
|---|---|---|
| **Spoofing** | Falsificar identidade no placar | Tokens/sessões; apelidos sem login pessoal |
| **Tampering** | Alterar pontuação/arquivos | Validação no servidor; assinaturas/checksums |
| **Repudiation** | Negar uma ação | Logs de auditoria |
| **Info disclosure** | Vazar dados | HTTPS/TLS; mínimo de dados; criptografia |
| **DoS** | Derrubar o serviço | Rate limiting; WAF; auto-scaling |
| **Elevation** | Ganhar privilégios | Princípio do menor privilégio; revisão de acesso |

---

## 🛡️ Controles por camada

### Distribuição do executável (cenário atual)
- Disponibilizar **hash (SHA-256)** dos binários para verificação.
- **Assinar** o executável quando possível (evita "editor desconhecido").
- Manter a **Raylib atualizada** (dependência) e revisar avisos do compilador.

### Versão web / backend (cenário futuro)
- **HTTPS/TLS** obrigatório; sem dados sensíveis na URL.
- **Validação de entrada** e respostas no servidor (não confiar no cliente).
- **Rate limiting** e **CORS** restrito; cabeçalhos de segurança (CSP).
- **Segredos** em cofre (variáveis de ambiente), nunca no repositório.
- **Backups** e **logs**; plano de resposta a incidentes.
- Conferir o **OWASP Top 10** (injeção, autenticação, etc.).

---

## 🔁 Tríade CIA (ISO 27001)
- **Confidencialidade:** coletar o mínimo; criptografar o que for sensível.
- **Integridade:** validar pontuações/progresso no servidor; checksums.
- **Disponibilidade:** hospedagem com escala e backups.

## ✅ Checklist
- [ ] Mapa de dados (o que é coletado? idealmente **nada pessoal**)
- [ ] Conformidade **LGPD/ECA** documentada
- [ ] Modelagem STRIDE concluída
- [ ] Hash/assinatura dos binários
- [ ] (Se houver backend) HTTPS, validação, rate limiting, segredos protegidos
- [ ] Plano de resposta a incidentes
