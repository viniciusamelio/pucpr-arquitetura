# Primeira maneira

## Fluxo

- Pipeline de implantação


### Resumo da integração contínua

Controle de versão -> Processo de compilação -> Testes e análise de código

### Resumo de entrega contínua

Deploy em homolog -> testes e análise de código -> Pronto para deploy em prod

### Resumo de implantação contínua

Deploy em homolog -> testes e análise de código -> Deploy em prod


### Infra como código (IaC)

> Hoje a infraestrutura é um código

- Código e configuração dentro do controle de versão
- Criação automatizada e sob demanda em todos os ambientes, evitando trabalho manual
- Todos os estágios do fluxo de valor com ambientes iguais ou semelhantes ao de produção
- Infraestutura imutável: foco em recriar todo o ambiente de produção de forma rápida em vez de realizar alterações

### Serverless

- Backend as a service
- Function as a service

### Definition of done

- Compartilhada entre os times
- Garantia de qualidade

### Controle de versão

- Documentação específica e detalhada
- Rastreabilidade

### Testes automatizados

--

### Release de baixo risco

- Categorias de liberação release
    - Baseado no ambiente
        - Há 2 ou mais ambientes e apenas fica ativo para os clientes
        - Blue-green e Canary
    - Baseado no app
        - Novas features de forma seletiva usando configurações simples (Não precisa de deploy)
        - Alternância de recursos (Feature toggles) e Lançamento escuro

#### Azul-verde

- Balanceador define qual ambiente o usuárion estará acessando
- Existe um ambiente 100% ativo
- Implantação ocorre em ambientes com poucos usuários

#### Feature toggle

- Avaliar resultados sem o usuário perceber que está sendo testado
- Entregar release sem a preocupação com a "qualidade do código"

### Arquitetura de baixo risco

- Microsserviços
    - Cada unidade é simples, escalonamento independente, teste e implantação independente, facilita versão por produto
    - Latência na rede, Precisa de ferramentas para gerencias dependências
- Monolitos
    - Inicialmente simples, Baixa latência entre processos, Eficiente para recursos em pequena escala
    - Fraca escalabilidade e redundância, Implantação big bang, Longo período de build