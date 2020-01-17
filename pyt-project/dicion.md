# Dicionários em Python

Um **dicionário** é uma estrutura de dados do tipo coleção, ou seja, um objeto que contém mais de um valor. 
Diferentemente das listas em que os elementos são acessados através de uma posição ou índice, nos dicionários o acesso às informações 
ocorrem através de chaves (par chave e valor), conhecido como **key:value**. Os elementos de um dicionário são armazenados de forma não ordenada.

## Criando um dicionário

A criação de um dicionário é feita passando as informações entre **chaves ({})**. Os elementos seguem o formato **“chave” : “valor”**. 
``` python
In [1]: vazio = {} # criação de um dicionário vazio

In [2]: func = {"matricula":123, "nome": "José", "idade": 20, "salario": 9200.45}

In [3]: func
Out[3]: {'matricula': 123, 'nome': 'José', 'idade': 20, 'salario': 9200.45}
```

A função **dict()** constroi dicionários a partir de uma lista de tuplas  
``` python
In [1]: d = dict([('Ana',20),('Clara',25),('Pedro',21)])

In [2]: d
Out[2]: {'Ana': 20, 'Clara': 25, 'Pedro': 21}
```

Através da atribuição direta de valores:
``` python
In [3]: cts = dict(pi=3.14, e=2.7, alpha=1/137)

In [4]: cts
Out[4]: {'pi': 3.14, 'e': 2.7, 'alpha': 0.0072992700729927005}
```

O acesso aos dados de um dicionário, é semelhante ao formato das listas, usando o nome da chave entre 'colchetes' em vez de um índice numérico. 
``` python
In [4]: func['idade']
Out[4]: 20

In [5]: func['nome']
Out[5]: 'José'
```
Outra forma de acesso é feito através da função **get(chave)**, onde é obtido o valor associado a chave:
``` python
In [7]: sal = func.get('salario')

In [8]: sal
Out[8]: 9200.45
```
O acesso a uma chave inexistente irá gerar um erro pelo python:
``` python
In [6]: func['altura']   # Não existe a chave altura em func
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-6-fa7e358a2308> in <module>()
----> 1 func['altura']

KeyError: 'altura'

```
## Alterando e Removendo Valores dos dicionários

Os valores podem ser alterados diretamente em uma chave específica, isso pode ocorrer quando é necessário atualizar ou inicializar uma chave do dicionário. Por outro lado, a operação de deleção pode ser realizada tanto para uma chave específica (comando **del**), para o último elemento (função **popitem()**) como a remoção do dicionário inteiro (função **clear()**).  

``` python
In [10]: carro = {'marca': 'Jeep', 'versao': 'Renegade 1.8 Flex AT', 'ano': 2020, 'preco':89.990}

In [11]: carro
Out[11]: 
{'marca': 'Jeep',
 'versao': 'Renegade 1.8 Flex AT',
 'ano': 2020,
 'preco': 89.99}

In [12]: carro['versao']='Longitude 1.8 Flex AT'

In [13]: carro
Out[13]: 
{'marca': 'Jeep',
 'versao': 'Longitude 1.8 Flex AT',
 'ano': 2020,
 'preco': 89.99}

In [14]: del carro['marca']

In [15]: carro
Out[15]: {'versao': 'Longitude 1.8 Flex AT', 'ano': 2020, 'preco': 89.99}

In [16]: carro.popitem()
Out[16]: ('preco', 89.99)

In [17]: carro
Out[17]: {'versao': 'Longitude 1.8 Flex AT', 'ano': 2020}

In [18]: carro.clear()

In [19]: carro
Out[19]: {}

```
