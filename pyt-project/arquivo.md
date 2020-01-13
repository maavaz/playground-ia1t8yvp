# Arquivos em Python

Até agora, os dados utilizados em nossos programas ou são inseridos diretamente no código ou são digitados pelo usuário a medida que são lidos. 
Mas, no mundo real, armazenamos os dados em estruturas denominada **"arquivo"**.  um arquivo é um conjunto de dados que se relacionam de alguma forma, representando alguma informação ou conjunto de informações das mais diversas naturezas como imagens, áudio, texto, instruções para processadores, etc.
Um arquivo é quase sempre representado por um nome (seguido de um ponto euma extensão) e são armazenados em dispositivos permanentes, isto é, são dispositivos que mantém os dados de maneira permanente.

### Abertura e fechamento dos Arquivos

Para que um arquivo possa ser utilizado (leitura/gravação) é necessário abri-lo (comando open) antes de usá-lo e fechar (comando close) os arquivos quando tiver terminado de utilizá-lo. 
Os formatos gerais para utilizar esses comandos é apresentado abaixo:
Nome de Método	Uso	Explicação
open	open(nome_arquivo,'r')	Abre um arquivo chamado nome_arquivo e o usa para leitura. Retorna uma referëncia para um objeto file.
open	open(nome_arquivo,'w')	Abre um arquivo chamado nome_arquivo e o usa para escrita. Retorna uma referëncia para um objeto file.
close	ref_arquivo.close()	Utilização do arquivo referenciado pela variável ref_arquivo terminou.
