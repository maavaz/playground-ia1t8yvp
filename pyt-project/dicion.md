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
