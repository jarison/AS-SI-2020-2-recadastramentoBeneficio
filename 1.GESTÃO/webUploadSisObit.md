---
id: webUploadSisObit
title: Upload de arquivo SisObit
sidebar_label: Upload de arquivo SisObit
---

*Este artefato tem como objetivo especificar uma funcionalidade de um sistema, de forma a transcrever as necessidade do usuário aos desenvolvedores do projeto, assim como para basear a realização de testes e homologação.*

## Épico
> Com o recebimento mensal do arquivo sisobit, onde lista os registros cartorários de óbitos em território nacional, torna-se possível automatizar a realização de atualização cadastral e da extinção de benefícios de segurados falecidos. Esta funcionalidade tem como objetivo realizar o upload do arquivo, inserindo o mês e ano de referência do mesmo. Com a inserção, o sistema executará um serviço de identificação de registros no arquivo que estão na base cadastral da GoiásPrev, gerando um relatório contendo as extinções de benefícios executados automaticamente em aqueles que atenderem os requisitos, será contido também neste relatório aqueles que necessitam de confirmação por auditoria e, por último, será inserido no relatório as duplicatas inconsistentes que, também necessitará de uma análise por auditoria.
> O novo sistema SIRC trouxe uma resolução que demanda a inclusão de algumas RNs que trazem alguns requisitos não-funcionais de segurança e de acesso, esta funcionalidade deve-se atentar a estas regras linkadas ao final deste artefato.

## Pré Condições
> 1. Estar logado no sistema;
> 2. Ter permissão de acessa a tela;

## Atores
> + Usuário

## Fluxo Básico - Realizar Upload de Arquivo
![]()
> 1. Usuário após realizar [**Login**](../../sa/webLogin.md) no sistema clica no ítem "Arquivo Sisobit" no menu lateral;
> 2. Sistema exibe a tela de upload de arquivo Sisobit;
> 3. Usuário clica no botão selecionar arquivo;
> 4. Sistema abre seletor de arquivos no computador do Usuário;
> 5. Usuário seleciona arquivo SisObit a ser carregado;
> 6. Sistema valida extensão do arquivo e autopreenche o campo referência caso consiga; [RN087](../regrasNegocio#rn087---extensões-aceitas-para-upload-de-arquivo-sisobit) [RN088](../regrasNegocio#rn088---autopreenchimento-de-referência-de-arquivo-sisobit) [RN089](../regrasNegocio#rn089---upload-de-arquivo-sisobit-com-referência-pré-existente) [RN090](../regrasNegocio#rn089---upload-de-arquivo-sisobit-com-referência-pré-existente)

## Fluxo de Exceção 1 (EX01) - Extensão não permitida
![]()
> 1. Sistema detecta no passo 6 do fluxo básico que o arquivo inserido não atende a regra de de upload de arquivos [RN090](../regrasNegocio#rn089---upload-de-arquivo-sisobit-com-referência-pré-existente) e exibe a mensagem de erro;
> 2. Usuário visualiza a mensagem;
> 3. Fim do fluxo;

## Legislação base
> + [Resolução Nº4/2019 - SIRC](http://www.sirc.gov.br/static/arquivos/resolucao_04_sirc.pdf) DOU publicado em 05/07/2019

## Valores
```
Referencia = Data[MM/AAAA];
```

## Regras de Negócio
+ [RN087 - Extensões aceitas para upload de arquivo SisObit](../regrasNegocio#rn087---extensões-aceitas-para-upload-de-arquivo-sisobit)
+ [RN088 - Autopreenchimento de referência de arquivo SisObit](../regrasNegocio#rn088---autopreenchimento-de-referência-de-arquivo-sisobit)
+ [RN089 - Upload de arquivo SisObit com referência pré-existente](../regrasNegocio#rn089---upload-de-arquivo-sisobit-com-referência-pré-existente)
+ [RN090 - Processamento do arquivo SisObit](../regrasNegocio#rn090---processamento-do-arquivo-sisobit)
+ [RN091 - Detecção confirmada na base cadastral](../regrasNegocio#rn091---detecção-confirmada-na-base-cadastral)
+ [RN092 - Detecção a confirmar na base cadastral](../regrasNegocio#rn092---detecção-a-confirmar-na-base-cadastral)
+ [RN093 - Detecção de duplicata de registros idênticos](../regrasNegocio#rn093---detecção-de-duplicata-de-registros-idênticos)
+ [RN094 - Detecção de duplicata com registros diferentes ou inconsistentes](../regrasNegocio#rn094---detecção-de-duplicata-com-registros-diferentes-ou-inconsistentes)
+ [RN095 - Registro de Óbito automático por detecção confirmada no SisObit](../regrasNegocio#rn095---registro-de-óbito-automático-por-detecção-confirmada-no-sisobit)
+ [RN096 - Relatório de Processamento de arquivo SisObit](../regrasNegocio#rn096---relatório-de-processamento-de-arquivo-sisobit)