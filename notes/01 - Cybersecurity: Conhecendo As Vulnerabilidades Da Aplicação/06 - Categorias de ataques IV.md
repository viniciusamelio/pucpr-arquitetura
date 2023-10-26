# Categorias de ataques - parte 4

## Falha de monitoramento e de logs de segurança
- Falha na coleta de logs
- Detecções ou monitoramentos falhos
- Falhas de eventos auditáveis, como tentativas de login
- Logs inadequados ou ausentes
- Não rastreabilidade de eventos
- Falta de alertas/logs em tempo real
- Logs vazados ao atacante

### Controles
- Arquitetura prever log
- Onde serão salvos os logs e quem terá acesso?
- Que tipo de log salvarei no ambiente?
- Prazo de retenção
- Verificar formato do log, se invialibiza injeção contra o servidor
    - Não salvar usuário e senha se for salvo, por exemplo, num sistema de login
- Tratamento dos dados dos logs
- Garantir o mapeamento de ações dos usuários para auditoria, recriando passos do usuário no sistema
- DevOps ou DevSecOps deve garantir monitoramento
    - Dashboards com Kibana, por exemplo
- Ao identificar o incidente é preciso bolar um plano de resposta

### Impacto técnico
- Desgovernança 
- Instabilidade
- Vazamento de dados
- Acessos não autorizados
- Encadeamento de vulnerabilidades


## Forjar request do lado do server
- Permite o atacante direcionar chamadas para alvos não validados

### Controles
- Validações como forçar esquema de url, por exemplo
- Não enviar respostas puras, sempre trata-las
- App não fazer requisições diretas a qualquer domínio, sem verificação

### Impacto técnico
- Exposição do ambiente
- Necessidade de correção imediata
- Vazamento de dados
- Indisponibilidade