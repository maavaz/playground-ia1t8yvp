# Tuplas

Do ponto de vista técnico, as listas funcionam bem para armazenar conjuntos de itens que podem sofrer alterações durante a vida de um programa, isto é, são mutáveis. A capacidade de modificar listas é
particularmente importante quando trabalhamos com uma lista de
usuários em um site ou com uma lista de personagens em um jogo. No
entanto, às vezes, você vai querer criar uma lista de itens que não poderá
mudar. As tuplas permitir fazer exatamente isso. Python refere-se a valores
que não podem mudar como imutáveis, e uma lista imutável é chamada de
tupla.
Do ponto de vista técnico em Python uma tupla é imutável e uma lista é mutável.
Do ponto de vista conceitual você deveria usar tuplas para montar estruturas de dados heterogêneos enquanto a lista deveria ser usada para dados homogêneos, ou seja, todos seus elementos deveriam ser do mesmo tipo.
Como Python é uma linguagem dinâmica isto não pode ser garantido, cabe ao programador decidir fazer isto.
Por ser usado para dados heterogêneos (diversidade de tipos entre os membros) a tupla normalmente possui poucos elementos mas nada impede que tenha muitos. Tuplas frequentemente são usadas para simular classes que não precisam ser definidas, cujo uso é mais efêmero e não depende de contratos mais específicos.
Mas mesmo que você tenha uma lista de elementos que normalmente será pequena, se ela se parece mais como uma lista e não um conjunto limitado e fixo de dados, a lista deve ser usada.
Se os dados são do mesmo tipo, é quase certo que você tem uma lista, claro que existem exceções. Por exemplo um Point poderia ser uma tupla cujos elementos são dois inteiros. É óbvio que isto não é uma lista de dados, mas um conjunto limitado de dados que por acaso são do mesmo tipo.
A tupla funciona como um registro de dados, como uma linha de um banco de dados, um conjunto de colunas. A lista funciona como a tabela, são as linhas como um todo.
Eu imagino, mas nunca testei, que tuplas são ligeiramente mais rápidas, mas elas não devem ser usadas por causa disto, use de acordo com a semântica adequada.


