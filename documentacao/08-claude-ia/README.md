# 🤖 Uso de IA no Desenvolvimento (Claude)

Documenta, com **transparência**, como a IA (Claude, da Anthropic) foi usada para
apoiar o desenvolvimento — boa prática acadêmica e de engenharia.

## 🧭 Framework norteador: Prompt Engineering (Anthropic) + Responsible AI

- **Boas práticas de Prompt Engineering** (Anthropic) — ser claro e específico,
  dar exemplos, pedir passo a passo, definir formato de saída.
  Referência: <https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview>
- **Responsible / Transparent AI** — registrar onde a IA ajudou, **revisar e
  testar** tudo, e assumir a autoria/responsabilidade pelo resultado.

---

## 🎯 Princípios adotados
- **Transparência:** declarar o uso de IA como ferramenta de apoio.
- **Revisão humana:** todo código gerado foi **lido, testado e ajustado** pelo grupo.
- **Aprendizado:** usar a IA para entender conceitos, não só copiar.
- **Responsabilidade:** o grupo responde pelo produto final.

---

## 🛠️ Onde a IA apoiou (exemplos a preencher)
| Área | Como ajudou | Revisão do grupo |
|---|---|---|
| Estrutura do jogo (máquina de estados) | sugestão de organização | testada e adaptada |
| Minigames das fases | lógica inicial dos `Init/Upd/Draw` | ajustada (dificuldade, posições) |
| Correção de bugs | apontar travamentos (ex.: índice do quiz) | validada compilando/jogando |
| Documentação | rascunho de README e diagramas | revisada e completada |

> Preencher com os casos reais do grupo.

---

## ✍️ Boas práticas de prompt (resumo)
- **Seja específico:** diga linguagem, biblioteca, objetivo e restrições.
- **Dê contexto/exemplos:** anexe o código atual e descreva o resultado esperado.
- **Peça em partes:** uma tarefa por vez é mais fácil de validar.
- **Defina o formato:** "responda só com o trecho alterado", "explique em tópicos".
- **Itere:** teste, relate o erro exato e peça correção.

## 📋 Registro de uso (template)
| Data | Objetivo do prompt | Resultado | O que o grupo mudou |
|---|---|---|---|
| | | | |

## ⚖️ Ética e limites
- Conferir **fatos** (ex.: dados do CBMDF) em fontes oficiais.
- Não inserir dados pessoais sensíveis nos prompts.
- Citar a IA como **ferramenta de apoio**, mantendo a autoria do grupo.
