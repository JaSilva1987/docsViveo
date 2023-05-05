---
sidebar_position: 2
---

# Terminologia

Terminologia é o conjunto de vocábulos próprios utilizado na **VIVEO** para identificação dos processos relacionados a camada de integração.

## Cliente

Geralmente utilizado para se referir a um potencial usuário da API

## Servidor

Responsável por recebe e processar as requisições enviadas pelos clientes retornando uma resposta de sucesso ou falha

## Recurso

Um recurso pode ser qualquer objeto sobre o qual a API possa oferecer informações.

#### Exemplo

Caso de uma API do Twitter, um recurso pode ser um usuário, hashtag ou qualquer tipo de mídia como uma imagem. Todo recurso possui um identificador distinto que pode ser um nome ou número

## URI

URI (Uniform Resource Identifier) – é um identificador utilizado para denominar um recurso facilitando o seu uso, dentro da API esse recurso deve possui uma URI única.

### Definindo uma URI

Dentro da nossa estrutura do FLOW API podemos ter a necessidade de ter uma URI de order para o ERPProtheus e ISOCRM, dessa forma a URI deverá ser única, mas identificando facilmente o seu objetivo.

- URL/erpProtheus/order
- URL/isoCrm/order

Note que entre a URL e o termo order temos o caminho da pastas indicando o objetivo do endpoint que será complementado com a verbalização seguindo o padrão API Restful.

## RestFul

REST não é um protocolo ou padrão, mas sim um conjunto de restrições de arquitetura.
Quando um cliente faz uma solicitação usando uma API RESTful, essa API transfere uma representação do estado do recurso ao solicitante ou endpoint. Essa informação (ou representação) é entregue via HTTP utilizando um dos vários formatos possíveis: Javascript Object Notation (JSON), HTML, XLT, Python, PHP ou texto sem formatação. O formato JSON é a linguagem de programação mais usada porque, apesar de seu nome, é independente de qualquer outra linguagem e pode ser lido por máquinas e humanos.

### Verbos API Rest

Quando começamos a desenvolver – ou consumir - nossos primeiros serviços RESTful, a primeira coisa que precisamos entender é o papel dos verbos HTTP dentro do contexto REST.

#### GET

Utilizado quando existe a necessidade de se obter um recurso(obter/pegar dados)

#### POST

Utilizado para a criação de um recurso a partir do uso de uma representação

#### PUT

utilizado como forma de atualizar um determinado recurso.

#### DELETE

tem como finalidade a remoção de um determinado recurso

#### PATCH

solicita alteração parcial de um determinado recurso
