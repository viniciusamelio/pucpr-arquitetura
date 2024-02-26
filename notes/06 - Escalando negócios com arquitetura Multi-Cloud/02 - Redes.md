# Redes

O principal desafio nessa modalidade de multi-cloud é, de fato, a conectividade

## VPN

- Forma mais fácil de lidar com essas conexões
- Ficamos a deriva da internet "pública" nesse modo
- Recomendado ser usado com um TLS

## Azure ExpressRoute

- Opção dedicada, por uma rede de parceiros do provedor da Cloud;
- Seu datacenter precisa de uma conexão física até o local do parceiro;
- O parceiro se encarrega de ter uma conexão física até o provedor de cloud;
- Essa topologia permite um SLA, que é definido pelo parceiro (Partner edge);
- Conexão entre o Datacenter e o provider não necessariamente é segura;
- Recomendado TLS;
- Boa prática: ter duas conexões entre o datacenter e o parceiro (caminhos distintos);
- Garantia de uma velocidade estável de conexão;
- Possibilidade de redundância na conexão;
- Centenas de redes parceiras espalhadas pelo mundo;

## Google Dedicated Interconnect

- Seu roteador possui uma conexão direta com o roteador do provider
- Aumento no SLA
- Diminunição dos riscos de problemas, por não ter um terceiro envolvido
- Mesmo com uma conexão direta é necessário a existência de redundâncias

## Topologias de network em multi-cloud

### Mirrored

- Fazer com que o ambiente de VPN e Nuvem se espelhem
- Comum em ambientes híbridos
    - HML e Dev em um ambiente
    - STG e Prod em outro
- Regras de firewall para evitar comunicação entre ambientes (para CI e CD)

### Meshed

- Configurações em camadas, particionadas (bursting)
- Workloads dentro dos limites de TCP e UDP
- Pode usar regras de firewall
- Migração para cloud ou ambientes híbridos
- Entrada para o ambiente feita pelo provider

### Gated egress

- Apps de múltiplas camadas, com acessos feitos via API
- Dar acesso a API que está no seu datacenter para outras APIS hospedadas nos providers

### Gated ingress

- O oposto do egress
- Workloads majoritariamente na cloud

### Gated ingress and egress

- Espelho dos workloads entre os dois ambientes