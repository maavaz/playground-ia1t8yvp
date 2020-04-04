# Função Lambda

O python provê um tipo diferente de função denominado de **função Lambda**. Num primeiro momento, funções locais (**def**) e **expressões lambda** são muito semelhantes. Em muitos casos, a escolha entre usar expressões lambda e funções locais é uma questão de estilo e preferência pessoal.

Todas as características de uma função lambda são muito parecidas com as funções locais, com exceção de duas coisas: elas não possuem uma definição em código, ou seja, são declaradas como variáveis e não possuem um **def** próprio; e elas são funções de uma linha, que funcionam como se houvesse a instrução **return** antes do comando.

Veja o exemplo a seguir:

``` python runnable
def ex_soma (a, b):
   s = a + b
   return s
   
soma_lambda = lambda numero1, numero2: numero1 + numero2  # Função soma escrita como Função Lambda

soma = ex_soma(10, 20)         # Chamada da função ex_soma

print('Soma = ', soma)

soma = soma_lambda(10,20)     # Chamada da função lambda soma_lambda

print ('Soma Lambda = ', soma)
```
A forma geral para criação da Função Lambda é:
![funcao](/imagens/lambda.png)

As **variáveis** que aparecem na definição da função são os parâmetros e **fórmula** é a expressão da função.

 <b> Exemplo:  </b>
```
In [1]: cubo = lambda numero: numero * numero * numero
In [2]: cubo(3)

Out[2]: 27

In [3]: cubo(5)

Out[3]: 125
```
## <b>Expressões lambda com Map(), Reduce() e Filter()</b>
A função lamda pode ser utilizada em conjunto com outras funções como map, reduce e filter. 

### <b>Função Map()</b>
A **função map()** tem como objetivo aplicar uma função a todos os elementos de uma lista gerando uma nova lista como resultado.
O formato geral é:
![funcao](/imagens/map.png)
``` python runnable
lista = [1, 2, 3, 4, 5, 6]
lista1 = [map(lambda x: X**2, lista)] #eleva ao quadrado os elementos de lista para criar lista1
print("lista = ", lista)
print("\n\nlista1 = ", lista1)
```


