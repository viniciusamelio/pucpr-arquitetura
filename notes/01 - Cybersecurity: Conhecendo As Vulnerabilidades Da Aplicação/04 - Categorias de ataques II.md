# Categorias de ataques II

## Injeção
- Entradas não validadas
- Em SO´s os danos podem ser mais severos

### Dificuldade
- Fácil

### Controle
- De dificuldade mediana
- Validação de parâmetros recebidos pelo sistema, com formatações esperadas
- Tratamento no front e no backend
- Em consultas SQL, usar a clausula LIMIT
- WAF: Web Application Firewall
- Fluxo sadio e robusto de desenvolvimento, com modelagem de ameaças
- DAST: Dynamic Application Security Test
- Teste manual de superfície
- Binds ao invés de usar os parâmetros diretamente nas queries (SQL)

### Impacto
- Vazamento de dados
- Execução de comandos no sistema
- Perda de dados
- Brecha para engenharia social com os dados vazados

## Design inseguro
- Aplicação especificada de maneira incorreta
- Concepção do sistema inaderente a segurança da informação
- Alto impacto
- Ocorre quando não há um envolvimento de profissional de segurança no planejamento do sistema, assim como falta de cultura da empresa
- Falta de perfil do negócio
- Falta da modelagem de ameaça

### Controle
- Dificuldade baixa
- Frameworks e bibliotecas
- Determinar limites em MVP
- Determinar controles de autenticação
- Especifique o fluxo de dados
- Especifique os estados da aplicação
    - Não retorne uma mensagem que diga que o usuário não existe
- Determine ameaças
- Segregue ambientes
- Segregue a rede
- Segregue serviços e usuários
    - Política do menor acesso
- Especifique limites
    - Consumo de API, consumo de recursos
- Fluxo de testes constantes
- Logs

### Impacto
- Multa
- Indisponibiidade
- Vazamento de dados
- Perda financeira, no geral

## Erros de configuração
- Configs ou parâmetros não estão realizadas ou são insuficientes
- Falta de controle do que pode ser chamado na rede
- Falha na configuração de servers
- Configuração de ambiente falha
- Falta de atualização do SO do servidor
- Apps instalados de forma desprotegida
- Excesso de permissão
- Servidor não envia headers


### Controle
- Processo da empresa
- Padronização
- Permissões mínimas
- Revisar as configurações, no geral
- Revisar permissões herdadas
- Processos de revisão de ambientes cíclicos (auditorias)

### Impacto
- Lentidão
- Acesso a recursos não autorizados do servidor
    - Multa
    - Vazamento de dados
- Indisponibilidade