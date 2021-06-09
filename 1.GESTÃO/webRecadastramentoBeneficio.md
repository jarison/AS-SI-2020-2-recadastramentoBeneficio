---
id: webRecadastramentoBeneficio
title: Recadastramento de Benefício
sidebar_label: Recadastramento de Benefício
---

*Este artefato tem como objetivo especificar uma funcionalidade de um sistema, de forma a transcrever as necessidade do usuário aos desenvolvedores do projeto, assim como para basear a realização de testes e homologação.*

## Épico
> O Módulo Censo deverá tratar da manutenção bem como da atualização do status de benefício(s) de Segurados através do cruzamento de dados com sistemas terceiros. 
> A funcionalidade Recadastramento de Benefícios deve permitir o recadastramento, indiferente de qual seja o benefício, desde que esteja habilitado para tal, podendo ou não ser através de um representante legal, de acordo com o Art. 19 da LC 77/2010. Também deve ser possível consultar o histórico de recadastro do beneficiário bem como retificar informações do último recadastro feito, desde que esteja dentro do prazo limite permitido de retificação.

## Pré Condições
> 1. Estar logado no sistema;
> 2. Ter permissão de acessa a tela;

## Atores
> + Atendente;

## Fluxo Básico - Realizar Recadastramento
![Protótipo 01](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoInicial.png) *Protótipo de tela 01 - Página inicial do Módulo Censo na versão web*

![Protótipo 02](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoBusca.png) *Protótipo de tela 02 - Resultado da busca de Beneficiário na versão web*

![Protótipo 03](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoAposentadoria.png) *Protótipo de tela 03 - Formulário de Recadastro de Aposentadoria na versão web*

![Protótipo 04](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoPensaoAposentadoria.png) *Protótipo de tela 04 - Formulário de Recadastro de Pensão e Aposentadoria*

![Protótipo 05](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoPensaoAposentadoria2.png) *Protótipo de tela 05 - Formulário preenchido de Recadastro de Pensão e Aposentadoria*

![Protótipo 06](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/modeloComprovanteCenso.png) *Modelo de Comprovante de Recadastramento (censo)*

> 1. Atendente realiza [**Login**](../../sa/webLogin.md) no sistema;
> 2. Sistema abre a Página inicial (Recadastramento de Benefícios - Protótipo 01) do Módulo Censo;
> 3. Atendente insere o CPF do Beneficiário(a) e clica no botão "Buscar";
> 4. Sistema valida CPF, busca na base de dados e exibe na tela as informações pessoais e benefícios ativos do respectivo Beneficiário(a) (Recadastramento de Benefícios - Protótipo 02):
>     1. Informações pessoais do Beneficiário(a):
>         + CPF;
>         + Nome completo;
>         + Sexo;
>         + Data de Nascimento;
>         + Nome completo da Mãe;
>         + Nome completo do Pai;
> 5. Atendente seleciona o(s) beneficio(s) habilitados para recadastro e clica no botão "Recadastro [ano vigente]"
> 6. Sistema abre o formulário de recadastro (Protótipo 03 ou 04), habilitando a edição de informações pessoais, Endereço cadastrado e para inserção de telefone e certidões (caso o atendente esteja recadastrando uma pensão):
>     1. Informações de Endereço:
>         + País;
>         + CEP / Zip Code;
>         + Endereço;
>         + Número;
>         + Complemento;
>         + UF;
>         + Cidade;
>         + E-mail;
>     2. Informações de Telefone:
>         + Telefone;
>         + Nome do Telefone;
>     3. Informações de Certidão:
>         + Tipo de Certidão;
>         + Número / Matrícula da Certidão;
>         + Livro;
>         + Folha;
>         + Nome do Cartório;
> 7. Atendente atualiza e preenche todos os campos obrigatórios e opcionais e clica no botão "Finalizar Recadastro";
> 8. Sistema valida campos do Formulário de Recadastramento, e exibe modal de confirmação de recadastramento do(s) benefício(s) selecionado(s)
> 9. Atendente confirma recadastramento;
> 10. realiza registro do recadastro, altera a situação de recadastramento do Beneficiário(a) e abre uma nova aba do navegador com o arquivo de Comprovante de Recadastramento (modelo de Comprovante de Recadastramento);
> 11. Atendente visualiza o documento, retorna para o sistema e clica no botão "Ok" na mensagem [MSG005](../listaMensagens#msg005) exibida, confirmando o êxito do recadastro e finalizando o recadastro do Beneficiário(a);
> 12. Sistema retorna para o passo 2 deste fluxo;

## Fluxo Alternativo 1 (FA01) - Consultar Histórico de Recadastramento do Beneficiário
![Protótipo 07](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoHistorico.png) *Protótipo de tela de Histórico de recadastramento do Beneficiário em anos anteriores na versão web*

> 1. Atendente insere o CPF do Beneficiário(a) e clica no botão "Buscar";
> 2. Sistema valida CPF, busca na base de dados e exibe na tela as informações pessoais e benefícios ativos do respectivo Beneficiário(a) (Recadastramento de Benefícios - Protótipo 02):
>     1. Informações pessoais do Beneficiário(a):
>         + CPF;
>         + Nome completo;
>         + Sexo;
>         + Data de Nascimento;
>         + Nome completo da Mãe;
>         + Nome completo do Pai;
> 3. Atendente clica no botão "Histórico" (Protótipo 02) para visualizar o Histórico de recadastro do beneficiário;
> 4. Sistema abre modal com histórico de recadastros do respectivo Beneficiário; 
> 3. Atendente clica no ícone/botão "Visualizar Comprovante" no ano desejado;
> 4. Sistema abre em uma nova aba do navegador o arquivo comprovante de recadastro do Beneficiário;
> 5. Atendente visualiza o documento, retorna a aba do sistema e clica no botão "Fechar" no modal de histórico de recadastros do Beneficiário;
> 6. Sistema retorna ao passo 4 do Fluxo Básico;


## Fluxo Alternativo 2 (FA02) - Retificar Recadastramento
> 1. Atendente insere o CPF do Beneficiário(a) e clica no botão "Buscar";
> 2. Sistema valida CPF, busca na base de dados e exibe na tela as informações pessoais e benefícios ativos do respectivo Beneficiário(a) (Recadastramento de Benefícios - Protótipo 02):
>     1. Informações pessoais do Beneficiário(a):
>         + CPF;
>         + Nome completo;
>         + Sexo;
>         + Data de Nascimento;
>         + Nome completo da Mãe;
>         + Nome completo do Pai;
> 3. Atendente clica no botão "Histórico" (Protótipo 02) para visualizar o Histórico de recadastro do beneficiário;
> 4. Sistema abre modal com histórico de recadastros do respectivo Beneficiário; 
> 5. Atendente clica no ícone/botão "Retificar Recadastramento" no último Recadastro realizado do respectivo usuário;
> 6. Sistema abre para edição o Formulário de Recadastro (Protótipo 03 ou 04) com as informações inseridas no último recadastro;
> 7. Atendente realiza a retificação, alterando informações dos campos e clica no botão "Finalizar Retificação";
> 8. Sistema valida campos do Formulário de Recadastramento, realiza registro da retificação, altera a situação de recadastramento do Beneficiário(a) de "Concluído" para "Retificado", e abre uma nova aba do navegador com o arquivo de Comprovante de Recadastramento retificado (modelo de Comprovante de Recadastramento);
> 9. Atendente visualiza o documento, retorna para o sistema e clica no botão "Ok" na mensagem [MSG006](../listaMensagens#msg006) exibida, confirmando o êxito da retificação e finalizando a retificação do recadastramento do Beneficiário(a);
> 10. Sistema retorna para o passo 2 do Fluxo Básico;

## Fluxo Alternativo 3 (FA03) - Cadastrar Representante Legal
![Protótipo 08](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoCadRepLegal.png) *Protótipo de tela de formulário de cadastro de Representante Legal na versão web*
![Protótipo 09](https://github.com/jarison/AS-SI-2020-2-recadastramentoBeneficio/blob/main/1.GEST%C3%83O/censo/webRecadastramentoRepLegal.png) *Protótipo de tela de formulário preenchido de cadastro de Representante Legal na versão web*

> 1. Atendente clica no botão "Cadastrar Representante Legal" no Formulário de Recadastramento de Benefício (passo 6 - Fluxo básico);
> 2. Sistema abre modal com Formulário de Cadastro de Representante Legal, habilitando para inserção de Informações Pessoais, Endereços, Telefone e Comprovante de representação legal:
>    1. Informações pessoais do Representante Legal:
>         + CPF;
>         + RG;
>         + Nome completo;
>         + Sexo;
>         + Data de Nascimento;
>         + Nome completo da Mãe;
>         + Nome completo do Pai;
>     2. Informações de Endereço:
>         + País;
>         + CEP / Zip Code;
>         + Endereço;
>         + Número;
>         + Complemento;
>         + UF;
>         + Cidade;
>         + E-mail;
>     3. Informações de Telefone:
>         + Telefone;
>         + Nome do Telefone;
>     4. Informações de comprovação de representação legal;
>         + Tipo de Representante Legal;
>         + Anexo de Comprovante de Representação Legal;
> 3. Atendente preenche todos os campos obrigatórios e opcionais e clica no botão "Cadastrar";
> 4. Sistema valida informações dos campos do formulário e registra representante legal no formulário de recadastramento de benefício(s) do Beneficiário;
> 5. Fluxo retorna para passo 6 do Fluxo Básico;

## Fluxo Alternativo 4 (FA04) - Editar Representante Legal
> 1. Atendente clica no botão/ícone "Visualizar Representante Legal" no formulário de recadastramento de benefício (Protótipo 03 ou 04, passo 6 do Fluxo Básico);
> 2. Sistema abre modal com o formulário com as informações do Representante Legal cadastradas;
> 3. Atendente edita as informações do Representante Legal e clica no botão "Cadastrar";
> 4. Sistema valida informações dos campos do formulário e altera o registro do Representante Legal no formulário de recadastramento de benefício(s) do Beneficiário;
> 5. Fluxo retorna para passo 6 do Fluxo Básico;

## Fluxo Alternativo 5 (FA05) - Excluir Representante Legal
> 1. Atendente clica no botão/ícone "Visualizar Representante Legal" no formulário de recadastramento de benefício (Protótipo 03 ou 04, passo 6 do Fluxo Básico);
> 2. Sistema abre modal com o formulário com as informações do Representante Legal cadastradas;
> 3. Atendente clica no botão "Excluir" e clica na confirmação da exclusão;
> 4. Sistema exclui o registro do formulário de recadastramento de benefício(s) do Beneficiário;
> 5. Fluxo retorna para o passo 6 do Fluxo Básico;

## Fluxo de Exceção 1 (EX01) - Bloqueio de Recadastramento
> 1. Atendente insere o CPF do Beneficiário(a) e clica no botão "Buscar";
> 2. Sistema valida CPF, e consta que o benefício possui data de bloqueio [RN056](#rn056---bloqueio-de-recadastro) superior a 6 meses e exibe a mensagem [MSG012](../listaMensagens#msg012);
> 3. Atendente visualiza a mensagem e clica no botão 'Limpar';
> 4. Sistema limpa os dados da tela;
> 5. Fluxo retorna para o passo 1 do Fluxo Básico;

## Legislação base
> [Lei Complementar Nº161/2020](https://legisla.casacivil.go.gov.br/api/v2/pesquisa/legislacoes/103671/pdf#:~:text=LEI%20COMPLEMENTAR%20N%C2%BA%20161%2C%20DE,GO%20e%20d%C3%A1%20outras%20provid%C3%AAncias.)
> + Seção IV, Art. 16, 17,18, 19 e 20.

## Valores
```
CPF* = Numérico (CPF)[11];
Nome Completo* = Alfanumérico [300];
Sexo* = Radio [Feminino, Masculino];
Data de nascimento* = Data [DD/MM/AAAA];
Nome Completo da Mãe = Alfanumérico [300];
Nome Completo do Pai = Alfanumérico [300];
Benefícios = Checkbox [Benefícios do segurado];
País* = Lista [países];
CEP/ZIP Code* = Numérico (CEP)[8];
Endereço* = Alfanumérico [300];
Número = Numérico[4];
Complemento = Alfanumérico [300];
UF = Lista [UF];
Cidade = Lista [Cidades];
E-Mail = Alfanumérico (e-mail)[150];
Telefone* = Numérico (Telefone)[9];
Nome Telefone = Alfanumérico [300];
Tipo de Certidão* = Lista [Nascimento, Casamento];
Número / Matrícula da Certidão = Numérico (certidão)[32]
Livro = Numérico [4];
Filha = Numérico [4];
Nome do Cartório = Alfanumérico [150];
CPF Representante Legal* = Numérico (CPF)[11];
RG Representante Legal* = Numérico [7];
Órgão expedidor = Alfanumérico [10];
Nome Representante Legal = Alfanumérico [300];
Tipo de Representante Legal = Lista [Guardião, Curador, Administrador Provisório]
Parentesco = Lista [Pai/Mãe, Avô/Avó Filho(a), Neto(a), outro];
```

## Regras de Negócio
+ [**RN053**](../regrasNegocio#rn053---documentos-obrigatórios-para-recadastramento)
+ [**RN054**](../regrasNegocio#rn054---calendário-de-recadastramento)
+ [**RN055**](../regrasNegocio#rn055---recadastramento-presencial)
+ [**RN056**](../regrasNegocio#rn056---bloqueio-de-recadastro)
+ [**RN057**](../regrasNegocio#rn057---bloqueio-de-benefícios)
+ [**RN058**](../regrasNegocio#rn058---suspensão-de-benefícios)
+ [**RN059**](../regrasNegocio#rn059---cancelamento-de-benefícios)
+ [**RN060**](../regrasNegocio#rn060---extinção-de-benefícios)
+ [**RN061**](../regrasNegocio#rn061---desbloqueio-de-benefícios)
+ [**RN062**](../regrasNegocio#rn062---informações-obrigatórias-para-recadastramento)
+ [**RN063**](../regrasNegocio#rn063---consultar-informações-de-recadastramentos-anteriores)
+ [**RN064**](../regrasNegocio#rn064---consulta-situação-de-beneficiários)
+ [**RN065**](../regrasNegocio#rn065---retificação-de-recadastramento)
+ [**RN066**](../regrasNegocio#rn066---dispensa-de-recadastro)
+ [**RN067**](../regrasNegocio#rn067---mostrar-data-de-alteração-de-situação-de-benefício)
+ [**RN068**](../regrasNegocio#rn068---representatividade-legal-para-recadastramento)
+ [**RN069**](../regrasNegocio#rn069---regra-de-seleção-de-benefícios-para-recadastramento)
