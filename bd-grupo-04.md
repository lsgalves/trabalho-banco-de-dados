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

### Venda
| campo           | tipo     | tamanho | nulo    | indice | default |
| --------------- | -------- | ------- | ------- | ------ | ------- |
| id              | serial   |         | notnull | PK AI  |         |
| idfuncionario   | int      |         | notnull | FK     |         |
| idmesa          | int      |         | notnull | FK     |         |
| nomerespon      | varchar  | 50      |         |        |         |
| status          | char     | 1       |         |        | A       |
| valortotal      | numeric  | 15,2    |         |        |         |
| datavenda       | date     |         |         |        |         |
| horavenda       | time     |         |         |        |         |
| datafechamento  | date     |         |         |        |         |
| horafechamento  | time     |         |         |        |         |


### ItensVenda
| campo           | tipo     | tamanho | nulo    | indice | default |
| --------------- | -------- | ------- | ------- | ------ | ------- |
| serial          | int      |         | notnull | PK     |         |
| idvenda         | int      |         | notnull | FK     |         |
| idcardapio      | int      |         | notnull | FK     |         |
| idfuncionario   | int      |         | notnull | FK     |         |
| valorunit       | numeric  | 15,2    |         |        |         |
| qtd             | numeric  | 15,2    |         |        |         |
| valortotal      | numeric  | 15,2    |         |        |         |
| datavenda       | date     |         |         |        |         |
| horavenda       | time     |         |         |        |         |

### FORMAS DE PAGAMENTO
| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| descricao       | varchar | 100     | not null |        |         |
| status          | char    | 1       |          |        | 'A'     |

### CENTRO DE CUSTO
| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| descricao       | varchar | 100     | not null |        |         |
| status          | char    | 1       |          |        | 'A'     |

### CONTAS A PAGAR
| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| idcentrocusto   | int     |         | not null | FK     |         |
| idformapagamento| int     |         | not null | FK     |         |
| descricao       | varchar | 100     | not null |        |         |
| datalanc        | date    |         |          |        |         |
| horalanc        | time    |         |          |        |         |
| datapgmt        | date    |         |          |        |         |
| horapgmt        | time    |         |          |        |         |
| vlconta         | numeric | 15,2    |          |        |         |
| vlpago          | numeric | 15,2    |          |        |         |

### CONTAS A RECEBER
| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| idvenda         | int     |         | not null |        |         |
| dtvencimento    | date    |         |          |        |         |
| dtlancamento    | date    |         |          |        |         |
| status          | char    | 1       |          |        | 'A'     |
| valor           | numeric | 15,2    |          |        |         |
