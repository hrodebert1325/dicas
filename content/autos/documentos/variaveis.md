---
title: "Variáveis"
date: 2022-11-23T17:57:39-03:00
weight: 6
---

{{<table "variaveismodelo">}}

| **Descrição** | **Variável** | **Outras informações** |
|:---|---|:---:|
| Número do Processo | #{processoTrfHome.instance.numeroProcesso} |  |
| Número do processo referência (o número do drap estará nessa variável) | #{processoTrfHome.instance.processoReferencia} |  |
| Assuntos do Processo | #{processoTrfHome.instance.assuntoTrfListStr} |  |
| Nome Autor Processo | #{processoTrfHome.instance.tipoNomeAutorProcesso} |  |
| Nome Réu Processo | #{processoTrfHome.instance.nomeReuProcesso} |  |
| Partes Polo Passivo | #{processoTrfHome.processoPartePoloPassivoSemAdvogadoStr} |  |
| Nome Autor Ativo Processo | #{processoTrfHome.instance.nomeAutorAtivoProcesso} |  |
| Nome Outros Interessados | #{processoParteHome.processoParteTerceiroSemVinculacaoList} |  |
| Lista Nome Autor | #{processoTrfHome.nomeCpfAutorList} |  |
| Partes polo Ativo | #{processoTrfHome.processoPartePoloAtivoSemAdvogadoStr} |  |
| Endereço Partes Polo Ativo | #{processoTrfHome.processoParteEnderecoPoloAtivoStr} |  |
| Endereço Partes Polo Passivo | #{processoTrfHome.processoParteEnderecoPoloPassivoStr} |  |
| Lista Tipo Nome Advogado Autor | #{processoTrfHome.instance.tipoNomeAdvogadoAutorList} |  |
| Lista Tipo Nome Advogado Réu | #{processoTrfHome.instance.tipoNomeAdvogadoReuList} |  |
| Tipo Nome Réu Processo | #{processoTrfHome.instance.tipoNomeReuProcesso} |  |
| Endereço Advogado Polo Ativo | #{processoTrfHome.advogadoEnderecoPoloAtivoStr} |  |
| Endereço Advogado Polo Passivo | #{processoTrfHome.advogadoEnderecoPoloPassivoStr} |  |
| Classe do Processo | #{processoTrfHome.instance.classeJudicial} |  |
| Data da Distribuição | #{processoTrfHome.dataDistribuicao} |  |
| Data da Audiência | #{processoTrfHome.dataAudiencia} |  |
| Tipo de Audiência | #{processoTrfHome.tipoAudiencia} |  |
| Endereço da Sala de Audiência | #{processoTrfHome.enderecoSalaAudiencia} |  |
| Sala de Audiência | #{processoTrfHome.salaAudiencia} |  |
| Data Atual | #{currentDate} |  |
| Data Atual Abreviada | #{dataAtualAbreviada} |  |
| Data Atual Extenso | #{dataAtual} |  |
| Data atual Formatada | #{dataAtual} |  |
| Data e Hora Atual | #{currentDatetime} |  |
| Hora Atual | #{currentTime} |  |
| Data Semana Hoje Extenso | #{dataAtualExtenso} |  |
| Órgão Julgador Processo | #{processoTrfHome.instance.orgaoJulgador} |  |
| Cidade Órgão Julgador Processo | #{processoTrfHome.instance.orgaoJulgador.localizacao.endereco.cep.municipio} |  |
| UF Órgão Julgador | #{processoTrfHome.instance.orgaoJulgador.localizacao.endereco.cep.municipio.estado.codEstado} |  |
| Juiz Órgão Julgador | #{processoTrfHome.instance.nomeJuizOrgaoJulgador} |  |
| Endereço Órgão Julgador | #{processoTrfHome.instance.orgaoJulgador.localizacao.endereco.enderecoCompleto} |  |
| Objeto do processo | #{processoTrfHome.instance.objeto} |  |
| Cargo do órgão julgador do processo | #{processoTrfHome.instance.orgaoJulgadorCargo} |  |
| Usuário Logado | #{usuarioLogado.nome} |  |
| Papel usuário logado | #{usuarioLogadoLocalizacaoAtual.papel} |  |
| Login Usuário Logado | #{usuarioLogado.login} |  |
| Nome do Usuário Logado | #{usuarioLogado.nome} |  |
| Partes formatadas | #{processoJudicialAction.recuperarParteFormatada(true, true, 'A', 'P', 'T')} | Detalhamento |
| Presidente da sessão | #{sessaoComposicaoOrdemManager.obterPresidenteSessao(sessaoPautaProcessoTrfManager<br>.getSessaoPautaProcessoTrfJulgado(tramitacaoProcessualService.recuperaProcesso()).sessao, true)} |  |
| Procurador da sessão | #{pessoaProcuradorManager.getTituloProcurador(sessaoPautaProcessoTrfManager<br>.getSessaoPsautaProcessoTrfJulgado(tramitacaoProcessualService.recuperaProcesso()).sessao)} |  |
| Revisor | #{pessoaMagistradoManager.getMagistradoTitular(orgaoJulgadorColegiadoOrgaoJulgadorManager<br>.recuperarOrgaoJulgadorRevisorPadrao(tramitacaoProcessualService.recuperaProcesso()).orgaoJulgadorRevisor.orgaoJulgador).getNome().toUpperCase()} |  |
| Partes dentro da certidão de julgamento | #{processoJudicialManager.recuperarParteFormatada(sessaoProcessoDocumentoHome.sessaoPautaProcessoTrf.processoTrf, false,true,false,'A','P','T')} |  |
| Cabeçalho do processo com cadeia recursal em siglas dentro da sessão | #{sessaoProcessoDocumentoHome.sessaoPautaProcessoTrf.processoTrf} |  |
| Cabeçalho do processo com cadeia recursal em siglas | #{processoTrfHome.instance} |  |
| Cabeçalho do processo com cadeia recursal por extenso, exceto classe do principal | #{processoTrfHome.instance.extensoClasse != null ? processoTrfHome.instance.extensoClasse : processoTrfHome.instance.classeJudicial} |  |
| Cabeçalho do processo com cadeia recursal por extenso, exceto classe do principal dentro da sessão | #{sessaoProcessoDocumentoHome.sessaoPautaProcessoTrf.processoTrf.extensoClasse != null ? <br>sessaoProcessoDocumentoHome.sessaoPautaProcessoTrf.processoTrf.extensoClasse : sessaoProcessoDocumentoHome.sessaoPautaProcessoTrf.processoTrf.classeJudicial} |  |
| Escreve título Juiz ou Juíza de acordo com a informação sexo do cadastro do magistrado relator | #{processoTrfHome.getRelator(processoTrfHome.instance) != null and processoTrfHome.getRelator(processoTrfHome.instance).sexo == 'F'? 'Juíza': 'Juiz'} |  |
| Número do processo para uso em modelos de oficial de justiça | #{processoExpedienteCentralMandadoHome.instance.processoExpediente.processoTrf.processo.numeroProcesso} |  |
| Classe do processo para uso em modelos de oficial de justiça | #{processoExpedienteCentralMandadoHome.instance.processoExpediente.processoTrf.classeJudicial} |  |
| Partes do processo para uso em modelos de oficial de justiça | #{processoJudicialManager.recuperarParteFormatada(processoExpedienteCentralMandadoHome<br>.instance.processoExpediente.processoTrf, false,true,false,'A','P','T')} |  |
| Recupera conteúdo do documento ementa vinculada à última sessão onde o processo foi "Julgado" e a sessão teve movimento registrado ou o processo teve o julgamento individual finalizado | #{sessaoProcessoDocumentoManager.getEmenta()} |  |
| Recupera conteúdo do documento relatório à última sessão onde o processo foi "Julgado" e a sessão teve movimento registrado ou o processo teve o julgamento individual finalizado | #{sessaoProcessoDocumentoManager.getRelatorio(null)} |  |
| Recupera conteúdo do documento voto vinculado à última sessão onde o processo foi "Julgado" e a sessão teve movimento registrado ou o processo teve o julgamento individual finalizado. O sistema procura o voto do vencedor. Caso não encontre, procura o voto do relator | #{sessaoProcessoDocumentoManager.getVoto(null)} |  |
| Recupera data da última sessão de julgamento onde o processo foi "Julgado" | #{sessaoProcessoDocumentoManager.getDataUltimaSessaoJulgamento(null)} |  |
| Recupera a última composição do processo na sessão. False = não traz o presidente. True = traz o presidente | #{sessaoComposicaoOrdemManager.obterComposicaoSessao(sessaoHome.instance, false)} |  |

{{</table>}}