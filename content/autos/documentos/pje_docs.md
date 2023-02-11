---
title: "PJe Docs"
date: 2023-01-17T19:20:19-03:00
weight: 8
---
O PJe Docs criou novos filtros (diferentes critérios) para download de processos e, no arquivo pdf gerado, foi adicionado uma marca d’água de Sigiloso quando o 
processo/documento tiver sigilo. Para processos sigilosos, a marca d'água aparece em todos os documentos. Quando apenas alguns documentos do processo são sigilosos, só esses terão a marcação de sigiloso.

Também foi acrescentada a informação, no rodapé da página, de quem foi o usuário responsável pelo download (“Este documento foi gerado pelo usuário 000.***.***-
00 em DD/MM/AAAA HH:MM:SS).

Quando o usuário solicita o download dos autos de um processo ou de alguns documentos deste, o PJe adota dois comportamentos, conforme o tamanho do arquivo a ser baixado.

## Download síncrono

Sempre que o documento tiver um tamanho de até 50Mb, o download será processado de forma síncrona, ou seja, será realizado na hora da solicitação.

## Download assíncrono

Quando o documento tiver um tamanho superior a 50Mb, o download será processado de forma assíncrona, ou seja, será será enviado para uma fila de processamento e disponibilizado para baixar na opção **Área de download** após a conclusão do processamento.

O usuário receberá uma mensagem de alerta, informando que documento será gerado e disponibilizado no menu **Download - Área de download.**

A permissão de acesso a página Download/Área de download é configurável por meio da funcionalidade **Configuração - Controle de acesso - Funcionalidades.**

Na Área de download são listados todos os processos que tiveram o download realizado de forma assíncrona, exibindo a data de expiração e a situação do download, que pode ser:
+ Concluído: Um ícone azul, com uma seta, indica que os docuementos estão prontos para serem baixados;
+ Na fila de processamento - indica que está aguardando ser processado;
+ Processando... – indica que já está em processamento.

Apenas após a conclusão do processamento, quando o usuário clicar no ícone azul com a seta, o documento será baixado.
