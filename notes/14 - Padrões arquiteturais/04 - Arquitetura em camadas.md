# Arquitetura em camadas

- Cada camada é responsável por um determinado papel na aplicação
    - Ex: Apresentação, negócio, persistência, dados

> Existe um mapeamento relativamente simples entre as capacidades das pessoas, as competências das pessoas e a arquitetura técnica que você está propondo

## Camada aberta / Camada fechada

- Um princípio que diz respeito ao "pulo" de camadas
    - Domínio nunca chama camada de persistência

## Quando utilizar

- Domínio único de negócio
- Aplicações simples

## Ratings

| Característica          | Rating  |
| ----------------------- | ------- |
| Tipo de particionamento | Técnico |
| Unidades de implantação | 1       |
| Deployability           | 1       |
| Elasticidade            | 1       |
| Evolução                | 1       |
| Tolerância a falhas     | 1       |
| Modularidade            | 1       |
| Custo                   | 5       |
| Performance             | 2       |
| Confiabilidade          | 3       |
| Escalabilidade          | 1       |
| Simplicidade            | 5       |
| Testabilidade           | 2       |

