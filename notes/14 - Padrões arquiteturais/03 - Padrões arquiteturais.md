# Padrões arquiteturais

## Definição

- Um "apelido" para um conjunto de componentes usados de uma determinada maneira, com determinadas características
- Uma forma mais eficiente de comunicação
- Não é um padrão de design

## Padrões fundamentais

### Big ball of mud

- Ausência de estrutura reconhecível
- Cenário típico:
    - Aplicações web com chamadas SQL diretamente nas views
    - PoC ou demo que era para ser descartado

### Cliente-servidor

- Cliente faz requests diretamente ao servidor, aguardando uma resposta

### Monolito

- Apenas uma unidade de implantação
- Simpes de implementar
- Mais barato de implementar inicialmente
- Mais rápido de implementar

### Distribuído

- Mais de uma unidade de implantação