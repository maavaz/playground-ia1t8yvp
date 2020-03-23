# Compreensão de Listas (Exemplos)

**Problema:** Criar uma lista **b** onde seus elementos são os elementos da lista **a** (apresentada abaixo) elevados ao cubo. <br>
**a = [2, 3, 4, 5, 6]** <br>

### Solução em python:
``` python runnable
a = [2,3,4,5, 6]
b = []

for elemento in a:
    b.append(elemento**3)

print(b)
```

### Solução utilizando compressão:
``` python runnable
a = [2,3,4,5, 6]

b = [elemento ** 3 for elemento in a]

print(b)
```
