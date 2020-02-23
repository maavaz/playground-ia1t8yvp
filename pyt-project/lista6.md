### Percorrendo string com comando <b>for</b>
---
Podemos percorrer todos os elementos (caracteres) de uma string utilizando o comando <b>for</b>, por exemplo:

<b>frase = "Um teste"</b><br>
<b>for letra in frase:</b><br>
<b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print(letra)</b><br>

O Resultado da execução do código acima será a exibição de cada caracter da frase em uma linha.<br>
U</br>
m</br>
 </br>
t</br>
e</br>
s</br>
t</br>
e</br>
Execute o exemplo abaixo (sufixos na lingua inglesa):
``` python runnable
prefixos = "JKLMNOPQ"
sufixo = "ack"

for p in prefixos:
    print(p + sufixo)
```
### Strings são Imutáveis

As strings não podem ser modificadas, isto é, você não pode alterar uma string existente. Por exemplo: </br>
<b>nome = "Wilton"</b><br>
<b>nome[0] = "M"          #isso produz um erro em tempo de execução TypeError </b><br>

O melhor a ser feito é criar uma nova string que é uma variação do original:</br>
<b>nome = "Wilton"</b><br>
<b>novo_nome = "M" + nome[1: ]</b><br>

A string resultante em <b>novo_nome</b> será <b>"Milton"</b>

### Operadores **in** e **not in**
---
São operadores que efetuam testes de verificação, isto é, resultam em um valor **Falso** ou **Verdadeiro**, caso a string do lado esquerdo do operador **está ou não** contida na string do lado direito. Por exemplo:
``` python
#Verifica a existencia da string caco em Macaco
In [8]: "caco" in "Macaco"
Out[8]: True

#Verifica a existencia da string telo em Martelo
In [9]: "telo" not in "Martelo"
Out[9]: False
```
Execute os exemplos a seguir:
``` python runnable
print("Python"[1])
print("Strings are sequences of characters."[5])
print(len("wonderful"))
print("Mystery"[:4])
print("p" in "Papaia")
print("pai" in "Papaia")
print("pera" not in "peralta")
```


