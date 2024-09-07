# Microkernel

- "Core" do sistema
    - Kernels menores ou "Plugins" complementares ao core
    - Gerencia a existência dos outros plugins
- Lógica de negócio distribuída pelos plugins
- Arquitetura em camadas utilizadas em nível micro
- Nos plugins as funcionalidades encontradas são bem especializadas
    - Responsabilidades bem definidas
- Os plugins podem se comunicar com o núcleo em JIT ou AOT
- Os plugins são auto-contidos e independentes, permitindo uma maior escalabilidade
- Uso de Registry, onde esses plugins são registrados.
    - Contratos dinâmicos
    - Mecanismo de propagação de conhecimento entre os plugins
    - Uso de metadados
- Discovery
    - Padrão do Core de descobrir quais os plugins existentes
        - Ex: Identificar todas as dlls carregadas no projeto

## Eclipse

- IDE que utiliza arquitetura Microkernel
    - OSGI é o core
- Plugins em arquivos .jar
    - Arquivo de manifest define os metadados daquele plugin


## Quando utilizar

- IDEs ou aplicações de desenvolvimento
- Sistemas de automação com suporte a diversos devices diferentes
- Aplicações no modelo Freemium


- Aplicações com conceito de plugabilidade por design
