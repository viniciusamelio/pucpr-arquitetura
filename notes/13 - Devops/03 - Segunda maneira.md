# Segunda maneira

## Telemetria

> Sem medição você não faz nada

- Ter a visão do todo
    - Exp do cliente em relação ao seu produto
    - Erros na pipeline
    - Heatmaps


### Tipos

- Sistema operacional
- Lógico de negócio
- Aplicativo

Todos esses registros são armazenados e podem emitir alertas

### Telemetria self-service

- Todo mundo precisa conhecer e analisar esses resultados
- Acesso liberado sem abertura de tickets
- Métricas devem ser criadas como parte do trabalho diário das equipes
- Sugerido usar irradiadores de infos visível para todos


## Feedback

- Visão clara do fluxo de valor em todos os estágios do ciclo de vida do serviço
- Usado para tomar decisão rapidamente

### Opções para resolver os problemas

- Fast foward
    - Executar o fix no ambiente de prod
- Rollback


### Site Reliability Engineering - SRE

- Um representante da equipe que entende tanto operação quanto engenharia, que garante que o time entenda todas as questões operacionais
    - Quase uma "consultoria"
    - Garante uma transição tranquila para produção
    - Mede quanto a aplicação está saudável

### UX

- Entender como os clientes usam o software
    - Pesquisa contextual


### Testes A/B

- Testar acurácia de funcionalidades "concorrentes"
- Experimentação de novos recursos
- Baseado em fatos e dados
- Pode ser utilizado com feature toggle e rollout faseado


### Desenvolvimento orientado por hipóteses

- Confirmar se as features realmente serão usadas


### Pull Request

- Evitar pensamentos de "Nem vou revisar pq foi fulano quem fez"
> É importante alguém avaliar o que você faz

- Pessoas mais próximas tem uma probabilidade maior de contribuir melhor

#### Técnicas de revisão

- Análise horizontal
- Revisão de código assistido por ferramentas
- Pair Programming