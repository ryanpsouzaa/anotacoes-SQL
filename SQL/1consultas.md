## <span style="color: steelblue;"> SQL -> Structured query language (linguagem de consulta estruturada) </span>


### <span style="color: steelblue;">Mostrar todos os dados da tabelapedidos</span>
``` 
SELECT * FROM tabelapedidos;
```

### <span style="color: steelblue;">WHERE: clausula para indicar de onde esta algo</span>
+ Selecione os pedidos que possuem pais_origem = China
```
SELECT * FROM tabelapedidos WHERE pais_origem = 'China';
```

### <span style="color: steelblue;">DISTINCT: seleciona apenas valores unicos (sem repeticao)</span>
+ Selecione os clientes (sem repetir o mesmo cliente) da tabelapedidos
```
SELECT DISTINCT cliente FROM tabelapedidos;
```

+ Selecione os clientes (sem repetir o mesmo cliente) que possui um pedido com status 'Pendente'
```
SELECT DISTINCT cliente FROM tabelapedidos WHERE status = 'Pendente';
```

## Exercicios sobre consultas SQL
### 1. Liste os id`s unicos dos produtos vendidos pela empresa
```
SELECT DISTINCT id_produto FROM tabelavendas;
```

### 2. Identifique os clientes que se cadastraram na empresa antes de 2020. Liste o nome e a data de cadastro desses clientes
```
SELECT nome_do_cliente, data_cadastro FROM tabelacliente WHERE data_cadastro < '2020-01-01';
```
