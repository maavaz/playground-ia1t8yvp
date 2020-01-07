# Funções em Python

Na programação, funções são blocos de comandos que realizam determinadas tarefas que normalmente precisam ser executadas diversas vezes 
dentro de uma aplicação. Em outras palavras, pode-se dizer que é um pequeno "programa" com vários comandos agrupados em uma função, à qual é dado um nome e que poderá ser chamada/executada em diferentes partes do programa.
 A utilização de funções, muito comum na programação estruturada, visa subdividir um programa em partes (módulos) menores que realizam uma tarefa bem definida.

#### Benefícios da utilização de funções:
+ Permite o reaproveitamento de código já construído(por você ou por outros programadores);
+ Evita que um mesmo trecho de código seja repetido várias vezes dentro de um mesmo programa e, com isso, qualquer alteração é feita apenas nesse trecho e de forma simples.
+ Para que os blocos do programa não fiquem grandes demais e, por conseqüência, mais difíceis de entender;
+ Facilita a leitura do programa de maneira que os blocos de código possam ser logicamente compreendidos de forma isolada.~

A forma geral de uma função definida pelo usuário é:

```
def nome da função(variável 1, variável 2, ... , variável n):
 comandos
 return valor

```
Uma função necessariamente deve retornar um valor (resultado) ao programa que a chamou através da comando **return**. Mas, existem situações onde uma função não retorna valor algum (sem comando return), nesse caso, a função é denominada de procedimento ou sub-rotina.

As variáveis que aparecem dentro do parênteses da função são denominadas de **parâmetros ou argumentos da função**. 

Uma função pode ter 0 (zero) ou n argumentos ou parâmetros. Parâmetros funcionam como a interface de comunicação (passagem de valores/dados) entre o programa (chamador) e a função, isto é, a forma que um programa passa valores para dentro das funções. 

Os valores não necessariamente precisam estar dentro de variáveis para serem passados para as funções. O programador pode escrever o valor (estático) diretamente nos parênteses.



O programa exemplo, a seguir, mostra uma função e uma sub-rotina.
``` runnable python
def ex_soma(num1, num2):
  s = num1 + num2
 return s

def exibir(msg, valor):
  print(msg, valor)
  
numero1 = 10
numero2 = 100
soma = ex_soma(numero1, numero2)
exibir("A soma dos números é igual a", 
```
