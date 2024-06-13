# Explorando dados e preparando o treinamento

## Jupyter notebook

- Plataforma que une texto e código
- Visualização simplificada
- Execução por pedaços
    - Manipular os dados aos poucos

## R Studio

- Plataforma de análises estatísticas
- Simplifica o desenvolvimento estatístico
- Visualização gráfica simplificada
- Execução por pedaços
- Debugging
- Suporta R

## Preparação de dados

- Onde os cientistas de dados gastam mais tempo (60 + 19%)
- O trabalho mais pesado é fazer essa preparação
- Um dataset normalmente não está pronto para ser consumido (dados transacionais para uma base relacional, por exemplo)
- A maneira armazenada na aplicação não é a forma que é usada para realizar o treinamento
- Remoção de outlayers
- Regularização/Normalização de dados


## Feature engineering

- Manipulação dos dados para ficarem compatíveis com o consumo do modelo
- Uma feature pode ser criada
    - Criar um campo composto através dos dados pré-existentes no dataset
- Segregação de dados
    - Quanto de volume usar para treinar e quanto usar para validar o treinamento
    - Em média o volume de dados treinados é levamente maior do que o volume de dados validados
