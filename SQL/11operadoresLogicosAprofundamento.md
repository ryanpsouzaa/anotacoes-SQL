## Aprofundamento: operadores logicos

### IN
+ Testa se o valor esta contido em uma lista de valores
```
SELECT * FROM empregados
WHERE departamento IN ('Financeiro', 'TI', 'Vendas');
```
+ Obtem registros que tenham ```departamento``` do tipo 'Financeiro', 'TI' ou 'Vendas'

### NOT IN
+ Testa se o valor nao esta contido na lista
```
SELECT * FROM empregados
WHERE departamento NOT IN ('Financeiro', 'TI');
```
+ Registros que nao sao do 'Financeiro' e do 'TI' nao entram nessa consulta

### Definindo condicoes
+ o uso do () eh essencial para demarcar bem as condicoes -> garantindo a logica correta da consulta
```
SELECT * FROM tabelatreinamentos
WHERE
(curso LIKE 'O direito%' AND instituicao = 'Da Rocha)
OR
(curso LIKE 'O conforto%' AND instituicao = 'Das Neves');
```
+ Sem ( ), o SQL poderia avaliar na ORDEM errada, levando a consultas indesejadas
