# 🔎 Elicitação de Requisitos

Levantamento e organização dos requisitos: **5W2H**, **público-alvo**,
**stakeholders** e **custo computacional**.

## 🧭 Framework norteador: 5W2H + MoSCoW + BABOK

- **5W2H** — estrutura clara para descrever o problema/solução em 7 perguntas.
- **MoSCoW** — classifica requisitos em **Must / Should / Could / Won't**, dando
  prioridade objetiva.
- **BABOK** (referência) — boas práticas de análise de negócio para validar e
  rastrear requisitos.

---

## 🧩 5W2H

| Pergunta | Resposta |
|---|---|
| **What** (O quê) | Um jogo educativo digital sobre o trabalho do CBMDF e prevenção em emergências. |
| **Why** (Por quê) | Ensinar crianças a agir corretamente em emergências, conhecer os bombeiros e despertar interesse pela profissão. |
| **Who** (Quem) | **Equipe:** alunos do projeto. **Usuários:** crianças de 6–12 anos. **Apoio:** professores e CBMDF. |
| **Where** (Onde) | Escolas e residências do DF; computadores desktop (futuro: navegador). |
| **When** (Quando) | Durante a disciplina (definir cronograma/sprints e data de entrega). |
| **How** (Como) | Em **C + Raylib**, pixel-art, 10 fases + museu, com minigames e quizzes. |
| **How much** (Quanto) | **Financeiro:** ~R$0 (ferramentas livres). **Computacional:** baixo (ver abaixo). |

---

## 👥 Público-alvo

- **Primário:** crianças de **6 a 12 anos**.
- **Secundário:** professores e educadores (uso em sala).
- **Terciário:** responsáveis e adolescentes (em campanhas de prevenção).

Características: leitores iniciantes/intermediários → priorizar **textos curtos,
ícones e cores**; sessões curtas; reforço positivo.

---

## 🤝 Stakeholders

| Stakeholder | Interesse | Influência |
|---|---|---|
| Equipe de desenvolvimento (alunos) | Entregar e ser avaliada | Alta |
| Professor/orientador | Qualidade técnica e didática | Alta |
| Crianças (jogadoras) | Diversão + aprendizado | Média (usuário final) |
| Professores das escolas | Ferramenta pedagógica confiável | Média |
| Responsáveis | Segurança e conteúdo adequado | Média |
| **CBMDF** | Imagem institucional e prevenção | Alta (validação) |
| Secretarias de Educação/Segurança | Alcance social | Baixa/Média |

---

## ✅ Requisitos (MoSCoW — exemplos)

**Must:** menu, 10 fases jogáveis, ensino do 193, tela de conclusão, acessível offline.
**Should:** save de progresso, áudio/narração, acessibilidade (contraste/fonte).
**Could:** versão web, placar, conquistas extras, idiomas.
**Won't (agora):** multiplayer online, cadastro de usuários.

### Requisitos não funcionais
- Rodar a **60 FPS** em hardware básico; iniciar em poucos segundos.
- **Não coletar dados pessoais** de menores (privacidade desde o projeto).
- Texto em **UTF-8**; legibilidade para crianças.

---

## 💻 Custo computacional

| Recurso | Estimativa |
|---|---|
| **CPU** | Modesta (dual-core); lógica leve por quadro |
| **GPU** | Não exige dedicada (Raylib/OpenGL básico) |
| **Memória** | Poucas dezenas de MB |
| **Armazenamento** | Executável pequeno (poucos MB) |
| **Rede** | **Nenhuma** (jogo offline) |
| **Desempenho** | 60 FPS estáveis em PCs simples |
| **Build** | Compilação rápida em um único arquivo `.c` |

> O baixo custo computacional é um diferencial: roda em laboratórios escolares
> com máquinas antigas.
