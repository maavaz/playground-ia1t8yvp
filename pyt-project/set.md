# Sets

**Set** é uma coleção (estrutura de dados) não ordenada e não indexada de itens únicos. Os **Sets** podem ser usados para executarem operações matemáticas de conjuntos, tais como: união, interseção, etc.

### <b> Criando e acessando dados em Sets </b>

Um **set** é criado colocando-se os seus the itens (elementos) entre **chaves ({})**, separados por vírgulas ou usando a função pré-definida **set()**, que transforma sequências de valores em **sets**.
``` python


In [23]: set1 = {"Luiz", "Marco", "Ana", "Alfredo", "Ana", "Carolina", "Carolina", "Marco"}

In [24]: set1
Out[24]: {'Alfredo', 'Ana', 'Carolina', 'Luiz', 'Marco'}   # Set não possui duplicata


In [25]: set2 = set(["Luiz", "Marco", "Ana", "Alfredo", "Ana", "Carolina", "Carolina", "Marco"]) # Função set()

In [26]: set2
Out[26]: {'Alfredo', 'Ana', 'Carolina', 'Luiz', 'Marco'}

set2 = {"cachorro", "gato", "papagaio", "cachorro", "papagaio", "macaco", "galinha"}
print(set2)

# Para criarmos um set vazio obrigatoriamente devemo usar a função set()

In [27]: set3 = set()

In [28]: set3
Out[28]: set()

```
 
 ### <b> Incluindo, Alterando itens e Excluindo itens em Sets </b>
 
**Set** são mutáveis mas, como não são ordenados, a indexação não tem significado. Logo, não podemos acessar ou alterar um elemento do conjunto usando indexação ou slice, conjunto não suporta.

Podemos adicionar um único elemento usando o método **add()** e vários elementos usando o método **update()**. O método **update()** pode levar tuplas, listas, strings ou outros conjuntos como argumento. Em todos os casos, duplicatas são evitadas.
Um item específico pode ser removido do conjunto usando métodos, **discard()** e **remove()**. A diferença entre as duas funções está realcionada a existência do item no conjunto, isto é, usando **discard()** se o item não existir no conjunto, ele permanecerá inalterado, mas a função **remove()** gera um erro nessa condição.

``` python
In [29]: set1 = {1,3}

In [30]: set1
Out[30]: {1, 3}

In [31]: set1.add(2)

In [32]: set1
Out[32]: {1, 2, 3}

In [33]: set1.update([2,3,4,5])  # não inclui elemento duplicado

In [34]: set1
Out[34]: {1, 2, 3, 4, 5}

In [35]: set1.remove(6)                            # O item 6 não existe no conjunto, gera erro
---------------------------------------------------------------------------
KeyError                                  Traceback (most recent call last)
<ipython-input-35-722c24176164> in <module>()
----> 1 set1.remove(6)

KeyError: 6

In [36]: set1.discard(6)                       # Nesse caso, não irá gerar erro.

In [37]: set1
Out[37]: {1, 2, 3, 4, 5}
```` 

