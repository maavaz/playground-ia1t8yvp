# Compreensão de Listas (Exemplos)

**Problema 1:  for** Simples <br>
Criar uma lista **b** com os elementos da lista **a** (apresentada abaixo) elevados ao cubo. <br>
**a = [2, 3, 4, 5, 6]** <br>

### Solução em python:
``` python runnable
a = [2,3,4,5,6]
b = []

for elemento in a:
    b.append(elemento**3)

print(b)
```

### Solução utilizando compressão:
``` python runnable
a = [2,3,4,5,6]

b = [elemento ** 3 for elemento in a]

print(b)
```

**Problema 2:  for** com seleção condicional **if** <br>
Seguindo o problema anterior, criar a lista **b** apenas com elementos divisíveis por 8.<br>

### Solução em python:
``` python runnable
a = [2,3,4,5,6]
b = []

for elemento in a:
    x = elemento ** 3
    if x % 8 == 0:
       b.append(x)

print(b)
```

### Solução utilizando compressão:
``` python runnable
a = [2,3,4,5,6]

b = [elemento ** 3 for elemento in a if (elemento**3) % 8 == 0]

print(b)
```

**Problema 3:  for** com seleção condicional composta **if-else** <br>
Criar uma lista **b** com os elementos da lista **a** (apresentada abaixo) elevados ao quadrado caso o elemento seja par, do contrário elevado ao cubo. <br><br>

### Solução em python:
``` python runnable
a = [2,3,4,5,6]
b = []

for elemento in a:
    if elemento % 2 == 0:
       b.append(elemento ** 2)
    else:
       b.append(elemento ** 3)

print(b)
```

### Solução utilizando compressão:
``` python runnable
a = [2,3,4,5,6]

b = [elemento ** 2 if elemento % 2 == 0 else elemento ** 3 for elemento in a]

print(b)
```

**Problema 4:** Múltiplos **for** <br>
Criar uma lista **list** com os elementos pares da matriz 3x3 **mat** (apresentada abaixo). <br><br>

### Solução em python:
``` python runnable
mat = [[2,3,4],
     [7,9,10],
     [12,13,14]]
list = []

for linha in mat:
  for elemento in linha:
    if elemento % 2 == 0:
       list.append(elemento)

print(list)
```

### Solução utilizando compressão:
``` python runnable
mat = [[2,3,4],
     [7,9,10],
     [12,13,14]]

list = [elemento for linha in mat for elemento in linha if elemento % 2 == 0]

print(list)
```
