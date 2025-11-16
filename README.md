# 📊 Análise de Sentimentos em Avaliações da Amazon

Processamento de Linguagem Natural (PLN) + Machine Learning (ML)

Este projeto realiza análise de sentimentos em avaliações reais de consumidores da Amazon.
Ele abrange desde limpeza e padronização de textos até a criação de um modelo de Machine Learning utilizando TF-IDF + Regressão Logística, capaz de classificar novas avaliações como positivas ou negativas.
---
# 🎯 Objetivos do Projeto

Classificar avaliações em positivo ou negativo.

Comparar diferentes estágios de pré-processamento.

Demonstrar o impacto da limpeza textual nos modelos.

Criar um pipeline realista usando técnicas modernas de NLP.

Salvar e testar o modelo em avaliações novas.
---
# 📁 Estrutura do Projeto

O notebook contém as seguintes etapas:

## 1. Carregamento do Dataset

Dataset com 15 mil avaliações, contendo:

texto da avaliação

nota (1 a 5 estrelas)

sentimento rotulado
---
## 2. Pré-processamento dos Textos
O texto passa por várias camadas de transformação:
✔ Remoção de stopwords
✔ Tokenização
✔ Remoção de pontuação
✔ Remoção de acentuação
✔ Normalização (lowercase)
✔ Stemming (RSLP)

Cada etapa gera uma nova coluna:

tratamento_1

tratamento_2

tratamento_3

tratamento_4

tratamento_5 (versão final e mais limpa)
---
## 3. Exploração dos Dados (EDA)

Contagem de palavras mais frequentes

WordCloud geral e por sentimento

Análise das palavras positivas vs negativas

Distribuições de sentimentos
---
## 4. Vetorização dos Textos

Foram testadas várias técnicas de vetorização:

Bag of Words

TF-IDF

TF-IDF com ngrams (1,2)

Teste com diferentes quantidades de features (50, 100, 1000, todas)
---
## 5. Modelagem e Avaliação

O principal modelo utilizado foi Regressão Logística, gerando resultados para cada etapa.

# 📈 Melhor resultado obtido
Técnica	Pré-processamento	Acurácia
TF-IDF (ngrams 1–2)	tratamento_5	91.85%
---
## 6. Interpretação do Modelo

Foi analisado o peso das palavras no modelo:

🔹 Palavras mais associadas a sentimentos positivos
ex.: ótimo, excelente, perfeito, adorei, satisfatório

🔹 Palavras mais associadas a sentimentos negativos
ex.: péssimo, defeito, frágil, decepção, devolução
---
## 7. Exportação dos Modelos

O projeto salva:

tfidf_vectorizer.pkl

modelo_regressao_logistica.pkl

Para uso posterior.
---
## 8. Função de Classificação para Novas Avaliações

Foi criada uma função que:

Processa o texto (todas as etapas do tratamento)

Vetoriza

Prediz o sentimento

Exemplo:

prever_sentimento("Ótimo produto, super recomendo!")
# Resultado → positivo
---
# 🧪 Tecnologias Utilizadas

Python

Pandas

Matplotlib

Seaborn

NLTK

Scikit-learn

WordCloud

Joblib

Unidecode
---
# 📌 Exemplos de Classificação

| Avaliação                                                      | Resultado |
|---------------------------------------------------------------|-----------|
| "Ótimo produto, super recomendo!"                             | positivo  |
| "Entrega atrasou muito, decepcionado."                        | negativo  |
| "Produto danificado, precisei devolver."                      | negativo  |
| "Bom custo-benefício, atendeu às expectativas."               | positivo  |
---
#🚀 Resultados e Conclusão

O projeto demonstra como pré-processamento textual e vetorização adequada elevam significativamente a performance do modelo.

Bag of Words: ~79%

TF-IDF bruto: ~79%

TF-IDF + tratamento completo: 91.85%
---
