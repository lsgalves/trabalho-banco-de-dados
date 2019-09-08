# Restaurante

> Objetivo: BD para um restaurante

## Grupo 03

### Integrantes

- **Leonardo Galves**
- Edgar
- Gabriel Viana
- Murilo
- Pedro Sardelari

### Tabelas

- Mesa
- Reserva
- Cardapio
- Tipos de alimentos

### Mesa

| campo  | tipo    | tamanho | nulo    | indice | default |
| ------ | ------- | ------- | ------- | ------ | ------- |
| numero | int     |         | notnull | PK     |         |
| status | varchar | 8       | notnull |        |         |

### Reserva

| campo      | tipo    | tamanho | nulo    | indice | default         |
| ---------- | ------- | ------- | ------- | ------ | --------------- |
| id         | int     |         | notnull | PK AI  |                 |
| status     | varchar | 8       | notnull |        | 'Não reservada' |
| data       | date    |         | notnull |        |                 |
| hora       | time    |         | notnull |        |                 |
| mesa_id    | int     |         | notnull | FK     |                 |
| cliente_id | int     |         | notnull | FK     |                 |

### Cardapio

| campo     | tipo    | tamanho | nulo    | indice | default |
| --------- | ------- | ------- | ------- | ------ | ------- |
| id        | int     |         | notnull | PK AI  |         |
| nome      | varchar | 100     | notnull |        |         |
| preco     | numeric | 15,2    | notnull |        |         |
| descricao | text    |         | notnull |        |         |
| tipo_id   | int     |         | notnull | FK     |         |

### Tipos de alimentos

| campo | tipo    | tamanho | nulo    | indice | default |
| ----- | ------- | ------- | ------- | ------ | ------- |
| id    | int     |         | notnull | PK AI  |         |
| nome  | varchar | 100     | notnull |        |         |
