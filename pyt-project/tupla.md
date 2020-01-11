# Tuplas

Do ponto de vista técnico, as listas funcionam bem para armazenar conjuntos de itens que podem sofrer alterações durante a vida de um programa, isto é, são mutáveis.Por outro lado, há situações que não gostaríamos que os valores de uma determinada lista fossem alterados. O python possui uma lista onde os valores armazenados são imutáveis, denominada de **Tuplas**.

## Definindo uma tupla

As tuplas se parecem exatamente com as listas, exceto por usarem parênteses no lugar de colchetes. Após a definição da tupla, pode-se acessar os elementos individualmente usando um índice, como é feito com as listas.
Por exemplo, se tivermos um retângulo que sempre deva ter determinado
tamanho, podemos garantir que seu tamanho não mudará colocando as
dimensões em uma tupla:
Do ponto de vista conceitual você deveria usar tuplas para montar estruturas de dados heterogêneos enquanto a lista deveria ser usada para dados homogêneos, ou seja, todos seus elementos deveriam ser do mesmo tipo.
Como Python é uma linguagem dinâmica isto não pode ser garantido, cabe ao programador decidir fazer isto.
Por ser usado para dados heterogêneos (diversidade de tipos entre os membros) a tupla normalmente possui poucos elementos mas nada impede que tenha muitos. Tuplas frequentemente são usadas para simular classes que não precisam ser definidas, cujo uso é mais efêmero e não depende de contratos mais específicos.
Mas mesmo que você tenha uma lista de elementos que normalmente será pequena, se ela se parece mais como uma lista e não um conjunto limitado e fixo de dados, a lista deve ser usada.
Se os dados são do mesmo tipo, é quase certo que você tem uma lista, claro que existem exceções. Por exemplo um Point poderia ser uma tupla cujos elementos são dois inteiros. É óbvio que isto não é uma lista de dados, mas um conjunto limitado de dados que por acaso são do mesmo tipo.
A tupla funciona como um registro de dados, como uma linha de um banco de dados, um conjunto de colunas. A lista funciona como a tabela, são as linhas como um todo.
Eu imagino, mas nunca testei, que tuplas são ligeiramente mais rápidas, mas elas não devem ser usadas por causa disto, use de acordo com a semântica adequada.


