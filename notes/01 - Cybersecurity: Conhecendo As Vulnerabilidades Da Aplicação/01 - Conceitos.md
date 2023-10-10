# Termos e Conceitos

## Ativo
- Tudo que tem valor para uma organização é um ativo para segurança da informação
    - Ex: Funcionários, Dados e informações, Bens físicos, Domínios
    - Segurança da informação não se trata apenas de cybersecurity

## Vulnerabilidade
- Fraqueza de um ativo, que pode se dar por uma má constituição ou uso

## Ameaça
- Tudo que pode impactar negativamente a organização

## Incidente
- Quando a vulnerabilidade é explorada
    - Ex: ataque DDOS

## Impacto
- Forma de medir oque um incidente causará para a organização
    - Depende do contexto da empresa/sistema afetados

### Perguntas a serem feitas para medir o impacto
- Causaria constragimento a alguém (terceiro, colaborador, instituição) ?
- O quanto atrapalharia a operação da instituição?
- Qual o custo ao negócio?
- A vulnerabilidade é fácil ou difícil de ser explorada?
    - Impacta na probabilidade de exploração da mesma
- Qual o custo para consertar?

### Níveis de impacto
- Varia de empresa para empresa
    - Muito baixo, baixo, médio, alto, muito alto
    - Baixo, médio, alto
- Risco = probabilidade * o impacto causado
- O nível de impacto pode variar de acordo com fatores externos, como por exemplo, uma campanha de marketing trazendo visibilidade para o negócio

## Qual o motivo para conhecer as vulnerabilidades?
**Conhecer as vulnerabilidades nos ajuda a saber onde investir**
**Conhecer as vulnerabilidades nos ajuda a saber nossos pontos fracos**
**Conhecer as vulnerabilidades nos ajuda a melhor a eficiência do negócio**


## Regras da segurança da informação (Relembrar é viver)

- Princípio do menor acesso (Segregação de função e acesso)
    - Somente o menor acesso ofertado para o acesso aos recursos
- A segurança é tão forte quanto seu elo mais fraco
    - Se um dos processos for fraco a chance de exploração é alta
- Todo acesso/envio de dados é mal intencionado até que se prove o contrário
    - Validações ineficazes, por exemplo
- Dividir para conquistar
    - Quando divído eu pratico o princípio do menor acesso

## Pilares da segurança da informação

- Confidencialidade
    - Tornar confidencial uma informação que tem um público seleto, restrito
- Integridade
    - Alterações feitas no documento precisam ser feitas por quem pode fazê-las apenas
- Disponibilidade
    - Estar acessível ao público destinado
- Conformidade
    - Legislações internas e externas
- Não-repúdio
    - Toda ação executada deve inibir a ação de negação por parte do usuário (logs, por exemplo)
- Autenticidade
    - Colabora com integridade e não repúdio


## Criptografia

- Escrita escondida
- Envolve chaves, conjuntos de valores matemáticos para embaralhar textos
    - Parte A e parte B
- Chaves
    - Simétrica e Assimétrica

### Chave simétrica
- Baixo custo computacional
- Mesmo meio
    - Ambas as partes ficam juntas

### Chave assimétrica
- Baseada em um par de chaves
    - Pública e privada
    - Ambas vinculadas
    - Quem abre a criptografia é a chave privada
- Alto custo computacional

### HTTPS
- Modelo híbrido, utiliza as duas formas

## OWASP
- É uma sigla para Open Web Application Security Project
- Documentos de categorias de vulnerabilidades
- Objetiva a conscientização
- Dividida em capítulos (Regionais)

### Top ten (2021)
- Quebra de acesso
- Falhas de criptografia
- Injeções
- Design inseguro
- Config incorreta
- Componentes vulneráveis e desatualizados
- Falhas de autenticidade
- Falha de integridade
- Falha no monitoramento ou insuficiência do mesmo
- Falsificação de request (SSRF)

### Ferramentas
- Dependency Check
- Dependency track monitor
    - Pode ser integrada com Pipelines
- Zed attack proxy
- Documentos
