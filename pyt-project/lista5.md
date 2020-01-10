# Listas e Strings

Uma string é uma sequência de caracteres e uma lista é uma sequência de valores, mas uma lista de caracteres não é a mesma coisa que uma string. Mas, em ambos os casos você pode individualizar os itens (caracteres) utilizando índices. O comando **list** é usado para conversão de uma string em uma lista de caracteres:
``` python
In [1]: str = 'Programação Python' # Criação de uma string

In [2]: str[0] #Primeiro caracter da String
Out[2]: 'P'

In [3]: ling = str[12:]  # Fatiamento (Slice) de String

In [4]: ling
Out[4]: 'Python'

In [5]: listastr = list(str) # Transformando uma string numa lista de caracteres

In [6]: listastr  
Out[6]:  ['P', 'r', 'o', 'g', 'r', 'a', 'm', 'a', 'ç', 'ã', 'o',' ', 'P', 'y', 't', 'h', 'o', 'n']
```

O método **.split()** pode ser usado para quebrar uma string (com várias palavras) numa lista de strings (palavras):
``` python

In [7]: palavras = str.split()   # Cria a lista palavras com 2 strings

In [8]: palavras
Out[8]: ['Programação', 'Python']
```
A função split pode ter um argument, chamado delimiter, para especificar quais caracteres podem ser usados para demonstrar os limites das palavras (o padrão é o espaço). O exemplo seguinte usa um hífen como delimitador:
``` python
In [9]: str = 'Aprenda+programação+Python'

In [10]: delimiter = '+'

In [11]: palavras = str.split(delimiter)

In [12]: palavras
Out[12]: ['Aprenda', 'programação', 'Python']
```

A função **.join()** é o contrário de split. Ele toma uma lista de strings e concatena os elementos. join é um método de string, então é preciso invocá-lo no delimitador e passar a lista como parâmetro:
``` python
In [13]: delimiter=' '

In [14]: str = delimiter.join(palavras)

In [15]: str
Out[15]: 'Aprenda programação Python'
``` 
