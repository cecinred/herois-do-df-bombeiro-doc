# 🏗️ Arquitetura do Projeto

Arquitetura documentada em Markdown usando o **C4 Model** (4 níveis de zoom).
Os diagramas usam **Mermaid**, que o GitHub renderiza automaticamente.

## 🧭 Framework norteador: C4 Model + arc42

- **C4 Model** (Simon Brown) — descreve o sistema em 4 níveis: **Contexto →
  Contêineres → Componentes → Código**. Simples e visual.
- **arc42** — estrutura de referência para documentação de arquitetura
  (decisões, restrições, qualidade).

---

## Nível 1 — Contexto

```mermaid
flowchart LR
    Crianca([👧 Criança 6-12]) -->|joga| Jogo[Heroi do DF: Missao Bombeiro]
    Professor([👩‍🏫 Professor]) -->|usa em aula| Jogo
    Jogo -.->|conteudo validado| CBMDF([🚒 CBMDF])
    Jogo -.->|futuro: placar/progresso| Backend[(Backend opcional)]
```

O jogo é **desktop, single-player e offline**. Um backend é apenas uma
possibilidade futura (placar, progresso, painel do professor).

## Nível 2 — Contêineres

```mermaid
flowchart TB
    subgraph PC[Computador do jogador]
        EXE[Executavel do jogo - C/Raylib]
        ASSETS[Recursos embutidos - desenhos por codigo]
        EXE --- ASSETS
    end
    EXE -->|OpenGL| GPU[Placa de video/Tela]
    EXE -->|entrada| HID[Teclado e Mouse]
```

Hoje há **um único contêiner**: o executável. Todo o conteúdo visual é desenhado
por código (pixel-art com retângulos), sem arquivos externos.

## Nível 3 — Componentes (módulos do código)

```mermaid
flowchart TB
    MAIN[main / Maquina de Estados\nMENU, JOGO, GAMEOVER, FIMJOGO, MUSEU]
    RENDER[Render em tela cheia\nRenderTexture + mouse virtual]
    HUD[HUD e telas padrao]
    QUIZ[Quiz generico\nfases 2, 6, 10]
    HOSE[Mangueira generica\nfases 5, 9, 10]
    FASES[Fases 1..10\nInitFx / UpdFx / DrawFx]
    PERS[Personagens\nClara, Almeida, Ana, Silva]
    CEN[Cenarios de Brasilia\nCatedral, Congresso, Estadio]
    FX[Particulas e foguetes]
    MUSEU[Museu dos Bombeiros]

    MAIN --> RENDER
    MAIN --> FASES
    MAIN --> MUSEU
    FASES --> HUD
    FASES --> QUIZ
    FASES --> HOSE
    FASES --> PERS
    FASES --> CEN
    FASES --> FX
```

## Nível 4 — Código (padrão de cada fase)

Quase toda fase segue **três funções**:

| Função | Responsabilidade |
|---|---|
| `InitFx()` | inicializa estado, posições e contadores |
| `UpdFx(...)` | lógica por quadro (entrada, colisões, regras, vitória) |
| `DrawFx(...)` | desenha a fase na tela |

O `main()` roda o laço: lê entrada → atualiza a fase atual → desenha em uma
**textura virtual 600×800** que é escalada para a tela cheia (com o mouse
convertido para as coordenadas virtuais).

---

## Decisões de arquitetura (ADR resumido)

| Decisão | Motivo |
|---|---|
| **C + Raylib** | leve, multiplataforma, ótimo para 2D e ensino |
| **Arquivo único** | simples de compilar e distribuir no contexto acadêmico |
| **Arte por código** | sem dependência de assets externos |
| **Máquina de estados** | clareza no fluxo entre menu, fases e museu |
| **RenderTexture** | tela cheia nítida mantendo a proporção 600×800 |

## Atributos de qualidade
- **Desempenho:** 60 FPS em hardware simples.
- **Portabilidade:** Windows, Linux e macOS (mesmo código).
- **Manutenibilidade:** funções compartilhadas (quiz, mangueira, HUD) evitam repetição.
- **Evolutividade:** novas fases entram só adicionando `case` na máquina de estados.
