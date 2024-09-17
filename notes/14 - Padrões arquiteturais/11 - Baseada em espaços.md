# Baseada em espaços

- Utiliza caches para desempenhar de forma superior
- Proposta a partir de soluções que tenham uma demanda altíssima de
  processamento simultâneo
- Cache que recebes tuplas de dados
- Todas as camadas operam em cima do cache ao invés da persistência (DB)
- DataPumps e DataWriters
- Elemento que faz uma carga inicial dos dados
- Processador de dados: Análogo a um microsserviço
- Justificativa: Banco de dados resulta em gargalo de performance

## Como implementar (Componentes necessários)

- Ferramentas de cache
  - Redis, MainCache, etc
- Middleware
  - Roteamento de mensagens para comunicação entre componentes
- Datagrid
  - Replica os dados entre instâncias do cache
- Componente de orquestrações das requests
- DataPumps
  - "Bombeia" os dados gerados pelos fluxos transacionais
- DataWriters
  - Faz a persistência

> Tudo resolvido em memória

## Características

- Fluxo de atualização
  - Atualização no cache -> Publicação de evento de atualização -> Consumo do
    evento-> Atualização na base de dados
- Delay entre replica de dados entre os caches
  - Pode ser mitigado com uso do Redis, por exemplo
- Carga inicial do cache
  - Em clusters já operantes a cópia é adquirida por nodes ativos
  - Para operações de cargas frias a implementação típica é através do disparo
    de um evento que inicia a alimentação do cache
- Sistemas 24/7

## Quando utilizar

- Baixa latência
- Baixa latência + Alto volume simultâneo

## Cuidados

- Base de dados, normalmente, precisará ser utilizada somente pelos mecanismos
  de cache
- Se houver o uso de transactions a arquitetura pode estar sendo utilizada de
  forma errada

## Ratings

| Característica          | Rating          |
| ----------------------- | --------------- |
| Tipo de particionamento | Técnico/Domínio |
| Unidades de implantação | 1...*           |
| Deployability           | 3               |
| Elasticidade            | 5               |
| Evolução                | 3               |
| Tolerância a falhas     | 3               |
| Modularidade            | 3               |
| Custo                   | 2               |
| Performance             | 5               |
| Confiabilidade           | 4               |
| Escalabilidade          | 5               |
| Simplicidade            | 1               |
| Testabilidade           | 1               |
