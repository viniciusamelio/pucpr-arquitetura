# Monitoramento de software

- Mecanismos adicionados ao software
    - Contadores de performance
        - Perf Mon (Windows)
            - Identifica gargalos em threads geradas pelo software
    - Coleta de telemetria
        - Capacidades coletadas do softwares e enviadas para cloud
            - Autorização explícita do usuários 
- Gerenciamento de incidentes (Segurança, não troubleshooting)
    - Pode ser outro time além do time de desenvolvimento
- Gerenciamento de mudanças
- Backup
    - Procedimento de recovery através do backup, e a funcionalidade do software após


## Suportabilidade do sofware

- Suporte a versões anteriores, com patches de correção e melhorias de segurança durante um determinado período
- End of life policy


## Supply Chain

- Ataque de supply chain é quando um grupo de atacantes quer chegar a um determinado destinatário, atacando a linha de supply (fornecimento) que aquele alvo consome
- Num exemplo prático, isso poderia ser feito atacando um provedor de alguma ferramenta que seu software utiliza
- Para evitar essa situação é necessário um time para realizar um teste de assurance
- ICS: Industry control system
    - Sistemas que não possuem grandes mudanças
    - Até o uso intensivo de IOT não precisavam de preocupar e dar tanta atenção a esse tipo de ameaça, pela consolidação dos padrões e meios utilizados


> Todos estão sucetíveis a ataques de supply chain na indústria hoje em dia