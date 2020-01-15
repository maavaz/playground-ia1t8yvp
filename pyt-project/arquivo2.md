# Arquivos

## Gravando dados em um arquivo

Para se gravar dados em um arquivo é necessário que seja usado o modo **'w'** na função **open()**. A seguir, para que os dados sejam gravados utiliza-se a função **write()** para
escrever no arquivo aberto.  
``` python

>>> f = open('saida.txt', 'w')                # Abrindo arquivo para gravação. O arquivo saida.txt é criado no diretório corrente.
>>> f.write('Isso e um teste de gravação\n')  # Grava a primeira linha do arquivo. \n no final é para quebrar a linha  
28                                            # valor de retorno do write informando a quantidade de caracteres gravados
>>> f.write('gravando a segunda linha\n')
25
>>> f.close()
```
O comando **Open** com o modo **'w'** sempre criará uma arquivo vazio, isto é, se já existir um arquivo com o mesmo nome, o open apagará o conteúdo do arquivo, reiniciando a gravação. Mas, caso haja necessidade de manter os dados já existentes, o modo de abertura 'a' permite acrescentar novos dados ao final do arquivo sem apagar os dados anteriores.
``` python
>>> f = open('saida.txt', 'a')
>>> 
>>> f.write('Incluindo nova linha no arquivo\n') #Inclui essa nova linha ao final do arquivo saída.
32
>>> f.close()
```
Arquivo: saida.txt
Isso e um teste de gravação
gravando a segunda linha
Incluindo nova linha no arquivo

### Abrindo arquivo no modo r+
O modo **'r+'** permite tanto a leitura quanto a escrita em arquivos. A posição inicial ao abrir o arquivo neste modo é 0, de forma que qualquer coisa que. seja escrita sem que se mova a posição substituirá o que está no começo. A função(comando) que possibilita posicionar o cursor do arquivo na próxima possição de gravação é **seek(posição)**.
``` python
>>> f = open("novo_arquivo.txt", "r+")
>>> s ="Testando r+"
>>> f.write(s)
11
>>> i = len(s)
>>> f.seek(i)           # Posicionando o cursor no início da próxima gravação
11
>>> s="Novo teste do r+"
>>> f.write(s)
16
>>> f.close()
```
Arquivo: novo_arquivo.txt<br>
Testando r+Novo teste do r++
