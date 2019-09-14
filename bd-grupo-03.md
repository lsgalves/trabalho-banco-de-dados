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

- Mesas
- Reservas
- Cardapios
- Tipos de alimentos

### Mesas

| campo  | tipo    | tamanho | nulo     | indice | default |
| ------ | ------- | ------- | -------- | ------ | ------- |
| numero | integer |         | not null | PK     |         |
| status | varchar | 50      | not null |        |         |

### Reservas

| campo      | tipo    | tamanho | nulo     | indice | default         |
| ---------- | ------- | ------- | -------- | ------ | --------------- |
| id         | serial  |         | not null | PK     |                 |
| status     | varchar | 50      | not null |        | 'Não reservada' |
| data       | date    |         | not null |        |                 |
| hora       | time    |         | not null |        |                 |
| mesa_id    | integer |         | not null | FK     |                 |
| cliente_id | integer |         | not null | FK     |                 |

### Cardapios

| campo     | tipo    | tamanho | nulo     | indice | default |
| --------- | ------- | ------- | -------- | ------ | ------- |
| id        | serial  |         | not null | PK     |         |
| nome      | varchar | 150     | not null |        |         |
| preco     | numeric | 15,2    | not null |        |         |
| descricao | text    |         | not null |        |         |
| tipo_id   | integer |         | not null | FK     |         |

### Tipos de alimentos

| campo | tipo    | tamanho | nulo     | indice | default |
| ----- | ------- | ------- | -------- | ------ | ------- |
| id    | serial  |         | not null | PK     |         |
| nome  | varchar | 150     | not null |        |         |
