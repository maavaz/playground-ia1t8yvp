# Tuplas

Do ponto de vista técnico, as listas funcionam bem para armazenar conjuntos de itens que podem sofrer alterações durante a vida de um programa, isto é, são mutáveis.Por outro lado, há situações que não gostaríamos que os valores de uma determinada lista fossem alterados. O python possui uma lista onde os valores armazenados são imutáveis, denominada de **Tuplas**.

## Definindo uma tupla

As tuplas se parecem exatamente com as listas, exceto por usarem parênteses no lugar de colchetes. Após a definição da tupla, pode-se acessar os elementos individualmente usando um índice, como é feito com as listas.
``` python
In [1]: z = (1,2,3,4,5)   # Criação de uma tupla

In [2]: z
Out[2]: (1, 2, 3, 4, 5)

In [3]: sum(z)          # Soma dos elementos da Tupla
Out[3]: 15

In [4]: z[2:]           # Fatiamento da Tupla 
Out[4]: (3, 4, 5)

```
Pode-se declarar uma tupla sem o uso de parenteses, como no exemplo abaixo:
``` python
In [10]: t = 1,2,3,4

In [11]: t
Out[11]: (1, 2, 3, 4)
```
Outra forma de criar uma tupla é com a função integrada **tuple**, com apenas 1 argumento. Se você quiser criar uma tupla contendo letras do alfabeto poderíamos usar **tuple** com uma string:
``` python
In [14]: z = tuple("ABCDEFGH")

In [15]: z
Out[15]: ('A', 'B', 'C', 'D', 'E', 'F', 'G', 'H')
```


Do ponto de vista conceitual poderíamos usar as tuplas para montar estruturas de dados heterogêneos enquanto a lista deveria ser usada para dados homogêneos, ou seja, todos seus elementos deveriam ser do mesmo tipo. Claro que cabe ao programador essa decisão.  Pode-se utiliar as tuplas para dados heterogêneos (diversidade de tipos entre os membros) funcionando como um registro de dados, como uma linha de um banco de dados, um conjunto de colunas.  
``` python
In [1]: alunos = ((1111, 'Ana', 'Rua x'),(2222, 'Marco', 'Rua Y'), (3333, 'Pedro', 'Rua Z'))

In [2]: alunos
Out[2]: ((1111, 'Ana', 'Rua x'), (2222, 'Marco', 'Rua Y'), (3333, 'Pedro', 'Rua Z'))

In [3]: alunos[1:]
Out[3]: ((2222, 'Marco', 'Rua Y'), (3333, 'Pedro', 'Rua Z'))

In [7]: for al in alunos:      # Loop na Tupla alunos
   ...:     print(al)
   ...:     
(1111, 'Ana', 'Rua x')
(2222, 'Marco', 'Rua Y')
(3333, 'Pedro', 'Rua Z')
```

 


