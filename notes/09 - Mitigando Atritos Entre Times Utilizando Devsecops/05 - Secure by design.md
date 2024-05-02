# Secure by design

- Cultura nos times para que toda e qualquer app e produto desenvolvido tenha segurança como requisito, assim como UX

- Programa educacional é um pré requisito
- Aplicar boas práticas no design de soluções
- Adotar técnicas de threat modelling

## Evitando Ameaças

- Um bom design é baseado em **Simplicidade**
- Clean code
- Desenhar arquitetura mais simples para resolver o problema
- Code reviews

## Threat modelling

- Parte do grooming
- Olhar para uma solução proposta e pensar o que pode dar errado, e como se proteger em caso de algum ataque

### Tipos de ameaças CIA

- Confidencialidade
    - Ataques que comprometem a confidencialidade de dados sensíveis de um sistema
    - Vazamento de cartões
- Integridade
    - Ataques que compromentem a integridade de dados que transitam através de um sistema
    - Man in the middle
- Disponibilidade
    - Comprometem a disponibilidade de uma aplicação, causando impactos na operação
    - DDOS

### Começando

- Comece desenhando um DFD (Diagrama de fluxo de dados)
    - Desenhe os componentes e os dados trafegados entre esses componentes
- Aplique uma técnica de thread modelling, como a STRIDE

#### STRIDE

- Spoofing
    - Um hacker assume a identidade de outra pessoa, viola a autenticidade
- Tempering
    - Infrator modifica o conteúdo de algum arquivo, item na memória, configuração de rede e etc
- Repudiation
    - Quando uma pessoa nega conhecer alguma ação feita no sistema
- Information disclosure
    - Acesso não autorizado a dados sensíveis
- Denial of service
    - Sobrecarrega o sistema e compromete sua capacidade de resposta
- Elevation of privilege
    - Infrator consegue privilégios elevados para executar ações no sistema