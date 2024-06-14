# Treinamento e otimização (Tunning)

## Algoritmos

- No ML temos a máquina "aprendendo" através de um alto volume de dados
- Cada área tem suas especificações
    - Regressão linear, logística, object detection, etc
    - Uma vez preparado os dados o treinamento se inicia
- Model fit
    - Início do treinamento
- Underfitting
    - Possui dados para ser melhor mas não performa como esperado
    - Percepção dos dados longe da realidade
- Overfitting
    - Quando treino o modelo que ele fica tão bom que ele só oferece o problema dos dados oferecidos a ele
    - Muito bom para aqueles dados especificamente
    - Percepção apurada somente para a realidade dos dados inputados
- Balanceamento

## Hiperparâmetros

- Configs de variação para treinamento do modelo
- Cada vez que alterados os hiperparâmetros existe uma tendência de obtenção de resultados diferentes no treinamento


## Model tunning

- Otimização de hiperparâmetros (HPO)
- Métrica de validação (mAP)
    - Precisão média do modelo


### Técnicas

- Grid
    - Testa todas as possibilidades em divisões simétricas
- Random
    - Valores escolhidos de maneira randômica
- Teorema Bayesiano
    - Orientado pela acurácia de tentativas, concentrando as tentativas com parâmetros próximos da maior acurácia
    - Funcionalidade padrão da maioria das ferramentas
