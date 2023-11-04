# Modelos de arquitetura de dados moderna

## O que é uma arquitetura de dados?
- Conjunto integrado de artefatos de especificação utilizado para definir os requisitos de dados

**Não existe modelo certo ou errado**

## Dois principais modelos
- Lambda
    - 2 canais de captura de dados
    - 1 Canal stream, processamento online, recebe dados de algum sistema ou fonte, de maneira fonte
    - 1 Canal batch, processa de dados de volume maior ou dados baseados numa história, bases relacionais, dados de sistemas
    - Processamentos dependem da necessidad de negócio
- Kappa
    - 1 Canal de ingestão de dados somente, apenas Stream
    - Formatada em eventos

### Lambda
- Batch e speed layers
- O pós processamento depende do negócio

### Kappa
- Muito utilizada em situações onde preciso fazer o processamento da informação em tempo real
- Não existe de fato um "real time", apenas um "near real time"
- Está dentro da arquitetura Lambda
- Menos empregada que a Lambda

## Outras variações
- Modern DW
    - Entreprise DW
    - Modernizar o conceito de DW, de forma mais escalável
- DataLake House
    - Resolvo todas as necessidades de processamento de dados somente com tecnologias de big data
- Data Mesh

### Modern DW
- Camada de ingestão é similar a Lambda
- Dados armazenados num data lake
- Plataforma de big data para processamento dos dados de maneira robusta
    - Com spark, por exemplo, para preparar os dados de maneira otimizada
- Continuo trabalhando com uma plataforma de DW para modelar o consumo dos dados
    - Tunning melhor
    - Melhores camadas de segurança
- Extrai o melhor dos dois mundos
- Datalake fica apartado, desacoplado

### Lake House
- Projeto delta, visa o datalake armazenar metadados desde o seu processamento
    - Estado inicial, transformações aplicadas no dado, etc
- Abstrai a camada de DW

### Data mesh
- Baseada em service mesh
    - Conceitos de microservices
    - Alinhado a distribuição de funções
- Visa criar os domínios dos dados
- Cada domínio tem suas próprias inteligências para consumo dos dados
- Data infra as a platform
    - Organização de uma plataforma centralizada que entrega:
        - Armazenamento
        - Pipelines de transformação
- Funciona bem para empresas grandes com dptos independentes
- Catálogo de dados
- Governança
