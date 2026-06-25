# 📚 Heróis do DF: Missão Bombeiro — Documentação do Produto

Repositório de **artefatos e documentação** do projeto **Heróis do DF: Missão
Bombeiro** — um jogo educativo (C/Raylib) que ensina crianças de 6 a 12 anos
sobre o **Corpo de Bombeiros Militar do Distrito Federal (CBMDF)**, prevenção e
como agir em emergências.

> 💻 O **código-fonte do jogo** está na pasta [`../jogo/`](../jogo/) deste mesmo repositório. Aqui estão
> os **documentos de engenharia e gestão do produto** exigidos na avaliação.

---

## 🧭 Visão geral

Cada pasta corresponde a um **artefato avaliado** e traz: um README explicando
o conteúdo, o **framework norteador** (boas práticas) e um **modelo pré-preenchido**
com os dados do projeto, pronto para o grupo finalizar.

| # | Pasta | O que contém | Framework norteador |
|---|-------|--------------|---------------------|
| 1 | [📋 Product Management](01-product-management/) | Planejamento e gestão do produto, roadmap, backlog e **Matriz SWOT** | Lean Inception + Scrum + RICE |
| 2 | [🔎 Elicitação](02-elicitacao/) | 5W2H, público-alvo, stakeholders e custo computacional | 5W2H + MoSCoW + BABOK |
| 3 | [🏗️ Arquitetura](03-arquitetura/) | Arquitetura do projeto em Markdown (diagramas) | C4 Model + arc42 |
| 4 | [🎨 UX/UI](04-ux-ui/) | Plano de UX/UI, Design System e Material Design | Material Design 3 + Atomic Design + Heurísticas de Nielsen |
| 5 | [🔐 Segurança](05-seguranca/) | Plano de segurança da informação (cenário cliente/servidor) | OWASP (Top 10 / ASVS) + ISO/IEC 27001 + STRIDE |
| 6 | [☁️ Cloud](06-cloud/) | Plano de instanciamento em nuvem | AWS Well-Architected + 12-Factor App |
| 7 | [🎤 Apresentação](07-apresentacao/) | Apresentação e simulação/demo do jogo | Pitch Canvas + Golden Circle |
| 8 | [🤖 Claude / IA](08-claude-ia/) | Uso de IA no desenvolvimento (transparência e boas práticas) | Prompt Engineering (Anthropic) + Responsible AI |

> As pastas estão numeradas só para manter a ordem; os nomes podem ser ajustados
> conforme o padrão pedido pelo professor.

---

## 🎯 Sobre o produto (resumo)

- **Nome:** Heróis do DF: Missão Bombeiro
- **Tipo:** jogo educativo 2D (single-player, desktop, offline)
- **Tecnologia:** Linguagem **C** + biblioteca **[Raylib](https://www.raylib.com/)**
- **Público-alvo:** crianças de **6 a 12 anos** (e educadores/responsáveis)
- **Conteúdo:** 10 fases + Museu dos Bombeiros desbloqueável
- **Objetivo educativo:** ensinar a ligar **193**, prevenir acidentes, nunca
  brincar com fogo, chamar um adulto e informar o endereço corretamente.

---

## 📊 Matriz SWOT (resumo)

Objetivo estratégico: **promover o trabalho dos bombeiros e impactar positivamente
crianças e adolescentes.**

| 💪 Forças | ⚠️ Fraquezas |
|-----------|--------------|
| Tema de alto valor social e credibilidade (CBMDF) | Distribuição exige compilar/instalar (sem loja/web ainda) |
| Conteúdo educativo alinhado à faixa 6–12 | Sem save persistente nem áudio/narração |
| Roda em máquinas simples, offline e leve | Pixel-art simples pode não atrair adolescentes |
| Identidade local (cenários de Brasília) | Conteúdo precisa de validação pedagógica/CBMDF |
| 10 fases + museu = engajamento e retenção | Equipe pequena e recursos limitados |

| 🚀 Oportunidades | ⛔ Ameaças |
|------------------|-----------|
| Parceria com CBMDF e escolas do DF | Concorrência com jogos comerciais de alta produção |
| Versão **web (WebAssembly)** amplia alcance | Riscos de privacidade com menores (LGPD/ECA) |
| Uso em campanhas, feiras e eventos | Manutenção pode parar após a disciplina |
| Expansão para SAMU, Defesa Civil, outras regiões | Mudanças nas diretrizes oficiais exigem updates |
| Editais de educação/segurança pública | Uso indevido se não licenciado corretamente |

> Versão completa e comentada em
> [01-product-management/matriz-swot.md](01-product-management/matriz-swot.md).

---

## 👩‍💻 Equipe

Amanda Soares · Cecilia Alemi · Eduarda Moura · Isabelle Reis · Mariana Nogueira ·
Maria Jhuliana Brito · Thiago Campêlo.

## 📜 Licença

Documentação sob licença **CC BY 4.0** (sugestão) — pode ser ajustada pelo grupo.
