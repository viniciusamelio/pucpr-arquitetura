# Melhorias

## Service mesh

- Service mesh é uma camada que resolve responsabilidades de forma a permitir que o desenvolvedor foque mais no negócio
- Canary release pode ser feito com K8S, através de quantidade de réplicas com round robbin, por exemplo, mas com service mesh esse número pode ser feito sem ter que aumentar a quantidade de réplicas
- Teste A/B
- Controle de tráfego
- Observabilidade
- MTLS -> Toda comunicação independente se inter-node, inter-cluster, vai conter criptografia
- Traffic Mirroring