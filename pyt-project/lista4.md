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
Faça um programa que receba a temperatura média de cada mês do ano e armazene-as em uma lista. Após isto, calcule a média anual das temperaturas e mostre todas as temperaturas acima da média anual, e em que mês elas ocorreram (mostrar o mês por extenso: Janeiro, Fevereiro, . . . ).

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

#### Exercício 2
Quatro candidatos foram para o segundo turno nas eleições para presidente de um país da America do Sul:
    1 - Candidato A, 2 - Candidato B, 3 - Candidato C, 4 - Candidato D. 
Faça um programa que receba os votos dos eleitores(final da votação voto = -1) e ao final exiba a quantidade de votos e o percentual que cada canditado obteve e qual candidato foi declarado vencedor (maioria simples). 
    
Obs: para realizar a soma total dos votos dos candidatos utilize a função sum(lista).
Obs1: O primeiro índice da lista é zero e, para compatibilizá-lo ao número do candidato subtraia 1 unidade.
    
::: Solução
``` python
totais = [0,0,0,0]
candidatos =['Candidato A', 'Candidato B', 'Candidato C', 'Candidato D']

print('1 - Candidato A \n2 - Candidato B\n3 - Candidato C\n4 - Candidato D\n')
voto = int(input('Digite o número do Candidato:'))
while voto != -1:
    totais[voto-1] += 1                              #voto -1 serve para compatibilizar a posição do candidato na lista
    print('1 - Candidato A \n2 - Candidato B\n3 - Candidato C\n4 - Candidato D\n')
    voto = int(input('Digite o número do Candidato:'))

totalvotos = sum(totais)                             # função sum(lista) soma os valores dos itens da lista
vencedor = max(totais)                               # função max(lista) retorna o maior valor da lista 

for i in range(len(totais)):
    perc = totais[i]/totalvotos * 100
    print('\nCandidato: {0}\nvotos: {1}\nPercentual:{2:.2f}%'.format(candidatos[i],totais[i], perc))
    if vencedor == totais[i]:
        v = i

print('\n\nO candidato', candidatos[v], ' foi eleito PRESIDENTE')
```
:::
