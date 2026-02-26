# 🏀 NBA Player Profiling with Clustering  
### Unsupervised Learning Project | Data Mining

Projeto de **Machine Learning não supervisionado** aplicado à segmentação de jogadores da National Basketball Association (NBA) – Temporada 2023-24.

O objetivo foi identificar **perfis estatísticos de jogadores** com base exclusivamente em métricas de desempenho, utilizando técnicas de **clusterização**.

---

## 📌 Contexto do Problema

Times esportivos frequentemente utilizam dados para:

- Identificar perfis táticos  
- Encontrar jogadores similares  
- Apoiar decisões de scouting  
- Otimizar composições de elenco  

Este projeto busca responder:

> É possível identificar perfis funcionais de jogadores apenas a partir de estatísticas numéricas?

---

## 📊 Dataset

- 538 jogadores da temporada 2023-24  
- Estatísticas *per game*  
- Variáveis ofensivas e defensivas  
- Dados tratados e padronizados para modelagem  

Principais features utilizadas:

- Minutos por jogo (MP)  
- Field Goal % (FG%)  
- 3-Point % (3P%)  
- 2-Point % (2P%)  
- Free Throw % (FT%)  
- Rebotes ofensivos e defensivos  
- Volume de arremessos  
- Outras métricas quantitativas relevantes  

---

## ⚙️ Pipeline do Projeto

### 1️⃣ Data Cleaning & Preprocessing

- Remoção de duplicatas  
- Seleção de variáveis numéricas  
- Tratamento de valores ausentes  
- Padronização com `StandardScaler`  
- Preparação do dataset para aprendizado não supervisionado  

---

### 2️⃣ Modelagem

Algoritmo utilizado:

**K-Means (k-means++)**

Principais parâmetros:
- `init = "k-means++"`
- `n_init = 10`
- `random_state = 42`

Motivação:
- Eficiência computacional  
- Boa interpretabilidade  
- Adequado para segmentação baseada em distância  

---

### 3️⃣ Escolha do Número de Clusters

Métodos aplicados:

- Método do Cotovelo (Inércia)  
- Silhouette Score  

A decisão final foi baseada na maximização da coesão interna e separação entre grupos.

---

## 📈 Resultados

O modelo identificou agrupamentos com perfis bem definidos, como:

- Jogadores de alto volume ofensivo  
- Especialistas em perímetro  
- Defensores com foco em rebote  
- Jogadores de baixa utilização  

Os clusters apresentaram **boa separabilidade**, validada por métricas quantitativas.

---

## 🛠️ Stack Tecnológica

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Jupyter Notebook  

---
## 🚀 Aplicações Reais

Esse tipo de abordagem pode ser utilizado para:

- Scouting automatizado  
- Identificação de jogadores substitutos  
- Segmentação de perfis de mercado  
- Análise estratégica esportiva  

---
