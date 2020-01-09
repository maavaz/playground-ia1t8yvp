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

In[1]: lista = []   #Criando uma Lista vazia
In[2]: lista
Out[2]: []
In[3]: lista = ['O carro','peixe',123,111] # Os elementos de uma lista não precisam ser do mesmo tipo
In[4]: lista
Out[4]: ['O carro', 'peixe', 123, 111]
In[5]: nova_lista = ['pedra',lista]
In[6]: nova_lista
Out[6]: ['pedra', ['O carro', 'peixe', 123, 111]]
In[7]: semana = ['Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira','Sábado', 'Domingo'] 
In[8]: semana
Out[8]: ['Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira','Sábado', 'Domingo'] 
In[9]: In[1]: x = [0, 1, 2, 3, 4, 5] 
In[10]: x
Out[10]: [0, 1, 2, 3, 4, 5]
