# ANN - Artificial Neural Network (Perceptron) #

## I.	 INTRODUÇÃO ##
Esse projeto tem como objetivo exemplificar a aplicação do algorítimo de Redes Neurais Arificiais (RNA), também chamado 
de ANN (Artificial Neural Network) utilizado para aprendizado de máquina, na qual pode ser aplicado para problemas de regressão
e classificação.<br>
O modelo de neuronio proposto por esse projeto é o Perceptron com apenas uma camada e a função de ativação é a degrau.

## II.	FUNDAMENTAÇÃO TEÓRICA ##

### A.	MÉTODO DOS MÍNIMOS QUADRADOS ###
O Método dos Mínimos Quadrados é um dos métodos utilizado para tratamento estatístico de dados experimentais (frequentemente
utilizado em Física e outras ciências), utilizado para obter estimativas com base em dados.[1]<br>
A base matemática contextualizada a seguir foi retirada de [2], mais detalhes podem ser analisado utilizando [1] ou [2].<br>
A ideia básica é aproximar o sistema de equações a funções de reta, tomando com base um vetor de entrada X, como:

![Alt text](images/lms-eq1.png?)

Se a uma função de reta é dado por "Y = ax + b", na qual temos o termo independente e o termo que multiplica a variável,
podemos transpor isso a um vetor de "p" estados, da seguinte maneira:

![Alt text](images/lms-eq2.png?)

Beta0 é o termo independente da função, também conhecido em Machine Learning como BIAS e cada outro termo do vetor Beta,
ou seja, Beta1 ... BetaP refere-se a como a variável se relaciona a função Y de estudo. Podendo ser de três maneiras:

<b>Relação positiva e Linear:</b><br>
 ![Alt text](images/lms-graph-01.png?)<br>

<b>Relação negativa e Linear:</b> <br>
 ![Alt text](images/lms-graph-02.png?)<br>
 
 <b>Sem Relacionamento:</b><br>
 ![Alt text](images/lms-graph-03.png?)<br>
 
Na qual Beta é obtido calculando o mínimo erro quadrático, dada pela função:
![Alt text](images/lms-eq3.png?)

Ao fim podemos inferir que o vetor de Beta pode ser calculado da seguinte maneira:

![Alt text](images/lms-eq4.png?)

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

Para a primeira proposta temos:

![Alt text](images/alpswater-dataset.png?)

## V. CONCLUSÃO ##
Dado os resultados vistos em IV podemos inferir que o Método dos Mínimos Quadrados chegou ao resultado esperado e
graficamente é possível inferir que o erro de aproximação é relativamente baixo.<br>
Um dos objetivos do projeto em curso é implementar o algorítimo do MMQ. Se analisarmos os dados chegamos a conclusão de 
que o algorítimo foi implementado corretamente, porém não é possível fazer inferências relativas aos problemas abordados 
anteriormente devido a não implementação de funções que calculem o erro, erro médio quadrático, implementação do Teste F,
Teste T e outras abordagens estatísticas que validem a solução de regressão proposta anteriormente.

## VI. AGRADECIMENTOS ##

Agradecimentos especiais a CAPES e ao Centro Universitário FEI por financiar o mestrado que está em curso; 
ao professor Reinaldo Bianchi por proporcionar visões sobre o mundo acadêmico e orientar trabalhos científicos 
com o objetivo de lapidar os conhecimentos abordados em sala; aos meus pais e a minha família que sempre me 
apoiaram em meio a dificuldades.

## VII. REFERÊNCIAS ##

[1]	O. A. M. Helene, Método dos mínimos quadrados com formalismo matricial: guia do usuário, Editora: Livraria da Física, São Paulo, 2016<br>
[2]	R. Bianchi, Tópicos Especiais em Aprendizagem, 2019, ppt slide Centro Universitário FEI.