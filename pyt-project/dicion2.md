# Exercitando

?[Qual das alternativas abaixo é verdadeira com relação aos dicionários em python]
-[ ] Os itens do dicionários são inseridos ordenadamente pelo valor da chave 
-[ ] Um dicionário pode ser composto por qualquer tipo de dado exceto outro dicionário
-[ ] Os itens do dicionários são acessados pela posição
-[x] Dicionários são mutáveis

?[Dada a seguinte definição de dicionário: d = {'foo': 100, 'bar': 200, 'baz': 300}, que item representa o acesso ao valor 200 do dicionário]
-[ ] d[3]
-[x] d['bar'] 
-[ ] d[200] 
-[ ] d[bar] 

?[Dada a seguinte definição de dicionário: d = {'foo': 100, 'bar': 200, 'baz': 300}, que comando representa a remoção de todos os itens]
-[ ] del['foo', 'bar', 'baz']
-[x] d.clear() 
-[ ] clear.d() 
-[ ] del d

?[Dada a seguinte definição de dicionário tel = {'iphone 3G': 2008, 'iphone 4S': 2011, 'iphone': 2007}, qual o resultado do comando: tel['iphone 3G','iphone']]
-[ ] [2008,2007]
-[ ] 2008,2007 
-[x] erro! 
-[ ] {2008, 2007} 

---

### Exercício 1
---

Digite uma frase qualquer:Faça um programa para contar e exibir a quantidade e percentual de cada vogal em uma frase digitada pelo usuário na entrada. Utilize a estrutura de dicionário para armazenar os contadores das vogais. Utilize uma das funções **upper()** ou **lower()** para comparação.

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor6.sh" })

::: Solução
``` python
soma = lambda x: sum([ int(x) for x in dic.values() ])
def conta(dic, letra):
    if letra.lower() in dic:
       dic[letra.lower()] += 1
    return dic   
dic = {'a':0, 'e':0, 'i':0, 'o':0, 'u':0}
frase = input('Digite uma frase qualquer:')
for car in frase:
     dic = conta(dic, car)

s = soma(dic)  
print ('vogal      qtd    frequência')
for vog, qtd in dic.items():
    y = int(qtd)/s*100
    print ("  ",vog, ':     ', qtd, '     ', '{0:.2f}'.format(y), '%')

```
:::
