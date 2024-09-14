# Baseada em microsseviços

- Só faz sentido num ambiente distribuído
- Domínio representado de maneira evidente na composição dos componentes
- Um componente nunca acessa dados de outro domínio
- Cada componente é independente para ser implementado de acordo com o time
  atuante
- Essa arquitetura ganhou fama através da Netflix

## Trade offs

- Diminuição da possibilidade de reusabilidade do código desenvolvido
- Diminuição do reaproveitamento de profissionais em diferentes times
- Observabilidade difícil
- Micro = Responsabilidade, ao invés de tamanho
- Revisão da granularidade

## Dicas

- Circuit breaker
- Sidekick
  - Garante recursos para uso de forma homogênea ao longo dos serviços
  - Pode conter inclusive o próprio circuit breaker, além de logging,
    monitoramento e etc

## Saga

- Padrão de orquestração para microsserviços
- Garante que determinado processamento composto por diversas etapas vá até o
  fim, e se não for até o fim, faz o rollback de tudo que foi feito

## Ratings

| Característica          | Rating    |
| ----------------------- | --------- |
| Tipo de particionamento | Domínio   |
| Unidades de implantação | 1 domínio |
| Deployability           | 4         |
| Elasticidade            | 5         |
| Evolução                | 5         |
| Tolerância a falhas     | 4         |
| Modularidade            | 5         |
| Custo                   | 1         |
| Performance             | 2         |
| Confiabilidade          | 4         |
| Escalabilidade          | 5         |
| Simplicidade            | 1         |
| Testabilidade           | 4         |
