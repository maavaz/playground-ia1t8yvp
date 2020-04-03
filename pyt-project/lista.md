# Tipos de dados Estruturados

Os tipos de dados estruturado são dados compostos que funcionam como coleções. Existem três tipos de dados estruturados que são nativos: 
+ Listas
+ Tuplas 
+ Dicionários.  
+ Sets

###  <b> Listas  </b>
O tipo de dado lista é uma coleção de itens, armazenados em um lugar e dispostos em uma ordem em particular. Esse conjunto de itens está organizado de forma linear, na qual cada um pode ser acessado a partir de um índice, que representa sua posição na coleção (iniciando em zero).
A forma geral para se definir uma Lista é:
![funcao](/imagens/nlista.png)

 <b> Exemplos de criação de listas </b>

```python runnable
lista = []   #Criando uma Lista vazia

print("\n\nlista = ", lista)

x = [0, 1, 2, 3, 4, 5]  #Lista com todos os item de mesmo tipo (int)

print("\n\nx =", x)

l = list((1,2,3,4,5))  # usando o método list() transforma uma sequência em lista
print("\n\nl = ", l)

lrange = list(range(5))    #criando listas com Range()
print("\n\nlrange = ", lrange)

semana = ['Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira','Sábado', 'Domingo']

print("\n\nsemana = ", semana)

lista = ['O carro','peixe',123,111]        # Os elementos de uma lista não precisam ser do mesmo tipo
 
print("\n\nlista = ", lista)

nova_lista = ['pedra',lista] # um elemento da lista pode ser outra lista

print("\n\nnova_lista = ", nova_lista)


```
