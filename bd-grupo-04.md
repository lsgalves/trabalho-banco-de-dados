# Restaurante

> Objetivo: BD para um restaurante

## Grupo 04

### Integrantes

- **Bruno Postingel**
- Bruno Duarte
- Caio
- Gabriel Gimenez
- Pedro Cruz

### Tabelas

- Vendas
- Contas a pagar
- Contas a receber
- Formas de pagamento

### Vendas

| campo          | tipo    | tamanho | nulo     | indice | default |
| -------------- | ------- | ------- | -------- | ------ | ------- |
| id             | serial  |         | not null | PK     |         |
| idfuncionario  | integer |         | not null | FK     |         |
| idmesa         | integer |         | not null | FK     |         |
| nomerespon     | varchar | 50      |          |        |         |
| status         | char    | 1       |          |        | 'A'     |
| valortotal     | numeric | 15,2    |          |        |         |
| datavenda      | date    |         |          |        |         |
| horavenda      | time    |         |          |        |         |
| datafechamento | date    |         |          |        |         |
| horafechamento | time    |         |          |        |         |

### Formas de pagamento

| campo     | tipo    | tamanho | nulo     | indice | default |
| --------- | ------- | ------- | -------- | ------ | ------- |
| id        | serial  |         | not null | PK     |         |
| descricao | varchar | 100     | not null |        |         |
| status    | char    | 1       |          |        | 'A'     |

### Contas a pagar

| campo              | tipo    | tamanho | nulo     | indice | default |
| ------------------ | ------- | ------- | -------- | ------ | ------- |
| id                 | serial  |         | not null | PK     |         |
| id_centro_custo    | integer |         | not null | FK     |         |
| id_forma_pagamento | integer |         | not null | FK     |         |
| descricao          | varchar | 100     | not null |        |         |
| datalanc           | date    |         |          |        |         |
| horalanc           | time    |         |          |        |         |
| datapgmt           | date    |         |          |        |         |
| horapgmt           | time    |         |          |        |         |
| valor_conta        | numeric | 15,2    |          |        |         |
| valot_pago         | numeric | 15,2    |          |        |         |

### Contas a receber

| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| id_venda        | integer |         | not null |        |         |
| data_vencimento | date    |         |          |        |         |
| data_lancamento | date    |         |          |        |         |
| status          | char    | 1       |          |        | 'A'     |
| valor           | numeric | 15,2    |          |        |         |
