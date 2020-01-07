# Passagem de Parâmetros para as Funções em Python
Além da forma padrão de passar parâmetros/argumentos para as funções, há outras formas que serão apresentadas a seguir:

### Parâmetros com Valor Padrão

Pode-se definir um valor padrão para os argumentos e, na ausência de valor na chamada, a função usuará o padrão.
``` python runnable

def ex_soma_1(a, b=10):  # foi definido o valor 10 como padrão de b. Caso não seja fornecido pelo programa a função usará esse valor
    s = a + b 
    return i + j

soma = ex_soma_1(7)  # usará o valor padrão
print('soma1 = ',soma)

soma = ex_soma_1(7, 3)  # Nesse caso usará o 3 como o valor de b
print('soma2 = ',soma)

 ```

### parâmetros com palavra chave
Pode-se passar argumentos com valores até para os argumentos posicionais bastando explicitar o nome da variável e até em uma ordem diferente daquela originalmente definida.
Exemplo:
``` python runnable
def ex_soma_2(a, b=10, c=0):   # Os parâmetros b e c possuem valores padrão, caso não seja enviados
        s = a + b + c
        return s
 

soma = ex_soma_2(1, c=2)  # O valor 10 do parâmetro b é mantido
print('soma1 =', soma)

soma = ex_soma_2(1, c=2, b=1)
print('soma2 =', soma)

# Quando usamos variáveis com nomes diferentes não podemos usar as facilidades acima
x = 10
y = 100
z = 1000

# soma = ex_soma_2(x, y=2, z=1) Essa chamada de função dará erro

soma = ex_soma_2(x, y, z)  # essa chamada está correta 
print('soma3 =', soma)

# soma = ex_soma_2(b=0, a=2, 10) Essa chamada dará erro também. Veja a explicação a seguir
# print('soma4 =', soma)

```

**OBS:** Você não pode usar argumentos posicionais depois dos argumento com palavra chave “(b=0, c=1, 10)”.

Erro:
```
File "main.py", line 29
    soma = ex_soma_2(b=0, a=2, 10)
                               ^
SyntaxError: positional argument follows keyword argument
```


