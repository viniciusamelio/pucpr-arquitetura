# Construindo um modelo de ML

## Dados e lake

- Toda operação de negócio gera dados
    - Dados do cliente, interações do cliente, localização, como o produto é consumido, etc
- Todos esses dados ajudam na composição de um data lake

### Passos para começar a implementar um lakehouse

- Um datalake deve armazenar tais dados
- Deve haver uma catalogação de dados
- Governança dos dados
    - Compliance com GDPR, LGPD e afins

## Construção do modelo

- CRISP DM
    - Padrão de consumo de dados para resolução de problema de negócio
        - 6/7 passos tradicionais:
            - Business Understanding
            - Data understand
            - Data preparation
            - Modeling
            - Evaluation
            - Deployment
    - Iterativo

- Feature engineering
    - Entender quais os dados mais importantes para chegar na inferência com sucesso
- Preparação dos dados
    - Normalização de acordo com o modelo escolhido para treinamento
- Segregação de dados
    - Cortar parte do dataset para treinar do modelo e outra metade para avaliar se a inferência está acertando de acordo com os dados usados para alimentação
- Treinamento
- Avaliação
- Deploy
- Consumo

## Principais fases de construção

### Exploração dos dados
- Preparação, feature engineering e modelagem dos dados

### Treino
- Corte do dataset em recortes para inferência e treinamento

### Consumo
- Deploy
- Tunning


## Consumindo
O Consumo pode ser feito de algumas formas, mas normalmente em batch, real-time ou edge.

### Batch
- Larga escala de dados (normalmente usado em jobs)

### Realtime
- Respostas no momento requisitado

### Edge
- Uso do modelo o mais próximo do cliente quanto for possível
- IA num celular
    - Reconhecimento facial, por exemplo.