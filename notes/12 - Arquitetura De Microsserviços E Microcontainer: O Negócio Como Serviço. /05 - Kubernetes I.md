# Kubernetes I

- Kubernetes é um orquestrador de containers
- Uma forma de transformar sistema imperativos em declarativos
- Masters
    - Gerenciamento do cluster
    - API Server (KubeAPI)
    - Etcd - Banco chave valor onde tudo relacionado ao cluster é persistido
    - Scheduler - Organiza o cluster em relação a recursos
    - Kubedns - Gerenciador de DNS para comunicação intra-cluster
    - Cluster outscaling - quem adiciona mais nodes
- Nodes
- Kubernetes evita lock-in
- Oferece versões gerenciadas
- Overcomitting
    - Vários sistemas compartilharem o mesmo node
- Segurança
    - Políticas de segurança

## Exposição de serviços

- Interna - Cluster IP
- TCP/HTTP/UDP
- O que será feito com essa exposição?
- Reescrita