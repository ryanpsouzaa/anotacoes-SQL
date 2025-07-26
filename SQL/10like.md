## LIKE
+ Realizar buscas por padroes em valores Strings

### '%String'
+ % -> Diz que ha texto para seguir, representando qualquer sequencia de caracteres
```
SELECT * FROM tabelaclientes
WHERE nome LIKE 'Gab%';
```
+ Essa consulta trara registros como 'Gabriel', 'Gabriela' e todo o resto que comece com **Gab** e termine com outros quaisquer caracteres

```
SELECT * FROM tabelaclientes
WHERE nome LIKE '%son';
```
+ Essa consulta trara registros como 'Jeferson', 'Anderson' e todo o resto que termine com **son** e comece com outros quaisquer caracteres

```
SELECT * FROM tabelaclientes
WHERE nome LIKE '%a%';
```
+ Essa consulta trara registros que tenham a tenham a letra **a**, comecando ou terminando com quaisquer outros caracteres.

### '__String'
+ Usado em consultas como: Procurar nomes com exatamente **4** letras, onde o **segundo** caractere eh **a**

```
SELECT * FROM tabelaclientes
WHERE nome LIKE '_ _ a _';
```
+ Essa consulta trara registros como: 'Raul', 'Lara', e outros nomes que tenham **a** no como segunda letra e que possuam **4 letras** no total