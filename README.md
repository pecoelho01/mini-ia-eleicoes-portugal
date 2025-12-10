# 🇵🇹 Mini AI: Portuguese Legislative Elections Predictor 📊

This project implements a simple **Machine Learning** model to predict the **vote share of major political parties** in the Portuguese Legislative Elections, focusing on the **Lisbon** and **Porto** districts.  

The model uses an optimized **Random Forest Regressor** to analyze historical voting trends and macroeconomic factors.

## 🔍 Overview
- **Prediction Target:** Vote percentage for **PS**, **AD/PSD**, and **CH**.  
- **Core Model:** Optimized Random Forest Regressor.  
- **Most Important Feature:** `%_Votos_Anteriores` (previous election vote share).  
- **Performance:** Achieved **MAE = 3.39%** after feature engineering and hyperparameter tuning.  
- **Training Data:** Filtered to election years **2019, 2022, and 2024**.

---

## 🧠 Model Architecture & Optimization
The final model uses a compact and refined feature set for maximum generalization on a small dataset.

### 🔧 Algorithm Optimization
- `max_depth = 3` to prevent overfitting.  
- Random Forest chosen for robustness with mixed-type variables.  
- Designed to learn only the most general and stable patterns.

### 📊 Key Input Variables
- **Votos_Anteriores** – Lagged vote percentage  
- **Governo** – 1 if the party was in Government; 0 if in Opposition  
- **Inflacao** – Annual inflation rate  
- **Desemprego** – Annual unemployment rate  
- **Abstencao** – Electoral abstention percentage  
- **Partido_Existia** – Binary flag for party existence in prior election  

---

## 🛠️ Getting Started

### ✔️ Requirements
Install Python and the following libraries:

```bash
pip install pandas scikit-learn
```

---

### ▶️ Running the Model

1. Clone the repository:

```bash
git clone https://github.com/pecoelho01/mini-ia-eleicoes-portugal.git
cd mini-ia-eleicoes-portugal
```

2. Add the data file **dados_eleicoes.csv**.

3. Run the main script:

```bash
python seu_script_principal.py
```

The model will automatically train on historical data and generate predictions for the 2025 scenario, including the MAE score.

---

## 📂 Data File Setup

You must include a file named **dados_eleicoes.csv** in the root directory.

### 📑 Required Column Structure

| Column Name | Description | Type |
|-------------|-------------|------|
| **Ano** | Election year | Numerical |
| **Distrito** | Lisbon or Porto | Categorical |
| **Partido** | Political party | Categorical |
| **%_Votos_Atuais (TARGET)** | Target variable | Numerical |
| **%_Votos_Anteriores (LAG)** | Previous election vote % | Numerical |
| **Governo (1) Oposição (0)** | 1 = Government, 0 = Opposition | Binary |
| **Inflacao_Anual** | Annual inflation rate | Numerical |
| **Desemprego_Anual** | Annual unemployment rate | Numerical |
| **Partido_Existia** | 1 = Party existed previously; 0 = New | Binary |
| **Abstencao** | Abstention rate | Numerical |

---

## ✍️ Contribution
Feel free to suggest improvements — especially new **feature engineering ideas** to reduce the MAE below **3.39%**.

