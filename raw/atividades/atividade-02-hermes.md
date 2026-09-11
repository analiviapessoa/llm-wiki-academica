# Atividade 02: Um agente seu, acessível por chat

## O que quis tentar
Quis criar um agente que pudesse ser acessado pelo Telegram e que tivesse acesso ao meu fork do repositório do CriaComp. A ideia era conseguir enviar uma notícia pelo celular e fazer o agente editar o arquivo 2026-2-NEWS.md, criar a alteração no Git e enviar uma contribuição para o repositório sem precisar fazer todo o processo manualmente pelo computador.

## O que usei
Usei o Hermes Desktop no Windows, conectado ao Telegram por meio de um bot criado com o BotFather. Como modelo, utilizei o Nemotron 3.5 Lightning. Também usei o Git, o GitHub, o VS Code e um fork do repositório filipecalegario/criacomp. Configurei a pasta clonada do repositório como workspace do Hermes e, no final, instalei o gateway do Hermes como uma tarefa agendada do Windows para que ele continuasse funcionando em segundo plano. Para me ajudar com o BotFather utilizei o GPT.

## O que aconteceu
Primeiro configurei o Hermes e conectei o bot do Telegram. Depois, ajustei o workspace para que o agente conseguisse localizar o repositório clonado e identificar o arquivo 2026-2-NEWS.md. Pelo Telegram, enviei uma notícia e o Hermes abriu o link, identificou o título e adicionou uma nova seção no arquivo com a data e a autoria. Em seguida, ele criou uma branch, fez commit e push da alteração.

Na primeira tentativa de criar o Pull Request, o Hermes criou o PR apenas dentro do próprio fork, em vez de enviá-lo para o repositório original da disciplina. Depois de especificar melhor o destino, tentei novamente. Durante essa tentativa o provedor do modelo apresentou um erro e o Hermes informou que havia esgotado as tentativas de recuperação. Ao repetir a operação algum tempo depois, ela funcionou e o Pull Request foi criado corretamente para filipecalegario/criacomp.

Por fim, executei a instalação persistente do gateway. O Hermes registrou a tarefa Hermes_Gateway no Windows e iniciou o processo em segundo plano. Dessa forma, não preciso manter o PowerShell aberto, embora o agente ainda dependa de o computador permanecer ligado.

## O que aprendi
Aprendi que conectar um agente a um chat envolve mais do que apenas configurar um modelo, é necessário cuidar de autenticação, diretório de trabalho, permissões do Git, integração e execução persistente do gateway. Também percebi que agentes podem interpretar uma tarefa de forma diferente da esperada, como aconteceu com o primeiro Pull Request, por isso instruções mais explícitas sobre repositório de origem e destino fazem diferença.

Outro aprendizado foi que falhas de infraestrutura ou do provedor do modelo podem acontecer mesmo quando a configuração está correta. Nesse caso, o erro do Nemotron foi temporário e a mesma operação funcionou posteriormente.
