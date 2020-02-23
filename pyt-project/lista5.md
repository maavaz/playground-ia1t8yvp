# Listas e Strings

Uma string é uma sequência de caracteres e uma lista é uma sequência de valores, mas uma lista de caracteres não é a mesma coisa que uma string. Mas, em ambos os casos você pode individualizar os itens (caracteres) utilizando índices. O comando **list** é usado para conversão de uma string em uma lista de caracteres:

``` python
# Criando de uma string
In [1]: str = 'Programação Python'

# Usando índice para selecionar um caracter da String
In [2]: str[0] 
Out[2]: 'P'

# Realizando o fatiamento (slicing) de string para selecionar uma substring
In [3]: ling = str[12:]  

In [4]: ling
Out[4]: 'Python'

 # Transformando uma string numa lista de caracteres
In [5]: listastr = list(str)

In [6]: listastr  
Out[6]:  ['P', 'r', 'o', 'g', 'r', 'a', 'm', 'a', 'ç', 'ã', 'o',' ', 'P', 'y', 't', 'h', 'o', 'n']</b>
```


O método **.split()** pode ser usado para quebrar uma string (com várias palavras) numa lista de strings (palavras):

``` python
In [1]: str = 'Programação Python'
....

# Usando o método split() para dividir a string (usando como separador o caracter espaço) em uma lista em 2 substrings
In [7]: palavras = str.split()   

In [8]: palavras
Out[8]: ['Programação', 'Python']
```
A função  <b>split() </b> pode ter um argumento, chamado delimiter, para especificar quais caracteres podem ser usados para demonstrar os limites das palavras (o padrão é o espaço). O exemplo seguinte usa um hífen como delimitador:

``` python
# Usando o método split() para dividir a string (usando como separador o caracter +) em uma lista em 3 substrings
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
