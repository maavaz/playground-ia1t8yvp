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

Faça um programa que receba a temperatura média de cada mês do ano e armazene-as em uma lista. Após isto, calcule a média anual das temperaturas e mostre todas as temperaturas acima da média anual, e em que mês elas ocorreram (mostrar o mês por extenso: 1 – Janeiro, 2 – Fevereiro, . . . ).
