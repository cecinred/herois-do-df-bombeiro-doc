# 🚒 Heróis do DF: Missão Bombeiro

Jogo educativo em **C + Raylib** que ensina crianças de **6 a 12 anos** a agir
em emergências e a conhecer o trabalho do **Corpo de Bombeiros Militar do
Distrito Federal (CBMDF)**. O jogador é a **Cadete Clara** e passa por **10 fases**
até se tornar **Bombeiro Honorário do DF**.

> Este repositório reúne **tudo em um só lugar**: o **código do jogo** e toda a
> **documentação de engenharia e gestão do produto**.

---

## 📂 Estrutura do repositório

| Parte | Pasta | O que é |
|---|---|---|
| 🎮 **Jogo** | [`jogo/`](jogo/) | Código-fonte completo + uma pasta por fase explicada |
| 📚 **Documentação** | [`documentacao/`](documentacao/) | Artefatos de avaliação (gestão, arquitetura, UX, segurança, cloud...) |
| 🚀 **Guia** | [`COMO_SUBIR_NO_GITHUB.md`](COMO_SUBIR_NO_GITHUB.md) | Passo a passo para publicar no GitHub |

---

## 🎮 Jogo

| Item | Link | Observação |
|---|---|---|
| **Jogo completo (compila e roda)** | [`jogo/jogo-completo/`](jogo/jogo-completo/) | É o arquivo único `HeroisDoDF_Bombeiro.c` |
| **Fases explicadas** | [`jogo/fases/`](jogo/fases/) | Uma pasta por fase, com o trecho de código + README |

### Como compilar
```bash
# Windows (MinGW)
gcc jogo/jogo-completo/HeroisDoDF_Bombeiro.c -o herois.exe -lraylib -lopengl32 -lgdi32 -lwinmm

# Linux
gcc jogo/jogo-completo/HeroisDoDF_Bombeiro.c -o herois -lraylib -lm -lpthread -ldl -lrt -lX11
```
> Precisa da biblioteca **[Raylib](https://www.raylib.com/)** instalada.
> Mantenha os arquivos em **UTF-8** (por causa dos acentos).

### Controles
**Setas / A,D,W,S** mover e mirar · **Espaço** ação (água, sirene...) ·
**Mouse** menus e minigames · **F11** tela cheia · **ESC** sair.

---

## 📚 Documentação

| # | Pasta | Conteúdo | Framework norteador |
|---|-------|----------|---------------------|
| 1 | [Product Management](documentacao/01-product-management/) | Roadmap, backlog e **Matriz SWOT** | Lean Inception + Scrum + RICE |
| 2 | [Elicitação](documentacao/02-elicitacao/) | 5W2H, público-alvo, stakeholders, custo computacional | 5W2H + MoSCoW + BABOK |
| 3 | [Arquitetura](documentacao/03-arquitetura/) | Arquitetura em Markdown (diagramas) | C4 Model + arc42 |
| 4 | [UX/UI](documentacao/04-ux-ui/) | Design System, Material/Atomic Design | Material Design 3 + Atomic Design + Nielsen |
| 5 | [Segurança](documentacao/05-seguranca/) | Plano de segurança (cliente/servidor) | OWASP + ISO/IEC 27001 + STRIDE |
| 6 | [Cloud](documentacao/06-cloud/) | Instanciamento em nuvem | AWS Well-Architected + 12-Factor |
| 7 | [Apresentação](documentacao/07-apresentacao/) | Apresentação e simulação do jogo | Pitch Canvas + Golden Circle |
| 8 | [Claude / IA](documentacao/08-claude-ia/) | Uso transparente de IA no projeto | Prompt Engineering + Responsible AI |

📊 **Matriz SWOT completa:**
[`documentacao/01-product-management/matriz-swot.md`](documentacao/01-product-management/matriz-swot.md)

---

## 🗺️ As 10 fases

| # | Fase | Minigame |
|---|------|----------|
| 1 | Conhecendo o Quartel | Vestir o EPI |
| 2 | Chamada de Emergência | Ligar 193 e responder o atendente |
| 3 | Preparação da Viatura | Carregar os itens certos |
| 4 | Deslocamento pela Cidade | Dirigir com sirene |
| 5 | Incêndio Residencial | Apagar os focos com a mangueira |
| 6 | Primeiros Socorros | Quiz de socorro (192) |
| 7 | Resgate Animal | Resgatar o cachorro |
| 8 | Acidente de Trânsito | Isolar a área com cones |
| 9 | Temporada de Queimadas | Conter focos (com vento) |
| 10 | Grande Missão | Tudo junto + resgate de vítimas |

Ao concluir as 10 fases, o **Museu dos Bombeiros** é desbloqueado no menu.

---

## 👩‍💻 Equipe

Amanda Soares · Cecilia Alemi · Eduarda Moura · Isabelle Reis · Mariana Nogueira ·
Maria Jhuliana Brito · Thiago Campêlo.

Inspirado no trabalho do **Corpo de Bombeiros Militar do Distrito Federal**.

## 📜 Licença

Código sob licença **MIT** — veja [LICENSE](LICENSE).
