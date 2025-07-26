## INSERT

### Inserindo dados em uma tabela
```
INSERT INTO tabelaClientes 
    (id_cliente, nome_cliente)
    VALUES ('1', 'Joao Silva');
```
+ Primary Key é um texto, no caso de digitos coloque sem aspas simples

### Inserindo multiplos dados na tabela

```
INSERT INTO tabelaClientes
    (id_cliente, nome_cliente)
    VALUES 
    ('1', 'Joao Silva'),
    ('2', 'Ana Souza'),
    ('3', 'Bob Ferreira');
```

### Inserindo dados na tabela: os dados vem de outra tabela
Exemplo: pedidos que custam 400 ou mais devem ser inseridos nos pedidos gold

```
CREATE TABLE pedidosGold(
    id_gold INT PRIMARY KEY,
    nome_pedido_gold VARCHAR(250),
    preco_gold DECIMAL(10,2),
    cliente_gold INT
    FOREIGN KEY (cliente_gold) REFERENCES tabelaClientes(id)
);

INSERT INTO pedidosGold (id_gold, nome_pedido_gold, preco_gold, cliente_gold) 
    SELECT id_pedido, nome_pedido, preco, cliente FROM pedidos
    WHERE preco >= 400;
```

