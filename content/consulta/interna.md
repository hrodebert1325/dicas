---
title: "Consulta interna"
date: 2022-11-29T16:19:55-03:00
menuTitle: "Interna"
weight: 5
---

A **Consulta de Processos** disponiveis para usuários logados pode ser acessada pelo menu **Processo - Pesquisar - Processo** (você também pode utilizar o acesso rápido para digitar a expressão de busca):

IMAGEM_CONSULTA_1

Também é possível acessar a consulta pelo ícone da **lupa** disponível no **Painel do Usuário:**

IMAGEM_CONSULTA_2

A tela da consulta exibe uma variedade de campos de pesquisa, livres e tabelados, que podem ser utilizados de maneira isolada ou em conjunto, para filtrar o processo ou grupo de processos de acordo com os critérios desejados:

IMAGEM_CONSULTA_3

+ Consulta de processos para servidor de outra instância:

No PJe 1G há um perfil de servidor chamado **Consulta de processos para servidor,** exclusivamente para consulta, não sendo possível consultar processos sigilosos. 

O cadastro dos usuários vinculados a esse perfil deve ser feito pela funcionalidade **Configuração - Pessoa - Servidor,** selecionando apenas a Localização Física (Estado) e o opção Papel (Consulta de processos para servidor):

IMAGEM_CONSULTA_4

Nos TREs, os administradores locais podem criar um perfil semelhante em **Configuração - Controle de Acesso - Papéis.**

Basta Criar um novo papel com o nome Consulta de processos para servidor de outra instância, utilizando o identificador consulta. Na aba **Herdeiros** desse papel, deve ser vinculado o papel Colaborador e, na aba **Recursos**, deve ser associado o recurso Página Processo/Consulta/Consulta de Processo.

O cadastro dos usuários vinculados ao perfil é feito em **Configuração - Pessoa - Servidor,** da forma descrita acima, sendo que no PJe2G o preenchimento do campo **Órgão julgador colegiado** é facultativa:

IMAGEM_CONSULTA_5
