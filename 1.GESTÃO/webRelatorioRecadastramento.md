---
id: webRelatorioRecadastramento
title: Relatório Gerencial de Recadastramento
sidebar_label: Relatório Gerencial
---

*Este artefato tem como objetivo especificar uma funcionalidade de um sistema, de forma a transcrever as necessidade do usuário aos desenvolvedores do projeto, assim como para basear a realização de testes e homologação.*

## Épico
> O módulo deve emitir relatório do status do recadastramento de beneficiários, permitindo filtro por tipo de benefício, período com data de início (mês/ano) e data de fim (mês/ano), residencial (dentro ou fora de Goiás), status do recadastramento (ativo, bloqueado ou extinto) e quantidade de meses bloqueados. Os campos do relatório serão: Status de Recadastramento, CPF, Nome, Aniversário, Tipo de Benefício e Meses Bloqueados.

## Pré Condições
> 1. Estar logado no sistema;
> 2. Ter permissão de acessa a tela;

## Atores
> + Administrador de Cadastro;

## Fluxo Básico - Emitir Relatório Gerencial de Recadastramento
![Protótipo 01](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRelatorioGerencial.png) *Protótipo de tela de Emitir Relatório Gerencial de Recadastramentos na versão web*
![Protótipo 02](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRelatorioGerencialFiltro.png) *Protótipo de tela de Emitir Relatório Gerencial de Recadastramento com filtros aplicados na versão web*
![Protótipo 03](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRelatorioGerencialResultado.png)
*Modelo de Relatório Gerencial de Recadastramento*
> 1. Administrador de Cadastro clica no botão "Relatório Gerencial de Recadastramento", no Menu Esquerdo da tela;
> 2. Sistema carrega a tela de Relatório Gerencial de Recadastramento os ítens:
>       + Combo de seleção de ítens de filtro;
>       + Combo de seleção de campos a serem visualizados;
>       + Botão de adição de campos;
>       + Botão de busca de resultado;
>       + Botão de geração de relatório;
> 3. Administrador de Cadastro seleciona e preenche os filtros contidos no relatório:
>       + CPF do Beneficiário;
>       + Nome do Beneficiário;
>       + Data de Aniversário do Beneficiário;
>       + Tipo de Benefício [Igual a / Diferente de], [Lista Tipo de Benefício];
>       + Período [Data Início / Data Fim];
>       + Residência [Dentro da UF / Fora da UF];
>       + Status Recadastramento [Lista tipo status Recadastramento];
>       + Meses de Bloqueio [Maior que / Menor que], [Lista quantidade de meses];
> 4. Administrador de Cadastro clica no botão "Buscar" para filtrar resultado;
> 5. Sistema exibe resultado bom base no filtro selecionado pelo Administrador de Cadastro;
> 6. Administrador clica no botão "Salvar Relatório";
> 7. Sistema inicia o download do relatório em formato.pdf e o abre em uma nova guia para visualização;
> 8. Usuário visualiza o relatório em nova aba;
> 9. Fluxo retorna para passo 5 deste fluxo;

## Valores
```
CPF = Numérico (cpf)[11];
Nome do Beneficiário = Alfanumérico [150];
Data de Aniversário do Beneficiário = Data [DD/MM/AAAA];
Tipo de Benefício = Lista [Todos os benefícios, Aposentadoria, Pensão];
Período Inícial = Data [DD/MM/AAAA]
Período Final = Data [DD/MM/AAAA]
Residência = Switch [Dentro da UF, Fora da UF];
Situacao Beneficio = Lista [Ativo, Bloqueado, Suspenso, Cancelado, Extinto];
Meses de Bloqueio = Numérico [3];
```

## Regras de Negócio
+ 
