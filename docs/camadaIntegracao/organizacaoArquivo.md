---
sidebar_position: 4
---

# Organização dos Arquivos

A API foi divida em duas partes macros seguindo a orientação da documentação do moleculer. Essas duas partes foram organizadas como pastas: service e src(Source)

## services

Essa pasta é default do framework utilizada para organizar todos os serviços/microserviços criados no sistema.

As pastas dentro de service são criadas com o nome do sistema e as subpastas com o nomes dos processos macros. Exemplo de estrutura da pasta service.

```shell
  services
  ├── alcis
  │   └── consumer
  │   └── healthCheck
  │   └── invoice
  │   ...
  ├── climba
  │   └── attributes
  │   └── brand
  │   ...
  ├── erpProtheus
  │   └── expressa
  │   │  └── custome
  │   │  └── invoice
  │   │  ...
  │   └── viveo
  │   │  └── category
  │   │  └── order
  │   │  ...
  ├── README.md
  └── CHANGELOG.md
  ...
```

- A pasta **erpProtheus** é a unica excessão na estrutura, possui uma camada subpasta indicando o sistema/empresa e dentro dessas pastas temos as pastas de processos

## src(Source)

Utilizada na organização e implementação dos controllers, entities, repositories e etc. Nessa pasta será encontrado os arquivos auxiliares utilizados pelos serviços.
