---
title: "Variáveis"
date: 2022-11-23T17:57:39-03:00
weight: 7
---

Variável recupera parte formatada:

`#{processoJudicialAction.recuperarParteFormatada(true, true, ‘A’, ‘P’, ‘T’)}`

Esta variável permite que se recupere os nomes das partes do processo e os respectivos tipos, juntamente com os advogados. 

Pode-se recuperar os advogados com o número da OAB ou não.

Pode-se recuperar em formato de tabela (alinhado) ou não (alinhamento pode ter alguma variação, mas não causará problemas na publicação do Diário antigo).

Pode-se recuperar todos os polos ou especificar quais deseja. 

A variável retorna o nome social, caso tenha sido cadastrado. 

Se a parte for sigilosa, retorna “Em segredo de justiça” em lugar do nome da parte. 

Ao utilizar a expressão acima em modelos de documentos, o documento resultante será construído exibindo, no lugar da expressão, as partes do processo junto com representantes advogados em linhas separadas e com colunas alinhadas, de forma que sejam exibidos os nomes dos tipos de parte respectivos junto com os nomes das partes. Para o caso de advogados, o alinhamento é feito de forma que o advogado fique vinculado à parte que ele representa.

Utilizando diferentes parâmetros entre os parênteses, pode-se alterar o que será retornado:
+ o primeiro item dentro dos parênteses indica se a resposta virá dentro de uma tabela (true) ou fora (false); 
+ o segundo item indica se,  quando houver advogados, deve ser exibida a OAB (true) ou não (false); 
+ o terceiro item “A” informa que devem ser retornadas as partes do polo ativo; 
+ o quarto, “P” informa que devem ser retornadas as partes do polo passivo; 
+ o quinto, “T” informa que devem ser retornadas os terceiros cadastrados no processo.

A variável pode ser utilizada em modelos de documentos utilizados em tarefas e também no juntar documentos dos autos digitais, comportando diversas formas de configuração, conforme explicações acima.
