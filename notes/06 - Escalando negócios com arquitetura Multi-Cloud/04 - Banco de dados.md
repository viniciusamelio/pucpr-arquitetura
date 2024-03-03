# Banco de dados em Multicloud

- Provedores tem criado bancos com compatibilidade de APIs SQL, que permitem escalabilidade vertical e horizontal
- Conceito de DB global com consistência de dados garantida (DB Serverless)

## BDs por arquitetura de implantação

- Bancos de dados pré-nuvem
    - Executados em Bare-metal ou VMs (MySQL, Postgres)
    - Dificuldade de mandar consistência quando há o crescimento horizontal
- Bancos de dados gerenciados por parceiros ou provedores
    - Quando possuem empresas que fazem o gerenciamento do DB na nuvem
    - MongoDB e MariaDB
- Bancos de dados nativos da nuvem
    - BDs criados pensados na nuvem
    - CockroachDB e YugaByte
- Bancos de dados compatíveis, criados pelo provedor de nuvem
    - Gerenciados pelo provedor de nuvem
    - Serverless
    - Amazon Aurora


## Casos de uso

- Cloud bursting
    - Usufruir temporáriamente da cloud para aumentar capacidade do DB
- Portabilidade Cross-Cloud
- Seleção Best-of-Breed
    - Uso de diferentes BDs de diferentes tipos
- Recuperação de desastres


### Cloud Bursting

Caso de nuvem híbrida em que um workload básico e estável pode ser gerenciado por um data center privado.
Aumento na atividade do cliente durante determinados períodos do ano que excede a capacidade convencional

### Cross-Cloud

Dados replicados entre réplicas do banco Master, nas nuvens escolhidas.
Arquitetura mestre-mestre, permite escritas simultâneas, lidando com conflitos de chaves, por exemplo.

### Seleção Best-of-Breed

Nuvens muito diferentes umas das outras em muitos aspectos, especialmente em tecnologias específicas do provedor que só estão disponíveis em uma nuvem específica.

Diferentes partes do app são executadas em diferentes nuvens usando diferentes tecnologias de BDs

**Uso de Change Data Capture (CDC)** para sincronização entre bancos

### Recuperação de desastres

Diferente de alta disponibilidade

Uso de nuvens em uma mesma região

Load balancing sempre joga para a mesma nuvem, quando ocorre indisponibilidade, existe a troca para a nuvem 2

Load balancers normalmente pertencem a regiões maiores, ou são globais, com a finalidade justamente de não ficar indisponível

Processo de fail-over, ou seja, transforma um DB réplica em um mestre

**RPO** - Recovery Point Objective - Ponto específico que quero recuperar da base de dados

**RP** - Recovery Point, tempo para recuperação, de acordo com tolerância de perda de dados

**RTO** - Recovery Time Objective - Quanto tempo leva para o app voltar a funcionar

Quando a região volta a funcionar, existe a sincronização entre as bases, voltando a condição anterior, com a mudança de mestre entre as nuvens, novamente

#### Recuperação de desastres com RPO e RTO zero

Uso de arquitetura mestre-mestre

## Seleção de banco de dados multi-cloud

- Com base nos padrões de gerenciamento de dados:
    - Sistema de BD existente
    - Novo Sistema de BD
- Compatibilidade
    - Compatibilidade entre nuvens
    - Mudar o sistema ou explorar alternativas
- Relação entre os dados nas duas nuvens
    - Dados particionados
    - Replicação unidirecional
    - Replicação bidirecional