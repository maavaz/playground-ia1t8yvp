# Exercitando

?[Dado o caminho c:\veterinaria\ e o arquivo gatos.txt, assinale a opção contendo o comando correto para abertura do arquivo no modo leitura e gravação]
-[ ] open('veterinaria.txt', 'rw')
-[x] open('c:\veterinaria\gatos.txt', 'r+')
-[ ] open('c:gatos.txt\veterinaria', 'r+')
-[ ] open(c:gatos.txt\veterinaria, 'rw')

?[Ao ler um arquivo usando o objeto file(f), qual o melhor método para ler o arquivo inteiro em uma única string?]
-[ ] f.readline()
-[ ] f.read_file_to_str()
-[x] f.read()
-[ ] f.readlines()

?[Qual dos seguintes comandos pode ser usado para ler a próxima linha em um arquivo usando o objeto file f ?]
-[ ] f.read (n)
-[ ] f.read ()
-[x] f.readline ()
-[ ] f.readlines ()
---
### <b> Exercício 1 (Desafio) </b>


**ATENÇÃO:** Para execução do exercício é necessário que você abra uma nova aba (nomeie como **alunos.tx**) no **Editor Trinket** abaixo, copie e cole os dados apresentados, a seguir. Após feito isso, retorne a aba **main.py** e desenvolva a solução do problema descrito abaixo. 
Para abrir uma nova aba no **trinket** aperte o símbolo de **"+"** no canto superior direito do editor.
``` txt
Amanda,4.00
Ana,7.00
Bernardo,9.00
Clarisse,5.50
Cristina,3.90
Danilo,8.40
Emilia,10.0
Fernando,7.00
Gilda,6.50
Hugo,2.0
Ilan,2.6
Janio,4.9
Larissa,7.6
Maria,8.4
Neto,6.5
Otavio,4.7
Patricia,6.7
Roberto,7.8
Sergio,3.8
Tatiana,5.9
Ulisses,1.2
Valeria,9.6
Zenon,4.3
```
Faça um programa que leia os dados armazenados no arquivo: **alunos.txt**. Crie um dicionário (nome:nota) com as informações lidas. A seguir, calcule e exiba a média geral da turma; maior nota da turma, com respectivo nome do aluno; menor nota com respectivo nome do aluno e, por fim, imprima o nome e a nota dos alunos que tiveram a nota maior que a média da turma. <br>  

**Dica1:** crie duas listas e armazene as informações de nomes e notas, uma em cada lista e, a partir daí, crie o dicionário usando a função **zip**. Utilize a função **split** com **delimiter = ','** para quebrar as linhas do arquivos em nome e nota.
 

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor7.sh" })

::: Solução
``` python
soma = lambda x:sum([float(z) for z in x.values() ])

maior = lambda x:max([(float(z[1]),z[0]) for z in x.items() ])

menor = lambda x:min([(float(z[1]),z[0]) for z in x.items() ])

compara = lambda al, md:[(x[0],x[1]) for x in al.items() if float(x[1]) > md]

f = open('alunos.txt','r')

delimiter = ','
x = {}
nomes=[]
notas=[]

for linha in f:
  nomes.append((linha.replace("\n","")).split(delimiter)[0])
  notas.append((linha.replace("\n","")).split(delimiter)[1])

alunos = dict(zip(nomes,notas))
print(alunos)
s = soma(alunos)
mediageral = s / len(alunos)
mx = maior(alunos)
mn = menor(alunos)
acima = compara(alunos,mediageral)
print('Média Turma: {0:.2f}'.format(mediageral))
print('Maior Média: {0:.2f}  Aluno: {1}'.format(mx[0],mx[1]))
print('Menor Média: {0:.2f}  Aluno: {1}'.format(mn[0],mn[1]))
print('Alunos com as médias acima Media da Turma')
print('   Aluno                Média')
for i in acima:
    print('  ',i[0], ' '*(20-len(i[0])), i[1])
```
:::

