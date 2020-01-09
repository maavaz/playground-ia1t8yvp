### Operadores de lista
A linguagem Python dispõe de vários métodos e operadores para auxiliar na manipulação de listas. O operador de acesso aos itens de uma lista permite acessar o conteúdo (item) a partir de um índice que marca a posição do item no conjunto. Para compreendê-lo, é importante entender como os dados são armazenados nessa estrutura:

![lista](/imagens/lista.gif)

O primeiro elemento da lista está posicionado sempre na posição 0 (zero) e o útimo na posição n - 1, onde n é o comprimento da lista. Note pela figura que o python permite acessar os elementos na ordem inversa utilizando um índice negativo. Nesse, caso o primeiro elemento está na posição -1 e o último na posição -n, onde n é o comprimento da lista.

Exemplos:
``` python
In [1]: semana = ['SEG', 'TER', 'QUAR', 'QUI', 'SEX','SAB', 'DOM']  # Criando a Lista SEMANA

In [2]: semana[3] #Acessando o conteúdo do quarto elemento da lista (índice = 3)
Out[2]: 'QUI'

In [3]: semana[-4] #Acessando o conteúdo do quarto elemento da lista utilizando o índice negatico (índice = -4)
Out[3]: 'QUI'
```
#### Comprimento da Lista

É possível saber o comprimento (número de itens) de uma lista, através da função **len()**, como mostra o exemplo abaixo.
``` python
len(semana)
Out[4]: 7
```
Podemos percorrer todos os elementos da lista utilizando a estrutura **for**. Isso pode ser feito de 2 maneiras vistas no exemplo abaixo.
``` python runnable
semana = ['SEG', 'TER', 'QUAR', 'QUI', 'SEX','SAB', 'DOM']

for i in range(len(semana)):
    print(semana[i])
    
for i in semana:
    print(i)
```    

