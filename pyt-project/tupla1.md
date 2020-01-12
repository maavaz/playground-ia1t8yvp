# Exercitando
?[Dada as tuplas x e y: x = (3, "Alô", "Velho", "Novo") y = (4, "Ano", "Mundo", "Feliz", "Natal"). Qual das opções abaixo exibirá a frase: "Feliz Ano Novo"?]
- [ ] print(y[1] + y[3] + x[3])
- [ ] print(y[3] + ' ' + y[2] + ' ' + x[2])
- [X] print(y[3] + ' ' + y[1] + ' ' + x[3])
- [ ] print(y[3] + y[2] + x[2])

?[Parece uma Listam mas seus elementos são fixos.Qual das opções abaixo apresenta o nome da estrutura?]
- [ ] Set
- [x] Tupla
- [ ] Dicionário
- [ ] Vetor

#### Exercício 1
---
Faça um programa para calcular o valor pago no pedido de um usuário em uma lanchonete. Para isso, o programa deve receber do usuário, os códigos dos sanduiches e as respectivas quantidades. Calcule e mostre o nome do sanduiche, valor unitario, quantidade e o valor a ser pago pelo item  e o total geral do pedido.
O programa termina quando o código do sanduiche for igual a 0 (zero).
A seguir é apresentado o Menu da lanchonete:
<br>
Codigo&nbsp;&nbsp;&nbsp;Sanduíche&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Preço <br>
100&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hamburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 12,00<br>
200&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Cheeseburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 15,00<br>
300&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Duplo Cheeseburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 20,00<br>
400&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;cheeseFrango&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 18,00<br>
500&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hot Linguiça&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 19,00<br>
Fazer uma função que retorna o nome e o preço unitário do sanduiche escolhido. <br>Entrada da função: Código do Sanduíche. <br>Saída: Uma tupla contendo o nome e o preço unitário (faça uma pesquisa como retornar uma tupla de função). A função deverá ter a tabela contendo o menu (cada item da tabela é uma tupla com código sanduiche e preço).

::: Solução
``` python
def sanduba(cod):
    menu = [(100,'HamBurger',12.00), (200,'CheeseBurger', 15.00), (300, 'Duplo CheeseBurger', 20.00),(400,'CheeseFrango', 18.00),(500, 'Hot Linguiça', 19.00)]
     
    for c, sand, pr in menu:
        if c == cod:
           return sand, pr 
    return '',0.0
def imprimenota(ped):
    tot = 0
    totg = 0
    print('Sanduiche            Quantidade        V.Unit        Total')
    
    for (sand,qtd,pr) in pedido:
        tot = qtd * pr 
        print(sand, (24 - len(sand))*' ', qtd, '           ', pr, '        ', tot)
        totg += tot
    print('                                    total da Nota: ', totg)
          
pedido = []
cod = int(input('Digite o código do sanduiche ou -1 para fechar o pedido:'))
while cod != -1:
     sand, pr = sanduba(cod)
     if sand != '':
        qtd = int(input('Digite a quantidade:'))
        pedido.append((sand,qtd,pr)) 
     cod = int(input('Digite o código do sanduiche ou -1 para fechar o pedido:'))
imprimenota(pedido)    
```

:::

---
#### Exercício 2
---
Faça um programa para ajudar o administrador de rede de uma empresa que precisa saber qual o espaço em disco ocupado pelos arquivos dos usuários, e identificar os usuários com maior espaço ocupado. A entrada do programa é a lista abaixo onde cada linha possui o nome do usuário e o total (em bytes) ocupado pelos arquivos:<br>
alexandre&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;456123789<br>
anderson&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1245698456<br>
antonio&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;123456456<br>
carlos&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;91257581<br>
cesar&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;987458<br>
rosemary&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;789456125<br>
A partir desta lista de entrada, você deve criar um programa que gere um relatórioabaixo, no seguinte formato:<br>
Empresa&nbsp;&nbsp;&nbsp;&nbsp;Uso do espaço em disco pelos usuários<br>
------------------------------------------------------------------------<br>
Nr.&nbsp;&nbsp;&nbsp;&nbsp;Usuário&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Espaço utilizado&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;% do uso <br>

1&nbsp;&nbsp;&nbsp;&nbsp;alexandre&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;434,99 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;16,85%<br>
2&nbsp;&nbsp;&nbsp;&nbsp;anderson&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1187,99 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;46,02%<br>
3&nbsp;&nbsp;&nbsp;&nbsp;antonio&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;117,73 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4,56%<br>
4&nbsp;&nbsp;&nbsp;&nbsp;carlos&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;87,03 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3,37%<br>
5&nbsp;&nbsp;&nbsp;&nbsp;cesar&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0,94 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0,04%<br>
6&nbsp;&nbsp;&nbsp;&nbsp;rosemary&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;752,88 MB&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;29,16%<br>
<br>
Espaço total ocupado: 2581,57 MB<br>
Espaço médio ocupado: 430,26 MB<br>
Os dados de entrada devem ser lidos e armazenados em memória, caso sejam necessários, de forma a agilizar a execução do programa. A conversão do espaço ocupado em disco, de bytes para megabytes (1 Mb = 2<sup>20</sup> bytes) deverá ser feita através de uma função separada, que será chamada pelo programa principal. O cálculo do percentual de uso também deverá ser feito através de uma função, que será chamada pelo programa principal.
