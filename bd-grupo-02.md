# Restaurante

> Objetivo: BD para um restaurante

## Grupo 02

#### Integrantes
* **Anne**
* Taiane
* Thiago
* Moisés
* Wilian

### Tabelas
- Fornecedor
- Funcionarios
- Caixa
- Produtos

## Fonecedor

| Campo           | Tipo    | Tamanho | Nulo    | Indice | Default |
| --------------- | ------- | ------- | ------- | ------ | ------- |
| id              | int     |         | notnull | PK AI  |         |
| razao_social    | varchar | 280     | notnull |        |         |
| nome_fant       | varchar | 280     | null    |        |         |
| cnpj            | varchar | 14      | notnull |        |         |
| ie              | varchar | 12      | null    |        |         |
| logradouro      | varchar | 200     | null    |        |         |
| numero          | varchar | 7       | null    |        |         |
| cidade          | varchar | 200     | notnull |        |         |
| bairro          | varchar | 200     | null    |        |         |
| cep             | varchar | 8       | notnull |        |         |
| estado          | varchar | 2       | notnull |        |         |
| complemento     | varchar | 150     | null    |        |         |
| telefone1       | varchar | 14      | notnull |        |         |
| telefone2       | varchar | 14      | null    |        |         |
| email1          | varchar | 150     | null    |        |         |
| email2          | varchar | 150     | null    |        |         |

## Funcionarios

| Campo       | Tipo    | Tamanho | Nulo    | Indice | Default |
| ----------- | ------- | ------- | ------- | ------ | ------- |
| id          | int     |         | notnull | PK AI  |         |
| nome        | varchar | 280     | notnull |        |         |
| cpf         | varchar | 11      | notnull |        |         |
| idade       | int     |         | null    |        |         |
| logradouro  | varchar | 200     | null    |        |         |
| numero      | varchar | 7       | null    |        |         |
| cidade      | varchar | 200     | null    |        |         |
| bairro      | varchar | 200     | null    |        |         |
| cep         | varchar | 8       | null    |        |         |
| estado      | varchar | 2       | null    |        |         |
| sexo        | char    |         | null    |        |         |
| senha       | varchar | 6       | notnull |        |         |
| comissao    | numeric | 5.2     | notnull |        |         |
| email       | varchar | 200     | null    |        |         |
| telefone    | varchar | 15      | notnull |        |         |
| salario     | numeric | 5.2     | notnull |        |         |
| cargo       | varchar | 100     | notnull |        |         |
| contratacao | date    |         | null    |        |         |
| demissao    | date    |         | null    |        |         |

## Caixa

| Campo           | Tipo    | Tamanho | Nulo    | Indice | Default |
| --------------- | ------- | ------- | ------- | ------ | ------- |
| id              | int     |         | notnull | PK AI  |         |
| id_funcionario  | int     |         | notnull |        |         |
| total           | numeric | 7.2     | notnull |        |         |
| dinheiro        | numeric | 7.2     | notnull |        |         |
| cheque          | numeric | 7.2     | notnull |        |         |
| cartao          | numeric | 7.2     | notnull |        |         |
| data            | date    |         | notnull |        |         |
| d_c             | char    |         | notnull |        |         |
| desc_mov        | varchar | 150     | notnull |        |         |

## Produtos

| Campo           | Tipo    | Tamanho | Nulo    | Indice | Default |
| --------------- | ------- | ------- | ------- | ------ | ------- |
| id              | int     |         | notnull | PK AI  |         |
| descricao       | varchar | 200     | notnull |        |         |
| unidade         | varchar | 10      | notnull |        |         |
| grupo           | varchar | 150     | null    |        |         |
| subgrupo        | varchar | 150     | null    |        |         |
| departamento    | varchar | 150     | null    |        |         |
| ult_fornecedor  | int     |         | null    |        |         |
| estoque         | numeric | 7.2     | notnull |        |         |
| preco_venda     | numeric | 7.2     | notnull |        |         |
| preco_compra    | numeric | 7.2     | notnull |        |         |
| custo           | numeric | 7.2     | notnull |        |         |
| cod_barras      | varchar | 13      | null    |        |         |
| vencimento      | date    |         | null    |        |         |
