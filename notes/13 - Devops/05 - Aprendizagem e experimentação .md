# Aprendizagem e experimentação

## Aprendizado com falhas

- Netflix criou um processo de injeção de falhas chamado Chaos Monkey que aumenta a resiliência
- O foco é desenvolver aprendizado contínuo nas equipes e evitar a cultura de culpa e punição

## Exercício de Símios Netflix

### Chaos Gorilla

- Simula uma falha de zona de disponibilidade inteira, como AWS

### Chaos Kong

- Simula indisponibilidade em pequenas zonas (SA,EU, Virginia, etc)

### Latency Monkey

- Causa atrasos em dependências de serviços, como se o ambiente estivesse se degradando aos poucos

### Janitor Monkey

- Garante que o serviço está livre de desperdício, procura recursos não utilizados e os desliga

### Conformity Monkey

- Localiza e desliga instâncias AWS que não seguem as melhores práticas

### Doctor Monkey

- Verifica integridade de cada instância

