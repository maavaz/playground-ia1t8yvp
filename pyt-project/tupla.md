# Tuplas

Do ponto de vista técnico, as listas funcionam bem para armazenar conjuntos de itens que podem sofrer alterações durante a vida de um programa, isto é, são mutáveis. Por outro lado, há situações que não gostaríamos que os valores de uma determinada lista fossem alterados. O python possui uma lista onde os valores armazenados são imutáveis, denominada de **Tuplas**.

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

In [8]: for mat, nome, ender in alunos:    # Loop na Tupla alunos individualizando os itens
    ...:     print(mat, nome,ender)
    ...:     
1111 Ana Rua x
2222 Marco Rua Y
3333 Pedro Rua Z
```
### Atribuições de Tuplas

De vez em quando, é necessário trocar entre si os valores de duas variáveis. Com operações de atribuição convencionais, temos que utilizar uma variável temporária. Por exemplo, para fazer a troca entre a e b:
```python
In [21]: a = 5

In [22]: b = 6

In [23]: temp = a

In [24]: a = b

In [25]: b = temp

In [26]: a
Out[26]: 6

In [27]: b
Out[27]: 5
```
O Python fornece uma forma de atribuição de tupla que resolve esse problema elegantemente:

``` python
In [21]: a = 5

In [22]: b = 6

In [23]: a,b =b,a

In [24]: a
Out[24]: 6

In [25]: b
Out[25]: 5

In [26]: a =(5,6)

In [27]: b =(7,8)

In [28]: a,b = b,a

In [29]: a
Out[29]: (7, 8)

In [30]: b
Out[30]: (5, 6)
```
 


