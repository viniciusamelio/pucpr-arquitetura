# Baseada em eventos

- O processamento ocorre em função de reações do sistema a diferentes eventos
- Modelos "tradicionais" = request/response
- Forma distinta de descrever o comportamento
- Exemplo: Consulta de extrato
  - Normal: UI envia uma requisição de extrato para o serviço de extrato, que
    consulta a base e retorna
  - Eventos: UI publica um evento solicitando o extrato, serviço de extrato
    consome o evento e publica um segundo evento de extrato disponível. Um
    consumidor independente na UI consome este evento e exibe os dados

## Topologia

- É possível utilizar brokers de messageria
  - Sem coordenação centralizada dos eventos
  - Ex: RabbitMQ, ActiveMQ, SQS
- É possível utilizar um mediador

## Checklist para arquitetura baseada em eventos

- Iniciador
  - Quem tipicamente gera o evento inicial, que desencadeia uma série de outros
    eventos para execução de uma funcionalidade de negócio
- Processadores
  - Tomam decisões, fazem processamento e publicam um outro evento
- Eventos
  - Mensagens semânticas de acordo com o domínio do negócio

## Características: Broker

- Vantagens: Desacoplamento, escabalibilidade, responsividade, performance,
  tolerância a falhas
- Desvantagens: Falta de visão do fluxo, tratamento de erros, recuperação de
  erros, consistência

## Características: Mediador

- Componente orquestrador (Event mediator), agregando na arquitetura a
  visibilidade do fluxo
- Processamento assíncrono
- Recuperação de erros mais simples (Tanto broker quanto mediator)

- Vantagens: Controle do fluxo de procesamento, recuperação de erros, tratamento
  de erros, melhor consistência, tolerância a falhas
- Desvantagens: Acoplametno dos processadores de eventos, escalabilidade,
  performance, confiabilidade, modelagem de fluxos complexos

## Características gerais

- Implementação de watch dogs
- Implementação de estado para controle de fluxos excepcionais
- Modelo de broadcasting
- Alguns cenários podem exigir uma resposta no momento da requisição
  - Request-reply ou pseudo-síncrono
    - Filas de respostas

## Eventos x Tradicional

- Vantagens: Responsividade e performance, escalabilidade e elasticidade,
  agilidade para incorporar alterações, reação em tempo real
- Pontos negativos: Consistência eventual, controle de fluxo de processamento,
  fluxos de processamento podem cair em cenários indeterminados, mais difícil de
  serem testados

## Ratings

| Característica          | Rating            |
| ----------------------- | ----------------- |
| Tipo de particionamento | Técnico           |
| Unidades de implantação | 1 por processador |
| Deployability           | 3                 |
| Elasticidade            | 3                 |
| Evolução                | 5                 |
| Tolerância a falhas     | 5                 |
| Modularidade            | 4                 |
| Custo                   | 3                 |
| Performance             | 5                 |
| Confiabilidade          | 3                 |
| Escalabilidade          | 5                 |
| Simplicidade            | 1                 |
| Testabilidade           | 2                 |
