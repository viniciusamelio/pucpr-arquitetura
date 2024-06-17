# Tipos de consumo de modelos de IA

## Batch
Quando temos um grande volume de dados e o consumo destes não precisa ser em realtime, jobs de batch fazem a diferença.

- Inferências diárias
    - Exemplo: Análise de clientes em risco
- Variação baixa
- Grande número de registros com necessidade de inferência a esse grande número de registros

### Passos

- Nem sempre o dado chega pronto como necessitado para a inferência
- Pode ser necessário uma transformação (Batch transform)
- Após a inferência uma base dados, normalmente, armazena o resultado
- Importante monitorar o modelo

## Realtime
Cenário oposto ao batch, inferência necessária em ms's.

- Cenário muito dinâmico

### Passos

- Pré-processamento em ms
- Modelo servido em uma API
- Monitoramento
- Retreinar o modelo

## Edge
Acesso à internet limitado, como em drones, carros, trens.

### Passos

- Otimizar o artefato do modelo pro hardware
- Modelo servido localmente
- Atualizações OTA
- Monitorar e re-treinar ao longo do tempo