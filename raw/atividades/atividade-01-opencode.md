# Atividade 01: Instalar e testar o OpenCode

## O que quis tentar
Quis testar o OpenCode na criação de um gerador de plano de estudos. A ideia era verificar se o agente conseguiria interpretar os requisitos, criar os arquivos necessários, organizar a lógica de distribuição das matérias por prioridade e disponibilidade e testar o programa sozinho.

## O que usei
Usei o GPT para gerar o prompt inicial enviado para o OpenCode e o próprio OpenCode com o modelo gratuito Nemotron 3.5 Lightning para realizar a tarefa. Enviei o prompt pedindo a criação de um programa em Python que lesse as matérias e a disponibilidade de horários a partir de arquivos JSON e gerasse automaticamente um plano de estudos. O projeto foi pensado para usar apenas Python e bibliotecas padrão, com arquivos como main.py, materias.json, disponibilidade.json e README.md.

## O que aconteceu
O projeto funcionou corretamente nos testes principais: distribuição round-robin de matérias por prioridade, respeitando limites diários e informando horas pendentes quando insuficiente. Ele enfrentou inicialmente conflitos de nomes de dias (JSON "Segunda" vs código "Segunda-feira"), corrigido com mapa de tradução, e ajuste no cálculo de horas pendentes. Todas as validações (prioridade 1-5, horas positivas, arquivos inexistentes/mal formatados) funcionaram.

## O que aprendi
Aprendi sobre o OpenCode que ainda não conhecia e sobre o projeto percebi a importância de padronizar nomenclaturas entre dados e código, da ordem de operações ao calcular totais e da necessidade de rastrear quais dias cada matéria já utilizou para distribuição efetiva em múltiplos dias.