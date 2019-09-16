# Restaurante

> Objetivo: BD para um restaurante

## Grupo 01

### Integrantes

- **Tatiana Matumoto**
- Bruno Zanata
- Murilo Jubertoni
- Ranilson

### Tabelas

- Serviços
- Reputação
- Financeiro
- Clientes

### Serviços

| campo          | tipo    | tamanho | nulo     | indice | default |
| -------------- | ------- | ------- | -------- | ------ | ------- |
| id             | serial  |         | not null | PK     |         |
| descricao      | varchar | 200     | not null |        |         |
| valor          | numeric | 15,2    | not null |        |         |
| id_cliente     | integer |         |          | FK     |         |
| id_funcionario | integer |         |          | FK     |         |
| id_pagamento   | integer |         |          | FK     |         |
| id_satisfacao  | integer |         |          | FK     |         |

### Reputação

| campo                | tipo    | tamanho | nulo     | indice | default |
| -------------------- | ------- | ------- | -------- | ------ | ------- |
| id                   | serial  |         | not null | PK     |         |
| id_mesa              | integer |         | not null | FK     |         |
| data                 | date    |         | not null |        |         |
| primeira_vez_aqui    | char    | 1       |          |        | 'S'     |
| nota_atendimento     | integer | 1       |          |        |         |
| nota_estabelecimento | integer | 1       |          |        |         |
| nota_refeicao        | integer | 1       |          |        |         |
| nota_preco           | integer | 1       |          |        |         |
| preco_melhor_onde    | varchar | 150     |          |        |         |

### Financeiro

| campo                 | tipo    | tamanho | nulo     | indice | default |
| --------------------- | ------- | ------- | -------- | ------ | ------- |
| id                    | serial  |         | not null | PK     |         |
| numero_transacao      | integer |         | not null |        |         |
| id_caixa              | integer |         |          | FK     |         |
| total_caixa           | numeric | 7,2     |          |        |         |
| id_contas_pagar       | integer |         |          | FK     |         |
| id_contas_receber     | integer |         |          | FK     |         |
| despesas              | float   |         |          |        |         |
| numero_vendas         | integer |         |          | FK     |         |

### Clientes

| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| nome            | varchar | 100     | not null |        |         |
| endereco        | varchar | 200     | not null |        |         |
| data_nascimento | date    |         |          |        |         |
| telefone        | varchar | 11      |          |        |         |
| celular         | varchar | 11      |          |        |         |
