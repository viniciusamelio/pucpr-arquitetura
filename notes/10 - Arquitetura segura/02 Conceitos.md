# Conceitos

## Confidencialidade

- Preocupação de não revelar informações a quem não deve ter acesso a tais infos

## Integridade

- Preocupação de não permitir alteração indevida ou não autorizada do dado

## Disponibilidade

- Preocupação com a disponibilidade daquele dado

## Camadas
### MFA
    - Biometria
    - Senha
    - PIN

### Autorização
- Requisitor/subject = O usuário que requisita o acesso 
- Objeto = Aquilo que o usuário requisita acesso
- Tipo = Leitura, execução

### Auditoria
- Tem gente habilitando os logs?
- Alguém revisa os logs?
- Logs detalhados
- Combate o não repúdio com o Audit Trail

### Gerenciadores de sessão
- Evitar roubo de sessão na comunicação inter/intra processos
    - RPC ou IPC

### Gerenciadores de exceção
- Erros = Condições não conhecidas pelo software
- Tratar erros para exibi-los de maneira amigável e segura para o usuário
- Fail safe = Priorizar segurança sobre compatibilidade

### Gerenciadores de configurações
- Setup, ou carga, inicial para as aplicações quando estas iniciam
    - Env vars, arquivos de sistema, etc

### Security gateway
- Validam se tudo que foi estabelicido no começo do projeto está de acordo
- Necessita uma equipe para auditar antes do avanço nas etapas do desenvolvimento

### Bug track
- Eventualmente alguns bugs serão relacionados a segurança
- Formas de rastrear os dados, checando status de acordo com versões do software
- Impacto x probabilidade
    - Dano, usuários afetados, possibilidade do paliativo durante o desenvolvimento do hotfix
    - Facilidade de reprodução, facilidade de exploração (exploit) e dificuldade de descoberta 
