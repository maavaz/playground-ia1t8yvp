# Funções em Python

Na programação, funções são blocos de comandos que realizam determinadas tarefas que normalmente precisam ser executadas diversas vezes 
dentro de uma aplicação. Em outras palavras, pode-se dizer que é um pequeno "programa" com vários comandos agrupados em uma função, à qual é dado um nome e que poderá ser chamada/executada em diferentes partes do programa.
 A utilização de funções, muito comum na programação estruturada, pois visa subdividir um programa em partes (módulos) menores que realizam uma tarefa bem definida.

####  <b> Benefícios da utilização de funções: </b>
+ Permite o reaproveitamento de código já construído (por você ou por outros programadores);
+ Evita que um mesmo trecho de código seja repetido várias vezes dentro de um mesmo programa e, com isso, qualquer alteração é feita apenas nesse trecho e de forma simples.
+ Para que os blocos do programa não fiquem grandes demais e, por conseqüência, mais difíceis de entender;
+ Facilita a leitura do programa de maneira que os blocos de código possam ser logicamente compreendidos de forma isolada.

A forma geral de uma função definida pelo usuário é:

![funcao](/imagens/funcao.png)

Uma função necessariamente deve retornar um valor (resultado) ao programa que a chamou, através da comando **return**. Mas, existem situações onde uma função não retorna valor algum (sem comando return), nesse caso, a função é denominada de **procedimento ou sub-rotina**.

As variáveis que aparecem dentro do parênteses da função são denominadas de **parâmetros ou argumentos da função** (variável, 1, variável 2...). 

Uma função pode ter 0 (zero) ou n argumentos ou parâmetros. Parâmetros funcionam como a interface de comunicação (passagem de valores/dados) entre o programa (chamador) e a função, isto é, a forma que um programa passa valores para dentro das funções. 

Os valores não necessariamente precisam estar dentro de variáveis para serem passados para as funções. O programador pode escrever o valor (estático) diretamente nos parênteses.

Os parâmetros são passados para uma função de acordo com a sua posição, isto é, serão atribuídos às variáveis na ordem (posição) em que estas foram declaradas. Ou seja, o primeiro parâmetro da chamada (programa) define o valor do primeiro parâmetro na definição da função, o segundo parâmetro do programa define o valor do segundo parâmetro da função e assim por diante.


O programa exemplo, a seguir, mostra duas funções (com **return**) e um procedimento ou sub-rotina (sem return).
``` python runnable 
def dez():                    # Função sem parâmetro
  return 10
  
def ex_soma(num1, num2):      # Função com parâmetro
  s = num1 + num2
  return s

def exibir(msg, valor):       # Procedimento ou sub-rotina 
  print(msg, valor)
  
numero1 = dez()               # Função irá retornar o número 10

exibir('O valor armazenado em numero1 =', numero1) # Chama a subrotina para exibir a mensagem e o valor armazenado em numero1

numero2 = dez()**2            # O número 10 retornado da função será elevado ao quadrado

exibir('O valor armazenado em numero2 =', numero2) # Chama a subrotina para exibir a mensagem e o valor armazenado em numero2

soma = ex_soma(numero1, numero2)  # Chama a função para realizar a soma de 10 (numero 1) e 100 (numero2)

exibir("A soma dos números é igual a", soma)  # Chama a subrotina para exibir a mensagem e o resultado da soma
```
