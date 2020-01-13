# Dicionários em Python

Um dicionário (python) é uma estrutura de dados do tipo coleção, ou seja, um objeto que contém mais que um valor. 
Diferentemente das listas em que os elementos são acessados através de uma posição ou índice, nos dicionários o acesso às informações 
ocorrem através de chaves (par chave e valor), conhecido como **key:value**. Os elementos de um dicionário são armazenados de forma não ordenada.

## Criando um dicionário

A criação de um dicionário é feita passando as informações entre chaves ({}). Os elementos seguem o formato “chave” : “valor”. 
``` python
In [1]: vazio = {} # criação de um dicionário vazio

In [2]: func = {"matricula":123, "nome": "José", "idade": 20, "salario": 9200.45}

In [3]: func
Out[3]: {'matricula': 123, 'nome': 'José', 'idade': 20, 'salario': 9200.45}
```
O acesso aos dados de um dicionário, é semelhante ao formato das listaS, usando o nome da chave entre 'colchetes' em vez de um índice numérico. 
``` python
In [4]: func['idade']
Out[4]: 20

In [5]: func['nome']
Out[5]: 'José'
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

