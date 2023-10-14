# Security by Design (Segurança por definição)
Parte da prerrogativa que toda a ideia de implementação de um software, desde sua concepção, seja fundamentado na segurança do mesmo

É uma metodologia de garantia de segurança que habilita clientes formalizar design de contas, automatizar controles de segurança e estar apta para com auditorias.

SbD é composta por quatro etapas de implementação que retratam casos de segurança e compliance.

**O documento usado como referência de estudo se chama "Intro to Security by Design", da AWS, publicado no ano de 2015**

    - Isso faz com que vários momentos eu cite "plataforma" ou "clientes", onde no documento original é referenciado como fazendo parte do contexto da própria da AWS, assim como seus serviços

## Etapas (ou fases)
1 - **Entenda seus requisitos**: Especifique suas políticas e documente os controles herdados da plataforma usada, documente os controles que você possui e opere seu ambiente, decidindo qual regra de segurança forçar a serem aplicados no ambiente.

2 - **Crie um "ambiente seguro" que atenda seus requisitos e implementação**: Defina a configuração necessária, como requisitos de criptografia (como forçar o uso de criptografia no serviço X), permissões de acesso a recursos (imagens, por exemplo), e o tipo de log que precisa ser implementado

3 - **Obrigue o uso de templates**: Na plataforma usada, habilite o obrigue o uso do template referente ao "ambiente seguro" que foi criado, isso previnirá qualquer um de criar um ambiente que não seja aderente ao seu ambiente seguro.

4 - **Performe validações**: Faça auditorias de acordo com coleta de evidências, referente ao uso do ambiente criado.

## Impactos da SbD
Uma arquitetura baseada em Secury by Design almeja os seguintes pontos:
- Criação de funções que não possam ser substituidas sem a modificação da política
- Estabelever controler de operação confiáveis
- Habilitar auditoria contínua e em tempo-real
- O roteiro técnico da sua política de governança

O resultado é um ambiente automizado que possibilita a garantia de segurança do cliente, governança e capacidades de compliance.