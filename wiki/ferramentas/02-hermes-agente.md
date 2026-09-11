# Hermes Desktop Agent

## Visão geral

O Hermes Desktop foi configurado como um agente acessível por Telegram, com conexão ao fork do repositório CriaComp. O agente ganhou capacidade de editar arquivos, criar commits e abrir Pull Requests.

## Configuração

- **Plataforma**: Windows Desktop
- **Integração**: Telegram via BotFather
- **Modelo**: Nemotron 3.5 Lightning
- **Workspace**: Pasta clonada do repositório filipecalegario/criacomp

## fluxo de trabalho

1. Configurar o Hermes e conectar o bot do Telegram
2. Ajustar o workspace para localizar o repositório clonado e o arquivo `2026-2-NEWS.md`
3. Enviar uma notícia pelo Telegram
4. O agente abre o link, identifica o título e adiciona nova seção no arquivo com data e autoria
5. Cria branch, faz commit e push da alteração
6. Cria Pull Request (é necessário especificar destino correto: fork → repositório original da disciplina)

## Desafios e aprendizados

- Conectar agente a chat envolve autenticação, diretório de trabalho, permissões do Git, integração e execução persistente do gateway
- Agentes podem interpretar tarefas de forma diferente da esperada (ex.: primeiro PR criado no fork em vez do repositório original)
- Falhas de infraestrutura ou do provedor do modelo podem acontecer mesmo com configuração correta — operações temporárias podem ser resolvidas com repetição
- Instruções explícitas sobre repositório de origem e destino fazem diferença

## Instalação persistente

- Instalar o gateway do Hermes como tarefa agendada do Windows (Hermes_Gateway)
- O agente continua em segundo plano, mas depende do computador permanecer ligado