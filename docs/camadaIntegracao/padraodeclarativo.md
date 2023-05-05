---
sidebar_position: 3
---

# Padrão declarativo

Para manter um entendimento e uma escrita padronizada em toda aplicação utilizamos alguns padrões declarativos para facilitar o entendimento.

## CamelCase

Começar com a primeira letra minúscula e a primeira letra de cada nova palavra subsequente maiúscula

```bash
dataNascimento

coisasParaFazer

valorInicial

dataFinal

idadeDoAmigo
```

## PascalCase

Conhecido como “upper camel case” ou “capital case”, pascal case combina palavras colocando todas com a primeira letra maiúscula

```bash
DataNascimento

CoisasParaFazer

ValorInicial

DataFinal

IdadeDoAmigo
```

## SnakeCase

Conhecido também como “underscore case”, utilizamos underline no lugar do espaço para separar as palavras

```bash
data_nascimento

coisas_para_fazer

valor_inicial

DATA_FINAL

idade_do_amigo

PRIMEIRO_NOME
```

## KebabCase

Utiliza o traço para combinar as palavras. Quando o kebab case está em caixa alta, ele é chamado de “screaming kebab case”

```bash
data-nascimento

coisas-para-fazer

valor-inicial

DATA-FINAL

idade-do-amigo

PRIMEIRO-NOME
```

## Pastas

As pastas devem ser criadas de acordo com o sistema e domínio/processo de atuação utilizando o camelCase.

### Exemplo

Foi solicitado a integração de ordens de Compra geradas no sistema BrasilCRM com o ERPProtheus, como as pastas não existem iremos seguindo o padrão camelCase.

```shell
  services
  ├── brasilCRM
  │   └── order
  src
  ├── controller
  ├── entity
  ├── repository
  │   └── brasilCrm
  │   │  └── order
  ...
```

## Arquivos

Os arquivos e pastas devem ser criados utilizando o padrão camelCase, seguindo as particularidades de cada pasta, já mencionado em orginazação de arquivos

### Service

Os arquivos criados na pasta service, devem estar dentro da pasta do seu sistema/domínio tendo ao final do nome o prefixo **service.ts** como extensão

Exemplo:

```shell
  services
  ├── erpProtheus
  │   └── expressa
  │   │  └── custome
  │   │  └── invoice
  │   │  ...
  │   └── viveo
  │   │  └── category
  │   │  │  └── category.service.ts
  │   │  └── order
  │   │  │  └── orderFuncional.service.ts
  │   │  │  └── saveOrder.service.ts
  │   │  ...
  ...
```

### src(Source)

Dentro da pasta source temos outras pastas onde cada uma possui sua extensão própria de acordo com a função designada.

Exemplo:

```shell
  services
  ├── controller
  │   └── integration
  │   │  └── consumer
  │   │  │  └── consumer.controller.ts
  │   │  └── order
  │   │  │  └── orderFuncional.controller.ts
  │   │  ...
  ├── entity
  │   └── integration
  │   │  └── productEcommerce.entity.ts
  │   │  └── stockPfs.entity.ts
  │   │  ...
  ├── interface
  │   └── integration
  │   │  └── order
  │   │  │  └── productEcommerce.interface.ts
  │   │  │  └── stockPfs.interface.ts
  │   │  ...
  ├── repository
  │   └── integration
  │   │  └── order
  │   │  │  └── productEcommerce.repository.ts
  │   │  │  └── stockPfs.repository.ts
  │   │  ...
  ...
```

## Criação de Classes

As classes criadas dentro da aplicação devem utilizar o padrão PascalCase, tendo a primeira letra de cada nome em maiúsculo.

```tsx
export default class OrdersFuncionalBusinessRule {
	broker: ServiceBroker;
	isRequest: string;
	mountingResponse: object;
	mountingMResponse: object;
	mountingEResponse: object;
  ...
```

## Declaração de Variaveis

let e const são dois conceitos relativamente novos para declarações de variáveis em JavaScript, let é similar a var em alguns aspectos, mas evita que alguns usuários caiam em momentos “te peguei” no JavaScript.
const é uma ampliação de let no qual previne reatribuições a uma variável.
Com TypeScript sendo uma extensão de JavaScript, a linguagem naturalmente suporta let e const, e todas as variáveis utilizandas dentro do novo Framework deve utilizar os padrões apresentados.

A declaração das variáveis deve ser realizada seguindo o padrão camelCase sempre acompanhado do tipo de dados, segue exemplo:

```tsx
let firstName: string;
let numberAddress: number;
```

Tambem podemos declarar as variáveis já definindo os valores.

```ts
const companyName: string = “Viveo Empresas”
const port: number = 3002
```

### Utlizando Interfaces

Interfaces, nas palavras mais simples, descrevem a estrutura do objeto, o que significa que descreve como o objeto deve se parecer. Dentro TypeScript, podemos trabalhar com “Interfaces”. No TypeScript, uma interface contém apenas a definição de métodos e propriedades, não sua implementação.

```ts
const configCrmIso: IConfigLogCrmIso = {};

let configCrmIso: IConfigLogCrmIso;
configCrmIso = {};
```

Interface

```ts
export interface IConfigLogCrmIso {
  id?: number;
  orderId: string;
  name: string;
  status: string;
  description: string;
  dateTimeSav: Date;
  dateTimeEvt: Date;
  branchId: string | null;
  orderIdERP: string | null;
  errorType: number | null;
  userViewer: string | null;
}
```
