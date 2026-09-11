# Relação entre OpenCode e Hermes

## Agentes de LLM

Both OpenCode e Hermes são exemplos de agentes de LLM, mas com focos diferentes:

### OpenCode

- Foco em **execução de código** e tarefas técnicas
- Forte capacidade de gerar e testar programas Python
- Interpreta requisitos e cria arquivos (JSON, Python, Markdown)
- Ótimo para automação de lógica (distribuição round-robin, cálculos, validação)
- Focado em desenvolvimento e manipulação de código dentro de projetos

### Hermes Desktop

- Foco em **interação via chat** e automação de fluxo de trabalho
- Integração com mensageiros (Telegram)
- Workflow Git/GitHub (branches, commits, PRs)
- Configuração de gateway e execução persistente
- Ideal para automação de conteúdo e contribuições colaborativas

## O que é um Agente? (De raw/aulas/anotacao-agentes.md)

Um agente não é apenas um chatbot. Ele combina um modelo de linguagem com contexto, ferramentas e um ambiente de execução. Um agente não é apenas um chatbot. Ele combina um modelo de linguagem com contexto, ferramentas e um ambiente de execução.

- OpenCode é mais voltado para desenvolvimento e manipulação de código dentro de projetos.
- Hermes pode funcionar como um agente acessível remotamente, inclusive por Telegram, e utilizar ferramentas como Git.
- Um problema importante é que o agente precisa receber contexto suficiente, mas contexto demais também pode prejudicar a execução.

## Pontos de conexão

- Ambos são construídos sobre modelos de linguagem (Nemotron 3.5 Lightning)
- Ambos conseguem interpretar requisitos naturais e transformar em ações concretas
- Ambos exigem configuração de workspace e compreensão de contexto
- Ambos podem operar de forma autônoma após configuração inicial
- Ambos exigem configuração adequada de workspace e contexto para operar de forma eficaz

## Quando usar cada um

- Use **OpenCode** para tarefas que exigem geração de código, cálculo, processamento de dados ou automação técnica
  - Melhor para desenvolvimento direto dentro de projetos
  - (De raw/aulas/anotacao-agentes.md: OpenCode é mais voltado para desenvolvimento e manipulação de código dentro de projetos.)
- Use **Hermes** para tarefas que exigem interação social, atualização de conteúdo, workflows Git ou comunicação via chat
  - Mais útil para acesso remoto por Telegram e ações persistentes
  - (De raw/projetos/notas-agentes-e-automacao.md e raw/aulas/anotacao-agentes.md: Hermes pode funcionar como um agente acessível remotamente, inclusive por Telegram, e utilizar ferramentas como Git.)