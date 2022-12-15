---
title: "Orientações para administradores"
date: 2022-11-29T16:27:17-03:00
---

+ O escopo das alterações dentro do PJe foi delimitado pela pendência Jira PJeII-21789.
+ Para configurar o sistema para aceitar o recurso interno, o administrador deve acessar a configuração da classe recursal e marcá-la como Recursal e adicionar a informação de natureza da classe como RECURSO INTERNO, bem como vincular essa classe a um fluxo e cadastrar o tipo de documento da petição inicial com o tipo de petição do recurso em questão. O fluxo associado será, em geral, o fluxo originárias.
+ O administrador deve também se certificar que o tipo de documento pode ser submetido por usuários externos (vinculação Suficiente ao papel advogado). Além disso o fluxo FLX_REGISTRAR_RECURSO deve estar associado ao tipo de documento.
+ O sistema sempre se comportará de forma a exibir o caderno processual principal por padrão, salvo no painel do usuário e nas telas de sessão, que abrirão os autos relacionados ao caderno que estiver em utilização.
+ Na consulta processual, o sistema não retornará todas as capas por padrão. Para que seja o padrão retornar todas as capas, o usuário deve estar vinculado ao papel “pje:papel:retornaRecursoInterno”.
+ A exclusão de uma capa poderá ser realizada pelo usuário que estiver vinculado ao papel “pje:papel:removeRecursoInterno”.
+ O sistema exibirá, a partir dos autos digitais, a aba Recursos e Sessões que exibe todas as capas vinculadas àquele processo e sessões em que foram pautadas. A aba será exibida para o usuário vinculado ao papel “pje:papel:pesquisaRecursoInterno”.
