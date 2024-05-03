# Automação

- Para a maior quantidade possível de checks normalmente é usado automação
- Utilizando checagem manual apenas para pontos estratégicos
- Não automatizar checks que possam trazer riscos quando feitos de maneira automatizada

## Pirâmide de testes de segurança

- Testes manuais
- DAST
- IAST/RASP
- Imagem/containers scan
- Scan de dependências
- SAST/ Testes unitários


> Quanto mais abaixo, mais barato para realizar esses testes

## SAST - Static app security testing

- Avalia todo o código fonte de uma app
- Busca por más práticas de coding
- Não simula ataques
- Muitos falsos positivos

## DAST - Dynamic app security testing

- Teste de caixa preta- sem acesso ao código fonte
- Simula ataques comuns a uma aplicação
- SQL injection, DDOS, XSS
- Custo mais elevado
- Menos falsos positivos

## MAST - Mobile app security testing

- Rodam em diversos tipos de devices
- Estão em uma rede aberta, mais exposta
- Dados devem ser armazenados de forma segura, evitando acesso por outros apps

## Container image scanning

- Immagens de containers carregam código e sistema operacional em um único artefato
- Executa checks para avaliar se existem brechas para invação - Ex: porta ssh aberta
- Verifica ferramentas instaladas no containers que podem trazer risco - Ex: bash shell