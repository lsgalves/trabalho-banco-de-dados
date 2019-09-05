# Trabalho de Banco de dados

**Professor** Alexandre Gonçalves

**[Email](mailto:gonc.alexandre@gmail.com)**

### Objetivos

- [x] Cada grupo deve criar a sua estrutura do banco de dados

- [x] Mesclar todas as estruturas das tabelas dos grupos, filtrando-as

- [x] Dividir as tabelas para os grupos criarem

- [ ] Mesclar no banco de dados todas as tabelas criadas

- [ ] Cada grupo deve criar os comandos SQL para gerar seu banco de dados (etapa individual)

### Como criar as tabelas?

Exemplo:

```markdown
### Cliente

| campo           | tipo    | tamanho | nulo    | indice | default |
| --------------- | ------- | ------- | ------- | ------ | ------- |
| id              | int     |         | notnull | PK AI  |         |
| nome            | varchar | 100     | notnull |        | 'Teste' |
| data_nascimento | date    |         | null    |        |         |
```

Resultado:

### Cliente

| campo           | tipo    | tamanho | nulo    | indice | default |
| --------------- | ------- | ------- | ------- | ------ | ------- |
| id              | int     |         | notnull | PK AI  |         |
| nome            | varchar | 100     | notnull |        | 'Teste' |
| data_nascimento | date    |         | null    |        |         |
