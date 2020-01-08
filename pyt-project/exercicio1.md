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

```python
valorum   = 5 ** 2
valordois = 5 ** 3
print(valorum, valordois, valorum+valordois)
```
?[Qual a implicação no resultado se o comando return não for usado em uma função?](single)
-[ ] retornará o valor 0 
-[ ] retornará o valor -1 (indicação de erro na execução)
-[x] não irá retornar valor algum
-[ ] Erro de Sinataxe!!!

?[Um programa deseja usar a função pi do pacote math, qual a sintaxe para sua utilização?](single)
-[ ] print(math.pi) 
-[ ] print(pi)
-[x] from math import pi
     print(pi)
-[ ] from math import pi
     print(math.pi)
---
### Exercícios
---

OBS:Os exercícios a seguir não possuem gabarito, caso desejem a correção favor enviar sua solução por mensagem no Tech.io. Desenvolva-os no editor python de sua preferência

---
 #### Exercício 1  
---

Faça um programa para calcular a quantidade de latas de tintas para pintar uma parede. O programa deverá solicitar ao usuário, a altura (float) e o comprimento(float) da parede. Considere que a cobertura da tinta é de 1 litro para cada 3 metros quadrados e que a tinta é vendida em latas de 3,6 litros, que custam R$ 107,00. Informe ao usuário a quantidades de latas de tinta a serem compradas e o preço total.

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
