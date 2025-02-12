# 📊 Projeto: Cálculo de Métricas de Classificação com Machine Learning

## 🎯 Objetivo

Este projeto tem como objetivo calcular e visualizar as principais métricas utilizadas para avaliar modelos de classificação em Machine Learning. Utilizamos um modelo de Árvore de Decisão para classificar um conjunto de dados sintético e, em seguida, geramos métricas como:

✅ Acurácia

🔄 Sensibilidade (Recall)

🎯 Precisão

🎭 Especificidade

📈 F-score

## Além disso, o projeto gera gráficos 📊 para melhor interpretação dos resultados.

🚀 Tecnologias Utilizadas

Python 🐍

Pandas 📑

Matplotlib 📊

Seaborn 🎨

Scikit-learn 🤖


## 📷 Análise dos Gráficos

## 📌 Matriz de Confusão



A matriz de confusão mostra a quantidade de acertos e erros do modelo de classificação. Cada célula representa:

Verdadeiros Positivos (VP): Previsões corretas para a classe positiva.

Falsos Negativos (FN): Casos positivos que foram classificados erroneamente como negativos.

Falsos Positivos (FP): Casos negativos que foram classificados erroneamente como positivos.

Verdadeiros Negativos (VN): Previsões corretas para a classe negativa.

Quanto mais acertos houver nas diagonais principais, melhor o desempenho do modelo.

``` python
# Visualizar a matriz de confusão
tick_labels = ["Classe Negativa", "Classe Positiva"]
sns.heatmap(matriz_confusao, annot=True, fmt="d", cmap="Blues", xticklabels=tick_labels, yticklabels=tick_labels)
plt.xlabel("Previsto")
plt.ylabel("Real")
plt.title("Matriz de Confusão")
plt.show()
```

![Matriz Confusao](https://github.com/Rafae1040/metricas_avaliacao/blob/main/Matriz%20Confusao.png)


## 📌 Gráfico de Métricas


Este gráfico de barras exibe os valores das principais métricas do modelo:

Acurácia: Proporção total de previsões corretas.

Sensibilidade (Recall): Capacidade do modelo de identificar corretamente os casos positivos.

Precisão: Proporção de previsões positivas que realmente são positivas.

Especificidade: Capacidade do modelo de identificar corretamente os casos negativos.

F-score: Média harmônica entre precisão e sensibilidade.

Valores mais altos indicam um modelo mais eficiente e confiável.

``` python
# Gráfico de barras para as métricas
plt.figure(figsize=(8, 5))
sns.barplot(x=df_metricas.index, y=df_metricas["Valor"], palette="viridis")
plt.ylim(0, 1)
plt.ylabel("Valor")
plt.title("Métricas de Avaliação do Modelo")
plt.xticks(rotation=45)
plt.show()
```

![Metricas de Avaliacao do Modelo](https://github.com/Rafae1040/metricas_avaliacao/blob/main/Metricas%20de%20Avaliacao%20do%20Modelo.png)
