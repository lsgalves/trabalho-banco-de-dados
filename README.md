# Trabalho de Banco de dados

**Professor** Alexandre Gonçalves

**[Email](mailto:gonc.alexandre@gmail.com)**

> **SGDB:** PostgreSQL

### Objetivos

- [x] Cada grupo deve criar a sua estrutura do banco de dados

- [x] Mesclar todas as estruturas das tabelas dos grupos, filtrando-as

- [x] Dividir as tabelas para os grupos criarem

- [x] Mesclar no banco de dados todas as tabelas criadas

- [x] Cada grupo deve criar os comandos SQL para gerar seu banco de dados (etapa individual)

### Como criar as tabelas?

Exemplo:

```markdown
### Cliente

| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| nome            | varchar | 100     | not null |        | 'Teste' |
| data_nascimento | date    |         |          |        |         |
```

Resultado:

### Cliente

| campo           | tipo    | tamanho | nulo     | indice | default |
| --------------- | ------- | ------- | -------- | ------ | ------- |
| id              | serial  |         | not null | PK     |         |
| nome            | varchar | 100     | not null |        | 'Teste' |
| data_nascimento | date    |         |          |        |         |
