## Consultando dados Null
Caso o banco de dados possua colunas com registros **null**

### ISNULL
+ Retorna apenas os registros que tem ```data_termino_contrato``` nulo (ainda nao foi atribuido valor a essa coluna) -> empregado ainda contratado
```
SELECT * FROM tabelaempregados
WHERE data_termino_contrato ISNULL;
```

### NOTNULL
+ Retorna apenas os registros que tem ```data_termino_contrato``` com valores -> emrpregado ja teve seu contrato encerrado
```
SELECT * FROM tabelaempregados
WHERE data_termino_contrato NOTNULL;
```