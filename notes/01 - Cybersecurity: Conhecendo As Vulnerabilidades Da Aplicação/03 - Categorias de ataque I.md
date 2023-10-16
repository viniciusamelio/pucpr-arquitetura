# Categorias de ataque - Parte I

**Classificação com base em recorrência, não em criticidade**

## Quebra do controle de acesso
- Broken Access Control: Ocorre quando um usuário, mesmo que autêntico, consiga acessar funcionalidades exclusivas de usuários de perfil superior.
- Não estamos falando do acesso de uma pessoa não autorizada, que conseguiu acesso, mas sim da quebra da gestão do acesso, ou seja, existe o acesso para o usuário autenticado, mas uma falha faz com que funções de perfis superiores sejam acessíveis.
 Exemplo: Gerente A acessa os clientes do Gerente B, numa aplicação bancária.

### Vetores
- Sistemas
- APIS
- Tudo que tenha perfilamento de responsabilidades e ações

### Dificuldade
- Médio para fácil, normalmente
    - Vai depender do sistema e suas gestões

### Controles
- Segregação de perfis de acesso de acordo com responsabilidades

### Segregação de função/acesso
- Tem haver com a função de exercício do usuário
- Bloqueio do uso de funções que não sejam inerentes a role do usuário

### Centralização de acesso
- Facilita na unificação do controle de roles e permissões, em diversas aplicações utilizadas na organização
- Pode evitar vulnerabilidades de processo também

### Como evitamos?
- Testando
- Monitoramento
- Evitar a obscuridade
- Princípio do menor acesso
    - 2FA, MFA e afins
        - MFA: O que sou? O que sei? O que tenho?
            - Ser: biometria
            - Ter: dispositivo autenticado
            - Saber: senhas
- Validação abstrata
    - Determinar bibliotecas de login, seguras, herdadas por todas as aplicações
- Auditorias

## Falhas de criptografia
Ocorre quando o algoritmo é reversível sem uma chave privada

### Vetores
- Tudo que utiliza criptografia
    - Chamadas, bancos de dados, protocolos smtp, ftp, http, https

### Controles
- Uso de algoritmos fortes de criptografia, evitando algoritmos fracos como o DES
- Exigir configuração de segurança no header das requests (HSTS)
- Monitorar e gerar alertas

### Como evitamos?
- Levantamento básico
    - Os endpoints e sistemas utilizados/consumidos requerem conexões seguras?
    - Atualização de algoritmos para encoding
    - Certificados digitais devidamente utilizados?
    - Como salvamos as senhas? 
        - Direto no BD?
        - Hashing?
        - HSM (Hardware security model) para proteger os certificados? 
        - Hashing obsoleto? (md5)
        - Protocolos obsoletos? (TLS 1.0)
        - Dados locais com criptografia aderente?

### Impacto
- Exposição de dados
- Sequestro de dados

### Dificuldade
- Difícil 