### Concatenação e multiplicação

Uma lista pode ser unida a outra para formar uma nova lista, através do operador aritmético de soma **+**.

``` python
In [8]: lista1 = [0, 1, 2, 3, 4, 5]

In [9]: lista2 = [6, 7, 8, 9, 10]

In [10]: lisconcat= lista1 + lista2

In [11]: lisconcat
Out[11]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

Pode-se também gerar várias cópias dos itens de uma lista, através do operador aritmético de multiplicação *****.  

``` python
In [8]: lista1 = [0, 1, 2, 3, 4, 5]
.....
In [13]: listmulti = lista1 * 2

In [14]: listmulti
Out[14]: [0, 1, 2, 3, 4, 5, 0, 1, 2, 3, 4, 5]
```

## Incluindo, alterando e removendo itens de uma lista

Após a criação de uma lista, é possível adicionar, alterar e remover elementos dela à medida que seu programa executar. 

#### Incluir itens na lista

Para incluir um elemento no final da lista usa-se o método **.append(valor)**, onde valor é o que se quer incluir na lista.
```python
In [9]: lista2 = [6, 7, 8, 9, 10]
.....

In [17]: lista2.append(11)  #incluir o valor 11 ao final da lista2

In [18]: lista2
Out[18]: [6, 7, 8, 9, 10, 11]
```
Pode-se querer inserir um elemnto numa posição qualquer da lista, para isso usa-se o método **.insert(posição, valor)**
```python
In [8]: lista1 = [0, 1, 2, 3, 4, 5]
.....

In [17]: lista1.insert(0, -1)  #incluir o valor -1 na primeira posição da lista1

In [18]: lista1
Out[18]: [-1, 0, 1, 2, 3, 4, 5]
```


#### Modificar itens na lista

Para modificar um elemento é semelhante à sintaxe para acessar um elemento de uma lista. Para alterar um elemento, use o nome da lista seguido do índice do elemento que você quer modificar e, então, forneça o novo valor que você quer que esse item tenha.
```python
In [9]: lista2 = [6, 7, 8, 9, 10]
.....

In [19]: lista2[0] = 12 #Alterando o valor do item na primeira posição de 6 para 12

In [20]: lista2
Out[20]: [12, 7, 8, 9, 10, 11]
```
#### Remover itens na lista

Para remover um elemento utiliza-se o método **.remove(valor)**. Esse valor deve pertencer a lista, do contrário dá erro.
```python
In [20]: lista2
Out[20]: [12, 7, 8, 9, 10, 11]


In [21]: lista2.remove(12)  #remove o elemento de valor 12 da lista

In [22]: lista2
Out[22]: [7, 8, 9, 10, 11]
```

