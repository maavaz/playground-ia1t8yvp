# Fatiamento (Slicing)
---

Uma operação muito interessante que Python fornece para manipulação de Listas,strings e tuplas é o fatiamento (slicing). Fatiamento significa extrair apenas uma parte (subconjunto) da Lista, String ou Tupla. 

Essa operação permite delimitar os limites inferior e superior do pedaço da lista que queremos acessar. Para delimitarmos esses limites usamos a seguinte forma geral:
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

In [8]: semana[-4:-1] # Índices negativos 
Out[8]: ['QUI', 'SEX', 'SAB']

In [9]: semana[-7:]  ## Índices negativos 
Out[9]: ['SEG', 'TER', 'QUA', 'QUI', 'SEX', 'SAB', 'DOM']

In [10]: semana[-5:]
Out[10]: ['QUA', 'QUI', 'SEX', 'SAB', 'DOM']
```
