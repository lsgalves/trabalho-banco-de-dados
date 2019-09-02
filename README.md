# Trabalho de Banco de dados

**Professor** Alexandre Gonçalves
**[Email](mailto:gonc.alexandre@gmail.com)**

### Objetivos

- [x] Cada grupo deve criar a sua estrutura do banco de dados

- [x] Mesclar todas as estruturas das tabelas dos grupos, filtrando-as

- [x] Dividir as tabelas para os grupos criarem

- [ ] Mesclar todas as tabelas criadas no banco de dados

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
