# Análise e Detecção de Transações Fraudulentas com Machine Learning

## Descrição

Este projeto tem como objetivo construir um modelo de Machine Learning para identificar transações fraudulentas em um conjunto de dados de transações bancárias. Através de diversas análises e modelagem, conseguimos prever se uma transação é fraudulenta com base em variáveis como distância da última transação, preço de compra, uso de chip e PIN, entre outras.

### Tecnologias Utilizadas

- **Python**
- **Pandas**: Para manipulação e análise de dados
- **Scikit-Learn**: Para criação e treinamento do modelo de Machine Learning
- **Seaborn e Matplotlib**: Para visualização de dados
- **Random Forest Classifier**: Algoritmo de aprendizado supervisionado utilizado para detecção de fraudes
- **Pickle**: Para salvar o modelo treinado

## Estrutura do Projeto

### 1. Introdução

O objetivo principal deste projeto é utilizar uma base de dados para prever se uma transação bancária é fraudulenta. Com base em várias variáveis coletadas de transações anteriores, como distância da última transação e uso de PIN, podemos treinar um modelo de Machine Learning para classificar transações.

### 2. Análise Descritiva dos Dados

- **Coleta de Dados**: O conjunto de dados foi carregado a partir de um arquivo CSV.
- **Análise Inicial**: Realizamos uma análise inicial do conjunto de dados, verificando a existência de valores nulos e realizando algumas estatísticas descritivas.
- **Visualização de Dados**: Utilizamos gráficos para analisar a correlação entre as variáveis e identificar padrões que indicam transações fraudulentas.

### 3. Modelagem de Dados

1. **Pré-processamento**: O conjunto de dados foi dividido em variáveis independentes (X) e dependentes (Y). A variável dependente (`fraud`) indica se uma transação é fraudulenta ou não.
2. **Seleção de Features**: Selecionamos as 3 principais variáveis mais importantes com base no teste de qui-quadrado (chi2).
3. **Treinamento do Modelo**: Utilizamos o algoritmo Random Forest Classifier para treinar o modelo, com a divisão dos dados em conjuntos de treino e teste.
4. **Avaliação do Modelo**: O modelo obteve uma acurácia de 100% e uma precisão de 100% em relação às transações fraudulentas.

### 4. Melhoria do Modelo

Após treinar o modelo inicial, decidimos reduzir o número de variáveis para testar se a precisão seria afetada. O modelo final com 4 variáveis obteve uma precisão de 98.6%, mostrando que, embora a redução de variáveis possa diminuir a precisão, a diferença não é tão significativa.

### 5. Salvamento do Modelo

O modelo final foi salvo em um arquivo `.sav` para ser utilizado em implementações futuras, como APIs ou sistemas de produção.

## Resultados

O modelo treinado foi capaz de classificar com alta precisão se uma transação era fraudulenta ou não. A acurácia e a precisão de 100% indicam que o modelo tem um desempenho excelente, mas podemos explorar mais técnicas de redução de dimensionalidade para verificar se é possível melhorar ainda mais.

## Instruções de Uso

1. **Instalação das Dependências**:
    - Certifique-se de ter o Python 3.x instalado.
    - Instale as bibliotecas necessárias com o comando:
    ```bash
    pip install -r requirements.txt
    ```

2. **Rodando o Modelo**:
    - Execute o código no Jupyter Notebook ou no seu ambiente Python preferido.
    - O modelo pode ser carregado e utilizado para prever novas transações fraudulentas a partir de dados similares.

3. **Carregando o Modelo Treinado**:
    - Para carregar o modelo treinado e utilizá-lo em novos dados, execute:
    ```python
    import pickle
    model = pickle.load(open('randomforestclassifier.sav', 'rb'))
    ```

## Conclusão

Este projeto demonstrou a eficácia do uso de Machine Learning para detectar transações fraudulentas com alta precisão. Embora a redução de variáveis tenha reduzido ligeiramente a precisão, o modelo final ainda fornece resultados sólidos. O modelo pode ser aprimorado com mais dados e técnicas de processamento de variáveis.

---

**Autor**: Paulo Roberto
**Data**: Dezembro de 2024  
