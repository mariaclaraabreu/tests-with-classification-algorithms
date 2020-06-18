# Relatório de testes de Algoritmos de classificação na base de dados Pima Indians Diabetes


<h2> 1. Introdução </h2>
<p>Algoritmos de classificação são utilizados para mapear elementos
semelhantes em categorias específicas. Neste trabalho, serão abordados os
seguintes algoritmos: kNN , Random Forest , Naive Bayes , Decision Tree e
Perceptron , cujos testes foram feitos na plataforma Jupyter Notebook e a
classificação individual de cada classificador fora feita baseada na sua acurácia.</p>

<h2>2. Descrição de experimentos <h2>
  <h2> 2.1. Base de dados </h2>
  
<p>A base de dados escolhida para os experimentos é a Pima Indians Diabetes,
que é composta por informações referentes a mulheres com pelo menos 21 anos
de idade, cuja origem é indígena dos povos Pima. Nela, estão inseridas 768
instâncias (número de linhas) com 9 atributos cada, sendo que o último, informa se a
pessoa possui a doença ou não.
Todos os atributos são preenchidos com valor numérico e correspondem a: </p>
<ul>
  
</ul>
<li>Número de vezes que a pessoa ficou grávida - preg </li>
<li>Concentração de glicose no plasma em um período de duas horas em
um teste oral de tolerância à glicose - plas </li>
<li>Pressão arterial diastólica (mm Hg) - pres </li>
<li>Espessura da dobra da pele do tríceps (mm) - skin</li>
<li>Insulina sérica de 2 horas (mu U / ml) - test</li>
<li>Índice de massa corporal - mass</li>
<li>Histórico de diabetes na família - pedi</li>
<li>Idade - age</li>
<li>Situação (0 - não possui a doença; 1 - possui a doença) - class</li>

  <h2> 2.2. Algoritmos de classificação </h2>
<p>Classificação é um método que aprende uma função, em termos
matemáticos, com valores de atributos em seu domínio e valores de classe em sua
imagem. Em outras palavras, dado um conjunto de valores de atributos, tal função
determina um valor de classe para esse conjunto. Essa função é também conhecida
como modelo de classificação (SILVA, 2007).</p>
<p>Essa classificação é feita através de algoritmos de aprendizagem. Esses
algoritmos conseguem “criar conhecimento” sobre o domínio tratado através de
dados de entrada. Quando esses dados de entrada já possuem suas classes
atribuídas dizemos que essa é uma aprendizagem supervisionada. Dessa forma, o
algoritmo consegue criar uma relação entre as características de cada entrada com
a sua classe final, gerando um “conhecimento” para fazer previsões sobre entradas
que ainda não possuem uma classe definida. Esses dados de entrada já
classificados são chamados de base de treino enquanto que os documentos que
serão classificados posteriormente ao treino são denominados como a base de teste
(SANTOS, 2013).</p>
<p>Quando a base de treino não possui uma classificação pré-definida são
utilizados algoritmos de aprendizagem não-supervisionada. Nesse caso, os
algoritmos tentam agrupar entradas com características semelhantes e classificá-los
por grupos. Esse tipo de classificação é chamada de clusterização (SANTOS, 2013).</p>

<h2> 2.2.1. Random Forest</h2>
O algoritmo Random Forest trata-se de um classificador que faz uso do
método de árvores de decisão criada por Breiman (2001) possibilitando a mineração
dos dados. Esta técnica possui uma ideia um pouco diferente
dos algoritmos de árvores de decisão, enquanto uma árvore possui o objetivo de
construção total de uma estrutura a partir de uma base de dados, o Random Forest
tem o objetivo de efetuar a criação de várias árvores de decisão usando um
subconjunto de atributos selecionados aleatoriamente a partir do conjunto original,
contendo todos os atributos e que estes possuem um tipo de amostragem chamado
de bootstrap, a qual é do tipo com reposição, possibilitando assim melhor análise
dos dados. (NETO, 2014). </br>

<b>Figura 1 -</b> Uso do algoritmo Random Forest</br>

![01](https://user-images.githubusercontent.com/44175992/84957612-f5feee80-b0d1-11ea-9387-df19c3e724ce.jpg)
</br>

<h2>2.2.2.kNN </h2>
<p>O algoritmo k-Nearest Neighbor (kNN) é um algoritmo de aprendizado supervisionado do tipo lazy. A ideia geral desse algoritmo consiste em encontrar os  k exemplos rotulados mais próximos do exemplo não classificado e, com base no rótulo desses exemplos mais próximos, é tomada a decisão relativa à classe do exemplo não rotulado. Os algoritmos da família kNN requerem pouco esforço durante a etapa de treinamento. Em contrapartida, o custo computacional para rotular um novo exemplo é relativamente alto, pois, no pior dos casos, esse exemplo será comparado com todos os exemplos contidos no conjunto de treinamento (FERRERO, 2009). </p></br>

<b>Figura 2 -</b> Uso do algoritmo kNN</br>

![02](https://user-images.githubusercontent.com/44175992/84959227-50e61500-b0d5-11ea-8340-a177c8482cfd.jpg)

</br>

<h2>2.2.3. Decision Tree</h2>
<p> O algoritmo Decision Tree ou Árvore de Decisão é uma representação simples de um classificador utilizada por diversos sistemas de aprendizado de máquina. Uma árvore de decisão é induzida a partir de um conjunto de exemplos de treinamento onde as classes são previamente conhecidas.</p>
<p>A estrutura da árvore é organizada de tal forma que:</p>
a)	cada nó interno (não-folha) é rotulado com o nome de um dos atributos previsores;</b>
b)	os ramos (ou arestas) saindo de um nó interno são rotulados com valores do atributo naquele nó;</bt>
c)	cada folha é rotulada com uma classe, a qual é a classe prevista para exemplos que pertençam àquele nó folha. </br>

<p>O processo de classificação de um exemplo ocorre fazendo aquele exemplo “caminhar” pela árvore, a partir do nó raiz, procurando percorrer os arcos que unem os nós, de acordo com as condições que estes mesmos arcos representam. Ao atingir um nó folha, a classe que rotula aquele nó folha é atribuída àquele exemplo (CARVALHO, 2005).</p>

<b>Figura 3 -</b> Uso do algoritmo Decision Tree</br></br>

![03](https://user-images.githubusercontent.com/44175992/84959336-7ffc8680-b0d5-11ea-8ffd-58253bc1d2d1.jpg)



<h2>2.2.4. Naive Bayes</h2>
<p>O algoritmo Naive Bayes é um classificador probabilístico simples que calcula um conjunto de probabilidades contando a frequência e as combinações de valores em um determinado conjunto de dados. O algoritmo usa o teorema de Bayes e assume que todos os atributos são independentes, dado o valor da variável de classe. Essa suposição de independência condicional raramente é verdadeira em aplicações do mundo real, daí a caracterização como ingênua, mas o algoritmo tende a ter um bom desempenho e aprender rapidamente em vários problemas de classificação supervisionada. Essa "ingenuidade" permite que o algoritmo construa facilmente classificações a partir de grandes conjuntos de dados sem recorrer a esquemas de estimativa de parâmetros iterativos complicados (DIMITOGLOU; ADAMS & JIM, 2012).</p>

<b>Figura 4 -</b> Uso do algoritmo Naive Bayes</br></br>

![04](https://user-images.githubusercontent.com/44175992/84959347-83900d80-b0d5-11ea-9158-3c6f7484dd95.jpg)
</br>


<h2>2.2.5.Perceptron</h2>
<p>O Perceptron consiste em uma única camada de neurônios com pesos sinápticos e bias ajustáveis. Se os padrões de entrada forem linearmente separáveis, o algoritmo de treinamento do Perceptron possui convergência garantida, ou seja, é capaz de encontrar um conjunto de pesos que classifica corretamente os dados. Os pesos dos neurônios que compõem o Perceptron serão tais que as superfícies de decisão produzidas pela rede neural estarão apropriadamente posicionadas no espaço (CASTRO F. & CASTRO M., 2001).</p>


<b>Figura 5 -</b> Uso do algoritmo Perceptron</br></br>

![05](https://user-images.githubusercontent.com/44175992/84959357-88ed5800-b0d5-11ea-936a-6fea2a2ded27.jpg)


<h2>3. Resultados</h2>
<p>Como resultado obtido, observa-se que o algoritmo knn obteve a maior acurácia, seguido pelo Random Forest.</p>

<b>Quadro  1-</b> Acurácia de cada algoritmo</br></br>

<table>
  <tr>
    <td>Algoritmo</td>
    <td>Acurácia</td>
  </tr>
  <tr>
    <td>Naive Bayes</td>
    <td>0.65748031496063</td>
  </tr>
    <tr>
    <td>kNN	</td>
    <td>0.7401574803149606</td>
  </tr>
  </tr>
    <tr>
    <td>Decision Tree	</td>
    <td>0.6811023622047244</td>
  </tr>
  <tr>
    <td>Perceptron	</td>
    <td>0.6535433070866141</td>
  </tr>
  <tr>
    <td>Random Forest	</td>
    <td>0.7362204724409449</td>
  </tr>
  
</table>

</br>

<h2>Referências</h2>
<p>SILVA, J. <b>Algoritmos de classificação baseados em análise formal de
  conceitos.</b> Master's thesis, Universidade Federal de Minas Gerais, 2007.</p>
<p>SANTOS, F. L.<b> Mineração de opinião em textos opinativos utilizando
  algoritmos de classificação </b>. 2013.</p>
<p>CASTRO, F. C. C.; CASTRO, M. C. F. Redes neurais artificiais .
DCA/FEEC/Unicamp, 2001.</p>
<p>FERRERO, C. A. <b>Algoritmo kNN para previsão de dados temporais: funções de
previsão e critérios de seleção de vizinhos próximos aplicados a variáveis
  ambientais em limnologia</b> . 2009. Tese de Doutorado. Universidade de São Paulo.
<p>CARVALHO, D. R. <b>Árvore de decisão/algoritmo genético para tratar o problema
  de pequenos disjuntos em classificação de dados </b>. Universidade Federal do Rio
de Janeiro, Rio de Janeiro, Brazil. Doctor Thesis. 162pp, 2005.</p>
<p>DIMITOGLOU, G.; ADAMS, J. A.; JIM, C. M. <b>Comparison of the C4. 5 and a Naïve
  Bayes classifier for the prediction of lung cancer survivability </b>. arXiv preprint
arXiv:1206.1121, 2012.</p>
<p>NETO, C. D. G. <b>Potencial de técnicas de mineração de dados para o
  mapeamento de áreas cafeeiras </b>. INPE, São José dos Campos, 2014.</p>













