# Analise-de-sentimento
Análise de sentimento com o dataset “Sentiment Labelled Sentences”; Este projeto demonstra a análise de sentimento utilizando o dataset "Sentiment Labelled Sentences", especificamente o arquivo `amazon_cells_labelled.txt`. O objetivo é construir um modelo capaz de classificar avaliações de produtos da Amazon como positivas ou negativas.

## Conteúdo
1. [Bibliotecas](#bibliotecas)
2. [Pré-processamento](#pré-processamento)
    * [Limpeza](#limpeza)
    * [Vetorização](#vetorização)
3. [Modelagem](#modelagem)
4. [Avaliação](#avaliação)
5. [Resultados](#resultados)
6. [Conclusão](#conclusão)

## 1. Bibliotecas <a name="bibliotecas"></a>

*   `pandas`: Para manipulação e análise de dados.
*   `string`: Para operações com strings.
*   `sklearn.model_selection`: Para dividir o dataset em treino e teste.
*   `sklearn.feature_extraction.text`: Para vetorização de texto com TF-IDF.
*   `sklearn.naive_bayes`: Para o modelo de classificação Naive Bayes.
*   `sklearn.pipeline`: Para combinar etapas de pré-processamento e modelagem.
*   `sklearn.metrics`: Para calcular a acurácia e matriz de confusão do modelo.
*   `nltk`: Para processamento de linguagem natural (PLN).
*   `re`: Para expressões regulares (limpeza de texto).
*   `matplotlib.pyplot` e `seaborn`: Para visualização de dados.

## 2. Pré-processamento <a name="pré-processamento"></a>

### Limpeza <a name="limpeza"></a>

A função `preprocess_text` realiza a limpeza do texto, incluindo:

*   Conversão para minúsculas.
*   Remoção de URLs, menções (@), hashtags (#), números e caracteres especiais.
*   Remoção de pontuação e espaços em branco adicionais.
*   Remoção de stopwords (palavras irrelevantes).

### Vetorização <a name="vetorização"></a>

A técnica TF-IDF (TfidfVectorizer) é utilizada para converter o texto em uma matriz de características numéricas, representando a importância de cada palavra em um texto.

## 3. Modelagem <a name="modelagem"></a>

O modelo Naive Bayes Multinomial é utilizado para classificar as avaliações como positivas ou negativas.  O pipeline do scikit-learn combina as etapas de vetorização e modelagem.

## 4. Avaliação <a name="avaliação"></a>

A acurácia do modelo é calculada utilizando a função `accuracy_score`. A matriz de confusão é gerada para avaliar o desempenho do modelo em mais detalhes.

## 5. Resultados <a name="resultados"></a>
A acurácia do modelo, foi de 85%.

![image](https://github.com/user-attachments/assets/091b7239-cad2-450d-8445-2c02d5d92a9a)

>(0 : Psitivos.  1: Negativos)

## 6. Conclusão <a name="conclusão"></a>
O modelo Naive Bayes apresentou um bom desempenho na classificação de sentimentos, com uma acurácia de 85%.  Futuros trabalhos podem explorar o uso de outros modelos, como Support Vector Machines (SVM) ou modelos mais complexos de Deep Learning, para tentar melhorar ainda mais a performance.  Também é possível experimentar com diferentes técnicas de pré-processamento, como lematização ou stemming.
