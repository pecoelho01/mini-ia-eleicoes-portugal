# 🇵🇹 Mini AI: Portuguese Legislative Elections Predictor 📊

Este projeto implementa um modelo simples de **Machine Learning** para prever a **percentagem de votos dos principais partidos políticos** nas Eleições Legislativas Portuguesas, com foco nos distritos de **Lisboa** e **Porto**.  
O modelo utiliza um **Random Forest Regressor** otimizado para analisar tendências históricas e fatores macroeconómicos relevantes.

## Overview
- Objetivo: Prever a percentagem de votos para **PS**, **AD/PSD** e **CH**.
- Modelo Base: Random Forest Regressor otimizado.
- Feature mais importante: `%_Votos_Anteriores`.
- Performance: **MAE = 3.18%**.
- Dados: anos **2019, 2022 e 2024**.

## Model Architecture & Optimization
### Otimização
- `max_depth = 3` para evitar overfitting.
- Random Forest pela robustez.

### Variáveis Principais
- Votos_Anteriores
- Governo
- Inflacao
- Desemprego
- Abstencao
- Partido_Existia

## Getting Started
### Instalar dependências
```
pip install pandas scikit-learn
```

### Executar
```
git clone https://github.com/pecoelho01/mini-ia-eleicoes-portugal.git
cd mini-ia-eleicoes-portugal
python seu_script_principal.py
```

## Data File Setup
É necessário um ficheiro `dados_eleicoes.csv`.

### Estrutura das Colunas
(Ano, Distrito, Partido, %_Votos_Atuais, %_Votos_Anteriores, Governo, Inflacao_Anual, Desemprego_Anual, Partido_Existia, Abstencao)

## Contribuições
Melhorias são bem-vindas para tentar baixar o MAE < 3.18%.

## License
Especificar licença aqui.
