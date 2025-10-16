[🇬🇧 For the English version, click here.](./README.md)

---

# Projeto 01: Modelo Preditivo de Churn de Clientes

## 🎯 Objetivo de Negócio
O objetivo deste projeto é construir um modelo preditivo de machine learning para identificar clientes com alto risco de cancelar o serviço (churn). Ao prever o churn com precisão, a empresa de telecomunicações pode engajar proativamente esses clientes com campanhas de retenção direcionadas, reduzindo a perda de receita.

## 📚 Bibliotecas e Conceitos Utilizados
-   **Bibliotecas:** `Pandas`, `Scikit-learn`
-   **Conceitos Principais:**
    -   **Fluxo de Trabalho de Machine Learning:** Um processo completo, de ponta a ponta, desde a preparação dos dados até a avaliação do modelo.
    -   **Problema de Classificação:** Previsão de um resultado binário (Churn vs. Não Churn).
    -   **Engenharia de Features:** Seleção e preparação das variáveis de entrada (`tenure`, `MonthlyCharges`).
    -   **Divisão em Treino e Teste:** `train_test_split` para garantir uma avaliação imparcial do modelo.
    -   **Treinamento do Modelo:** Uso da `Regressão Logística` como um modelo base.
    -   **Avaliação de Performance:** Análise de `Acurácia`, `Precisão`, `Recall` e da `Matriz de Confusão`.

## 📖 Descrição do Processo
O projeto seguiu o fluxo de trabalho padrão de machine learning:
1.  **Preparação dos Dados:** O dataset "Telco Customer Churn" foi carregado com Pandas. Os dados foram limpos, tratando valores não numéricos e ausentes, e a variável alvo ('Churn') foi convertida para um formato binário (0/1).
2.  **Divisão em Treino e Teste:** O dataset foi particionado em 80% para treino e 20% para teste, garantindo que o modelo pudesse ser validado em dados nunca vistos.
3.  **Treinamento do Modelo:** Um modelo de Regressão Logística foi inicializado e treinado nos dados de treino com o método `.fit()`.
4.  **Previsão:** O modelo treinado foi usado para fazer previsões no conjunto de teste.
5.  **Avaliação:** As previsões do modelo foram comparadas com os resultados reais do conjunto de teste. A análise focou não apenas na acurácia geral, mas criticamente na matriz de confusão para entender o impacto de negócio dos diferentes tipos de erros (especificamente os Falsos Negativos).

## 📊 Resultados e Insights
O modelo base de Regressão Logística atingiu uma **acurácia de ~78%**.

No entanto, o principal insight veio da **Matriz de Confusão**. O modelo apresentou um **recall baixo, de 43%**, para a classe de churn, o que significa que ele falhou em identificar 57% dos clientes que de fato cancelaram. Esses **Falsos Negativos** representam o custo mais significativo para o negócio, pois são oportunidades de retenção perdidas.

## 💡 Conclusão
Este projeto demonstra com sucesso todo o processo de construção e avaliação de um modelo preditivo. Embora o modelo base forneça um ponto de partida sólido, a análise conclui que ele é muito "conservador" para uma aplicação no mundo real.

**Próximos Passos:** Futuras iterações focariam em melhorar o recall do modelo através de:
-   Engenharia de features mais complexas.
-   Teste de algoritmos mais avançados (ex: Random Forest, Gradient Boosting).
-   Aplicação de técnicas para lidar com o desbalanceamento de classes.