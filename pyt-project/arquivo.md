# Arquivos em Python

Até agora, os dados utilizados em nossos programas ou são inseridos diretamente no código ou são digitados pelo usuário a medida que são lidos. 
Mas, no mundo real, armazenamos os dados em estruturas denominada **"arquivo"**.  um arquivo é um conjunto de dados que se relacionam de alguma forma, representando alguma informação ou conjunto de informações das mais diversas naturezas como imagens, áudio, texto, instruções para processadores, etc.
Um arquivo é quase sempre representado por um nome (seguido de um ponto euma extensão) e são armazenados em dispositivos permanentes, isto é, são dispositivos que mantém os dados de maneira permanente.

### Por que usar arquivos?

+ Permitem armazenar grande quantidade de informação;
+ Dados não são perdidos (persistência dos dados);
+ Acesso aos dados poder ser não seqüencial;
+ Acesso concorrente aos dados (mais de um programa pode usar os dados ao mesmo tempo).

Em geral, as operações com arquivos seguem uma ordem, a saber:<br>
&nbsp;&nbsp;&nbsp;**1 - Abrir** o(s) arquivo(s) <br>
&nbsp;&nbsp;&nbsp;**2 -** Efetuar operações de **Leitura e Gravação** dos dados <br>
&nbsp;&nbsp;&nbsp;**3 - fechar** o(s) arquivo(s) <br>

### Abertura e fechamento dos Arquivos

Para que um arquivo possa ser utilizado (leitura/gravação) é necessário abri-lo (comando open) antes de usá-lo e fechar (comando close) os arquivos quando tiver terminado de utilizá-lo. 
Os formatos gerais para utilizar esses comandos é apresentado abaixo:<br>
**Nome**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Uso**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Explicação**<br>
**open**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**open(nome_arquivo,'r')**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Abre um arquivo chamado nome_arquivo e o usa para leitura.<br>
**open**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**open(nome_arquivo,'w')**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Abre um arquivo chamado nome_arquivo e o usa para escrita.<br>
**close**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**ref_arquivo.close()**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Utilização do arquivo referenciado pela variável ref_arquivo terminou.<br>
**OBS:** **Ref_arquivo** refere-se a variável associada ao comando Open.

 Os arquivos são localizados no disco e através do seu caminho (path) e, por isso, o parâmetro nome do arquivo deve estar associado ao caminho para achá-lo no disco. Pode-se trabalhar com caminhos absolutos ou relativos:
+ **Caminho absoluto:** descrição de um caminho desde o diretório raiz. <br>
                **C:\MinhaPasta\arquivo.txt** <br>
+ **Caminho relativo:** descrição de um caminho desde o diretório corrente (onde o programa está salvo) <br>
                   **arquivo.txt ou ..\dados.txt**<br>
                   
### Modo de Abertura
O modo de abertura de arquivos em python define a operação que será realizada no arquivo, por exemplo, se queremos ler dados colocamos no comado open a letra **'r'**, se queremos gravar dados colocamos a letra **'w'**, mas se queremos gravar dados em arquivos já existentes colocamos a letra **'a' (append)** no comando. Por padrão, a gravação e leitura dos dados é efetuada no modo texto, mas se quisermos abrir o arquivo para leitura ou gravação de dados binários devemos especificar usando a letra **b**. O modo binário retorna bytes e esse é o modo a ser usado ao lidar com arquivos não-texto, como arquivos de imagem ou exe.

``` python
f = open("c:\temp\teste.txt")      # equivalente a 'r' ou 'rt' (abertura de arquivo texto)
f = open("c:\temp\teste.txt",'w')  # gravação no modo texto
f = open("img.bmp",'r+b') # leitura e gravação no modo binário
# As operações de leitura e gravação devem levar em conta a variável f (ref_arquivo)

f.close() # fechamento do arquivo
```
