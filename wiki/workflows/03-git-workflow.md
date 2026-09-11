# Workflow Git e GitHub

## Visão geral

Fluxo de trabalho Git utilizado pelo Hermes agente e manualmente pelos usuários para contribuir com o repositório CriaComp.

## Passos fundamentais

1. **Clonar o fork** do repositório da disciplina
2. **Configurar workspace** do Hermes para apontar para a pasta clonada
3. **Criar branch** para a nova alteração
4. **Editar o arquivo** adequado (ex.: `2026-2-NEWS.md`)
5. **Commit** with descriptive message including data e autoria
6. **Push** para o próprio fork
7. **Criar Pull Request** — especificar claramente:
   - Destino: repositório original da disciplina (não apenas o fork)
   - Base: branch correta do repositório destino
   - Comparação: branch do fork → branch do destino

## Problemas comuns

- PR criado apenas no fork em vez de enviar para o repositório original
- Erros do provedor de modelo durante a operação — podem exigir repetição da tarefa
- Falhas de autenticação do Git/GitHub quando o gateway não está em execução

## Manutenção

- Gateway Hermes deve estar em execução para operações Git em segundo plano
- Manter o Windows atualizado para tarefas agendadas (Hermes_Gateway)