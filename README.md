# 🎵 Análise e Predição de Popularidade Musical (Spotify 2025)

> Um estudo completo de Data Science aplicando Estatística Inferencial e Machine Learning para entender o que torna uma música um sucesso global.

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![PyCaret](https://img.shields.io/badge/PyCaret-%2324292e.svg?style=for-the-badge&logo=python&logoColor=gold)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

---

## 📋 Sobre o Projeto

Este projeto utiliza um dataset global do Spotify (atualizado em Setembro de 2025) para investigar padrões na indústria musical. O fluxo de trabalho vai além da modelagem básica, incorporando testes de hipótese rigorosos e diagnósticos estatísticos para garantir a validade das previsões.

O objetivo é prever a **Popularidade da Faixa** (Regressão) e classificar se uma música será um **Hit** (Classificação), comparando modelos tradicionais (Scikit-Learn) com AutoML (PyCaret).

---

## 🧠 Etapas do Projeto

### 1. Preparação e Limpeza de Dados
Carregamento automatizado via kagglehub.
Tratamento de tipos de dados (datas, variáveis categóricas).
Detecção e visualização de outliers (Boxplots e Histogramas).
Análise de correlação (Heatmap).

### 2. Inferência Estatística
Antes de modelar, validamos hipóteses de negócio:
**Teste T de Student (Welch):** Existe diferença significativa de popularidade entre músicas explícitas e não explícitas?
**Teste Qui-Quadrado ($\chi^2$):** O tipo de álbum (Single vs Álbum) influencia a presença de conteúdo explícito?

### 3. Modelagem de Regressão (Predict Popularity)
Predição do score contínuo de popularidade (0-100).
**Diagnóstico:** Análise de Multicolinearidade (VIF) e análise de resíduos (Homocedasticidade, QQ-Plot e Teste de Normalidade Shapiro-Wilk).
**Modelos Manuais:** Regressão Linear Simples e Polinomial.
**AutoML (PyCaret):** Comparação de múltiplos algoritmos, tuning automático de hiperparâmetros e seleção do melhor modelo baseado no $R^2$.

### 4. Modelagem de Classificação (Predict Hit)
Definição de Hit: track_popularity >= 70.
**Estratégias:** Tratamento de desbalanceamento de classes (fix_imbalance).
**Modelos:** Gaussian Naive Bayes, Regressão Logística (Otimizada via GridSearchCV).
**AutoML (PyCaret):** Seleção do melhor classificador focado na métrica **AUC**.

---

## 🛠️ Tecnologias Utilizadas

**Linguagem:** Python
**Manipulação:** Pandas, NumPy
**Visualização:** Seaborn, Matplotlib
**Estatística:** Scipy Stats, Statsmodels (OLS, VIF)
**Machine Learning:** Scikit-Learn, PyCaret

---

## 🚀 Como Executar

Para rodar este projeto localmente ou no Google Colab:

1. **Instale as dependências:**
bash

pip install -r requirements.txt
2. **Execute o Notebook:**
O script fará o download automático do dataset:
> wardabilal/spotify-global-music-dataset-20092025

---

## 📊 Estrutura de Análise

| Etapa | Descrição | Ferramenta Principal |
| :--- | :--- | :--- |
| **EDA** | Distribuição de dados e Outliers | Seaborn / Matplotlib |
| **Testes H0** | Validação estatística de hipóteses | Scipy |
| **Regressão** | OLS & Linear Regression | Statsmodels / Sklearn |
| **Classificação** | Logistic Regression & Naive Bayes | Sklearn / GridSearchCV |
| **AutoML** | Seleção massiva de modelos | **PyCaret** |

---

## 📈 Resultados Esperados

Ao final da execução, o projeto entrega:
1.  Resultados estatísticos (P-valor) rejeitando ou não as hipóteses nulas.
2.  Tabela de VIF indicando quais variáveis possuem alta colinearidade.
3.  Gráficos de diagnóstico de resíduos para validar o modelo linear.
4.  Ranking dos melhores modelos de ML gerados pelo PyCaret.
5.  Matriz de confusão e AUC para o modelo classificador de Hits.

---

## 🤝 Contribuição

Sinta-se à vontade para fazer um fork deste projeto e submeter pull requests.

---
Desenvolvido com ❤️ e Python.
