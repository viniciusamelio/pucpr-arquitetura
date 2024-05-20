# Testes I

Relizados após o threat modeling 

## Fuzzing

- Testes de entrada no software, esperando um output específico
    - Identifica crashes e saída de dados indesejados
- Fuzz as a service

## Revisões

- Ciclos de revisão do software
- Análise estática do código

## Vetores de ataque

- Expõe métodos de entrada que podem ser utilizados para ataques
- Identificando portas e protocolos que sirvam como vetores
- Hardening = Diminuir os vetores de ataque
    - Muito comum na configuração de SOs
- Baseline: determinado padrão, sem demais recursos além dos previstos técnicamente liberados

## Reutilização de código

- Uso de código não revisado corretamente pode abrir brecha para vulnerabilidades

## Antiadulteração

- Garantir que o software é genuíno
- Code signing

## Versão de código

- Build number


## Performance

- Testar condições de resposta do software em ambientes variáveis
- Dimensionamento de acordo com a SLA do produto/companhia
- DDOS explora performance
