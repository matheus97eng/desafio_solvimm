# desafio_solvimm

## Apresentação

Este diretório foi criado para resolução de um desafio de processo seletivo. Se trata de um problema de **machine learning** de **classificação múltipla**.

Na descrição do problema, uma empresa fictícia deseja classificar a categoria dos seus produtos de acordo com os reviews escritos pelos clientes. Se trata portanto de um desenvolvimento de **NLP** (Natural Linguage Processing). O modelo escolhido para realizar a classificação foi o algoritmo de **Naive Beyes**. O modelo, treinado, deve ser utilizado em uma função chamada `validate`, que recebe, além do modelo, uma instância `vect`, que realiza a preparação das strings para execução do modelo, e um dataframe que **não contém** a coluna da classificação dos produtos. Essa mesma função deve retornar o mesmo dataframe, mas com a coluna contendo as previsões do modelo, fazendo assim a classificação automática dos produtos.

+ vantagens do modelo - ele é simples e rápido de ser implementado
+ desvantagens - o modelo não considera contextualização dos textos, diferente de outros algoritmos como o BERT. O Naive Beyes analisa cada palavra do texto **individualmente**

## Resultados

O modelo treinado teve uma boa execução, em um tempo razoavelmente curto (alguns segundos para treinamento utilizando uma base de dados de 170582 linhas, cada linha contendo um texto de review diferente). Além disso ele consegue rapidamente prever a classificação de produtos de um dataframe e obteve uma acurácia de aproximadamente 73%.

## Bibliotecas

O notebook foi todo desenvolvido em **Python**, utilizando as seguintes bibliotecas:

- pandas - manipulação de dataframes
- nltk.corpus.stopwords - lista de palavras consideradas "stopwords"
- string - manipulação de strings
- re - biblioteca python para operação de strings com codificação. No caso iremos trabalhar com a codificação dos emojis.
- da biblioteca sklearn:
    - MultinomialMB - algoritmo de Naive Beyes do tipo multinominal, o mais indicado para multiclassificação
    - train_test_split - divide os dados em treino e teste
    - accuracy_score - método utilizado para validar o modelo

## Conteúdo do diretório

- [`notebook_de_apresentacao.ipynb`](https://github.com/matheus97eng/desafio_solvimm/blob/main/notebook_de_apresentacao.ipynb) - notebook onde foi realizado todo o desenvolvimento do trabalho. Contém as funções criadas, inclusive a função `validate`, juntamente com as explicações das tomadas de decisão e as explicações das funções.
- pasta [`data`](https://github.com/matheus97eng/desafio_solvimm/tree/main/data) - contém a base de dados `reviews.tsv` utilizada para treinamento e teste do modelo
