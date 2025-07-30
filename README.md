# Classificação de E-mails: Spam vs Não-Spam (Ham)

Este projeto tem como objetivo construir um modelo de **classificação de e-mails** para identificar se uma mensagem é *spam* (indesejada) ou *não-spam* (também chamada de *ham*), utilizando técnicas de **Processamento de Linguagem Natural (NLP)** e **Redes Neurais** com TensorFlow e Keras.

---

## Descrição

O dataset utilizado é o `spam.csv`, que contém mensagens de e-mail rotuladas como `spam` ou `ham`. O projeto cobre todo o processo, desde a leitura e exploração dos dados, balanceamento das classes, pré-processamento de texto (tokenização e padronização), construção e treinamento da rede neural, até a avaliação do modelo e análise dos resultados.

---

## Estrutura do Projeto

1. **Importação das bibliotecas:** manipulação de dados, visualização, pré-processamento e construção do modelo.
2. **Configuração de sementes aleatórias:** para garantir resultados reprodutíveis.
3. **Leitura e exploração dos dados:** análise do formato e distribuição das classes.
4. **Balanceamento da base:** equalização do número de exemplos entre `spam` e `ham` para evitar vieses.
5. **Codificação dos rótulos:** transformação das categorias em valores numéricos (0 e 1).
6. **Divisão dos dados:** separação em conjuntos de treino (70%) e teste (30%).
7. **Tokenização e padronização:** conversão do texto em sequências numéricas e uniformização do tamanho.
8. **Construção e treino da rede neural:** arquitetura simples com embedding, flatten, dense e dropout.
9. **Avaliação do modelo:** acurácia, loss, matriz de confusão e visualização.
10. **Análise dos dados:** gráficos para entender distribuição das classes e quantidade de palavras por e-mail.

---

## Como executar

1. Baixe o arquivo `ClassificacaoDeEmailESpam.ipynb` e o arquivo `spam.csv` para a mesma pasta.

2. Abra o notebook em Jupyter Notebook ou no Google Colab.

3. Execute as células na ordem.

---

## Resultados Esperados

* Treinamento do modelo por 20 épocas.
* Acurácia esperada acima de 90% (depende da base e configuração).
* Matriz de confusão indicando bom desempenho na distinção entre spam e ham.
* Visualizações evidenciando o balanceamento das classes e análise da distribuição do texto.

---

## Explicações Técnicas

* **Tokenização:** representa palavras por índices numéricos, limitando às 1000 palavras mais frequentes.
* **Padding:** uniformiza o tamanho das sequências para 500 palavras, adicionando zeros ao final quando necessário.
* **Rede Neural:**

  * Camada de entrada (`Input`) para sequência de 500 tokens.
  * Camada `Embedding` para transformar índices em vetores de dimensão 50.
  * Camada `Flatten` para achatar os vetores.
  * Camada `Dense` com 10 neurônios e ativação ReLU.
  * Camada `Dropout` para evitar overfitting.
  * Camada de saída `Dense` com ativação sigmoid para classificação binária.

---

## Visualizações Incluídas

* Distribuição original das classes (`ham` x `spam`).
* Distribuição balanceada após amostragem.
* Histograma da quantidade de palavras por tipo de e-mail.
* Matriz de confusão com heatmap para análise do desempenho.

