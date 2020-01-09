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
A sintaxe para modificar um elemento é semelhante à sintaxe para acessar
um elemento de uma lista. Para alterar um elemento, use o nome da lista
