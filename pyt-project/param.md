# Passagem de Parâmetros para as Funções em Python
Além da forma padrão de passar parâmetros/argumentos para as funções, há outras formas que serão apresentadas a seguir:

### parâmetros com palavra chave
Pode-se passar argumentos com valores até para os argumentos posicionais bastando explicitar o nome da variável e até em uma ordem diferente daquela originalmente definida.
Exemplo:
``` python runnable
def ex_soma_2(a, b=10, c=0):   # Os parâmetros b e c possuem valores padrão, caso não seja enviados
        s = a + b + c
        return s
 

soma = ex_soma_2(1, c=2)
print('soma =', soma)


soma = ex_soma_2(1, c=2, b=1)
print('soma =', soma)
```

>>> argumentos_padrao_2(k=1, i=2, j=3)
6
E lembrando que há uma limitação aqui. Você não pode usar argumentos posicionais depois dos argumento com palavra chave “(j=0, k=1, 10)” e muito menos repetir um mesmo valor já definido nos argumentos posicionais “(10, i=10)”.
