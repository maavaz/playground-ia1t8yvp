# Dicionários em Python

### items(), keys() e values()

Os dicionários são iteráveis, isto é, são objetos que podem ter os elementos da sequência percorridos um a um. A função **items()** retorna uma lista de tuplas com os pares “chave” : valor. A função **keys()** retorna uma lista apenas com as chaves do dicionário, enquanto que a função **values()** retorna uma lista apenas com os valores dos itens do dicionário. 
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

### Lista de Dicionários 

Os dicionários também podem ser armazenados em listas, através dos métodos já conhecidos como atribuição direta à variável, ou ainda, por meio do método append().
``` python
In [1]: jeep_basico={'compass':116990,'cherokee':359900,'renegade':89990,'wrangler':272990}

In [2]: chevrolet_basico={'onix':47590,'prisma':49590,'cruze':101190, 'tracker':92950}

In [3]: carros=[jeep_basico]   #atribuição direta

In [4]: carros.append(chevrolet_basico) # Acrescentando um item por append

In [5]: carros
Out[5]: 
[{'compass': 116990,
  'cherokee': 359900,
  'renegade': 89990,
  'wrangler': 272990},
 {'onix': 47590, 'prisma': 49590, 'cruze': 101190, 'tracker': 92950}]

In [6]: for carro in carros:
   ...:     for tipo, preco in carro.items():
   ...:         print(tipo, " :  ", preco)
   ...:         
compass  :   116990
cherokee  :   359900
renegade  :   89990
wrangler  :   272990
onix  :   47590
prisma  :   49590
cruze  :   101190
tracker  :   92950

```
### Associar uma lista de valores a uma chave

Pode-se associar múltiplos valores a uma chave, isso pode ser feito por meio de uma lista de valores. 
``` python

In [7]: # Preços das várias versões de cada carro

In [8]: jeep_basico={'compass':[116990,120990],'cherokee':[359900,365900],'renegade':[89990, 104990, 109990],'wrangler':[272990, 290990]}

In [9]: chevrolet_basico={'onix':[47590, 49990,59990],'prisma':[49590,58590],'cruze':[101190, 105190], 'tracker':[92950, 95900]}

In [10]: carros=[jeep_basico, chevrolet_basico]

In [11]: for carro in carros:
    ...:     for tipo, preco in carro.items():
    ...:         print('Tipo:',tipo, "Precos:")
    ...:         for x in preco:
    ...:             print(x)
    ...:             
Tipo: compass Precos:
116990
120990
Tipo: cherokee Precos:
359900
365900
Tipo: renegade Precos:
89990
104990
109990
Tipo: wrangler Precos:
272990
290990
Tipo: onix Precos:
47590
49990
59990
Tipo: prisma Precos:
49590
58590
Tipo: cruze Precos:
101190
105190
Tipo: tracker Precos:
92950
95900
```
