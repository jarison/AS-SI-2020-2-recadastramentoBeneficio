---
id: webAgendamentoBloqueio
title: Agendamento de Bloqueios
sidebar_label: Agendamento de Bloqueios
---

*Este artefato tem como objetivo especificar uma funcionalidade de um sistema, de forma a transcrever as necessidade do usuário aos desenvolvedores do projeto, assim como para basear a realização de testes e homologação.*

## Épico
> Esta tela tem como objetivo parametrizar a data de execução do serviço de agendamento de bloqueios de aposentadorias e pensões de beneficiários que não realizaram recadastramento dentro do período determinado pelo calendário. A data inserida neste parâmetro será a data de execução do serviço bloqueará o(s) benefício(s) e enviará um email com a lista de bloqueados para a área responsável.

## Pré Condições
> 1. Estar logado no sistema;
> 2. Ter permissão de acessa a tela;

## Atores
> + Administrador de Benefício;

## Fluxo Básico - Realizar Recadastramento
![Protótipo 01](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoInicial.png) *Página de Agendamento de Bloqueios*

> 1. Administrador de Benefício após realizar [**Login**](../../sa/webLogin.md) no sistema clica no ítem "Agendamento de Bloqueios" no menu lateral;
> 2. Sistema exibe a tela Agendamento de Bloqueios;
> 3. Administrador de Benefício insere a data que o serviço executará a rotina e clica no botão "Salvar";
> 4. Sistema emite alerta de confirmação da alteração do parâmetro;
> 5. Usuário confirma a alteração do registro [MSG013](../listaMensagens#msg013);
> 4. Sistema grava o parâmetro e executa todo mês, no dia registrado o serviço de agendamento de bloqueios;

## Valores
```
Data de agendamento* = Numérico[2];
```

## Regras de Negócio
+ [**RN070**](../regrasNegocio#rn070---agendamento-de-bloqueios-e-suspensões)
