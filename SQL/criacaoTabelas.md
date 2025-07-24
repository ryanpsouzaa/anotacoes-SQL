## Criacao de tabelas
### Deve especificar o nome das colunas
### Deve especificar o tipo de dado da coluna

** Criando tabela de clientes ** 
```
CREATE TABLE tabelaClientes (
    id_cliente INT PRIMARY KEY,
    nome_cliente VARCHAR(100),
    informacoes_contato VARCHAR(250)
);
```

### Banco de Dados
Container principal que armazena todos os dados e estruturas do sistema.
+ contem: tabelas, schemas, indices, usuarios, permissoes e etc

### Schema
Forma de organizar objetos dentro de um banco de dados
+ Organiza tabelas, views, funcoes e etc. Como uma subdivisao logica.
    - Separar dados por modulos (ex: financeiro, estoque, usuarios)
    - controlar permissoes (usuarios acessam so certos schemas)
    - evitar conflitos de nomes (duas tabelas clientes, mas em schemas diferentes)

```
CREATE DATABASE bibliotecaDB;
CREATE SCHEMA livrosSchema;
```

### Alterando colunas na tabela
```
ALTER TABLE tabelaClientes ADD endereco_cliente VARCHAR(250);
```

### Apagando toda a tabela (!!!)
```
DROP TABLE tabelaClientes;
```
+ Com o drop podemos excluir indices, tabelas, bancos de dados, usuarios, funcoes e entre outros
+ Um objeto deletado --> nao pode ser restaurado!
+ Com o comando **ALTER** podemos adicionar, modificar ou excluir colunas em uma tabela existente
```
ALTER TABLE tabelaClientes DROP COLUMN endereco_cliente;
```