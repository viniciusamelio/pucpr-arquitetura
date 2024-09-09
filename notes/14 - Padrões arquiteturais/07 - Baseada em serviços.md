# Baseada em serviços

- Arquitetura distribuída
  - Camadas técnias e de domínio
  - Não exige separação de bases por domínio
- Cada serviço normalmente utilizará da arquitetura de camadas em sua composição
- Baixa granularidade
  - Muitas funcionalidades
- Base de dados compartilhada entre os serviços
  - Maior consistência do que em cenário com bases diferentes
  - Transações centralizadas

## Características

- Flexível
- Se encontra num cenário de transição entre arquitetura monolítica e baseada em
  microsserviços
- Possui pontos de extensibilidade
- Camadas técnicas de acordo com a necessidade
- Variante comum: API Facade
  - API Layer (Proxy ou gateway)
    - Visão única dos serviços
    - Aspectos transversais
      - Throttling
      - Observabilidade
      - Segurança
- Mediação "Light"

## Ratings

| Característica          | Rating        |
| ----------------------- | ------------- |
| Tipo de particionamento | Domínio       |
| Unidades de implantação | 1 por serviço |
| Deployability           | 4             |
| Elasticidade            | 2             |
| Evolução                | 3             |
| Tolerância a falhas     | 4             |
| Modularidade            | 4             |
| Custo                   | 4             |
| Performance             | 3             |
| Confiabilidade           | 4             |
| Escalabilidade          | 3             |
| Simplicidade            | 3             |
| Testabilidade           | 4             |
