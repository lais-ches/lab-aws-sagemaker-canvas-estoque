# 📊 Relatório de Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

### 1. Selecionar Dataset

-   Nessa etapa foi escolhido o dataset '**dataset-1000-com-preco-promocional-e-renovacao-estoque**' para treinar o modelo de previsão de estoque.

### 2. Construir/Treinar

-   Com o dataset importado, a coluna analisada foi a de quantidade de estoque, focando no ID dos produtos para identificar os itens.

### 3. Analisar

-   Após o treinamento, as métricas obtidas foram:

| Avg. wQL  | MAPE | WAPE  | RMSE | MASE |
| :---:  | :---:  | :---:  | :---:  | :---:  |
| 0.060  | 0.148  | 0.100  | 5.765  | 0.301  |

- As métricas MAPE e WAPE indicam que o modelo possui uma precisão boa a excelente, com erros percentuais médios de 14.8% e 10%, respectivamente.
- O RMSE de 5.765 mostra que o modelo possui um erro absoluto médio moderado.
- Já o MASE de 0.301 destaca que o modelo é mais eficiente do que um modelo de referência simples, mostrando uma boa capacidade preditiva.

### 4. Prever

- Nessa etapa, foi feita a predição entre os dias 08/02/2024 e 09/02/2024 para o item de id '**1003**'.

| P10  | P50 | P90  | 
| :---:  | :---:  | :---:  | 
| 44.529  | 48.299  | 55.986  | 

Para esse produto, o modelo prevê que:

- Há uma probabilidade de 10% de que a quantidade de estoque será menor que 44.529 unidades.
- A quantidade de estoque mediana é de 48.299 unidades.
- Há uma probabilidade de 10% de que a quantidade de estoque será maior que 55.986 unidades.

### 5. Conclusão

- Com a previsão indicando que o estoque do produto 1003 pode variar entre aproximadamente 44.529 e 55.986 unidades, pode ser planejados reabastecimentos para garantir que o estoque se mantenha dentro dessa faixa.
- A métrica RMSE pode ser usada para ajustar os níveis de segurança de estoque, garantindo que o estoque seja suficiente para atender à demanda prevista.
