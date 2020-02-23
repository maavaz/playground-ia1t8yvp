### Percorrendo uma String com <b>for</b>

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


