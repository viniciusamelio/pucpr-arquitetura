# BaaS, FaaS e CaaS

- Produtos em nuvem nem sempre são classificados com as siglas
- Podem ser simplesmente chamados de serviço gerenciado

## BaaS
- Não apenas funções
- Autenticação como serviço, mensageria, armazenamento

**Exemplo: Database**
- Num modelo tradicional você seria responsável por absolutamente tudo
- Num BaaS você gerencia apenas a modelagem e o consumo desses dados

## FaaS
- Funções deployáveis numa estrutura de nuvem especializada
- O uso de funções acaba favorecendo o desacoplamento do código
- Ambiente Efêmero
  - Stateless
- Possível rodar Kubernetes OnPrem, com configuração e desenvolvimento de funções com Key Native

> Como mitigar o problema da portabilidade ou até zerar o vendor lock-in?

## CaaS - Container as a service
- Provedor de nuvem entrega um orquestrador
- Você se preocupa com um container completo
- Oferece maior portabilidade
- Exemplos: ECS, EKS, AKS.
