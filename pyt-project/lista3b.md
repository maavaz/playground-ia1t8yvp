# Compreensão de Listas (Exemplos)

**Problema 1:  for** Simples <br>
Criar uma lista **b** onde seus elementos são os da lista **a** (apresentada abaixo) elevados ao cubo. <br>
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

print([elemento ** 3 for elemento in a if elemento % 8 == 0])

#print(b)
```
