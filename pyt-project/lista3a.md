# Compreensão de Listas 

Compreensão de Listas (CL) é uma funcionalidade muito poderosa da linguagem Python que possibilita criar uma lista nova aplicando uma função para cada elemento da lista
original. Semelhante a notação de conjuntos da matemática. Permite a Economia de código, pois é escrita em uma linha apenas. O formato geral da compreensão é:
![funcao](/imagens/compreensão.png)

+ Um exemplo simples:<br>
     **S = { x | x &isin; N,x < 10}** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in range(0, 10)]** <br><br>
     **S = { x | x &isin; Z, x < 20, x é par}** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in range(0, 20) if x % 2 == 0]**<br>

     **S = { x | x é uma letra na palavra 'BANANA', x é vogal}** &nbsp;&nbsp;&nbsp;em python:&nbsp;&nbsp; **S = [x for x in 'BANANA' if x in ['A', 'E', 'I', 'O', 'U']]**
     
Agora vejamos os códigos Python correspondentes em CL, na mesma ordem:

[x**2 for x in range(0, 10)]
[x for x in range(1, 20) if x % 2 == 0]
[x for x in ‘MATEMÁTICA’ if x in [‘A’, ‘E’, ‘I’, ‘O’, ‘U’]]
Parece intuitivo, certo?

Não se preocupe se parecer um pouco confuso. Continue me acompanhando, vai ficar mais claro na medida em que avançamos. Vamos dar um passo atrás e analisar o que está acontecendo aqui. Cada um dos exemplos acima envolve 3 coisas – iteração, filtragem condicional e processamento. Por isso, talvez você possa dizer que se trata apenas de uma outra representação de loop FOR.

Em termo gerais, um loop FOR funciona assim:

for (conjunto de valores a iterar):
   if (filtro condicional):
      expressão_de_retorno()
O mesmo código pode ser construído de modo CL numa única linha:
[ expressão_de_retorno() for (conjunto de valores a iterar) if (filtro condicional) ]
Considere agora outro exemplo: {x: x é um número natural menor ou igual a 100, x é uma raiz quadrada exata}. Isso pode ser resolvido com um loop FOR da seguinte forma:

for i in range(1, 101):         #iterador
   if int(i**0.5) == i**0.5:    #filtro condicional
      print i                   #retorno
Agora, para criar o código CL, precisamos apenas plugar as diferentes partes:

[ i for i in range(1, 100) if int(i**0.5) == i**0.5 ]
