# Testando os conhecimentos....
---
``` python
funcao = lambda y: return y
h = funcao(4)
print(h)
```
?[Dado o trecho de código acima, qual será o resultado de sua execução?](single)
-[ ] 4
-[ ] 0 
-[x] Erro de Sintaxe !! 
-[ ] return 4    

``` python
funcao = lambda y: y ** 2
h = funcao(4)
print(h)
```
?[Dado o trecho de código acima, qual será o resultado de sua execução?](single)
-[ ] 8
-[x] 16
-[ ] 4
-[ ] Erro de Sintaxe !! 

``` python
def x(a, b):
   return a * b
```   
?[Dada a definição da função acima, qual seria a função lambda correspondente?](single)
-[ ] funcao = a lambda b: return a * b 
-[ ] funcao = lambda (a, b) : return a * b
-[x] funcao = lambda a, b: a * b
-[ ] funcao = lambda (a, b): a * b

``` python
def imprime(texto):
    print(texto, "é muito bom!!!")

imprime('Programar')
```
?[Qual o resultado da execução do trecho de código acima?](single)
-[x] Programar é muito bom!!!
-[ ] é muito bom!!!
-[ ] texto é muito bom!!!
-[ ] programar

?[Qual a implicação no resultado se o comando return não for usado em uma função?](single)
-[ ] retornará o valor 0 
-[ ] Erro na execução da Função !!!
-[x] não irá retornar valor algum
-[ ] Erro de Sinataxe!!!

_--
 #### Exercício 1  
---

Exercício 1
----
Faça um programa que leia duas notas de um aluno numa turma de 10 alunos. Para cada aluno, calcular a média ponderadas das notas, sabendo que a <b>nota1</b> tem <b>peso = 4</b> e a <b>nota2</b> tem <b>peso = 6</b>. Imprimir a média do aluno e o conceito final, conforme tabela abaixo:

 **Intervalo**   **Conceito** <p></p>
   0.0 a 4.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D     
   5.0 a 6.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; C     
   7.0 a 8.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B     
   9.0 a 10.0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A     


Fazer 2 funções:

+ Função lambda para calcular a media ponderada das notas. Argumentos de entrada duas notas, Saída a média. 
+ Função Local que irá receber como argumento de entrada a média das notas e retornar o conceito conforme a tabela acima.

---   
 #### Exercício 2  
---

Um determinado prêmio de loteria saiu para um bolão de três amigos. Uma lei garante que todo prêmio de loteria deva pagar um imposto de 7% para os cofres estaduais. Do total descontado o imposto, os amigos irão dividir o prêmio da seguinte maneira:

+ O primeiro ganhador recebera 46%;
+ O segundo recebera 32%;
+ O terceiro recebera o restante;
Faça um programa que leia o valor total do prêmio, calcule o desconto, o valor que cada um tem direito e imprima o total do prêmio, o premio descontado o imposto e a quantia recebida por cada um dos ganhadores.

---
 #### Exercício 3  
---

A padaria Sópão vende diariamente uma certa quantidade de pães franceses e uma quantidade de broas. Cada pãozinho custa R$ 0,80 e a broa custa R$ 2,50. Do total arrecadado, 43% corresponde aos custos de fabricação. Do restante, Seu joão guarda 15% numa conta de poupança e 15% ele converte em Euros para sua viagem Anual. Sabe-se que 1 Euro custa R$ 4,60. Com base nestes fatos, faça um progrma para ler as quantidades de pães e de broas, calcular a venda total de pãos e broas, o custo de fabricação, quanto irá guardar na poupança e quantos euros irá comprar. Ao final exibir os dados calculados.
