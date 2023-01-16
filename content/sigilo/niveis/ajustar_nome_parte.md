---
title: "Como ajustar o tipo de complemento “nome_da_parte” para processos sigilosos"
date: 2023-01-16T10:49:43-03:00
menuTitle: "Ajustar complemento de movimentação"
weight: 5
---
Para que o nome da parte de processos sigilosos não seja exposto em movimentos que utilizam esse complemento, há uma configuração que deve ser feita.

Como administrador, pesquise pela opção **Tipo de complemento (Configurações –  Tabelas Judiciais – Movimentações –  Complementos – Tipos).** A tela de configuração dos tipos de complementos será exibida, pesquise, no campo Nome, por nome_da_parte. 

Clique no ícone de edição (lápis) e verifique como está o campo Expressão de busca.

O valor correto é #{processoParteUtils.obterPartesProcesso(tramitacaoProcessualService.recuperaProcesso())}.
