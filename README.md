# Trabalho de Mineração de Dados - Seleção de Atributos

Este repositório contém o desenvolvimento do trabalho do 1º bimestre da disciplina de Mineração de Dados do curso de Desenvolvimento de Software Multiplataforma (DSM) da FATEC Franca - Dr. Thomaz Novelino. O projeto explora o uso de algoritmos de seleção de atributos para otimizar modelos de Machine Learning em tarefas de Regressão e Classificação.

---

## 🎯 Objetivo

O objetivo principal é aplicar a técnica de **Eliminação Recursiva de Atributos (RFE)** para reduzir a dimensionalidade de dois datasets distintos e analisar o impacto dessa redução na performance e interpretabilidade dos modelos preditivos, conforme especificado pela Prof.ª Jaqueline Brigladori Pugliesi.

---

## 📂 Estrutura do Projeto

O projeto está organizado da seguinte forma:

Trabalho-Mineracao/
├── notebooks/
│   ├── 1_Regressao_News_Popularity.ipynb
│   └── 2_Classificacao_Spambase.ipynb
├── .gitignore
└── README.md

---

## 📊 Datasets Utilizados

1.  **Regressão: [Online News Popularity](https://archive.ics.uci.edu/dataset/332/online+news+popularity)**
    * **Objetivo:** Prever o número de compartilhamentos (`shares`) de um artigo de notícia.
    * **Atributos:** 58 atributos preditivos.

2.  **Classificação: [Spambase](https://archive.ics.uci.edu/dataset/94/spambase)**
    * **Objetivo:** Classificar um e-mail como spam (1) ou não spam (0).
    * **Atributos:** 57 atributos preditivos.

---

## 🛠️ Tecnologias Utilizadas

* Python 3.10
* Conda (para gerenciamento de ambiente)
* Jupyter Notebook (executado via VS Code)
* **Bibliotecas Principais:**
    * Pandas
    * NumPy
    * Scikit-learn
    * Matplotlib / Seaborn
    * Requests

---

## 🚀 Como Executar o Projeto

Siga os passos abaixo para configurar e executar os notebooks localmente.

1.  **Clone o repositório:**
    ```bash
    git clone [URL_DO_SEU_REPOSITORIO_AQUI]
    cd Trabalho-Mineracao
    ```

2.  **Crie o ambiente Conda:**
    ```bash
    conda create --name mineracao_dados python=3.10
    ```

3.  **Ative o ambiente:**
    ```bash
    conda activate mineracao_dados
    ```

4.  **Instale as dependências necessárias:**
    ```bash
    conda install pandas numpy matplotlib seaborn scikit-learn requests
    ```

5.  **Abra o projeto no VS Code e execute os notebooks:**
    * Abra a pasta `Trabalho-Mineracao` no Visual Studio Code.
    * Certifique-se de que o Kernel do Jupyter está selecionado para o ambiente `mineracao_dados`.
    * Execute as células dos notebooks localizados na pasta `/notebooks`.

---

## 📈 Resultados

A seleção de atributos com RFE apresentou resultados distintos para cada tarefa, evidenciando o trade-off entre simplicidade e performance.

### Tarefa de Regressão (Online News Popularity)

A complexidade do modelo foi reduzida em 65%, com uma perda de performance (R²) insignificante, resultando em um modelo mais eficiente.

| Métrica | Modelo Inicial (58 atributos) | Modelo Final com RFE (20 atributos) |
| :--- | :---: | :---: |
| **R² (R-squared)** | 0.1274 | 0.1199 |
| **RMSE (log)** | 0.8649 | 0.8686 |

### Tarefa de Classificação (Spambase)

A redução de 74% no número de atributos teve um custo notável na performance, principalmente na capacidade do modelo de detectar spam (recall).

| Métrica | Modelo Inicial (57 atributos) | Modelo Final com RFE (15 atributos) |
| :--- | :---: | :---: |
| **Acurácia** | 0.9294 | 0.8697 |
| **Recall (spam)** | 0.90 | 0.76 |
| **Precisão (spam)** | 0.92 | 0.89 |

---

## 👤 Autor

* **Igor Owen Silva de Paula**