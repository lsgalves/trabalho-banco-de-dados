# Restaurante

> Objetivo: BD para um restaurante

## Grupo 02

### Integrantes

- **Thiago**
- Anne
- Taiane
- Moisés
- Wilian

### Tabelas

- Fornecedores
- Funcionarios
- Caixa
- Produtos

### Fonecedores

| campo        | tipo    | tamanho | nulo     | indice | default |
| ------------ | ------- | ------- | -------- | ------ | ------- |
| id           | integer |         | not null | PK AI  |         |
| razao_social | varchar | 280     | not null |        |         |
| nome_fant    | varchar | 280     |          |        |         |
| cnpj         | varchar | 14      | not null |        |         |
| ie           | varchar | 12      |          |        |         |
| logradouro   | varchar | 200     |          |        |         |
| numero       | varchar | 7       |          |        |         |
| cidade       | varchar | 200     | not null |        |         |
| bairro       | varchar | 200     |          |        |         |
| cep          | varchar | 8       | not null |        |         |
| estado       | varchar | 2       | not null |        |         |
| complemento  | varchar | 150     |          |        |         |
| telefone1    | varchar | 14      | not null |        |         |
| telefone2    | varchar | 14      |          |        |         |
| email1       | varchar | 150     |          |        |         |
| email2       | varchar | 150     |          |        |         |

### Funcionarios

| campo       | tipo    | tamanho | nulo     | indice | default |
| ----------- | ------- | ------- | -------- | ------ | ------- |
| id          | integer |         | not null | PK AI  |         |
| nome        | varchar | 280     | not null |        |         |
| cpf         | varchar | 11      | not null |        |         |
| idade       | integer |         |          |        |         |
| logradouro  | varchar | 200     |          |        |         |
| numero      | varchar | 7       |          |        |         |
| cidade      | varchar | 200     |          |        |         |
| bairro      | varchar | 200     |          |        |         |
| cep         | varchar | 8       |          |        |         |
| estado      | varchar | 2       |          |        |         |
| sexo        | char    |         |          |        |         |
| senha       | varchar | 6       | not null |        |         |
| comissao    | numeric | 5,2     | not null |        |         |
| email       | varchar | 200     |          |        |         |
| telefone    | varchar | 15      | not null |        |         |
| salario     | numeric | 5,2     | not null |        |         |
| cargo       | varchar | 100     | not null |        |         |
| contratacao | date    |         |          |        |         |
| demissao    | date    |         |          |        |         |

### Caixa

| campo          | tipo    | tamanho | nulo     | indice | default |
| -------------- | ------- | ------- | -------- | ------ | ------- |
| id             | integer |         | not null | PK AI  |         |
| id_funcionario | integer |         | not null | FK     |         |
| total          | numeric | 7,2     | not null |        |         |
| dinheiro       | numeric | 7,2     | not null |        |         |
| cheque         | numeric | 7,2     | not null |        |         |
| cartao         | numeric | 7,2     | not null |        |         |
| data           | date    |         | not null |        |         |
| d_c            | char    |         | not null |        |         |
| desc_mov       | varchar | 150     | not null |        |         |

### Produtos

| campo          | tipo    | tamanho | nulo     | indice | default |
| -------------- | ------- | ------- | -------- | ------ | ------- |
| id             | integer |         | not null | PK AI  |         |
| descricao      | varchar | 200     | not null |        |         |
| unidade        | varchar | 10      | not null |        |         |
| grupo          | varchar | 150     |          |        |         |
| subgrupo       | varchar | 150     |          |        |         |
| departamento   | varchar | 150     |          |        |         |
| ult_fornecedor | integer |         |          |        |         |
| estoque        | numeric | 7.2     | not null |        |         |
| preco_venda    | numeric | 7.2     | not null |        |         |
| preco_compra   | numeric | 7.2     | not null |        |         |
| custo          | numeric | 7.2     | not null |        |         |
| cod_barras     | varchar | 13      |          |        |         |
| vencimento     | date    |         |          |        |         |
