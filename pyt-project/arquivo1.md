# Arquivos

## Lendo dados em Python

Para ler um arquivo em Python, precisamos abrir o arquivo no modo de leitura.

Existem vários métodos disponíveis para esse fim. Podemos usar o método **read (size)** para ler do arquivo a quantidade de caracteres. 
Se o parâmetro **size** não for especificado, o comando **read** fará uma única leitura do início ao final do arquivo.
O exemplo a seguir irá utilizar o arquivo teste.txt com o conteúdo exibido abaixo:<br>

**teste.txt**<br>
Primeira linha de dados<br>
Segunda linha de dados<br>
Terceira linha de dados<br>

``` python
>>> f = open('teste.txt', 'r')    # Abre o arqvui teste.txt
>>> 
>>> f.read(5)                     # Lê os 5 primeiros caracteres da primeira linha
'Prime'
>>> f.read()                      # Lê  o restante do arquivo a partir do 6º caracter da primeira linha até o final do arquivo
'ira linha de dados\nSegunda linha de dados\nTerceira linha de dados'
>>> f.close()
>>> 
```` 
