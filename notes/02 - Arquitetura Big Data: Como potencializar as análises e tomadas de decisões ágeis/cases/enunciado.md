# Processamento de atendimentos e análise de trabalho por tipo de evento

## Relação com o tema da disciplina

- Dados de diversas Origens;
- Datalake para processamento dos dados;
- Pipelines de processamento de dados;
- Análise de dados estruturados e semi-estruturados;
- Banco de dados tabular.

## Ferramentas e métodos

- Análises Quantitativa e Preditiva;
- Datalake para processamento dos dados;
- Pipelines de processamento de dados;
- JSON, dados estruturados e semi-estruturados.


## Descrição do case

O gestor de uma equipe de sustentação (suporte à infraestrutura de TI) observou repetição de incidentes em seu sistema de monitoramento. Preocupado com o tempo consumido por sua equipe com atividades repetitivas e a possível indisponibilidade de analistas para suporte à novos eventos, iniciou uma análise do trabalho de equipe e dos eventos de monitoramento. <br>
Quais riscos foram identificados pelo gestor: <br>
- Alto índice de trabalho repetitivo, com potencial desmotivacional;
- Frequente sobrecarga de profissionais e pouca disponibilidade;
- Risco de falta de atendimento para novos casos ou de maior gravidade
- Risco de atendimento incompleto ou falho causado por atividades repetitivas (não seguimento do processo).
Para embasar suas preocupações, o gestor iniciou o armazenamento de todos os eventos gerados pelo monitoramento em uma área de armazenamento na nuvem. Os dados gerados pelo sistema de monitoramento são em formato JSON, enviados à nuvem no momento do disparo. <br>
**OBS: O Armazenamento de dados utilizado para este caso foi o Azure DataLake Gen2.**
Ao sumarizar os principais eventos, apenas durante um dia, ele pode observar:
/ 72 alarmes para erro de horário em servidores Linux;
/ 69 alarmes para tentativa de acesso com credenciais inválidas em servidores Windows;
/ 43 alarmes para erro de horário em servidores Windows;
/ 20 alarmes para erro de processamento acima do normal em servidores Linux.
O gestor pode facilmente observar um volume alto de servidores que apresentavam incoerência de horário, onde a máquina apresentava um horário acima de 60 segundos de diferença para o horário real.
Sabendo agora o montante de alarmes gerados pelos eventos e conhecendo o principal tipo de alarme gerado (horário com defasagem), restava analisar o impacto no consumo de horas dos analistas e confirmar o alto consumo de cada profissional. Para isso, foi montado um comitê para análise do consumo de horas em atividades por profissionais.
Todas as horas trabalhadas pelos profissionais são armazenadas em um ERP da companhia, onde constam as horas trabalhadas, o horário de início e fim da atividade, os passos executados para resolução do problema e o executor da atividade. Com esta necessidade, de uma análise mais aprofundada, todas as atividades trabalhadas do sistema de ERP, de forma diária, começaram a ser salvas na mesma nuvem onde o gestor de sustentação gravava os eventos de monitoramento. Os dados do ERP eram salvas em arquivos de planilha, em formato CSV.
Neste ponto, o gestor tinha todos os dados necessários para levantar as informações desejadas.
/ Alarmes gerados pelo monitoramento em formato JSON [semi-estruturado]
/ Atividades trabalhadas pelos analistas em CSV [semi-estruturado]
Para que fosse possível relacionar os conteúdos gerados e que sua apresentação fosse o mais legível possível, foi necessário o trabalho dos dados. No caso, os dados armazenados em um datalake foram trabalhados usando pipelines de processamento de dados e armazenados em tabelas num banco de dados tabular, na mesma nuvem.
OBS: Os pipelines foram trabalhados com Azure Synapse Analytics.
Com os dados formatados, normalizados e relacionados, foi possível acompanhar o trabalho da equipe e observar, com defasagem de um dia, os trabalhos repetitivos, permitindo ações pontuais para a resolução.

## Insights e perguntas para debate

/ Neste caso, apenas dois sistemas foram relacionados. Poderíamos adicionar um sistema financeiro e analisar o impacto financeiro das atividades repetitivas?
/ Sabendo que as atividades exercidas de forma repetitiva estão documentadas, poderíamos automatizá-las?
/ Podemos aplicar soluções de Machine Learning nos dados gerados para identificar vícios ou usuários com maior facilidade (melhor tempo) para determinados atendimentos?
/ Outras áreas da companhia podem se beneficiar desta solução?
/ Podemos entregar a outros gestores dashboards customizáveis para esta solução?
/ Quais cuidados devem ser tomados para que os dados não sejam vazados? Quais usuários podem acessar quais valores? Linhas? Arquivos?
/ Se modificarmos o sistema de ERP para enviar os dados no momento do lançamento ao datalake, poderíamos trabalhar em processamento Stream?
/ O que o gestor esqueceu de levantar (ou não informou) antes de executar as atividades?
    - Os sistemas analisados (?)

