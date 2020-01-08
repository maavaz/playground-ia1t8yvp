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

Faça um programa que leia duas notas de um aluno numa turma de 10 alunos. Para cada aluno, calcular a média ponderadas das notas, sabendo que a <b>nota1</b> tem <b>peso = 4</b> e a <b>nota2</b> tem <b>peso = 6</b>. Imprimir a média do aluno e o conceito final, conforme tabela abaixo:

 **Intervalo**   **Conceito** <p></p>
   0.0 a 4.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D     
   5.0 a 6.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; C     
   7.0 a 8.9  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; B     
   9.0 a 10.0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A     


Fazer 2 funções:

+ Função lambda para calcular a media ponderada das notas. Argumentos de entrada duas notas, Saída a média. 
+ Função Local que irá receber como argumento de entrada a média das notas e retornar o conceito conforme a tabela acima.

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor.sh" })

::: Solução
``` python
ponder = lambda n1, n2: n1 * 0.4 + n2 * 0.6

def conceito(media):
    if media < 5.0:
        m = 'D'
    elif media < 7.0:
        m = 'C'
    elif media < 9.0:
        m = 'B'
    else:
        m = 'A'
    return m
    
for i in range(10):
   nota1 = float(input('Digite a primeira Nota:'))
   nota2 = float(input('Digite a segunda Nota:'))
   media = ponder(nota1,nota2)
   conc = conceito(media)
   print("A média do aluno é:{0:.2f}".format(media)) 
   print("O conceito do aluno é:", conc) 
 ```  
:::

---   
 #### Exercício 2  
---

Faça um programa para calcular o valor das parcelas de um financiamento no regime de juros compostos com capitalização mensal. O programa deverá ler o valor do financiamento e o número de parcelas, calcular e exibir o valor da parcela. O programa termina quando o valor do financiamento for igual a zero. Abaixo apresentamos a tabela contendo os prazos de financiamentos e a taxa de juros anual:


**Prazo**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**taxa a.a.** <p></p>
   6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 7%    
  12&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 10%    
  18&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 12%    
  24&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 15%    
  36&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 18%    

Fazer uma função denominada <b>float financiamento()</b> que deverá receber o valor do financiamento e o número de parcelas, calcular e retornar o valor da prestação. Utilizar a estrutura </>switch ... case</b> apar selecionar a taxa de juros representada em valor decimal. Como a capitalização é mensal, dividir a taxa por 12. 
A fórmula de cálcula da prestação é: 

$`prestacao=valor financiamento × \frac{(1+taxa)^p × taxa}{(1+taxa)^p  - 1}`$

<b>*obs: p = número de parcelas</b>


---
 #### Exercício 3  
---

A padaria Sópão vende diariamente uma certa quantidade de pães franceses e uma quantidade de broas. Cada pãozinho custa R$ 0,80 e a broa custa R$ 2,50. Do total arrecadado, 43% corresponde aos custos de fabricação. Do restante, Seu joão guarda 15% numa conta de poupança e 15% ele converte em Euros para sua viagem Anual. Sabe-se que 1 Euro custa R$ 4,60. Com base nestes fatos, faça um progrma para ler as quantidades de pães e de broas, calcular a venda total de pãos e broas, o custo de fabricação, quanto irá guardar na poupança e quantos euros irá comprar. Ao final exibir os dados calculados.
