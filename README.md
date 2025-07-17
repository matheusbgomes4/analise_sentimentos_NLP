# 🧠 Análise de Sentimentos de Avaliações da Amazon

Este projeto tem como objetivo realizar uma análise de sentimentos com base em avaliações de produtos da Amazon, utilizando técnicas de Processamento de Linguagem Natural (PLN) e algoritmos de Machine Learning.

## 📌 Objetivos
- Classificar avaliações em positivas ou negativas.
- Comparar o desempenho de diferentes modelos de classificação.
- Criar um pipeline simples e eficiente para análise de sentimentos em português.

## 🗂️ Conteúdo
O projeto está estruturado em um notebook Jupyter, contendo as seguintes etapas:

**Carregamento dos Dados**
   - Dataset contendo avaliações de produtos (texto + rótulo)

**Pré-processamento**
   - Limpeza dos textos
   - Remoção de stopwords e pontuações

**Exploração de Dados**
   - Distribuição dos sentimentos

**Vetorização**
   - Transformação dos textos em vetores com `TF-IDF`

**Modelagem**
   - Treinamento dos modelos:
     - Regressão Logística
     - Random Forest
     - Naive Bayes

**Avaliação**
   - Acurácia
   - F1-Score
   - Matriz de Confusão

**Teste com Novas Avaliações**
   - Classificação de texto inserido manualmente

## 🧪 Tecnologias e Bibliotecas
- Python
- Pandas
- Matplotlib / Seaborn
- NLTK
- Scikit-learn

## 💡 Exemplos de Uso

```python
sentenca = "O produto chegou antes do prazo e funciona perfeitamente!"
modelo.predict(vectorizer.transform([sentenca]))

