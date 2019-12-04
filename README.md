# ANN - Artificial Neural Network (Perceptron) #

## I.	 INTRODUÇÃO ##
Esse projeto tem como objetivo exemplificar a aplicação do algorítimo de Redes Neurais Arificiais (RNA), também chamado 
de ANN (Artificial Neural Network) utilizado para aprendizado de máquina.<br>
O modelo de neuronio proposto por esse projeto é o Perceptron com apenas uma camada e a função de ativação é a degrau.

## II.	FUNDAMENTAÇÃO TEÓRICA ##

### A.	REDES NEURAIS ARTIFICIAIS ###
Tambem conhecido como Artificial Neural Network (ANN) ou modelos conexionistas, o RNA foi proposto em 1943 por McCulloch e Pitts.<br>
A idéia central das redes neurais veio da inspiração do funcionamento dos neuronios biológicos na qual os pesquisadores
acreditavam que modelos computacionais baseados na Máquina de Turing tinham limitações que os modelos computacionais baseados
no comportamento cerebral não tinham, tais como a capacidade de processamento de informação paralela e massiva.<br>
A primeira implementação do algoritimo foi feita desenvolvendo uma máquina, que ficou conhecida como Mark I Perceptron.
Projetada para reconhecimento de imagem na qual utilizava-se de fotocélulas conectadas aos 'neuronios' que tinham seus 
pesos atribuidos a partir do potenciometros controlados por motores. [1] [2]<br>

![Alt text](images/ann-mark.png?)

Os problemas solucionados pelo Perseptron são de natureza simples e devem ser separáveis linearmente, ou seja, dado o conjunto
de dados analisados pelas classes, para que exista uma solução utilizando Perseptron deve existir uma reta capaz de separar
os conjuntos analisados.<br>
Segundo [1] devemos utilizar RNAs quando: a entrada dos seus dados for vetorial, multidimensional, com valores discretos 
ou reais; e a saída for vetorial, multidimensional, valores discretos ou reais.
Pensando em como um neurônio biológico funciona, temos a frase a seguir retirada de [2] que expressa o funcionamento de
maneira direta. Um neurônio recebe um impulso através dos dendritos, processa o sinal e dispara um segundo impulso, que
produz uma substância neurotransmissora que flui do corpo celular para o axônio, e então para outro neurônio.
Analisando a frase de maneira computacional temos que:

![Alt text](images/ann-image-01.png?)

* Dado um conjunto de entradas {x0, ... , xn} ponderados por {w0, ... , wn} conectados a uma função de agregadora temos uma
saída expressa pela função de ativação do neuronio.

O aprendizado da rede dar-se por saber quais são os pesos corretos atribuidos ao conjunto de dados que tem o menor erro
possível.
O algoritimo de treinamento simplificado é:
* Iniciar os pesos 'w' com valores entre 0 e 1;
* Especificar a taxa de aprendizagem 'η'
* Iniciar o contador de número de épocas (época = 0)
* Apresentar as amostras dentro das épocas
* Atualizar os pesos da rede para minimizar o erro utilizando a seguinte função:

![Alt text](images/ann-func-01.png?)

## III.	METODOLOGIA ##
Para o projeto vigente foi utilizado python juntamente com o Notebook Jupyter para prototipar o modelo do
algorítimo.<br>
Tendo como base a fundamentação teórica abordada em II, o modelo do algorítimo esta proposto em <b>"./perceptron.py"</b>.
Para o teste e análise do algorítimo foram propostos alguns exemplos, tais como:<br>
* Composição da porta AND;
* Composição da porta OU;
* Composição da porta XOR;
* Iris Dataset, apenas para diferenciar a classe "setosa" da "versicolor"

## IV. RESULTADOS ##
Os detalhes das implementações dos problemas propostos na metodologia pode ser analisados em <b>"./ANN-Perceptron.ipynb"</b> 
ou <b>"ANN-Perceptron.html"</b>.<br>

Para a primeira proposta (Porta AND) temos:

![Alt text](images/ann-p-example01.png?)

Para a segunda proposta (Porta OR) temos:

![Alt text](images/ann-p-example02.png?)

Para a terceira proposta (Porta XOR) temos:

![Alt text](images/ann-p-example03.png?)

Para a quarta proposta, diferenciar a classe "setosa" da "versicolor" foi desenhada a seguinte rede:

![Alt text](images/ann-p-iris_rede.png?)

Tal rede segue a seguinte tabela da verdade:

![Alt text](images/ann-p-iris_tabela.png?)

Parte do resultado pode ser vista a seguir (ou em "ANN-Perceptron.html" em mais detalhes):

![Alt text](images/ann-p-example04.png?)

## V. CONCLUSÃO ##
Dado os resultados vistos em IV podemos inferir que o Perseptron é funcional para dados linearmente divisíveis (asssim
como abordados em II), porém para aplicações com dados não linearmente divisiveis, tais como a terceira proposta utilizando
a tabela da verdade da porta XOR, não foi obtido resultado satisfatório.<br>
Um dos objetivos do projeto em curso é a implementação do algorítimo do Perseptron. Se analisarmos os dados chegamos a
conclusão de que o algorítimo foi implementado corretamente.

## VI. AGRADECIMENTOS ##

Agradecimentos especiais a CAPES e ao Centro Universitário FEI por financiar o mestrado que está em curso; 
ao professor Reinaldo Bianchi por proporcionar visões sobre o mundo acadêmico e orientar trabalhos científicos 
com o objetivo de lapidar os conhecimentos abordados em sala; aos meus pais e a minha família que sempre me 
apoiaram em meio a dificuldades.

## VII. REFERÊNCIAS ##

[1]	R. Bianchi, Tópicos Especiais em Aprendizagem, 2019, ppt slide Centro Universitário FEI.<br>
[2] Vinicius, PERCEPTRON – REDES NEURAIS, 06/2017, link: https://www.monolitonimbus.com.br/perceptron-redes-neurais/, acessado em 11/2019<br>
[3] T. Countz, 19-line Line-by-line Python Perceptron: Learning Machine Learning Journal #4, link: https://medium.com/@thomascountz/19-line-line-by-line-python-perceptron-b6f113b161f3, acessado em 11/2019<br>