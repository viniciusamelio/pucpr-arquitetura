# Arquitetura orientada a eventos

- Um evento é baseado num acontecimento e sempre no passado
  - Ex: "order_finished"
  - Muito comum (e errado) eventos estarem no futuro
- Descreve um evento de negócio
- Eventos de negócios possibilitam a atualização quase em tempo real de um Dashboard

## Componentes de um EDA

### Pub/Sub
- Produtor: Quem produz o evento
  - Pode ser através de código, manual
  - Pode ser automatizado, através de providers, por exemplo

- Consumidor: Quem consome e reage ao evento
  - Sistemas/módulos satélites

- Canal: Por onde o evento trafega
  - Mecanismo de pub/sub ou streaming

- Evento: Mensagem enviada

### Streaming de dados
- Um único canal, onde todos os produtores fazem a publicação dos eventos e os consumidores reagem apenas aos que lhe interessarem
- Consumidor passa a ter a capacidade de busca através de um determinado offset
- Possibilidade de replay
- Conceito de particionamento
  - Partição primária e secundária
    - Pode causar problemas durante o scale-in
- Ex: Kafka

## Usecases
- Integração entre sistemas
- Mudança de estado
- Dashboards
- Escalabilidade e desacoplamento
- Data lakes
- IoT

## Erros comuns
- Tamanho do evento enviado
  - Não apenas em quesito de armazenamento, mas sim com a quantidade de dados vazados do domínio
- Excesso de eventos
  - Geram um alto consumo de infra
- Falta de estratégias de retries
  - Ausência de uma DLQ (Dead Letter Queue)
- Falta de idempotência
- Evento genérico demais
  - Ex: Pedido alterado (o que foi alterado?)
- Eventos não baseados em eventos de negócio
  - Eventos de infra encaminhados pelo mesmo canal/fluxo de tratamento de domínio
- Falta de observabilidade
- Orquestração e coreografia
  - Focar somente em orquestração, isso cria um ponto único de falha, com um componente sabendo tudo sobre os eventos, quase a criação de um workflow