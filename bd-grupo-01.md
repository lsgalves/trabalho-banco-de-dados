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
| id             | integer |         | not null | PK AI  |         |
| descricao      | varchar | 200     | not null |        |         |
| valor          | numeric | 15,2    | not null |        |         |
| id_cliente     | integer |         |          | FK     |         |
| id_funcionario | integer |         |          | FK     |         |
| id_usuario     | integer |         |          | FK     |         |
| id_pagamento   | integer |         |          | FK     |         |
| id_satisfacao  | integer |         |          | FK     |         |

### Reputação

| campo                | tipo    | tamanho | nulo     | indice | default |
| -------------------- | ------- | ------- | -------- | ------ | ------- |
| id                   | integer | 100     | not null | PK AI  |         |
| id_mesa              | integer |         | not null | FK     |         |
| data                 | date    |         | not null |        |         |
| primeira_vez_aqui    | integer | 1       |          |        | 'S'     |
| nota_atendimento     | integer | 1       |          |        |         |
| nota_estabelecimento | integer | 1       |          |        |         |
| nota_refeicao        | integer | 1       |          |        |         |
| nota_preco           | integer | 1       |          |        |         |
| preco_melhor_onde    | varchar | 150     |          |        |         |

### Financeiro

| campo                 | tipo    | tamanho | nulo     | indice | default |
| --------------------- | ------- | ------- | -------- | ------ | ------- |
| id                    | integer |         | not null | PK AI  |         |
| numero_transacao      | integer |         | not null |        |         |
| id_caixa              | integer |         |          | FK     |         |
| id_total_caixa        | numeric | 7,2     |          | FK     |         |
| numero_contas_pagar   | double  |         |          | FK     |         |
| numero_contas_receber | double  |         |          | FK     |         |
| despesas              | double  |         |          |        |         |
| salario_funcionario   | numeric | 5,2     |          | FK     |         |
| numero_vendas         | integer |         |          | FK     |         |

### Clientes

| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | integer |         | not null | PK AI  |         |
| nome            | varchar | 100     | not null |        |         |
| endereco        | varchar | 200     | not null |        |         |
| data_nascimento | date    |         |          |        |         |
| telefone        | varchar | 11      |          |        |         |
| celular         | varchar | 11      |          |        |         |
