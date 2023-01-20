---
title: "Pesos processuais"
date: 2022-11-29T16:21:05-03:00
weight: 3
---
As regras de distribuição do PJe se baseiam essencialmente na ideia de que cada processo representa uma determinada carga de trabalho, carga essa chamada de peso.

O peso processual é resultado da composição de alguns aspectos inerentes ao processo judicial: classe processual, assuntos (são os assuntos ou é o assunto principal), quantidade de partes componentes do processo, a existência ou não de situação de prevenção e circunstâncias próprias dos órgãos julgadores.

Ao criar um cargo judicial em um órgão julgador, o sistema pergunta se ele deve ser inicializado com os valores dos outros cargos existentes. Se sim, o sistema cria o cargo já com os pesos acumulados dos outros que já existem e estão recebendo distribuição.

Desse modo, para um magistrado que vai começar a atuar em uma ZE ou tribunal e não se deseja que ele inicie recebendo processos a mais, deve-se criar um cargo judicial dentro do órgão, com as seguintes características: 
+ Descrição: a critério do usuário; 
+ Sigla: a critério do usuário;
+ Cargo: Ministro; 
+ Recebe distribuição: Sim;
+ Cargo Auxiliar: Não; 
+ Divisor do peso do processo: 1.0; 
+ Ativo: Sim.

Ao selecionar a opção Incluir, o sistema exibirá a seguinte mensagem: “Deseja que o acumulador de cargos seja atualizado para não haver compensação na distribuição?” A resposta deve ser Sim.

Finalizada essa etapa, você deve vincular o magistrado como titular do órgão vinculado ao novo cargo judicial.

Mais informações sobre a distribuição: [Distribuição - PJe](https://www.pje.jus.br/wiki/index.php/Distribui%C3%A7%C3%A3o).
