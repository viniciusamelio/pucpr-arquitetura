# Ciso e gestão da privacidade

## Ciso
- Responsável por todas as estratégias de segurança de dados de uma organização, de ações e times
**Missão de um ciso**
-  Se propõe a trazer conceitos de segurança da informação de maneira aderente a organização em todos seus leveis
- Promover boas práticas
    - Arquitetura
        - security & privacy by design
    - Configuração
        - Ferramentas baseadas em padrões conceituados
- Atender a compliances
    - Auditorias
- Gerenciar risco
    - Conhecer vulnerabilidade e traçar prioridades
    - Mitigação de risco
- Gerenciamento de controles
    - Quais controles posso colocar na organização?
    - Não apenas métricas, mas também controles de autenticação, acesso a dados, segregações, etc
- Gerencia incidentes
    - **não apenas marcar o incidente, mas investigar a causa, onde existiu o erro**
    - Plano de resposta/contingência
- Constituir um time de segurança da informação forte
    - Como criar um time com diferentes skills para que se possa executar tarefas e criar processos que sejam robustos
    - Treinamentos para gerar habilidades
        - Investigação, monitoramento, Ataque, Defesa e afins.


### Ameaça externa
- Tudo ser digital hoje em dia implica num aumento de vetores de ataque
- Se a superfície de ataque aumenta, a visibilidade em rede também, isso resulta no risco de ser atacado
- Pode resultar na perda de clientes
- Apps podem ser fontes de vazamento de dados
    - Engenharia reversa

### 5 problemas que foram apontados por cisos em 2013
- Falta de consciência dos problemas de segurança
- Desenvolvimento inseguro
- Metodologia de testes fraca ou inadequada
- Falta da habilidade de equipe
    - Falta de conhecimento e prática
- Falta de orçamento

**Não adianta haver uma estratégia de segurança se eu não tenho uma cultura organizacional**
### Investimentos necessários
- Treinamento
    - Resulta em impactos positivos diretamente na qualidade dos produtos entregues, tal como na segurança do mesmo
- Testes
    - Garantia de força, aderência
- Aprimorar técnicas de segurança entre os produtos adotados
    - Backend com frontend, por exemplo
    - Como protejo um dispositivo de acesso aos dados
    - Qual a proteção do transporte de dados
    - Validação
- Aprimorar logs
    - Monitoramento da quebra de conduta de organização, por exemplo

### Quais os desafios?
- Promover investimento contínuo
- Especificar requisitos de segurança aderentes ao negócio
- Documentar 
- Promover arquitetura segura
- Revisão de códigos
- Testar casos de uso
- Promover ambiente de desenvolvimento bem configurado
- Realizar modelagem da ameaça de forma aderente

### Riscos à privacidade (OWASP - 2014)
- Apps vulnerábeis
- Vazamento de dados pelo operador
- Respostas de violação de dados insuficiente
- Exlusão de dados pessoais de forma insuficiente
- Termos sem transparência
- Coleta de dados sem propósito
- Compartilhamento de dados com terceiros
- Dados pessoais desatualizados
- Ausência de expiração de sessão
- Transferência de dados de forma insegura

### Como identificamos esses riscos?
- Realizar modelagem de ameaça
    - Procedimento para otimizar a segurança, identificado vulnerabilidades e traçando planos de mitigação
- Determinar controles

### Modelagem de ameaça
- Se dá através da documentação de possíveis ataques mapeados, por exemplo: 
    - Possível SQL Injection
    - Possível CSRF
    - Possível manuseio imprópio da sessão
- Com isso é possível automatizar análises, testes e até a própria defesa
    - Web application firewall
        - Definição de quantidade de requests por minuto
    - Sandbox/Firewall


### Gestão de vulnerabilidade
- Scan (verificação) dos ativos
    - Quem estimará/tratará o impacto
    - Quem deteminará o risco ao negócio
    - Prazo de correção
    - Quais controles estabelecidos até/após a correção?
    - Quem avaliará o processo?
    - Riscos dos processos já estabelecidos
    - Processo de avaliação de arquitetura
- Identificar metodologias de ataque
    - Tracking do processo de um ataque até seu impacto
- Medir o risco
    - Identifica a dificuldade, prevalência, facilidade de detecção e impacto técnico


