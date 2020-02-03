# Compreensão de Listas 

Compreensão de Listas (CL) é uma funcionalidade muito poderosa da linguagem Python que possibilita criar uma lista nova aplicando uma função para cada elemento da lista
original. Semelhante a notação de conjuntos da matemática. Permite a Economia de código, pois é escrita em uma linha apenas. O formato geral da compreensão é:
![funcao](/imagens/compreensão.png)

+ Um exemplo simples:<br>
     **S = { x | x &isin; N,x < 10}** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in range(0, 10)]** <br><br>
     **S = { x | x &isin; Z, x < 20, x é par}** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in range(0, 20) if x % 2 == 0]**<br>

     **S = { x | x é uma letra na palavra 'BANANA', x é vogal}** &nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in 'BANANA' if x in ['A', 'E', 'I', 'O', 'U']]**
     
Agora execute os exemplos e veja os resultados:
``` python runnable
 #Conjunto (lista)  dos números Naturais de 0 até 9 
S = [x for x in range(0, 10)]
print(S)
 
#Conjunto (lista) do números inteiros de 0 até 18
S = [x for x in range(0, 20) if x % 2 == 0]
print(S)

#Conjunto (lista) das vogais da palavra BANANA
S = [x for x in 'BANANA' if x in ['A', 'E', 'I', 'O', 'U']]**
print(S)
```
A compreensão que num primeiro momento parace confusa, mas exige apenas exercício. Fazendo uma comparação com a estrutura for, considere o seguinte exemplo: 
S = {x | x x &isin; N, x &le; 100, x é uma raiz quadrada exata}. 

Escrito utilizando a estrutura FOR:
``` python
for i in range(1, 101):         #iterador
   if int(i**0.5) == i**0.5:    #filtro condicional
      print i                   #retorno
```
Escrito em código CL:
``` python
[ i for i in range(1, 100) if int(i**0.5) == i**0.5 ]
```
