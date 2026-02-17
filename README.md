# 🧠 Employee Turnover Prediction

Projeto de Machine Learning para predição de rotatividade de funcionários (Employee Turnover) utilizando múltiplos algoritmos de classificação e técnicas de feature engineering.

O objetivo é prever se um funcionário irá deixar a empresa (`LeaveOrNot`) com base em características demográficas, profissionais e históricas.

---

## 📊 Dataset

Base de dados pública disponível no Kaggle:

https://www.kaggle.com/datasets/tawfikelmetwally/employee-dataset

O dataset contém informações sobre funcionários, incluindo:

| Variável | Descrição |
|----------|-----------|
Education | Nível educacional |
JoiningYear | Ano de ingresso |
City | Cidade de trabalho |
PaymentTier | Faixa salarial |
Age | Idade |
Gender | Gênero |
EverBenched | Já ficou sem projeto |
ExperienceInCurrentDomain | Experiência na área atual |
LeaveOrNot | Target (0 = Não saiu, 1 = Saiu) |

A base possui aproximadamente 4.600 registros e é utilizada para tarefas de classificação binária. :contentReference[oaicite:0]{index=0}  

---

## 🎯 Objetivo

Construir modelos preditivos capazes de identificar funcionários com maior risco de saída da empresa, auxiliando estratégias de retenção de talentos.

---

## ⚙️ Pipeline do Projeto

O fluxo de Machine Learning inclui:

1. Data Cleaning
2. Análise Exploratória (EDA)
3. Feature Engineering
4. Encoding de variáveis categóricas
5. Split treino/teste
6. Validação cruzada
7. Tratamento de desbalanceamento (SMOTE)
8. Treinamento de modelos
9. Avaliação comparativa
10. Interpretação dos resultados

---

## 🤖 Modelos Utilizados

Os seguintes algoritmos foram implementados:

- Logistic Regression
- Decision Tree Classifier
- SVC
- Random Forest Classifier
- AdaBoostClassifier
- GradientBoostingClassifier
- BaggingClassifier
- ExtraTreesClassifier
- XGBClassifier
- LGBMClassifier
- CatBoostClassifier
- 
Cada modelo foi avaliado em múltiplos cenários para garantir robustez dos resultados.

---

## 📈 Métricas de Avaliação

Foram utilizadas métricas adequadas para classificação desbalanceada:

- Balanced Accuracy
- F1-score
- Recall
- PR-AUC 

A métrica **Recall** foi priorizada.

---

## 🧪 Cenários Experimentais

Os modelos foram testados em diferentes condições:

- Dataset original
- Remoção de duplicados
- Balanceamento com SMOTE
- Feature Engineering avançada

---

## 🏆 Comparação de Modelos

| Modelo | Cenário | Balanced Accuracy | F1-Score | Recall | PR-AUC |
|--------|---------|------------------|----------|---------|--------|
Logistic Regression | L2 LBFGS - Keep Duplicates - Remove Features Scenario 2 | 0.77 | 0.7 | 0.68 | 0.82 |
SVC | Keep Duplicates - Remove Features Scenario 3 | 0.81 | 0.75 | 0.71 | 0.83 |
SVC | Keep Duplicates - Remove Features Scenario 2 - SMOTE | 0.80 | 0.74 | 0.74 | 0.83 |


---

## 🔍 Principais Insights Esperados

Algumas variáveis com forte influência na saída de funcionários:

- Funcionários que entraram recentemente na empresa têm mais chance de sair
- Funcionários do gênero Feminino tem mais chance de sair
- Funcionários em Pune ou Bangalore com Faixa Salarial 2 tem mais chance de sair
