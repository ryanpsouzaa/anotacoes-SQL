## SQL -> Structured query language (linguagem de consulta estruturada)


<ins> Mostrar todos os dados da tabelapedidos </ins>
``` 
SELECT * FROM tabelapedidos;
```

<ins> WHERE: clausula para indicar de onde esta algo
Selecione os pedidos que possuem pais_origem = China </ins>

```
SELECT * FROM tabelapedidos WHERE pais_origem = 'China';
```

<ins> DISTINCT: seleciona apenas valores unicos (sem repeticao)
Selecione os clientes (sem repetir o mesmo cliente) da tabelapedidos </ins>

```
SELECT DISTINCT cliente FROM tabelapedidos;
```


<ins> Selecione os clientes (sem repetir o mesmo cliente) que possui um pedido com status 'Pendente' </ins>

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
