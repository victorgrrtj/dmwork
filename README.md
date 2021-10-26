<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Trabalho Final de Data Mining

#### Aluno: [Victor Ribeiro](https://github.com/victorgrrtj)
#### Aluna: [Thaís Guarize](https://github.com/victorgrrtj)
#### Orientadora: [Manoela Kohler](https://github.com/manoelakohler) e [Felipe Borges](https://github.com/link_do_github).

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Data Mining".

Horse.ipynb (https://github.com/victorgrrtj/dmwork/blob/main/Horse.ipynb)

---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->

O objetivo deste trabalho é propor um modelo de classificação. O presente modelo usa os conceitos, ferramentas e bibliotecas ensinadas nas aulas de Mineração de Dados, como pandas, numpy, matpotlib, seaborn, SVM, Logistic Regression, Decision Tree, Random Forest e KNN. Para elaboração do modelo foram previamente elaboradadas as etapas de análise exploratória e pré processamento da base de dados, conforme demonstrados nas aulas. Por fim, salvamos o modelo para futura inferências.

### Abstract <!-- Opcional! Caso não aplicável, remover esta seção -->

<!-- trocar o texto abaixo pelo resumo do trabalho, em inglês -->

The work's purpose is build a classification model. This model uses concepts, tools and libraries learned in Data Mining's classes, like pandas, numpy, matpotlib, seaborn, SVM, Logistic Regression, Decision Tree, Random Forest e KNN. For model's elaboration, were previously elaborated steps of exploratory analsys and pre process of data, as demonstrated in class. Finally, we saved the model for futures inferences.

### 1. Introdução

A base de dados apresentada é de cavalos cujo classificação é categórica e dividida em três saídas: viveu, morreu e submetido à eutanásia. A base possui diversas classes de atributo, sendo todas elas esclarecidas neste [PDF](https://github.com/victorgrrtj/dmwork/blob/main/DataDict.pdf).
Para realizar as análises e a elaboração do modelo, utilizamos o Google Colab e bibliotecas como Pandas, Scikit Learning, dentre outras.
Na etapa de Análise Exploratória, vimos que se tratavam de 11 colunas com dados numéricos e 17 com dados categóricos (string). Sendo que, de acordo com os atributos esclarecidos da base, 3 colunas com dados numéricos eram na verdade categorias de doencças dos animais. Portanto, tratamos esta coluna como dado categórico. Também verificamos uma quantidade grande de dados faltantes, motivo pelo qual excluímos algumas colunas e linhas para a elaboração do modelo. Para tratamento dos dados faltantes, imputamos os dados numéricos pela média dos dados de cada coluna e imputamos os dados categóricos pela maior frequência. Após a imputação, realizamos normalização nas colunas com dados numéricos e OneHotEncoder nos dados categóricos.
Após o pré processamento da base, prosseguimos com a etapa de elaboração e testes dos modelos.

### 2. Modelagem

Na etapa de modelagem, fizemos testes com SVM, Logistic Regression, Decision Tree, Random Forest e KNN. Fizemos testes com dados balanceados, com RandomOverSampler e RandomUnderSampler, e também com os dados desbalanceados. Realizamos buscas com o GridSearchCV, a fim de validarmos melhores parâmetros para os modelos. Utilizamos Pipelines para realizar as transformações nas colunas e testes dos modelos.

### 3. Resultados

Após a modelagem e testes dos modelos, constatamos que o melhor modelo foi o KNN com os seguintes parâmetros: n_neighbors=3, weights='distance' e com a base balanceada pelo RandomOverSampler. Este modelo apresentou acurácia, kappa e F1 score com 100% de acerto na base de teste. Realmente para nós foi uma surpresa, uma vez que todos os testes foram feitos na base de teste e que não houve dados "vazados" da base de treino para base de teste. O mesmo modelo, porém com a base desbalanceada, apresentou apenas 1 erro, com Acurácia de 98,87%, Kappa de 97,96%, F1 de 98,86%.
O modelo Random Forest (max_features=4, n_estimators=100) com a base balanceada pelo RandomOverSampler também ficou muito bom, com Acurácia de 97,75% Kappa de 95,91% e F1 de 97,72, com apenas 2 erros.

### 4. Conclusões

A base sugerida foi excelente para exercício dos conceitos, práticas e abordagens em aula. Somos gratos aos professores que demonstraram muito bem como elaborar modelos de Machine Learning clássico. Conforme relatado em aula, não existe um modelo perfeito. Tudo é elaborado com ajustes nos parâmetros e com teste. 

---

Matrícula: 211.100.047

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
