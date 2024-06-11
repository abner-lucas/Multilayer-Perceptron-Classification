# Rede Perceptron Multicamadas

Este projeto tem como objetivo apresentar um estudo teórico/prático das Redes Neurais Perceptron Multicamadas (RNPM) através de simulações sobre os datasets [Skin Segmentation](https://archive.ics.uci.edu/ml/datasets/Skin+Segmentation) e [Breast Cancer](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)), ambos com saída de variável de classe binária (0 ou 1). Utilizamos duas arquiteturas de RNPM: redes de 3 camadas (entrada, oculta e saída) e 4 camadas (entrada, duas ocultas e saída) treinadas usando backpropagation, visando aferir a acurácia com variações nos parâmetros de treinamento.

Para as simulações nos datasets citados foram utilizadas duas arquiteturas de RNPM, com redes de 3 camadas (camada de entrada, uma camada oculta e camada de saída) e 4 camadas (com duas camadas ocultas) treinadas usando o algoritmo de retropropagação (backpropagation), com o intuito de aferir a acurácia (com a normalização da saída de cada rede efetivada através do ponto médio entre 0 e 1) do sistema proposto, com variações nos parâmetros de treinamento: número de neurônios na(s) camada(s) oculta(s) e taxa(s) de aprendizado e porcentagem de treinamento (para hold out).

## Simulações
Para o dataset Breast Cancer foi utilizado somente para verificação das implementações dos modelos, enquanto que, para o dataset Skin Segmentation, foram analisados 4 casos:
1. Classificação com a técnica de amostragem hold out no modelo 3C.
2. Classificação com a técnica de amostragem k-fold cross validation no modelo 3C.
3. Classificação com a técnica de amostragem hold out no modelo 4C.
4. Classificação com a técnica de amostragem k-fold cross validation no modelo 4C.

Em todas as simulações, utilizou-se como critério de parada do treinamento 60000 épocas ou um erro aceitável de 10^-5, estimado com o método Erro Médio Quadrático (EMQ), sob a função de ativação dos neurônios Sigmoid em todas as camadas com pesos iniciados com valores aleatórios entre -0.1 e 0.1, fazendo uso de um limiar de ativação (novo neurônio) de valor 1.0 da camada de entrada até a última camada oculta.

Para que os modelos fossem capazes de gerar resultados satisfatórios com as combinações de valores dos parâmetros dinâmicos apresentados, os datasets tiveram que ser normalizados e/ou balanceados e/ou ter seus registros e/ou features filtrados. Para as redes de três camadas, o conjunto de valores de neurônios da camada oculta foi {4, 16} combinado às taxas de aprendizado {0.9, 0.65, 0.3} usando o mesmo valor entre as camadas. Para as redes de quatro camadas, o conjunto de valores de neurônios da 1ª camada oculta foi {4, 16} combinado ao mesmo conjunto de valores de neurônios para a 2ª camada oculta, ainda, combinado às taxas de aprendizado {0.9, 0.3} (usando sempre o mesmo valor na primeira e última conexão de camadas – entrada/oculta_1 e oculta_2/saída).

## Resultados
Os resultados mostraram que a rede de 4 camadas com duas camadas ocultas apresentou melhor desempenho no dataset Skin Segmentation, especialmente quando utilizada a técnica de k-fold cross validation. A acurácia média foi superior em comparação com a rede de 3 camadas, demonstrando a eficácia de adicionar uma camada oculta adicional. Para o dataset Breast Cancer, a rede de 3 camadas foi suficiente para validar a implementação, apresentando resultados consistentes com a literatura.

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
