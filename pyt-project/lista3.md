# Fatiamento (Slicing)
---

Uma operação muito interessante que Python fornece para manipulação de Listas,strings e tuplas é o fatiamento (slicing). Fatiamento significa extrair apenas uma parte (subconjunto) da Lista, String ou Tupla. 

Essa operação permite delimitar os limites inferior e superior do pedaço da lista que queremos acessar. Para delimitarmos esses limites usamos a seguinte forma geral:
![funcao](/imagens/slice.png)
```
                      Lista[inferior:superior]
                      
 Obs: O limite superior não é incluído no fatiamento.
```
Exemplos:
``` python
In [1]: semana = ['SEG', 'TER', 'QUA', 'QUI', 'SEX','SAB', 'DOM']

In [2]: fat = semana[1:4] # Fatiamento inclui apenas os índices de 1 até 3

In [3]: fat
Out[3]: ['TER', 'QUA', 'QUI']

In [4]: fat = semana[:4] # Ausência do Limite Inferior indica fatiamento a partir do primeiro elemento 

In [5]: fat
Out[5]: ['SEG', 'TER', 'QUA', 'QUI']

In [8]: semana[-4:-1] # Índices negativos. O item da última posição (-1) não é exibido
Out[8]: ['QUI', 'SEX', 'SAB']

In [9]: semana[-4:]  ## Índices negativos. Nesse caso a última posição (-1) é exibida.
Out[9]: ['QUI', 'SEX', 'SAB', 'DOM']

In [10]: semana[-5:]
Out[10]: ['QUA', 'QUI', 'SEX', 'SAB', 'DOM']
```
Pode-se especificar o passo a ser somado ao índice para recuperação dos elementos. Forma geral:
```
                     Lista[inferior:superior:passo]
```
Exemplo:
```
In [12]: semana[1:6:2]  # Exibe os elementos de 2 em 2 a partir do índice 1 (índices: 1, 3, 5).
Out[12]: ['TER', 'QUI', 'SAB']
```
