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
não foi versionado devido ao seu tamanho e limitação do github.


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

📊 📌 Interpretação dos resultados

🔍 Avaliação do Modelo Supervisionado

O modelo Random Forest apresentou uma acurácia de aproximadamente 69,7%, indicando que ele consegue classificar corretamente a maioria dos voos quanto à ocorrência de atraso.

Ao analisar as métricas por classe, observa-se:

Para a classe 0 (voos sem atraso):

Precision: 0.78

Recall: 0.85

F1-score: 0.81

Para a classe 1 (voos com atraso):

Precision: 0.30

Recall: 0.21

F1-score: 0.25

Isso indica que o modelo tem bom desempenho para identificar voos sem atraso, mas apresenta dificuldade em identificar corretamente voos atrasados.

⚖️ Desbalanceamento

O desempenho inferior na classe de atraso ocorre devido ao desbalanceamento do dataset, onde há significativamente mais voos sem atraso do que com atraso.

🔲 Análise da Matriz de Confusão

Verdadeiros negativos: 38.062

Falsos positivos: 6.862

Falsos negativos: 10.916

Verdadeiros positivos: 2.887

O modelo apresenta um número elevado de falsos negativos, ou seja, muitos voos atrasados estão sendo classificados como não atrasados.

📌 Conclusão

O modelo é eficaz para identificar voos pontuais, mas ainda precisa de melhorias para prever atrasos, especialmente devido ao desbalanceamento dos dados e à complexidade do problema.

