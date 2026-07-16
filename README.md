# 🔧 Sistema Previsor de Falhas (SISPREV) - Machine Learning Pipeline

## 📌 Sobre o Projeto

O **SISPREV** é um software desenvolvido para prever falhas mecânicas em equipamentos industriais utilizando técnicas de Ciência de Dados e Machine Learning.

O projeto simula um ambiente industrial monitorado por sensores, onde diferentes variáveis operacionais são utilizadas para identificar antecipadamente máquinas com maior probabilidade de falha.

A previsão antecipada permite que equipes de manutenção realizem intervenções preventivas, reduzindo custos, aumentando a disponibilidade dos equipamentos e evitando paradas inesperadas na produção.

---

# 🎯 Problema que o software resolve

Em ambientes industriais, falhas inesperadas em máquinas podem gerar:

* Paradas na produção;
* Elevados custos de manutenção corretiva;
* Perda de produtividade;
* Desperdício de matéria-prima;
* Riscos operacionais.

Este projeto utiliza algoritmos de classificação para prever se uma máquina apresentará falha (**falha_maquina = 1**) ou não (**falha_maquina = 0**) com base nos dados coletados pelos sensores.

---

# 🛠 Tecnologias utilizadas

## Linguagem

* Python 3

## Bibliotecas

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* RandomUnderSampler
* Statsmodels (para cálculo do VIF)
* Imblearn (para balanceamento com Random Under Sampler)

## Algoritmos de Machine Learning

* K-Nearest Neighbors (KNN)
* Decision Tree Classifier

## Técnicas aplicadas

* Análise Exploratória de Dados (EDA)
* Limpeza de Dados
* Tratamento de Valores Ausentes
* Remoção de Duplicatas
* Identificação de Outliers
* Feature Engineering
* One-Hot Encoding
* Verificação de Multicolinearidade por meio de VIF (extra)
* Balanceamento de Classes com RandomUnderSampler
* Padronização com StandardScaler
* Ajuste de Hiperparâmetros
* Avaliação de Overfitting
* Avaliação por Acurácia

---

# 📊 Fluxo do Projeto

```text
                Dataset
                    │
                    ▼
        Análise Exploratória (EDA)
                    │
                    ▼
      Limpeza e Tratamento dos Dados
                    │
                    ▼
         Feature Engineering
                    │
                    ▼
      Balanceamento (RandomUnderSampler)
                    │
                    ▼
  Divisão Treino/Teste (seeds: 43, 123 e 64)
                    │
                    ▼
     Escalonamento (StandardScaler)
                    │
                    ▼
        Treinamento dos Modelos
          ├── KNN
          └── Árvore de Decisão
                    │
                    ▼
        Ajuste de Hiperparâmetros
                    │
                    ▼
         Avaliação dos Modelos
                    │
                    ▼
        Modelo Final Selecionado
```

---

# 📁 Estrutura do Projeto

```text
Projeto/
│
├─📁 imagens_exportadas (Pasta)
    └── box_plot_preditoreas.png
    └── gráfico_após_balanceamento.png
    └── histograma_variáveis_preditoras.png
    └── mapa_de_calor_com_feature_engineering.png
    └── mapa_de_calor_sem_feature_engineering.png
    └── taxa_desbalanceamento_target.png
├── Projeto_Final_Mod_1_SCTEC.ipynb
├── manutencao_preditiva.csv
├── README.md
├── gitignore
└── requirements.txt
```

---

# ▶ Como executar

## 1. Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

---

## 2. Entre na pasta

```bash
cd SEU_REPOSITORIO
```

---

## 3. Crie um ambiente virtual (opcional)

Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Linux / Mac

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 4. Instale as dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn notebook
```

ou

```bash
pip install -r requirements.txt
```

---

## 5. Execute o Notebook

```bash
jupyter notebook
```

Abra o arquivo e aponte para o dataset

```
Projeto_Final_Mod_1_SCTEC.ipynb
```

e execute todas as células na ordem.

---

# 📈 Etapas desenvolvidas

✔ Importação dos dados

✔ Análise exploratória

✔ Estatísticas descritivas

✔ Visualização gráfica

✔ Tratamento de valores ausentes

✔ Remoção de duplicatas

✔ Identificação de outliers

✔ Criação de novas variáveis (Feature Engineering)

✔ Codificação de variável categórica

✔ Balanceamento utilizando Random Under Sampler

✔ Separação entre treino e teste com 3 diferentes seeds

✔ Padronização dos dados

✔ Treinamento do KNN

✔ Treinamento da Árvore de Decisão

✔ Ajuste de hiperparâmetros

✔ Avaliação do overfitting

✔ Comparação entre os modelos

---

# 📌 Resultados

Ao final do projeto são comparados os modelos de classificação desenvolvidos, utilizando principalmente:

* Acurácia
* Comparação entre treino e teste
* Avaliação do overfitting
* Escolha do melhor modelo

---

# 🚀 Melhorias futuras

O projeto pode ser expandido com diversas melhorias, como:

* Implementação de Random Forest
* Implementação de XGBoost
* Utilização de LightGBM
* Aplicação de validação cruzada (Cross Validation)
* Otimização automática de hiperparâmetros com GridSearchCV ou RandomizedSearchCV
* Desenvolvimento de uma API utilizando FastAPI ou Flask
* Interface gráfica utilizando Streamlit
* Dashboard em Power BI ou Plotly Dash
* Deploy em ambiente de nuvem (AWS, Azure ou Google Cloud)
* Monitoramento contínuo do desempenho do modelo
* Inclusão de novos sensores industriais
* Explicabilidade das previsões utilizando SHAP ou LIME

---

# 👨‍💻 Autor

Fábio Rodrigues Spiazzi - fabiospiazzi@gmail.com
Desenvolvido como projeto final do módulo 1 do curso de IA para análise preditiva (SCTec - SENAI).


---

# 🔗 Link do Vídeo de Apresentação

https://drive.google.com/drive/folders/1BZN-ylh2af6EfBhIW_enJ9qtfGR5MoTD?usp=sharing
