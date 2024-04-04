# Serverless

## Características
- Mão preciso gerenciar a infra
- Serverless != FaaS 
- Pago somente pelo uso (Pay as you go)
- Alta disponibilidade
- Escalabilidade

## Complexidade essencial x acidental

### Essencial
> Caminho mais curto entre dois pontos
- Necessária para o desenvolvimento do produto

### Acidental
- Normalmente gerada por desenvolvedores ou arquitetos, através da implantação de determinados designs de aplicação

## Responsabilidade operacional

A responsabilidade operacional é diretamente proporcional ao número de componentes que eu tenho controle sobre

On-Premises->IaaS->CaaS->PaaS->FaaS

## Prós e contras

### Prós
- Pagar somente pelo uso
- Maximizar receita
- Não precisar gerenciar servidores
    - Relação direta com custos
- Alta disponibilidade por padrão
- Maior proximidade com o modelo de complexidade essencial
    - Nada a mais necessário para chegar do ponto A ao B
- Menor time to market
- Maximização de reuso
    - Especificamente para functions

### Contras
- Maior dependência do fornecedor (Vendor lock-in)
- Menos controle
- Observabilidade mais complexa
- Tunning se faz necessário numa maior escala
- Controle de lifecycle e coreografia de lambdas pode ser necessário de acordo com limites de execução
- Dificuldade de testes

> Comece utilizando devops desde o início do projeto
