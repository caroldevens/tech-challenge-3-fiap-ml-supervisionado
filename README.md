# ✈️ Tech Challenge 3 - Machine Learning (FIAP)

## 📌 Objetivo
Desenvolver um modelo de Machine Learning supervisionado para prever atrasos de voos com base em dados históricos.

---

## 📊 Dataset
O dataset contém informações de voos nos Estados Unidos, incluindo:

- Companhia aérea
- Aeroportos de origem e destino
- Horários de voo
- Distância percorrida
- Atrasos

⚠️ O arquivo `flights.csv` disponibilizado em:
https://drive.google.com/drive/folders/1aS7exW5N0qq1uIxvIBcAfc18OHojOMjj?usp=sharing
não foi versionado devido ao seu tamanho.  


---

## 🧪 Feature Engineering

Foram criadas variáveis adicionais para melhorar o modelo:

- `DEP_HOUR`: hora do voo
- `PERIODO_DIA`: manhã, tarde, noite ou madrugada
- `DISTANCE_CAT`: categorização da distância
- `IS_WEEKEND`: indicador de fim de semana

---

## 🤖 Modelo Supervisionado

Foi utilizado:

- **Random Forest Classifier**

Motivação:
- Capacidade de lidar com relações não lineares
- Boa performance com dados tabulares

---

## 📈 Resultados

### 🔹 Baseline

- Accuracy: ~69%
- Melhor desempenho na classe de voos sem atraso
- Baixa capacidade de prever atrasos

### 🔹 Observações

- Dataset desbalanceado (mais voos sem atraso)
- Alto número de falsos negativos (voos atrasados previstos como pontuais)

---

## ⚠️ Limitações

- Não inclui variáveis externas (clima, tráfego aéreo)
- Desbalanceamento impacta o desempenho
- Modelo tem dificuldade em prever eventos raros (atrasos)

---

## 🚀 Melhorias Futuras

- Ajuste de hiperparâmetros
- Balanceamento de classes
- Ajuste de threshold
- Teste com modelos mais avançados (ex: XGBoost)

---

## 🛠️ Tecnologias

- Python
- Pandas
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## 📁 Estrutura do Projeto

TC3
│
├── Data
│ ├── airlines.csv
│ ├── airports.csv
│
├── TC3_Modelo_Supervisionado.ipynb
├── TC3_Supervisioned.py
├── requirements.txt
