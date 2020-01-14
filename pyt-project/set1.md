# Sets

### OPerações em Sets (Conjuntos)

**Sets** podem ser usados em operações matemática como: união, interseçãon e diferença. Isto é realizado por operadores ou métodos.

### União

A união de dois conjuntos A e B é o conjunto composto por todos os elementos de A e de B. Em python, a união é executada através do operador **|**. Essa mesma operação também pode ser efetuada pelo método **union()**.
![conjuntos](/imagens/uniao.png)

``` python
In [1]: set1 = {'A', 'B', 'C', 'D'}

In [2]: set1
Out[2]: {'A', 'B', 'C', 'D'}

In [3]: set2 = {'C', 'D', 'E', 'F'}

In [4]: set2
Out[4]: {'C', 'D', 'E', 'F'}

In [5]: set3 = set1 | set2     # Poderíamos utilizar o método union: set1.union(set2)

In [6]: set3                           # União dos conjuntos set1 e set2
Out[6]: {'A', 'B', 'C', 'D', 'E', 'F'}
```

### Interseção

A interseção de dois conjuntos A e B é o conjunto de elementos comuns em ambos os conjuntos. Em python, a interseção é realizada usando o operador &. Essa mesma operação pode ser realizada usando o método intersection().
![conjuntos](/imagens/intersecao.png)

``` python
In [10]: set1 = {'A', 'B', 'C', 'D'}

In [11]: set2 = {'C', 'D', 'E', 'F'}

In [12]: set3 = set1 & set2    # Podemos usar o método Intersection: set1.intersection(set2)

In [13]: set3
Out[13]: {'C', 'D'}

```

### Diferença

A diferença entre dois conjuntos A e B (A - B) é um conjunto de elementos que estão apenas em A, mas não em B. Da mesma forma, a diferença entre os conjuntos B e A (B - A) é um conjunto de elementos em B, mas não em A. Em python, a diferença é realizada usando o operador **-**. Essa mesma operação pode ser realizado usando o método **difference()**.

``` python

```
