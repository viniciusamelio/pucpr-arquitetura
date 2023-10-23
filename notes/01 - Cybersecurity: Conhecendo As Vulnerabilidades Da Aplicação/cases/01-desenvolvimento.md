# Desenvolvendo um plano para Arquitetura e Procedimentos de Segurança para a ACME Development

## Descrição do case
A empresa ACME Development está entrando no mercado de meios de pagamento, e iniciando o desenvolvimento de uma solução para processamento de transações financeiras. Utilizando seus conhecimentos em Segurança por Design (SbD), requisitos de segurança e padrões de mercado exigidos, desenvolva um plano para uma melhor arquitetura de segurança para essa aplicação, que será hospedada na cloud AWS.

## Insights e perguntas para o debate
- Quais são os primeiros passos para iniciar o projeto?
    - Mapear os serviços a serem desenvolvidos, os recursos da AWS que irão compor o projeto, bem como pontos de contato entre os serviços internos, de maneira a validar os tratamentos necessários de input, além de realizar a modelagem de ameaças e suas contigências

- Quais os requisitos primordiais para adequar o projeto ao compliance do PCI-DSS?
    - Instalar e manter uma configuração de firewall para proteger os dados do titular do cartão
    - Utilizar um firewall suficientemente forte para ser efetivo
    - Não utilizar senhas e configuraçõess padrões fornecidas pelos vendedores
    - Proteger os dados armazenados do titular do cartão
    - Utilizar criptografia na transmissão dos dados dos titulares dos cartões
    - Utilizar software antivírus, antispyware e antimalware atualizados
    - Desenvolver e manter sistemas e aplicações seguras
    - Restringer acesso aos dados dos cartões de acordo com o cargo do empregado de cada empresa
    - Designar dados de login únicos para cada usuário
    - Restringir acesssos físicos e eletrônicos aos dados dos cartões
    - Rastrear e monitorar todos os acessos à rede e dados dos cartões
    - Testar a segurança de sistemas e processos regularmente
    - Definir uma política de segurança que seja seguida e mantida por todos 

- Quais são as responsabilidades da empresa desenvolvedora e do provedor de serviço, quanto à Segurança da Informação?
    - A empresa desenvolvedora deve ser responsável por aplicar conceitos/práticas que visem um aumento da garantia de segurança nas aplicações desenvolvidas, preferencialmente desde a concepção de design das mesmas, utilizando os recursos disponibilizados pelo provedor (AWS) para compor essa estrutura segura
    - O provedor, por sua vez, deve fornecer meios de integração, controle e manuseio dos seus serviços de maneira segura, dando suporte à decisões de segurança adotadas nas abordagens dos clientes (desenvolvedores) 

- Qual ferramenta podemos utilizar para nos basearmos sobre as vulnerabilidades mais utilizadas por atacantes na exploração de aplicações Web?
    - AWS Web Application Firewall (WAF)
        - Ajuda a proteger a aplicação contra ataque comuns como injeções
    - Amazon Inspector
        - Serviço de avaliação de segurança que ajuda a identificar vulnerabilidades e violações
    - AWS Config e AWS Trusted Advisor
        - Permite a avaliação do estado da sua infra AWS e identifique configurações que podem gerar vulnerabilidades

- Quais ferramentas podemos utilizar para analisar a aplicação e suas possíveis vulnerabilidades?
    - AWS Trusted Advisor
    - Amazon Inspector
    - AWS Security Hub
        - Agregador de vários de outras fontes, como Inspector, AWS Config e outros, fornecendo uma visão centralizada das descobertas de segurança
    - Amazon Guard Duty
        - Serviço de monitoramento que usa aprendizado de máquina para detectar atividades maliciosas, útil em tempo real