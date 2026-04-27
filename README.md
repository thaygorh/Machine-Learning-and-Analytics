# MVP: Machine Learning & Analytics - Predição de Fluxo de Massa a partir da Corrente de um Motor  

**Autor:** Thaygor Henrique Gonçalves  
**Data:** 28/09/2025  

---

## Objetivo
MVP desenvolvido na disciplina **Machine Learning & Analytics**, com o propósito de avaliar a viabilidade de prever o fluxo de massa (t/h) a partir da corrente elétrica de um motor (A), utilizando os dados de uma balança como referência.  

---

## Metodologia
- Problema formulado como **regressão supervisionada**.  
- Divisão dos dados em **90% treino/validação** e **10% holdout**.  
- Modelos avaliados: DummyRegressor (baseline), Ridge, RandomForest, GradientBoosting, LightGBM e CatBoost.  
- Otimização de hiperparâmetros com **GridSearchCV** e validação cruzada temporal (**TimeSeriesSplit**).  
- Métricas: **MAE, RMSE e R²**.  
- Melhor desempenho obtido com **CatBoost**.  
- A partir das predições do modelo, foi construída uma **função saturante híbrida**, fornecendo uma alternativa matemática e interpretável para a relação entre corrente e fluxo de massa.  

---

## Arquivos do Repositório
- **`predicao_fluxo_motor_vfinal.ipynb`** → Notebook com o código completo, desenvolvimento do MVP e resultados obtidos.  
- **`MVP_MLA_dados_tratados2.csv`** → Dataset com corrente do motor (A) e taxa da balança (t/h).  
- **`best_model.pkl`** → Artefato salvo do treinamento com validação cruzada, usado para evitar retreinamento a cada execução. 
- **`Funcao_Saturante_Hibrida_MVP.xlsx`** → Validação prática da função híbrida no Excel, aplicada sobre os dados reais de corrente e comparada com a taxa da balança em forma de gráfico.  
