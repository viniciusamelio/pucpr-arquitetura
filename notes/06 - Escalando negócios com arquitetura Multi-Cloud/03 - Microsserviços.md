# Microsserviços em Multicloud

- Primeiro conceito falado por volta da década de 70
- Kubernetes facilita a migração de providers e ambientes

## O que é Kubernetes?

- Orquestrador de containers
- Código aberto
- Automatiza o processo de dimensionamento e gestão de aplicações em containers

## Componentes

- Clusters: Conjuntos de nodes
- Nodes: Vms que abrigam os containers
- Configurações declarativas


### Na prática

- Um cluster possui um painel de controle
- Possui os nodes
- Cada node tem PODs, e dentro desses pods temos os containers


## Service mesh

- Antigamente as conexões eram feitas por conexão direta
- Isso foi resolvido com o uso de load balancers
- Service mesh permite uma gestão fácil da comunicação entre os serviços
- Conceito de side car
- Capta todas as requests feitas e aplica as políticas de segurança
- Políticas geridas através de um painel


## Network ingress

- Ingress é criado quando é necessária uma comunicação com a rede externa
- Protocolos http, https

## Namespaces

- Isola os clusters de acordo com esses nomes
- Possibilita a gestão de ambientes

## Cilium Multi-cluster e eBPF

- Comunicação entre dois clusters com comportamento como se fosse um único
- Cilium é a mais avançada nesse segmento de uso
- Comunicação sem ingress
- Base eBPF
