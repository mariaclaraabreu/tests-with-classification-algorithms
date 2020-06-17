# Relatório de testes de Algoritmos de classificação na base de dados Pima Indians Diabetes


<h2> 1. Introdução </h2>
Algoritmos de classificação são utilizados para mapear elementos
semelhantes em categorias específicas. Neste trabalho, serão abordados os
seguintes algoritmos: kNN , Random Forest , Naive Bayes , Decision Tree e
Perceptron , cujos testes foram feitos na plataforma Jupyter Notebook e a
classificação individual de cada classificador fora feita baseada na sua acurácia.

# **2. Descrição de experimentos**
# **2.1. Base de dados**
A base de dados escolhida para os experimentos é a Pima Indians Diabetes,
que é composta por informações referentes a mulheres com pelo menos 21 anos
de idade, cuja origem é indígena dos povos Pima. Nela, estão inseridas 768
instâncias (número de linhas) com 9 atributos cada, sendo que o último, informa se a
pessoa possui a doença ou não.
Todos os atributos são preenchidos com valor numérico e correspondem a:
● Número de vezes que a pessoa ficou grávida - preg ;
● Concentração de glicose no plasma em um período de duas horas em
um teste oral de tolerância à glicose - plas ;
● Pressão arterial diastólica (mm Hg) - pres ;
● Espessura da dobra da pele do tríceps (mm) - skin;
● Insulina sérica de 2 horas (mu U / ml) - test;
● Índice de massa corporal - mass;
● Histórico de diabetes na família - pedi;
● Idade - age;
● Situação (0 - não possui a doença; 1 - possui a doença) - class;

# **2.2. Algoritmos de classificação**
Classificação é um método que aprende uma função, em termos
matemáticos, com valores de atributos em seu domínio e valores de classe em sua
imagem. Em outras palavras, dado um conjunto de valores de atributos, tal função
determina um valor de classe para esse conjunto. Essa função é também conhecida
como modelo de classificação (SILVA, 2007).
Essa classificação é feita através de algoritmos de aprendizagem. Esses
algoritmos conseguem “criar conhecimento” sobre o domínio tratado através de
dados de entrada. Quando esses dados de entrada já possuem suas classes
atribuídas dizemos que essa é uma aprendizagem supervisionada. Dessa forma, o
algoritmo consegue criar uma relação entre as características de cada entrada com
a sua classe final, gerando um “conhecimento” para fazer previsões sobre entradas
que ainda não possuem uma classe definida. Esses dados de entrada já
classificados são chamados de base de treino enquanto que os documentos que
serão classificados posteriormente ao treino são denominados como a base de teste
(SANTOS, 2013).
Quando a base de treino não possui uma classificação pré-definida são
utilizados algoritmos de aprendizagem não-supervisionada. Nesse caso, os
algoritmos tentam agrupar entradas com características semelhantes e classificá-los
por grupos. Esse tipo de classificação é chamada de clusterização (SANTOS, 2013).

# **2.2.1. Random Forest**
O algoritmo Random Forest trata-se de um classificador que faz uso do
método de árvores de decisão criada por Breiman (2001) possibilitando a mineração
dos dados. Esta técnica possui uma ideia um pouco diferente
dos algoritmos de árvores de decisão, enquanto uma árvore possui o objetivo de
construção total de uma estrutura a partir de uma base de dados, o Random Forest
tem o objetivo de efetuar a criação de várias árvores de decisão usando um
subconjunto de atributos selecionados aleatoriamente a partir do conjunto original,
contendo todos os atributos e que estes possuem um tipo de amostragem chamado
de bootstrap, a qual é do tipo com reposição, possibilitando assim melhor análise
dos dados. (NETO, 2014).


