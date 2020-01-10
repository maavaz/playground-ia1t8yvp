# Exercitando

``` python
cores = ['Verde', 'Vermelho', 'Branco', 'Preto', 'Azul', 'Amarelo']

```
?[Dada a lista "cores" acima, utilizando a técnica de slice que opção abaixo irá gerar a lista fluminense - ('Verde', 'Vermelho', 'Branco')?]
-[ ] cores[ :4]
-[ ] cores[1:3]
-[x] cores[ :3]
-[ ] cores[-3:-1]

?[Ainda com relação a lista "cores", que opção abaixo irá gerar a lista flamengo - ('Vermelho', 'Preto')?]
-[ ] cores[ :3:2]
-[x] cores[1:5:2]
-[ ] cores[1:6:2]
-[ ] cores[ :5:2]

``` python
lista = ['ab'] * 5
print(lista)
```
?[Ao executar o trecho de código acima, o que será exibido? ]
-[x] ['ab', 'ab', 'ab', 'ab', 'ab']
-[ ] ['a', 'b', 'a', 'b', 'a', 'b', 'a', 'b', 'a', 'b']
-[ ] ['a', 'a', 'a', 'a', 'a', 'b', 'b', 'b', 'b', 'b']
-[ ] ['ababababab']

``` python
a=[1,2,3,4,5,6,7,8,9]
b = a[::2] + a[1::2]
print(b)
```
?[Ao executar o trecho de código acima, o que será exibido? ]
-[ ] [2, 1, 2] 
-[x] [1, 3, 5, 7, 9, 2, 4, 6, 8]
-[ ] [9, 8, 7, 6, 5, 4, 3, 2, 1]]
-[ ] Erro de Sintaxe!!! 
---

#### Exercício 1
---
Faça um programa que receba a temperatura média de cada mês do ano e armazene-as em uma lista. Após isto, calcule a média anual das temperaturas e mostre todas as temperaturas acima da média anual, e em que mês elas ocorreram (mostrar o mês por extenso: 1 – Janeiro, 2 – Fevereiro, . . . ).

+ Faça uma função local que retorne o mês por extenso (Criar uma lista de meses do ano). atributo de entrada: valor inteiro correspondente ao índice da lista do mês solicitado; atributo de saída: Mês por extenso.

+ Faça uma função lambda que calcule a média das temperaturas anuais. Atributo de entrada: Lista de temperaturas.

OBS: Utilize as funções sum(lista) e len(lista) para o cálcula da média

::: Solução
``` python
def extenso(ind):
    meses = ['Janeiro', 'Fevereiro','Março', 'Abril', 'Maio', 'Junho', 'Julho', 'Agosto', 'Setembro', 'Outubro', 'Novembro', 'Dezembro']
    return meses[ind]

media = lambda x: sum(x)/len(x)

tempano = [] #criar a lista de temperaturas anual vazia
for i in range(12):
    temp = float(input('Digite a temperatura do mês:'))
    tempano.append(temp) 

mediano = media(tempano)

for t in range(len(tempano)):
    if tempano[t] > mediano:
        mes = extenso(t)
        print('temperatura {0:.2f} maior que a média anual {1:.2f} ocorrida no mês: {2}'.format(tempano[t], mediano, mes))
```


