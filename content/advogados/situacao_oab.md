---
title: "Situação da Inscrição na OAB"
date: 2022-11-23T17:26:41-03:00
menuTitle: "Situação OAB"
---

No cadastramento inicial, o PJe utiliza o número do CPF para consultar o Cadastro Nacional dos Advogados (CNA). São retornadas inscrições de advogados, suplementares e de estagiários, mas apenas as inscrições em situação regular são consideradas.

Caso não exista inscrição ativa, o sistema exibirá uma mensagem informando que foram recuperadas informações no CNA, mas não há inscrição ativa, permitindo que o usuário prossiga o cadastro como Jus Postulandi.

No entanto, não existe impedimento técnico no sistema para que um usuário interno do tribunal torne essa pessoa um advogado e confirme seu credenciamento, mesmo sem número de inscrição na OAB. Nesse caso, somente na retificação de autuação será mostrada a situação da inscrição do advogado, e apenas para usuários internos:

![Situação OAB](/imagens/situacao_adv_tela_retificacao.png)

Caso o advogado possua mais de uma inscrição regular, a informação acima é baseada apenas na primeira OAB encontrada no momento do cadastramento (em geral a OAB principal), ignorando-se as demais, o que pode não refletir a exata situação cadastral do advogado.

{{% notice warning %}}
A Importante ressaltar que os dados apresentados tem apenas caráter informativo, mesmo que em situação irregular.
{{% /notice %}}

IMPORTANTE: Um advogado com a situação regular no momento do cadastro no PJe e que posteriormente teve sua inscrição cancelada e/ou tornada irregular, continua como regular no sistema até que um usuário interno do PJe, a partir da funcionalidade **Confirmar credenciamento,** utilize o botão **nova validação na OAB** para atualizar os dados do advogado.

Desse modo, a situação da inscrição da OAB do advogado causa impedimento apenas no momento do cadastro inicial do usuário. Uma vez cadastrado no sistema como advogado e independentemente da situação da inscrição em momento posterior, nenhum outro impedimento é feito.

Ou seja, é permitido ao advogado protocolizar novos processos, juntar documentos e inclusive solicitar habilitação nos autos, mesmo que em situação irregular.

{{% notice info %}}
Já existem demandas (PJEVII-4416, PJEVII-3889, PJEVII-3173 e PJEVII-4536) em andamento no Conselho Nacional de Justiça (CNJ) que visam melhorias na funcionalidade e desenvolvimento de alertas para advogados penalizados.
{{% /notice %}}
