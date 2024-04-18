# Boas práticas

## API Gateway
- Sempre utilize ao invés de chamar diretamente as functions
- Flexibilidade maior

## Uma função por rota
- Escopar e delimitar bem a função a ser exposta na rota
- Uma única função com várias responsabilidades produz erros diversos

## Testes
- Fluxos e frameworks em metodologias tradicionais de desenvolvimento de software podem ser reaproveitados aqui
- Ambientes distribuídos e desacoplados possuem maiores pontos e possibilidades de quebra

## Desenvolva localmente
- Diversos frameworks e ferramentas para desenvolvimento local
- Vários gateways podem ter acoplada uma estrutura de mockup, que ajuda nesse ponto

## Configs e parâmetros fora da função
- Uso de envs
- Etcd
- Redis
- Bases não relacionais

## Logs em todas as camadas
- Elastic Search

## Id único de transação
- Idémpotência para realizar o tracing do fluxo
- Use chaves não identificáveis, como uuid's
- Gere na borda (client)

## Funções efêmeras
- Não manterá o estado por um período longo de tempo
- Considere que o ambiente sempre será descartado

## Coldstart
- Delay do início do ambiente até a execução do código

## Evite wait time
- Modelo de pagamento pay as you go faz com que esperas gerem despesas
- Use assincronismo e coreografia

## Evite funções monolíticas
- Um monte de código sendo empacotado como uma única função

## Gerenciar dependências
- Verificar o uso das dependências e criar mecanismos para checar onde/quanto determinada lib é utilizada
- Diminui coldstart e custo

## CI/CD
- Comece desde o início a utilizar

## Tempo total de execução
- Não somente coldstart e nem execução do código
- Crie métricas para monitorar eventuais desvios

## Fine tunning de processos de cpu
-  Se o código for baseado em cpu, quanto mais cpu mais rápido ele executará, logo, quanto menos utilizar da cpu, melhor
- Acompanhar percentis 95~98
- Fazer com frequência durante o desenvolvimento das funções

## Custo total da solução
- Pode acontecer de uma solução serverless ter um custo maior
- custo != valor
    - considerar benefícios propostos por serverless

## Minificação do código
- Economiza o espaço da função
- Melhora o coldstart

## Separar handler de lógica de negócio
- Previne vendor lock-in
- Pacotes portáveis com lógica

## Idempotência
- Execução do código várias vezes sem alterar o resultado
- Tratar duplicidades
- + Coreografia e - orquestração
