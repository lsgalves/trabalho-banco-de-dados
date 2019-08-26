# Restaurante
> Objetivo: BD para um restaurante

## Grupo 03

#### Integrantes
* Leonardo Galves
* Gabriel Viana
* Edgar
* Pedro Sardelari
* Murilo

### Clientes
- id
- nome
- mesa (FK)
- id_pedido (FK)

### Alimentos
- id (PK)
- nome
- tipo (FK)
- valor
- id_pedido (FK)
- receita (FK)

### Pedidos
- id (PK)
- forma_de_pagamento (FK)
- quantidade
- id_cliente (FK)

### Financeiro
- 

### Ingredientes
- id (PK)
- nome
- id_ingrediente_receita (FK)

### Mesas
- id (PK)
- mesa

### Tipos de Alimentos
- id (PK)
- nome

### Formas de Pagamento
- id (PK)
- nome

### Receitas
- id (PK)
- nome
- id_ingrediente_receita (FK)

### Ingrediente Receita
- id (PK)
- id_receitas (FK)
- id_ingredientes (FK)
