---
title: "Como atribuir níveis de sigilo aos processos"
date: 2023-01-16T10:49:43-03:00
menuTitle: "Atribuir nível"
weight: 2
---
A atribuição dos níveis de sigilo depende de configuração realizada pelo administrador do sistema, previamente à entrada do processo no PJe.

Tal configuração é feita no item de menu **Cadastro de nível de acesso por competência (Configuração – Competência – sigilo)**, por meio da competência x classe x assunto (o nível de segredo das classes e assuntos processuais foram decididos em reunião do grupo de trabalho).

A definição do nível de segredo leva em conta a combinação de classe com o assunto processual. Nesse contexto, é possível existir uma classe processual sem nível específico de sigilo com assunto processual que possua segredo, caso em que o processo terá segredo em razão do assunto processual e não da classe. O inverso também é viável.

O nível da classe ou assunto será, no mínimo, 1. 

Em caso de haver uma combinação em que a classe é nível 1, mas o assunto é nível 3, prevalecerá o nível 3.

Assim, quando uma classe é considerada pública (prestação de contas, por exemplo), o advogado pode pedir sigilo, marcando Sim na opção **Segredo de Justiça,** na Aba Características. 

{{% notice warning %}}
Ainda que a combinação classe X assunto tenha configurada o nível 5 como padrão, o processo protocolado naquela combinação só será sigiloso se o usuário protocolador assim o solicitar (é necessário atribuir sigilo ao processo, após a atribuição do sigilo é que o sistema o classifica em níveis, conforme a configuração).
{{% /notice %}}

Regras importantes:
+ O usuário que peticiona não escolhe o nível de segredo do processo, isso é configurado pelo administrador do sistema;
+ Para que ao processo seja atribuído o nível de segredo que se deseja, é necessário escolher adequadamente a classe e o assunto processual.
