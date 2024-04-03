# Serverless

## Containers

> Na minha máquina funciona

- Antes era uma dor fazer o deploy de aplicações em um ambiente produtivo pela divergência de ambientes de desenvolvimento
- As VMs surgem como uma forma de encapsular tudo para rodar o software, na teoria. Na prática a granularidade das dependências e do SO faziam ainda haver uma dor
- Parâmetros de configurações bem definidos


### User Space

- Parte depois que o SO está inicializado
- Onde todas minhas apps estão sendo executadas
- Conceito difundido a partir de 2005, com o Solaris 10 (Sun Microsystems)
- Em 2013 surge o Docker

### User Space com Docker

Hardware->SO->Docker Engine->Containers->Apps