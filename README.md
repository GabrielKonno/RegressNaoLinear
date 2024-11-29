# Análise de Preços de Imóveis - Regressão Não Linear

Comparação de modelos não lineares (Random Forest, AdaBoost, Gradient Boosting) para previsão de preços de imóveis.

## Modelos Implementados

### Random Forest
```python
rf = RandomForestRegressor(n_estimators=1000, random_state=42)
```
- 1000 árvores de decisão
- Visualização de árvores individuais via pydot

### AdaBoost
```python
ada = AdaBoostRegressor(n_estimators=100)
```
- 100 estimadores
- Boosting adaptativo

### Gradient Boosting
```python
grb = GradientBoostingRegressor(n_estimators=100)
```
- 100 estimadores
- Otimização por gradiente

## Pré-processamento
```python
# Codificação one-hot
df = pd.get_dummies(df)
# Remoção de valores nulos
df.dropna(inplace=True)
```

## Avaliação
Métricas para cada modelo:
- R² (Coeficiente de Determinação)
- MAE (Erro Médio Absoluto)
- MSE (Erro Quadrático Médio)
- RMSE (Raiz do Erro Quadrático Médio)

## Requisitos
```bash
pip install pandas numpy matplotlib seaborn scikit-learn pydot
```

## Estrutura
- `regressãonãolinear.py`: Script principal
- `house.xlsx`: Dataset de imóveis
- `tree.png`: Visualização de árvore de decisão

## Uso
```bash
python regressãonãolinear.py
```

## Visualizações
- Árvores de decisão individuais
- Análise exploratória de dados
- Estatísticas descritivas

## Diferenciais
- Comparação de três algoritmos diferentes
- Visualização de árvores do Random Forest
- Tratamento automático de variáveis categóricas
