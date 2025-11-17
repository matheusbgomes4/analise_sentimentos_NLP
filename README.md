# 📊 Análise de Sentimentos — Avaliações da Amazon

Processamento de Linguagem Natural (NLP) + Machine Learning (ML) para classificar avaliações da Amazon como *positivas* ou *negativas*, a partir de um pipeline completo de pré-processamento, vetorização e modelagem.

---

## 🎯 Objetivos

- Classificar avaliações em positivo ou negativo  
- Comparar diferentes fases de pré-processamento  
- Avaliar impacto da limpeza textual no desempenho dos modelos  
- Construir pipeline realista usando TF-IDF + Regressão Logística  
- Permitir pré-classificação de novas avaliações

---

## 🧪 Pipeline do Projeto

1. Carregamento do dataset  
2. Pré-processamento de texto (5 níveis)  
3. Análise exploratória (EDA)  
4. Vetorização (Bag of Words / TF-IDF / n-grams)  
5. Construção do modelo (Regressão Logística)  
6. Avaliação de métricas  
7. Interpretação do modelo (importância das palavras)  
8. Exportação do modelo + vetorizador  
9. Função para prever sentimento de novas frases

---

## 📁 Estrutura dos Dados

| Coluna         | Descrição                              |
|----------------|------------------------------------------|
| `reviewText`   | Texto da avaliação                       |
| `rating`       | Nota de 1 a 5 estrelas                    |
| `sentiment`    | Rótulo de sentimento (positivo / negativo) |

---

## 🔧 Pré-processamento Textual

Para cada avaliação, aplicamos:

- Remoção de stopwords  
- Tokenização  
- Remoção de pontuação  
- Conversão para minúsculas  
- Remoção de acentos  
- *Stemming* (RSLP)

As transformações geram colunas intermediárias:

- `tratamento_1`, `tratamento_2`, ..., `tratamento_5`

---

## 📈 Vetorização & Modelagem

Testamos diferentes combinações:

- **Vetorização**:
  - Bag of Words  
  - TF-IDF  
  - TF-IDF com n-grams (1,2)  
  - TF-IDF com diferentes números de features (50 / 100 / 1000)

- **Modelo**:
  - Regressão Logística

**Melhor resultado obtido**:

| Técnica         | Pré-processamento | Acurácia |
|----------------|--------------------|----------|
| TF-IDF (ngrams) | tratamento_5        | **91.85 %** |

---

## 💡 Interpretação do Modelo

- **Palavras positivas** mais relevantes: *ótimo*, *excelente*, *perfeito*, *adorei*, *satisfatório*  
- **Palavras negativas** mais relevantes: *péssimo*, *defeito*, *frágil*, *decepção*, *devolução*

---

## 🧰 Tecnologias

- Python  
- Pandas  
- NLTK  
- Scikit-learn  
- Matplotlib & Seaborn  
- WordCloud  
- Joblib  
- Unidecode  

---

## 🚀 Como Usar

1. Clone o repositório:  
   ```bash
   git clone https://github.com/matheusbgomes4/analise_sentimentos_NLP.git
   cd analise_sentimentos_NLP

2. Instale dependências:
pip install -r requirements.txt
3. Execute o notebook no Jupyter ou Google Colab
4. Para prever o sentimento de uma nova avaliação:
from seu_script import prever_sentimento  
print(prever_sentimento("Ótimo produto, super recomendo!"))
---
# 📌 Exemplos de Classificação
| Avaliação                                       | Resultado |
| ----------------------------------------------- | --------- |
| “Ótimo produto, super recomendo!”               | positivo  |
| “Entrega atrasou muito, decepcionado.”          | negativo  |
| “Produto danificado, precisei devolver.”        | negativo  |
| “Bom custo-benefício, atendeu às expectativas.” | positivo  |
---
# 🔭 Possíveis Melhorias Futuras

Tunagem com Cross-Validation

Testar modelos mais robustos (SVM, Random Forest)

Testar embeddings modernos (Word2Vec, BERT)

Criar API ou dashboard para utilização real

Criar pipeline completo com MLflow
---

# ✔️ Conclusão

Este projeto demonstra como técnicas de pré-processamento, vetorização e modelagem podem formar um pipeline robusto de NLP, alcançando 91,85% de acurácia na classificação de sentimentos.

É um exemplo completo e replicável de Machine Learning aplicado em linguagem natural.
---

