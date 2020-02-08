# Arquivos

### <b> Gravando dados em um arquivo </b>

Para se gravar dados em um arquivo é necessário que seja usado o modo **'w'** na função **open()**. A seguir, para que os dados sejam gravados, utiliza-se a função **write()** para escrever no arquivo aberto. O comando **write()** retorna sempre a quantidade de dados gravados no arquivo. Isso é útil quando for necessário controlar a gravação dos dados, explicado mais a frente.   
``` python

>>> f = open('saida.txt', 'w')                # Abrindo arquivo para gravação. O arquivo saida.txt é criado no diretório corrente.
>>> f.write('Isso e um teste de gravação\n')  # Grava a primeira linha do arquivo. \n no final é para quebrar a linha  
28                                            # valor de retorno do write informando a quantidade de caracteres gravados
>>> f.write('gravando a segunda linha\n')
25
>>> f.close()
```
O comando **Open** com o modo **'w'** sempre criará um arquivo vazio, isto é, se já existir o arquivo com o mesmo nome, o comando **open** irá apagar o conteúdo do arquivo (dados), reiniciando a gravação. Mas, caso haja necessidade de manter os dados já existentes, o modo de abertura **'a'** irá permitir acrescentar novos dados ao final do arquivo existente, sem apagar os dados anteriores.
``` python
>>> f = open('saida.txt', 'a')
>>> 
>>> f.write('Incluindo nova linha no arquivo\n') #Inclui essa nova linha ao final do arquivo saída.
32
>>> f.close()
```
Arquivo: **saida.txt** <br>
Isso e um teste de gravação<br>
gravando a segunda linha<br>
Incluindo nova linha no arquivo<br>

### <b> Abrindo arquivo no modo r+ </b>
O modo **'r+'** permite tanto a leitura quanto a escrita em arquivos. O controle de gravação dos dados no arquivo é do programador. A posição de início de gravação dos dados ao abrir o arquivo neste modo é 0 (zero), portanto, se houver necessidade de gravar dados, o programador deverá considerar a quantidade de dados gravados, para posicionar o cursor na nova posição de gravação. Se não houver essa preocupação na movimentação da posição gravação, o programa irá sempre realizar a gravação do início (posição 0), sobrepondo o que foi gravado anteriormente. A função(comando) que possibilita posicionar o cursor do arquivo na próxima possição de gravação é **seek(posição)**.
``` python
>>> f = open("novo_arquivo.txt", "r+")
>>> s ="Testando r+"
>>> f.write(s)
11
>>> i = len(s)
>>> f.seek(i)           # Posicionando o cursor no início da próxima gravação (11). 
11                      #Se não houver esse reposicionamento o programa irá sobrepor os dados escritos antes. 
>>> s="Novo teste do r+"
>>> f.write(s)
16
>>> f.close()
```
Arquivo: **novo_arquivo.txt**<br>
Testando r+Novo teste do r+
