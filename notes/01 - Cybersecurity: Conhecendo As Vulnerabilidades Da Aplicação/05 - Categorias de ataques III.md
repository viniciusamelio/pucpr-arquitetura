# Categorias de ataque - parte 3

## Componentes desatualizados
- Ocorre quando não conhece as versões dos componentes utilizados no projeto, falta de governança
- Packages, APIs de terceiros, pacotes de sistemas operacionais
- Pacotes sem atualizações há um longo tempo
- Falta de testes por parte dos devs quando há mudança de pacotes
- Configuração incorreta do componente

### Controles
- Fácil/Média Complexidade
- Implementação de fase de dependency check numa pipeline
- Remover dependências desatualizadas ou não utilizadas
- Monitorar continuamente as atualizações das dependências
- Escrever-se para receber alertas de vulnerabilidades
    - cve.org
- Baixar dependências de fontes confiáveis
    - Código assinado
- Monitorar packages sem atualizações há muito tempo
- Atualização e alteração de configurações durante a vida útil do software

### Impacto Técnico
- Quebra do app
- Vulnerabilidades diversas e desconhecidas

### Impacto ao negócio
- É Variável de acordo com a aplicação
- Acesso direto ao ambiente
- Indisponibilidade

## Autenticação e identificação falhas
- Quando ocorre a falha no processo de login onde um atacante entra na aplicação de forma inautorizada
- Usuário não autorizado consegue realizar uma tarefa através de um processo legítimo

### Controles
- Fáceis
- Bom desenho de arquitetura
    - Quantas vezes o usuário pode errar a senha, número de requests (rate limiting), pinagem, validação de source por ips, tratamentos contra injeções, políticas de senha, MFA
- Bloqueio por tempo
    - WAF ou lógica própria
- Uso de hashes
- Faça links entre bloqueios
    - Bloqueio por geolocation + tentativas
- Controle do dispositivo
    - Vincular dispositivo ao user
- Análise comportamental
    - Rastreamento por acessos de geolocation, bloqueando quando há uma distância grande num curto período de tempo

### Impacto técnico
- Reconstruir sistema de autenticação
- Superfície de ataque aumenta uma vez que um ataque ocorre e é bem sucedido


### Impacto ao negócio
- Alto/Crítico
- Chantagem a empresa
- Sequestro de dados
- Multa
- Vazamento de dados
- Indisponibilidade

## Falha na integridade de dados e software
- Relacionada a atualização de software
- Ocorre quando o código ou infra não é protegido contra código ou dados

### Vetores
- Plugins
- Pacotes
- Pacotes com atualização automática sem verificação
- Serialização insegura

### Controles
- Assinatures e mecanismos semelhantes
- Repositórios confiáveis
- Softwares de validação
- Valide as permissões da pipeline
- Processo de review e análise de código
- Não envie dados ao client de maneira insegura

### Impactos Técnico
- Falta de governança
- Perda de código

### Impactos ao negócio
- Perda financeira
- Vazamento de dados