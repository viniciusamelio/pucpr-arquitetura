# CI/CD em multicloud

- CI
    - Integração contínua, é a prática de mesclar todas as cópias de trabalho dos desenvolvedores em uma linha principal compartilhada, várias vezes ao dia
- CD
    - Prática na qual as equipes produzem um entregável em ciclos curtos, garantindo que o software possa ser lançado com segurança a qualquer momento


## 12 Factor App

- Codebase: Código em um sistema de controle
- Dependencies: as dependências devem ser declaradas e isoladas
- Config: Configurações podem variar entre ambientes diferentes
- Baking services: A base de código não difere bibiliotecas e APIs
- Build, release, run: Separar estritamente os builds e executar em estágios
- Processes: Processos de 12 factors não gravam estado
- Port binding: A porta a qual o app está conectado também é salva no config
- Concurrency: concorrência é simples e confiável
- Disposability: Devem ser iniciados ou parados o mínimo possível
- Dev/Prod parity: São projetos para implantações contínuas, mantendo disparidades entre os ambientes de prod e dev
- Logs: Tratar logs como fluxo de eventos
- Admin process: Executar tarefas de gerenciamento, como processos únicos (execução de banco de dados ou execução de scripts)