# Tipos de dados Estruturados

Os tipos de dados estruturado são dados compostos que funcionam como coleções. Existem três tipos de dados estruturados que são nativos: 
+ Listas
+ Tuplas 
+ Dicionários.  

### Listas
O tipo de dado lista é uma coleção de itens, armazenados em um lugar e dispostos em uma ordem em particular. Esse conjunto de itens estão organizados de forma linear, na qual cada um pode ser acessado a partir de um índice, que representa sua posição na coleção (iniciando em zero).
A forma geral para se definir uma Lista é:
```
nome da lista = [elemento 1, elemento 2, elemento 3, … ]
```
exemplos de criação de listas
``` python
In [1]: lista = []   #Criando uma Lista vazia

In [2]: lista

Out[2]: []   #lista vazia

In [3]: x = [0, 1, 2, 3, 4, 5]  #Lista com todos os item de mesmo tipo (int)

In [4]: x

Out[4]: [0, 1, 2, 3, 4, 5]

In [5]: semana = ['Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira','Sábado', 'Domingo']

In [6]: semana

Out[6]: 
['Segunda-feira',
 'Terça-feira',
 'Quarta-feira',
 'Quinta-feira',
 'Sexta-feira',
 'Sábado',
 'Domingo']
 
 In [7]: lista = ['O carro','peixe',123,111]        # Os elementos de uma lista não precisam ser do mesmo tipo
 
In [8]: lista

Out[8]: ['O carro', 'peixe', 123, 111]

In [9]: nova_lista = ['pedra',lista] # um elemento da lista pode ser outra lista

In [10]: nova_lista

Out[10]: ['pedra', ['O carro', 'peixe', 123, 111]]  
```

