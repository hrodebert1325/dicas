---
title: "Correção de erros"
date: 2022-11-29T16:29:52-03:00
---

A remessa é uma das tarefas em que mais ocorrem erros no sistema PJE, isso porque ela faz uma série de validações na instância de origem e na instância de destino.

Vários erros estão devidamente tratados pelo sistema e retornam uma mensagem clara para o usuário, o que permite a correção pelo próprio servidor ou pelo administrador local, sem a necessidade de abertura de chamado no TSE. Na sequência, vamos apresentar os principais erros e as soluções.

+ CEP 
Esse erro aparece quando alguma das partes do processo está com o CEP inválido ou em branco.
Para correção, basta ir ao menu dos autos processuais, na opção retificar autuação, aba partes, dentro das partes verificar a aba endereço e conferir o CEP de todas as partes e advogados, procedendo às correções necessárias.
Feito isso, é preciso deletar a remessa (na aba processo) e fazer nova tentativa de envio.

+ Tipo de Documento
Esse erro acontece quando existe, no processo a ser remetido, um documento cujo tipo é inexistente na instância de destino. 
Para correção, deve-se, primeiro, verificar qual tipo de documento apresenta erro, pesquisando o número do id do documento na árvore processual. 
Delete a remessa e tramite o processo para a tarefa Reclassificar documentos, depois altere o tipo de documento para uma opção diferente. 
Feito isso, faça nova tentativa de remessa.

+ Falta de vinculação de Ente ou Autoridade
Esse erro acontece porque o ente ou autoridade, quando criado, foi vinculado a uma pessoa jurídica cadastrada no sistema sem CNPJ.
Para correção vá em **Configuração/Pessoa/Ente ou autoridade** do PJE da instância de origem e, após localizar a autoridade informada no erro, faça a devida vinculação na aba Formulário. Escolha uma pessoa jurídica que possua CNPJ.
Outra opção, é corrigir o cadastro da pessoa jurídica vinculada ao ente ou autoridade, incluindo o CNPJ. Isto pode ser feito em **Configuração/Pessoa/Pessoa Jurídica.**
Feito isso, é preciso deletar a remessa (na aba processo) e fazer nova tentativa de envio.

+ Expedientes abertos
Esse erro acontece quando o processo que está sendo remetido possui algum expediente em aberto. Normalmente o expediente que ainda está aberto é sem prazo.
Para correção, delete a remessa e tramite o processo para a tarefa Fechar expediente manualmente. Nela, os expedientes abertos deverão ser fechados.
Caso, ao realizar o procedimento descrito acima, não apareça nenhum expediente em aberto, vá no menu **Processo/Pesquisar/Consulta de prazos** e pesquise pelo número do processo e mais algum critério. 
Feito isso, faça nova tentativa de remessa.

+ Cadastro de pessoa
Esse erro acontece quando, na hora da remessa, por alguma instabilidade da integração com o sistema da Receita Federal, uma parte ou pessoa que assinou algum documento no processo, não consegue ser cadastrada automaticamente na instância de destino.
Para correção, basta que o Administrador do Sistema do PJE da instância de destino faça este cadastramento no menu **Configuração/Pessoa/Física** ou **Jurídica,** conforme o caso. Na opção pré-cadastro, faça o cadastro manual do CPF ou CNPJ que constar no erro e faça nova tentativa de remessa.

+ Documento de identificação
Esse erro acontece quando algum documento de identificação de uma das partes do processo está em branco. 
Para correção, retifique a atuação (aba partes), selecionando cada uma das partes e verificando, na aba documentos de identificação, os documentos constantes, procedendo às correções necessárias (verificar inclusive advogados).
Feito isso, é preciso deletar a remessa (na aba processo) e fazer nova tentativa de envio.

+ Ausência de novos documentos processuais:
Quando se tenta remeter um processo sem que tenha sido elaborado ou juntado algum documento na instância, o erro “Não foram encontrados novos documentos processuais” impede o envio. A solução consiste na elaboração de algum documento. Como sugestão, pode ser incluída uma certidão de remessa.
Feito isso, é preciso deletar a remessa (na aba processo) e fazer nova tentativa de envio.

Além destes erros tratados, existem casos em que a remessa é concluída com falhas, ou ainda, situações em que aparentemente a remessa foi feita, mas o processo não chegou ao destino. Na maior parte das vezes uma nova tentativa de remessa resolve o problema, na sequência, vamos abordar as formas de correção para estes casos.
