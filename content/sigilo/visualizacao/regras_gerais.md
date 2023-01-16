---
title: "Regras gerais"
date: 2023-01-16T10:49:43-03:00
weight: 1
---
No protocolo inicial do processo, de acordo com a classe e os assuntos cadastrados, o sistema utilizará os níveis de sigilo para estabelecer os visualizadores do processo.

É importante ressaltar a diferença entre servidores/magistrados e partes do processo/usuários externos:

+ Para servidores/magistrados, a visualização é determinada pelo nível de sigilo do processo. Se o servidor/magistrado não tiver permissão para visualizar pelo nível do processo, terá que ser incluído como visualizador.
+ Para partes do processo/usuários externos, a visualização sempre se dará de acordo com o cadastro na lista de visualizadores.

Deste modo, o servidor somente consegue enxergar nas tarefas os processos cujos níveis de sigilo são compatíveis com seu respectivo nível de acesso ou aqueles em que seja cadastrado como visualizador. Além disso, para fins de abertura dos autos digitais, o usuário precisará ser visualizador do processo ou:
+ ter o mesmo nível do processo ou maior; e
+ ser do mesmo órgão julgador do processo ou, caso não tenha órgão julgador,
+ ser do mesmo órgão julgador colegiado; e
+ se estiver vinculado a um cargo (magistrados são sempre vinculados ao cargo), deve ser o cargo responsável pelo processo ou ter a visibilidade “Todos” no cadastro do órgão julgador.

{{% notice warning %}}
Cuidado! Partes posteriormente incluídas no processo tem a visualização liberada automaticamente.
{{% /notice %}}

No ato de comunicação a parte citada/intimada é automaticamente adicionada como visualizadora.

A alteração do nível de sigilo não modifica as permissões de visualização já concedidas no processo. 

A marcação de uma parte como sigilosa faz com que essa parte não fique mais visível pelo polo contrário, mas não a impede de visualizar o processo sigiloso.
