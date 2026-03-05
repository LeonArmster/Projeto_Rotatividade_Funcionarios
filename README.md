# Projeto_Rotatividade_Funcionarios
# Employee Attrition Prediction

## Modelo Preditivo de Rotatividade de Funcionários

------------------------------------------------------------------------

## 1. Visão Executiva

Este projeto implementa um pipeline completo de Machine Learning para
previsão de rotatividade de funcionários (Employee Attrition),
utilizando técnicas de pré-processamento, balanceamento de classes,
comparação de algoritmos e otimização de hiperparâmetros.

O objetivo estratégico é permitir que a área de Recursos Humanos
identifique, de forma antecipada, colaboradores com maior probabilidade
de desligamento.

------------------------------------------------------------------------

## 2. Problema de Negócio

Alta rotatividade impacta diretamente:

-   Custos de recrutamento e onboarding
-   Perda de conhecimento organizacional
-   Performance operacional
-   Clima organizacional

Problema resolvido:

> Dado o histórico comportamental e profissional dos funcionários,
> prever se um colaborador irá deixar a empresa.

------------------------------------------------------------------------

## 3. Objetivo Analítico

Modelo supervisionado de classificação binária:

-   0 → Stayed (Permaneceu)
-   1 → Left (Saiu)

Variável alvo:

    Situacao

------------------------------------------------------------------------

## 4. Arquitetura Analítica

Fluxo do projeto:

Ingestão de Dados\
↓\
Análise Exploratória\
↓\
Tratamento de Inconsistências\
↓\
Feature Engineering\
↓\
Encoding\
↓\
Balanceamento\
↓\
Normalização\
↓\
Treinamento\
↓\
Otimização\
↓\
Persistência\
↓\
Simulação de Produção

------------------------------------------------------------------------

## 5. Pré-Processamento

Principais etapas:

-   Remoção de colunas inconsistentes
-   Imputação da mediana em Salario_Mensal
-   Criação de Faixa_Salarial
-   Encoding (Ordinal + OneHot)
-   Balanceamento com RandomUnderSampler
-   Separação treino/teste (70/30)
-   Normalização com MinMaxScaler

------------------------------------------------------------------------

## 6. Modelos Avaliados

-   KNN
-   SVM
-   Random Forest

O modelo selecionado foi o **Random Forest**, após otimização com
GridSearchCV.

Configuração final:

    RandomForestClassifier(
        criterion="entropy",
        max_depth=20,
        max_features="log2",
        min_samples_leaf=2,
        min_samples_split=2,
        n_estimators=300
    )

------------------------------------------------------------------------

## 7. Métrica Utilizada

-   Accuracy

Recomendação futura: incluir Recall, F1-Score e ROC-AUC.

------------------------------------------------------------------------

## 8. Persistência do Modelo

O modelo treinado é salvo via:

    joblib.dump()

Arquivo gerado:

    modelo_treinado_rotatividade_funcionarios.pk

------------------------------------------------------------------------

## 9. Stack Tecnológica

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Scikit-Learn
-   Imbalanced-Learn
-   Joblib

------------------------------------------------------------------------

## 10. Roadmap de Evolução

-   Implementar Pipeline do Scikit-Learn
-   Utilizar SMOTE
-   Criar API com FastAPI
-   Containerização com Docker
-   Monitoramento de Data Drift
-   Versionamento com MLflow

------------------------------------------------------------------------

## Conclusão

O projeto tem como objetivo, demonstrar domínio do ciclo completo de Machine Learning, desde
entendimento do problema até persistência e simulação de produção.
