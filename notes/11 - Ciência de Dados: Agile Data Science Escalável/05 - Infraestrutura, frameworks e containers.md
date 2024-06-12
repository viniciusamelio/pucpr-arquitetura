# Infraestrutura, frameworks e containers 

## Infra

- Poder de uso computacional vem alavancando cada vez mais o uso de IA
- Era um limitados em décadas anteriores, devido a necessidade de consumo em larga escala de dados
- Memória cache, velocidade de transferência, espaço em disco e principalmente CPU são muito exigidos tanto para treinamento quanto consumo de modelos
    - CPU, GPU e TPU

### Processamento

- Algoritmos de menor requisito conseguem lidar com modelos tabulares e redes neurais simplificadas sem muita necessidade de CPU
- Quanto maior a volumetria de dados para o treinamento, maior o requerimento de hardware, especialmente GPU
    - Deep Learning, visão computacional e redes neurais mais complexas necessitam de um processamento mais específico

- TPU também é utilizada em algoritmos mais complexos como DL, visão computacional e etc. Porém também processam tensores.
- A unidade de processamento está cada vez mais se especializando de acordo com a necessidade de treinamento de modelos
    - Criação de placas de vídeo específicas para treinamento e consumo de modelos

#### FPGA

- Processadores específicos para hardwares menores para consumo na borda (edge)
    - Previsões de um smart watch, reconhecimento de pessoas em fotos, carros autônomos


## Frameworks

Camada de software se especializando para atender a demanda de IA.

- Tensorflow
- Pytorch
- MXNet

### Ferramentas

- Gluon
- Keras
- Sekit Learn
- Deep Graph Library

## Containers

Também adotados pela camada de ML.

### Benefícios

Melhores práticas que também vemos no desenvolvimento de software, como:

- Isolamento
- Continuidade de desenvolvimento
- Versionamento
- Setup de ambiente e dependências
- Treinamento em escala reduzida durante o período de desenvolvimento