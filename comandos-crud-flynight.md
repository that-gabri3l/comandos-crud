# Comandos CRUD para banco de dados Fly By Night

## INSERT na tabela de Fornecedores
```sql

-- INSERT de fornecedores

INSERT INTO fornecedores (nome) VALUES('Eletrônicos Tabajara');
INSERT INTO fornecedores (nome) VALUES('Games ABCD'),('SuperMercado Tem de Tud0'),('Livraria Demais da Conta');
```

## INSERT na tabela de Produtos
```sql
INSERT INTO produtos(nome, descricao, preco, quantidade, fornecedor_id) VALUES ('Smartphone Galaxy S23', 'Equipamanto com sistema Android e câmera FULL HD e etc e tal',
 1599.45,
20,
1 --id do forncedor Eletrônicos Tabajara
);

INSERT INTO produtos(nome, descricao, preco, quantidade, fornecedor_id) VALUES ('Senhor dos Anéis: As duas Torres',
'Volume 2 da Serie de Livros criados pelo autor J.R.R Tolkien',
80.99,
100,
4
);

INSERT INTO produtos(nome, descricao, preco, quantidade, fornecedor_id) VALUES ('TV Led',
'Tela de 50 Polegadas, resolução 4k, 4 entradas HDMI e etc e tal',
3420,
12,
1
);

```

## INSERT na tabela de lojas

```sql
INSERT INTO lojas (nome) VALUES ('Casas Bahia'),('Shopping Zona Leste'),('Bazar das Coisas'),('Americanas');

