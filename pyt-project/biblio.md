# Biblioteca Padrão do Python

A biblioteca padrão do Python é muito extensa, oferecendo um amplo conjunto de módulos e funções úteis que minimizam o uso de código. 
Os módulos (funções) fornecem acesso à funcionalidade do sistema, bem como soluções padronizadas para muitos problemas que ocorrem em programação. 
Alguns desses módulos são explicitamente projetados para incentivar e aprimorar a portabilidade de programas em Python, abstraindo os detalhes das diferentes plataformas.

### <b> Como usar os módulos e sua Funções </b>

Para poder usar as funções é necessário importá-las de uma biblioteca/módulo. A importação de um módulo ou função só precisa ser feita uma única vez durante uma
seção. Comumente a importação é feita no inicio da seção, entretanto ele pode ser feita em qualquer momento.
Existem 2 maneiras de se importar:
+ Direta - Nesse caso, importa-se apenas a função ou funções que se deseja usar. O comando geral para a importação direta é:

![funcao](/imagens/import.png)
       
**módulo** é o nome do módulo contendo as funções (função 1, função 2 ..., função N) que se quer importar. 

####  <b>Exemplo </b>
``` python
In[1]:  from math import sin, pi          #importando apenas as funções sin e pi da biblioteca math

In[2]: sin(90)

Out[2]: 0.8939966636005579

In[3]: pi

Out[3]: 3.141592653589793
```

É possível importar todas as funções e variáveis de uma biblioteca usando o comando: 


![funcao](/imagens/import_asterisco.png)

A lista de funções é substituída pelo asterisco (*) que indica “todos”. 
 
-Exemplo:
``` python
In[1]: from math import *     # Importando todas as funções da biblioteca math

In[2]: cos(90)

Out[2]: -0.4480736161291701

In[3]: sin(60)

Out[3]: 0.70710678118654746 
```
+ Indireta - Nesse caso todo o módulo é importado e as funções e variáveis são acessadas com o nome do módulo seguido de um ponto e do nome da função (**módulo.função**). O comando usado para a importação indireta é:

![funcao](/imagens/import_mod.png)
 
####  <b> Exemplo  </b>
``` python
In[1]: import math          #Importando todas as funções da biblioteca math

In[2]: math.cos(90)         # nome do módulo na frente da função

Out[2]: -0.4480736161291701

In[3]: math.sin(60)

Out[3]: 0.70710678118654746 
```



