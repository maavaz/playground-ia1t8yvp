# Arquivos

## Lendo dados em Python

Para ler um arquivo em Python, precisamos abrir o arquivo no modo de leitura. Existem vários métodos disponíveis para esse fim. Podemos usar o método **read (size)** para ler do arquivo a quantidade de caracteres. 
Se o parâmetro **size** não for especificado, o comando **read()** fará uma única leitura do início ao final do arquivo.
O exemplo a seguir irá utilizar o arquivo teste.txt com o conteúdo exibido abaixo:<br>

**teste.txt**<br>
Primeira linha de dados<br>
Segunda linha de dados<br>
Terceira linha de dados<br>

``` python
>>> f = open('teste.txt', 'r')    # Abre o arquivo teste.txt
>>> 
>>> f.read(5)                     # Lê os 5 primeiros caracteres da primeira linha
'Prime'
>>> f.read()                      # Lê  o restante do arquivo a partir do 6º caracter da primeira linha até o final do arquivo
'ira linha de dados\nSegunda linha de dados\nTerceira linha de dados'
>>> f.close()
>>> 
```` 
O arquivo pode ser lido linha a linha através da estrutura **for** ou do comando **ref_arquivo.readline()**.
``` python
>>> f = open('teste.txt', 'r')
>>> 
>>> for linha in f: 
...   print(linha, end=' ')  # end=' ' associado ao print exibe o espaço ao final da linha em vez \n(quebra de linha)
...   
Primeira linha de dados
Segunda linha de dados
Terceira linha de dados  
>>> f.close()

>>> f = open('teste.txt', 'r')
>>> f.readline()                   # Leitura da primeira linha
'Primeira linha de dados\n'
>>> f.readline()                   # Leitura da segunda linha 
'Segunda linha de dados\n'
>>> f.readline()
'Terceira linha de dados'          # Leitura da terceira linha
>>> f.close()
```
Por fim, há ainda o comando **readlines()** que returna uma lista das linhas do arquivo. todos os métodos de leitura apresentados aqui irão retornar um valor "vazio" quando chegam ao final do arquivo (End Of File - **EOF**).
``` phyton
>>> f = open('teste.txt', 'r')
>>> 
>>> f.readlines()
['Primeira linha de dados\n', 'Segunda linha de dados\n', 'Terceira linha de dados']  # Lista com as linhas do arquivo
>>> f.close()
```
