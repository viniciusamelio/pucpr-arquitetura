# Threat Modeling

- Desenho para auxiliar a mitigar e identificar problemas de segurança durante o desenvolvimento do projeto
- Pode ser utilizado em qualquer fase do projeto
- Utilizado mais de uma vez ao longo do projeto, em cada etapa
- Pode ser utilizado em projetos onde você não participou desde o início do projeto, nesse caso, requerendo que você faça uma inspeção em ameaças presentes no projeto no estado atual

## Como fazer?

- Começar com um diagrama
    - Baixo nível ou prevendo todos os pontos de comunicação
    - Como o processo do app se comunicará com outros processos dentro do SO
- STRIDE
    - Categorização de ameaças
    - Spoofing: Acesso ilegal a uma informação de usuário
    - Tempering: Modificação maliciosa do dado
    - Repudiation: Negar uma ação feita
    - Information disclosure: Exposição de informação indevida
    - Denial of service: Perda de disponibilidade da aplicação
    - Elevation of privileges: Usuário escala privilégios incondizentes de acordo com sua role

## Exemplos

- Microsoft threat modeling tool
    - Processos genéricos
    - Após elaborar a diagramação da aplicação possíveis ameaças são detectadas nos pontos de comunicação desenhados