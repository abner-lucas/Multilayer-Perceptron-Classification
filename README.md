# Rede Perceptron Multicamadas

Este projeto tem como objetivo apresentar um estudo teórico/prático das Redes Neurais Perceptron Multicamadas (RNPM) através de simulações sobre os datasets [Skin Segmentation](https://archive.ics.uci.edu/ml/datasets/Skin+Segmentation) e [Breast Cancer](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)), ambos com saída de variável de classe binária (0 ou 1). Utilizamos redes com 3 camadas (entrada, oculta e saída) e 4 camadas (entrada, duas ocultas e saída) treinadas usando backpropagation para avaliar a acurácia com variações nos parâmetros de treinamento.

## Simulações
Para o dataset Breast Cancer, utilizamos apenas para verificação dos modelos. No dataset Skin Segmentation, analisamos quatro casos:

1. Classificação com amostragem hold out no modelo 3C.
2. Classificação com k-fold cross validation no modelo 3C.
3. Classificação com amostragem hold out no modelo 4C.
4. Classificação com k-fold cross validation no modelo 4C.

Critério de parada: 60000 épocas ou erro de 10^-5, utilizando Erro Médio Quadrático (EMQ). Função de ativação Sigmoid, pesos iniciais entre -0.1 e 0.1, e limiar de ativação 1.0.

## Resultados
Os resultados mostraram que a rede de 4 camadas apresentou melhor desempenho no dataset Skin Segmentation, especialmente com k-fold cross validation. A rede de 3 camadas foi suficiente para validar a implementação no dataset Breast Cancer.

## Funcionalidades
- Implementação de Redes Perceptron com 3 e 4 camadas.
- Carregamento e manipulação de dados de entrada.
- Visualização dos resultados obtidos.

## Uso
Para executar o algoritmo, utilize os notebooks:
- `mlp_breast_cancer.ipynb`: Implementação da MLP para o conjunto de dados Breast Cancer.
- `mlp_skin_segmentation.ipynb`: Implementação da MLP para o conjunto de dados Skin Segmentation.

## Estrutura do Projeto
- `dataset/`: Conjuntos de dados utilizados
- `resultados/`: Resultados das execuções do algoritmo
- `mlp_breast_cancer.ipynb`: Notebook para Breast Cancer
- `mlp_skin_segmentation.ipynb`: Notebook para Skin Segmentation

## Requisitos
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn`
- `imblearn`
- `tensorflow`
- `keras`
- `warnings`
- `random`
- `csv`

## Autor
- [@abner-lucas](https://github.com/abner-lucas)
  
## Licença
Este projeto está licenciado sob a licença MIT. Veja o arquivo [MIT](https://choosealicense.com/licenses/mit/) para mais detalhes.
