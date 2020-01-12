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
Faça um programa para calcular o valor pago nos pedidos de uma lanchonete. Para isso, o programa deve receber do usuário, os códigos 
dos sanduiches e as  respectivas quantidades. Calcule e mostre o nome do sanduiche valor unitario, quantidade e o valor a ser pago pelo item  e o total geral do pedido.
O programa termina quando o código do sanduiche for igual a 0 (zero).
A seguir é apresentado o Menu da lanchonete:
<br>
Codigo&nbsp;&nbsp;&nbsp;Sanduíche&nbsp;&nbsp;&nbsp;&nbsp;Preço <br>
100&nbsp;&nbsp;&nbsp;&nbsp;Hamburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 12,00<br>
200&nbsp;&nbsp;&nbsp;&nbsp;cheeseburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 15,00<br>
300&nbsp;&nbsp;&nbsp;&nbsp;Duplo cheeseburger&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 20,00<br>
400&nbsp;&nbsp;&nbsp;&nbsp;cheeseFrango&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 18,00<br>
500&nbsp;&nbsp;&nbsp;&nbsp;Hot Linguiça&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R$ 19,00<br>


---
#### Exercício 2
---
A ACME Inc., uma empresa de 500 funcionários, está tendo problemas de espaço em disco no seu servidor de arquivos. Para tentar resolver este problema, o Administrador de Rede precisa saber qual o espaço ocupado pelos usuários, e identificar os usuários com maior espaço ocupado. Através de um programa, baixado da Internet, ele conseguiu gerar o seguinte arquivo, chamado "usuarios.txt":
alexandre       456123789
anderson        1245698456
antonio         123456456
carlos          91257581
cesar           987458
rosemary        789456125
Neste arquivo, o nome do usuário possui 15 caracteres. A partir deste arquivo, você deve criar um programa que gere um relatório, chamado "relatório.txt", no seguinte formato:
ACME Inc.               Uso do espaço em disco pelos usuários
------------------------------------------------------------------------
Nr.  Usuário        Espaço utilizado     % do uso

1    alexandre       434,99 MB             16,85%
2    anderson       1187,99 MB             46,02%
3    antonio         117,73 MB              4,56%
4    carlos           87,03 MB              3,37%
5    cesar             0,94 MB              0,04%
6    rosemary        752,88 MB             29,16%

Espaço total ocupado: 2581,57 MB
Espaço médio ocupado: 430,26 MB
O arquivo de entrada deve ser lido uma única vez, e os dados armazenados em memória, caso sejam necessários, de forma a agilizar a execução do programa. A conversão do espaço ocupado em disco, de bytes para megabytes deverá ser feita através de uma função separada, que será chamada pelo programa principal. O cálculo do percentual de uso também deverá ser feito através de uma função, que será chamada pelo programa principal.
