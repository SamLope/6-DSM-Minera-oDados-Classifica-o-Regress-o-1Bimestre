🍷 Trabalho de Mineração de Dados — Seleção de Atributos
🧠 Descrição do Projeto

Este trabalho aplica técnicas de seleção de atributos em tarefas de classificação e regressão utilizando o Wine Quality Dataset.
O objetivo principal é explorar como diferentes métodos de feature selection impactam no desempenho e na interpretabilidade dos modelos de Machine Learning.

🎯 Objetivos

🔹 Classificação: prever a qualidade do vinho (binária: bom ou ruim)

🔹 Regressão: prever o valor do pH do vinho

🔹 Comparar 4 métodos de seleção de atributos

🔹 Analisar o trade-off entre performance e interpretabilidade

🔹 Avaliar ganhos em eficiência computacional

📊 Dataset

Fonte: UCI Machine Learning Repository — Wine Quality Dataset

🧪 Instâncias: 1.599 amostras de vinho tinto

⚙️ Atributos: 11 características físico-químicas

🎯 Targets:

quality_class → classificação binária

0 = qualidade < 7

1 = qualidade ≥ 7

pH → regressão (valor contínuo)

🧰 Tecnologias Utilizadas

Linguagem: Python 3.12+

Bibliotecas:

🧩 scikit-learn — Modelos e seleção de features

📊 pandas — Manipulação de dados

🔢 numpy — Computação numérica

🎨 matplotlib & seaborn — Visualizações

⚖️ imbalanced-learn — Balanceamento de classes (SMOTE)

⚗️ Métodos de Seleção Implementados
Método	Descrição	Tipo de Relação
1. SelectKBest (ANOVA F-value)	Seleção baseada em teste estatístico F	Linear
2. SelectKBest (Mutual Information)	Baseado em teoria da informação	Não-linear
3. RFE (Recursive Feature Elimination)	Eliminação recursiva com base na importância do modelo	Depende do modelo
4. Feature Importance (Random Forest)	Importância intrínseca de cada feature	Qualquer
🧹 Pré-Processamento
🔧 Limpeza

Remoção de 240 duplicatas

Verificação de valores nulos

🧪 Engenharia de Features

Criação do target binário para classificação

Normalização com StandardScaler

⚖️ Balanceamento

Aplicação de SMOTE para equilibrar classes

Melhorou a detecção de vinhos de alta qualidade

🧬 Metodologia Experimental
📂 Divisão dos Dados

70% treino / 30% teste

Estratificação para classificação

Validação cruzada: 5-fold

🤖 Modelos Base

Classificação: RandomForestClassifier

Regressão: RandomForestRegressor

📈 Métricas de Avaliação
Tarefa	Métricas
Classificação	Acurácia, Precision, Recall, F1-Score
Regressão	MSE, R²
🧾 Resultados Principais
🔹 Classificação
Método	Acurácia	Nº Features
Baseline	87.75%	11
Mutual Information	🥇 88.97%	5
Feature Importance	87.25%	5
ANOVA (F-Value)	87.25%	5
RFE	87.25%	5
🔹 Regressão
Método	R²	Nº Features
Baseline	98.81%	10
Feature Importance	🥇 99.46%	4
Mutual Information	98.92%	5
F-Regression (ANOVA)	62.57%	5
🔍 Insights e Análises
⭐ Features Mais Importantes
🧩 Classificação
Ranking	Feature	Importância
🥇	Álcool	17.6%
🥈	Sulfatos	13.0%
🥉	Acidez Volátil	10.9%
🧪 Regressão
Ranking	Feature
🥇	Acidez Fixa (99.8%)
🥈	Densidade
🥉	Álcool
⚙️ Eficiência Computacional

⏱️ Redução de 40% no tempo de treinamento

📉 Modelos mais simples

💡 Manutenção (ou melhoria) da performance

🧭 Conclusões
✅ Pontos Fortes

Manutenção da performance com menos atributos

Modelos mais interpretáveis

Ganhos expressivos em eficiência computacional

SMOTE balanceou efetivamente as classes

📚 Aprendizados

A seleção de atributos nem sempre melhora a acurácia, mas traz ganhos de interpretação e eficiência

Cada tipo de problema demanda um método diferente de seleção

O balanceamento é essencial em dados desbalanceados

A interpretabilidade é tão importante quanto o desempenho

👨‍💻 Autor

Nome: Samir Lopes Rosa
Disciplina: Mineração de Dados
Instituição: FATEC — Franca/SP

📚 Referências

UCI Machine Learning Repository — Wine Quality Dataset

Scikit-learn Documentation

IMB Learn — SMOTE Documentation