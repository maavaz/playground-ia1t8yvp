### <b> Concatenação e multiplicação  </b>

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

## <b> Incluindo, alterando e removendo itens de uma lista  </b>

Após a criação de uma lista, é possível adicionar, alterar e remover elementos dela à medida que seu programa executar. 

#### <b> Incluir itens na lista </b>

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


#### <b> Modificar itens na lista </b>

Para modificar um elemento é semelhante à sintaxe para acessar um elemento de uma lista. Para alterar um elemento, use o nome da lista seguido do índice do elemento que você quer modificar e, então, forneça o novo valor que você quer que esse item tenha.
```python
In [9]: lista2 = [6, 7, 8, 9, 10]
.....

In [19]: lista2[0] = 12 #Alterando o valor do item na primeira posição de 6 para 12

In [20]: lista2
Out[20]: [12, 7, 8, 9, 10, 11]
```
#### <b> Remover itens na lista </b>

Para remover um elemento utiliza-se o método **.remove(valor)**. Esse valor deve pertencer a lista, do contrário dá erro.
```python
In [20]: lista2
Out[20]: [12, 7, 8, 9, 10, 11]


In [21]: lista2.remove(12)  #remove o elemento de valor 12 da lista

In [22]: lista2
Out[22]: [7, 8, 9, 10, 11]
```
#### <b> Incluir vários Itens na Lista </b>

É possível incluir vários elementos (dispostos em uma lista) a lista atual, através do método **extend()**. Esse método estende a lista atual adicionando todos os itens da lista (passados como argumento) ao final. 
``` python
In [1]: alunos=['Ana', 'Bruno', 'Clara']

In [2]: alunos
Out[2]: ['Ana', 'Bruno', 'Clara']

In [3]: novos_alunos=['Hugo', 'Katia', 'Mônica']

In [4]: novos_alunos
Out[4]: ['Hugo', 'Katia', 'Mônica']

In [5]: alunos.extend(novos_alunos)

In [6]: alunos
Out[6]: ['Ana', 'Bruno', 'Clara', 'Hugo', 'Katia', 'Mônica']
```
#### <b> Descobrindo a posição de um item </b>

Suponha que você deseje saber onde está um determinado elemento em uma lista. Para isso, o python provê o método **index()** que retorna a posição do elemento na lista.
``` python
In [7]:alunos.index('Clara')
Out[7]: 2                     # Clara está na posição 2 da lista
```
Se você utilizar o método **index()** para um item que não está na lista, o python irá retonar um erro.
``` python
In [8]: alunos.index('Marco')
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-12-dbe05a01759e> in <module>()
----> 1 alunos.index('Marco')

ValueError: 'Marco' is not in list
```
#### <b> Ordenar os elementos da Lista </b>

Para ordenar os elementos de uma lista utilizamos o método **sort()**.
``` python
In [13]: lista = [6,8,4,9,2,3]

In [14]: lista
Out[14]: [6, 8, 4, 9, 2, 3]

In [15]: lista.sort()

In [16]: lista
Out[16]: [2, 3, 4, 6, 8, 9]

In [17]: lista.sort(reverse=True)   # Organiza os elementos na ordem inversa

In [18]: lista
Out[18]: [9, 8, 6, 4, 3, 2]

```
**OBS:** Existem vários outros métodos para manipulação de listas, mas, estes métodos, serão apresentados caso haja necessidade. Do contrário, sugiro fazer uma busca na web sobre o tema.

