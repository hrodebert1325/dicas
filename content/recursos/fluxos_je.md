---
title: "Alterações de Fluxo"
date: 2022-11-29T16:28:00-03:00
weight: 14
---

## FLX_REGISTRAR_RECURSO 
+ Nas tarefas Registrar recurso e Registrar recurso - Corregedoria, alterar as variáveis que estão nas duas para que referenciem o seguinte:Processo_Fluxo_Recurso_registrarRecurso no lugar de Processo_Fluxo_documento_recurso_registrarRecurso
+ Incluir no evento Criar tarefa das tarefas Registrar recurso e Registrar recurso - Corregedoria a ação #{taskInstanceUtil.setFrameDefaultTransition(‘Finalizar fluxo’)}

## FLX_ORIGINARIAS
+ Na tarefa Verificar e Certificar dados do processo, alterar a expressão que consta na quarta ação em iniciar tarefa (a que contém #{tramitacaoProcessualService.gravaVariavelTarefa(‘pageParam’,‘idProcesso=’.concat(tramitacaoProcessualService.recuperaProcesso().idProcessoTrf))}”) para conter o seguinte: #{tramitacaoProcessualService.gravaVariavelTarefa(‘pageParam’,‘idProcesso=’.concat(tramitacaoProcessualService.recuperaProcesso().processoTrfPrincipal.idProcessoTrf))
+ Na tarefa Definir procedimento, alterar transição Redistribuir de ofício e Apensar e desapensar processos para conter a condição de entrada (ícone de interrogação da transição) #{!tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}
+ Criar um nó de decisão de nome Verifica recurso que contenha a seguinte EL: #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()?‘T1’ : ‘T2’}. Atribuir à transição T1 o encaminhamento para Cumprimento de determinações do ministro e à transição T2 o encaminhamento para Processo com movimentação de magistrado?Substituir transição de saída do nó Gravar variáveis de fluxo de Processo com movimentação de magistrado? para Verifica recurso 
+ Criar um nó de decisão denominado Verifica recurso arquivo que contenha a seguinte EL: #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno() ? ‘T1’ : ‘T2’}. Atribuir à transição T1 o encaminhamento para Fluxo de arquivo e à transição T2 o encaminhamento para Realiza Baixa. Alterar transições T1 e Realiza Baixa para arquivamento disponíveis, respectivamente, nos nós Testar encaminhamento ao arquivo e Verificar Pendências para encaminhar para Verifica recurso arquivo.
+ Criar um nó de decisão denominado Verifica recurso reativa que contenha a seguinte EL: #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno() ? ‘T1’ : ‘T2’}. Atribuir à transição T1 o encaminhamento para Verifica se é cumprimento da Corregedoria e à transição T2 o encaminhamento para Reativa Processo.
+ Alterar transições Reativa processo disponível no nó Fluxo de arquivo para encaminhar para Verifica recurso reativa.

## CUMPRDET
+ Nas tarefas Analisar determinação, Analisar processos, Analisar Processos - Urgentes e Analisar determinação - Urgentes, alterar transições Redistribuir processo, Evoluir classe processual, Apensar e desapensar processos e Desmembrar processos para conter a condição de entrada (ícone de interrogação da transição) #{!tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}
+ Na tarefa Confirma prevenção processual, alterar transição Redistribuir processo para conter a condição de entrada (ícone de interrogação da transição) #{!tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}
+ Na tarefa Atualizar dados do processo, alterar a expressão que consta na quarta ação em iniciar tarefa (a que contém pageparam) para conter o seguinte: #{tramitacaoProcessualService.gravaVariavelTarefa(‘pageParam’,‘idProcesso=’.concat(tramitacaoProcessualService.recuperaProcesso().processoTrfPrincipal.idProcessoTrf))}
+ Acrescentar nó de tarefa cujo nome é Alterar partes, disponível para raia Secretaria Judiciária - Processamento, com a seguinte variável do tipo Frame: Processo_Fluxo_Recurso_alterarPartes.
+ Acrescentar transição para a tarefa a partir das tarefas Analisar determinação, Analisar processos, Analisar Processos - Urgentes e Analisar determinação - Urgentes com condição de entrada (ícone de interrogação da transição) #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}.
+ Acrescentar transição de saída para o nó testar encaminhado pelo Relator com o nome de Retornar. Na variável, a configuração de Escrita deve estar marcada e a configuração Obrig. não deve estar marcada.
+ Acrescentar nó de tarefa cujo nome é Alterar órgão julgador, disponível para raia Secretaria Judiciária - Processamento, com a seguinte variável do tipo Frame: Processo_Fluxo_Recurso_alterarOrgaoJulgador.
+ Acrescentar transição para a tarefa a partir das tarefas Analisar determinação, Analisar processos, Analisar Processos – Urgentes e Analisar determinação - Urgentes com condição de entrada (ícone de interrogação da transição) #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}.
+ Acrescentar transição de saída para o nó testar encaminhado pelo Relator com o nome de Retornar. Na variável, a configuração de Escrita deve estar marcada e a configuração Obrig. não deve estar marcada.

## FLX_ARQUIVO
+ Criar um nó de tarefa cujo nome é Manter recurso arquivado atribuí-la à raia Secretaria Judiciária. Criar uma transição de saída desta tarefa para o Término com o nome de Reativar recurso.
+ Criar um nó de decisão de nome Verificar recurso que contenha a seguinte EL: #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()? ‘T1’ : ‘T2’}
+ Criar transição de saída para o nó de decisão chamada T1 que encaminhe para a tarefa Manter recurso arquivado e transição de saída chamada T2 que encaminha para o nó Lançar Movimento de Arquivamento.
+ No nó de sistema Apagar relator do processo, substituir a transição de saída para encaminhar para o nó de decisão Verificar recurso.
+ Na tarefa Classificar Processo para Arquivamento, colocar condição de entrada (ícone de interrogação da transição) na transição Registrar arquivamento conforme a seguir: #{!tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}.
+ Na tarefa Classificar Processo para Arquivamento, acrescentar transição para Manter recurso arquivado com a condição de entrada (ícone de interrogação da transição) conforme a seguir: #{tramitacaoProcessualService.recuperaProcesso().isRecursoInterno()}
