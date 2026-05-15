# MVP Machine Learning & Analytics

**Autor:** Thaygor Henrique Gonçalves  
**Data:** 28/09/2025  

---

## Objetivo
Este projeto aborda um problema de regressão aplicado à predição da taxa de material transportado (lb/s) a partir da corrente elétrica de um motor (A) em um transportador de grãos.

O estudo busca avaliar se a corrente elétrica pode ser utilizada como alternativa indireta para estimativa da taxa de material, utilizando os dados da balança como referência para validação.

Além da modelagem preditiva, também foi desenvolvida uma representação matemática baseada nas previsões do modelo, permitindo aproximar o comportamento observado de forma simplificada e interpretável.

---

## Metodologia

Foram avaliados diferentes modelos de regressão supervisionada, incluindo:

- DummyRegressor (baseline)
- Ridge
- RandomForest
- GradientBoosting
- LightGBM
- CatBoost

A etapa de modelagem contemplou:

- divisão dos dados em 90% treino/validação e 10% holdout
- otimização de hiperparâmetros com GridSearchCV;
- validação cruzada utilizando TimeSeriesSplit;
- avaliação utilizando MAE, RMSE e R².

Além da etapa de modelagem, também foram ajustadas funções saturantes locais e globais para construção de uma função híbrida baseada nas previsões do modelo selecionado.

---

## Estrutura do Notebook

O notebook está organizado a partir dos seguintes tópicos:

1. Escopo, objetivo e definição do problema  
2. Reprodutibilidade e ambiente  
3. Entendimento, carga e preparação inicial dos dados  
4. Definição do target, variáveis e divisão dos dados  
5. Pré-processamento e pipeline de transformação  
6. Baseline e modelos candidatos  
7. Validação, otimização e resultados  
8. Avaliação final e aproximação matemática do modelo  
9. Conclusão

---

## Arquivos do Repositório

- [mvp_machine_learning_and_analytics.ipynb](https://github.com/thaygorh/Machine-Learning-and-Analytics/blob/86f3e02d28bc57089c552d1197299c867385a86b/mvp_machine_learning_and_analytics.ipynb)  
Notebook com o código completo, desenvolvimento do MVP e resultados obtidos.

- [Grain-Handling-Conveyor-Operational-Data-tratados.csv](https://github.com/thaygorh/Machine-Learning-and-Analytics/blob/86f3e02d28bc57089c552d1197299c867385a86b/Grain-Handling-Conveyor-Operational-Data-tratados.csv)  
Dataset utilizado no treinamento e validação dos modelos.

- [best_model.pkl](https://github.com/thaygorh/Machine-Learning-and-Analytics/blob/86f3e02d28bc57089c552d1197299c867385a86b/best_model.pkl)  
 Artefato salvo do treinamento com validação cruzada, usado para evitar retreinamento a cada execução.

---

## Uso e autoria

Este projeto foi desenvolvido para fins de estudo e portfólio.

O código está disponível para fins educacionais e pode ser utilizado como referência.

Caso utilize este material, por favor, atribua o devido crédito ao autor original:

GitHub: https://github.com/thaygorh/Machine-Learning-and-Analytics

LinkedIn: https://www.linkedin.com/in/thaygorh
