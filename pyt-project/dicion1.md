# Dicionários

### items(), keys() e values()

Os dicionários são iteráveis, isto é, são objetos que podem ter os elementos da sequência percorridos um a um. A função **items()** retorna uma lista de tuplas com os pares “chave” : valor. A função **keys()** retorna uma lista apenas com as chaves do dicionário, enquanto que a função
**values()** retorna uma lista apenas com os valores dos itens do dicionário. 
```python
In [1]: cesta_frutas = {'maça':60, 'uva':20, 'pera':35, 'abacaxi':25, 'laranja':55}

In [2]: cesta_frutas.items()
Out[2]: dict_items([('maça', 60), ('uva', 20), ('pera', 35), ('abacaxi', 25), ('laranja', 55)])

In [3]: cesta_frutas.keys()
Out[3]: dict_keys(['maça', 'uva', 'pera', 'abacaxi', 'laranja'])

In [4]: cesta_frutas.values()
Out[4]: dict_values([60, 20, 35, 25, 55])
````
Também podemos percorrer os elementos da sequência através da estrutura **for**, iterando através de variáveis que recebem a chave e o valor, definidas no corpo do comando. 
```python
In [6]:   for fruta, qtd in cesta_frutas.items():
   ...:     print('nome:', fruta, (12 -len(fruta))*' ','qtde:',str(qtd))
   ...:   
   ...:   
nome: maça          qtde: 60
nome: uva           qtde: 20
nome: pera          qtde: 35
nome: abacaxi       qtde: 25
nome: laranja       qtde: 55
```

### Associar uma lista de valores a uma chave

