# Arquiteturas referência

## Website
- Auth
    - Cognito
- Conteúdo estático
    - S3
- API´s de conteúdo dinâmico
    - DynamoDB
    - Lambda
    - API Gateway


## Autorizador customizado
- Autorização
    - Lambda

## Transformação de mídias
- Lambdas para tratar as imagens

## Envio massivo de mensagens
- CSV -> S3 -> Lambda -> SES

## Transformação de dados em tempo real
EC2 -> Streaming de dados
        [->Consumer 

## Cloud job / Cron job
- Executar determinadas funções a cada quantidade x de tempo

## Slack
- CloudWatch->SNS->Lambda->Slack

## IoT
- Gateway -> Lambda -> Dynamo

- IoT device -> Backend -> Lambda -> Dynamo