# Sets

**Set** é uma coleção (estrutura de dados) não ordenada e não indexada de itens únicos. Os **Sets** podem ser usados para executarem operações matemáticas de conjuntos, tais como: união, interseção, etc.

## Criando e acessando dados em Sets

Um **set** é criado colocando-se os seus the itens (elementos) entre chave ({}), separados por vírgulas ou usando a função pré-definida **set()**, que transforma sequências de valores em **sets**.
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
 
 ## Incluindo e Alterando itens em Sets
 
**Set** são mutáveis mas, como não são ordenadas, a indexação não tem significado. Logo, não podemos acessar ou alterar um elemento do conjunto usando indexação ou slice. O conjunto não suporta.

Podemos adicionar um único elemento usando o método **add()** e vários elementos usando o método **update()**. O método **update()** pode levar tuplas, listas, strings ou outros conjuntos como argumento. Em todos os casos, duplicatas são evitadas.
