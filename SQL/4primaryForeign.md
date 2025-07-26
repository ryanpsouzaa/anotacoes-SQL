## Primary Key e Foreign Key

## Chave Primaria/Primary Key
Identifica de forma exclusiva cada registro na tabela
+ Unicidade: cada valor é unico
+ nao nulo: cada registro de id deve ter um valor associado
+ eficiencia de pesquisa: é usada para acelerar a pesquisa de registros no banco de dados

## Chave estrangeira/Foreign Key
Referencia outra tabela

```
CREATE TABLE produtos (
    categoria INT,
    fornecedor INT,
    FOREIGN KEY (categoria) REFERENCES tabelaCategorias(id)
    FOREIGN KEY (fornecedor) REFENCES tabelaFornecedores(id)
);
```
+ Chave estrangeira sempre se liga com a chave primaria
