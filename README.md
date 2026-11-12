# coronary_monorepo

# Predição de Doença Coronariana e Desfecho Clínico: Abordagem Híbrida (Estatística Clínica & Machine Learning)

Este repositório contém o pipeline analítico desenvolvido para investigação de fatores de risco cardiovascular e predição de desfecho clínico (presença de estenose coronariana significativa / risco de evento agudo), integrando **estatística inferencial tradicional**, **métricas de acurácia diagnóstica** e **aprendizado de máquina interpretável**.

## 📊 Base de Dados
- **Fonte:** Heart Attack Analysis & Prediction Dataset (UCI Cleveland / Kaggle).
- **Amostra:** $N = 303$ pacientes, 13 variáveis preditoras clínicas/eletrocardiográficas e 1 desfecho binário (`output`).

## 🔬 Metodologia Estatística & Computacional
1. **Estatística Inferencial (Tabela 1):** Testes de normalidade (Shapiro-Wilk), comparação entre grupos (Teste $t$ de Student / Mann-Whitney U para contínuas; $\chi^2$ de Pearson / Exato de Fisher para categóricas) e Regressão Logística Multivariada para extração de *Odds Ratios* ajustados (IC 95%).
2. **Modelagem Preditiva:** Validação cruzada estratificada ($k=10$) comparando Regressão Logística Penalizada (L2), Random Forest, XGBoost e LightGBM.
3. **Avaliação Clínica:** Discriminação (AUROC, AUPRC), Calibração (Brier Score e Curva de Calibração), Métricas Diagnósticas no ponto ótimo de Youden (Sensibilidade, Especificidade, VPP, VPN, Razões de Verossimilhança) e Análise de Curva de Decisão (*Decision Curve Analysis* - Net Benefit).
4. **Explicabilidade:** Valores SHAP (*SHapley Additive exPlanations*).

## 🚀 Execução no Google Colab
1. Faça upload do arquivo `heart.csv` quando solicitado pelo script (ou monte seu Google Drive).
2. Execute todas as células.
3. Ao final, o arquivo `resultados_analise_coronariana.zip` será baixado automaticamente para sua máquina local contendo todas as tabelas e gráficos (300 DPI).
