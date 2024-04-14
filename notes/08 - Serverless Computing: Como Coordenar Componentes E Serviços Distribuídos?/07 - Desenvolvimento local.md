# Desenvolvimento local

## Problema de desenvolver online
- Necessidade de estar conectado o tempo todo para testar
- O fluxo de upload em alguns serviços FaaS são muito manuais
    - Zipar o código e subir através de um input


### Serverless Framework
- Suporta AWS, Azure, Google Cloud, Knative, e mais
- Arquivos de definição YAML
- Simula utilizando containers o ambiente desejado em sua máquina
- Centro de utilidades para desenvolver para serverless localmente

### Dependências externas
- Existem bds, filas, streamings e outros componentes envolvidos na arquitetura
- Localtack
    - Um conjunto de containers, simulando serviços da AWS
- Serverless Dynamodb Local
- Serverless S3 Local
- ElasticMQ

> Homologue em um ambiente com os serviços reais

### Mockup
- Mockar outra API que está sendo desenvolvida localmente
- Geração de um container com o mock da API sendo desenvolvida e disponibilizado para outros devs usarem
