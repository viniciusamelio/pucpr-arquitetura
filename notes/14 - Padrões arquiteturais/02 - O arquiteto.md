# O arquiteto

- Entende compromissos e o equílibrio entre requisitos para atender ao cliente
    - Levando em conta: tempo, orçamento, time, infraestrutura, políticas internas.

## Como escolher?

- Identificar os motivadores de negócio
    - NOTA: Motivador nem sempre aparece como requisito
    - O que é óbvio para a área de negócio nem sempre é óbio para outros
    - Pergunte, pergunte, pergunte
    - Pergunte para várias pessoas
- Prova de conceito
- Analisando requisitos e identificando características

### Tópico X Fila (Exemplo)

- Fila fornece privacidade e segurança, além de uma especialização
- Tópico fornece uma grande extensibilidade


### Características

- Operacional
- Design
    > A característica de design é influenciada pela arquitetura
- Estruturais
    - Como o sistema está modularizado
    - Configuração e parametrização do sistema para atender diferentes ambientes e cenários
    - Extensibilidade
    - Localização
    - Facilidade de implantação
    - Facilidade de manuteção
    - Fácilidade de portabiliade
- Transversais (Difícil de identificar como um tipo)
    - Acessibilidade
    - Autenticação e autorização
    - Parte legal do sistema
    - Privacidade de dados


## Selecionando Características

> Cada característica adiciona complexidade e podem ser conflitantes

- Como o arquiteto deve atuar?
    - Priorização
    - Iteração
- Origem das características
    - Domínio da aplicação/negócio
    - Requisitos
    - Conhecimento prévio

### Extraindo características de domínio

- Crítico para priorizar corretamente as características
- Motivadores de negócio > Características

| Motivador | Características   |
| -------- | -------------------|
| Time-to-market | Agilidade, testabilidade, velocidade de implantação |
| Custo        | Simplicidade |
| Satisfação do cliente| Performance, segurança, testabilidade, disponibilidade | 

> Você tem que olhar além dos requisitos apresentados


## Componentes de arquitetura

- Unidade de implementação
    - Desenvolvida por um/alguns desenvolvedor(es) que geram um artefato a ser incorporado na arquitetura

### Definindo componentes

Identificar componentes iniciais (1) -> Atribuir requisitos aos componentes (2) -> Rever papéis e responsabilidades (3) -> Analisar características (4) -> Reestruturar componentes (5) -> Atribuir requisitos aos componentes (2)

- Identificar componentes iniciais
    - Apenas um rascunho para inicial o processo
    - aka Sopa de Pedra
- Atribuir requisitos aos componentes
    - Mapear requisitos/histórias em um "teste de mesa"
    - Quebra-los e consolida-los
- Revisão de papeis e responsabilidades
    - Revisar a granularidade dos componentes
- Analisar características de arquitetura
    - As características da arquitetura utilizada para o componente batem com suas responsabilidades?
- Reestruturar componentes

