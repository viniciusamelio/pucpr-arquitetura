# Outras necessidades

## Escalabilidade

- Vertical: Mais recursos para atender a necessidade
- Horizontal: Adicionar máquinas para atender a necessidade

## Otimização

- Mitigação de desperdício de recurso

## Alta disponibilidade

- Com boa performance, sem taxa de erros
- Consistência pensando num ambiente heterogêneo

## Modernização de aplicação

- Cobre vários temas além de microserviços
- Apenas migrar para a nuvem não basta, é preciso mudar comportamentos tidos como "legado"

### Técnicas

- Desacoplamento de aplicação
    - Quebrar o app em partes menores, de maneira que sejam independentes e administradas de forma única e separada
- Serviços gerenciados
- Serverless
- Portabilidade
- Devops

## SRE

- Site relayability engineering
    - Diz respeito a forma de fazer gerenciamento dos serviços
- Reduz silos organizacionais (horizontalidade de grupos como devs, infra, etc)
- Compartilhar responsabilidades
    - Aceitar falhas como normal (fail fast e iterate)
        - Blameless post-mortem (Descobrir a causa raiz sem achar culpados)
        - Error budget (Orçamento de erro)
            - Tempo de falha
- Implementar mudanças graduais
    - Rolling-releases
        - Uma pequena porção do tráfego recebendo atualizações, aumentando gradualmente ao longo dos dias
- Tunning e automation
- Telemetria e observabilidade

### Service-level

- Service Level Indicator
    - Métrica
- Service level objective
    - Objetivo
- Service level agreement
    - Penalidade
