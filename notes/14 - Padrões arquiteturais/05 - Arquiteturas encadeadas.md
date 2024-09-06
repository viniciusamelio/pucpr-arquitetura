# Arquiteturas encadeadas

- Caracterizado pela organização dos componentes em cascata
- Cada módulo/etapa/filtro é uma unidade autônoma de processsamento
- Cada etapa se comunica com a seguinte
    ->a->b->c

## Definição

**Pipe**: Conexão ponto-a-ponto e unidirecional
**Filtros**: Elemento onde ocorre o processamento
    - Independente dos demais filtros
    - Tipicamente não possuem estado
**Tipos comuns de filtros**: 
    - Produtores
    - Transformadores
    - Condicionais
    - Consumidores


## Quando utilizar?

- Processamento sequencial de informação
- Processamento de alto volume


## Ratings

| Característica          | Rating  |
| ----------------------- | ------- |
| Tipo de particionamento | Técnico |
| Unidades de implantação | 1       |
| Deployability           | 2       |
| Elasticidade            | 1       |
| Evolução                | 3       |
| Tolerância a falhas     | 1       |
| Modularidade            | 3       |
| Custo                   | 5       |
| Performance             | 2       |
| Confiabilidade          | 3       |
| Escalabilidade          | 1       |
| Simplicidade            | 5       |
| Testabilidade           | 3       |
