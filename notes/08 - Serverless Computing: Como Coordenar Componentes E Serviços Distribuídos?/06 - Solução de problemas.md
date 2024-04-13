# Solução de problemas

## Vendor lock-in
- Contratual
- Ferramental
  - Bancos de dados
  - Equipamentos de rede e infra
- SaaS
- PaaS

## Padrões de projeto que facilitam na diminuição do vendor lock-in
- Abstração do código por camadas
- Pipelines 

## Dependência externa
- Apontamentos para bds
- Especificidades dos cloud providers


### Alternativas
- Env vars
- Consul
  - Ajuda a gerenciar o I/O no cluster
  - Contém parâmetros
- etcd
  - Base de dados key/value distribuída
- Bases NoSQL
  - Maior performance que bases SQL
  - Caching
- Armazenamento em memória
  - Bases de dados in-memory
  - Caching
  - Redis e Memcached