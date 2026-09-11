# OpenCode e Geração de Planos de Estudo

## Visão geral

O OpenCode foi testado para criar um gerador de plano de estudos em Python. O agente interpretou requisitos, criou os arquivos necessários e organizou a lógica de distribuição das matérias por prioridade.

## O que foi utilizado

- **Modelo**: Nemotron 3.5 Lightning (via OpenCode)
- **Prompt**: GPT gerou o prompt inicial enviado ao OpenCode
- **Ferramenta**: OpenCode com modelo gratuito Nemotron 3.5 Lightning

## Lógica implementada

- Leitura de matérias e disponibilidade de horários a partir de arquivos JSON
- Distribuição round-robin de matérias por prioridade (escala 1-5)
- Respeito a limites diários de estudo
- Cálculo de horas pendentes quando a disponibilidade é insuficiente

## Desafios encontrados

- Conflitos de nomenclatura entre dados JSON ("Segunda") e código ("Segunda-feira") — corrigido com mapa de tradução
- Ajuste no cálculo de horas pendentes
- Validação de prioridade (1-5), horas positivas e formatação de arquivos

## Arquivos típicos

- `main.py` — script principal
- `materias.json` — definição das matérias e prioridades
- `disponibilidade.json` — horários disponíveis por dia
- `README.md` — documentação do projeto