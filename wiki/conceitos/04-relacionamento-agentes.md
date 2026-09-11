# Relação entre OpenCode e Hermes

## Agentes de LLM

Both OpenCode e Hermes são exemplos de agentes de LLM, mas com focos diferentes:

### OpenCode

- Foco em **execução de código** e tarefas técnicas
- Forte capacidade de gerar e testar programas Python
- Interpreta requisitos e cria arquivos (JSON, Python, Markdown)
- Ótimo para automação de lógica (distribuição round-robin, cálculos, validação)
- Usado para criar sistemas autônomos como o gerador de planos de estudo

### Hermes Desktop

- Foco em **interação via chat** e automação de fluxo de trabalho
- Integração com mensageiros (Telegram)
- Workflow Git/GitHub (branches, commits, PRs)
- Configuração de gateway e execução persistente
- Ideal para automação de conteúdo e contribuições colaborativas

## Pontos de conexão

- Ambos são construídos sobre modelos de linguagem (Nemotron 3.5 Lightning)
- Ambos conseguem interpretar requisitos naturais e transformar em ações concretas
- Ambos exigem configuração de workspace e compreensão de contexto
- Ambos podem operar de forma autônoma após configuração inicial

## Quando usar cada um

- Use **OpenCode** para tarefas que exigem geração de código, cálculo, processamento de dados ou automação técnica
- Use **Hermes** para tarefas que exigem interação social, atualização de conteúdo, workflows Git ou comunicação via chat