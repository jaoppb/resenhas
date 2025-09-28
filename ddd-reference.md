# Domain Driven Design Reference

Artigo: [https://www.domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf](https://www.domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf)

Esta resenha contempla os capítulos 4, 5 e 6 do artigo.

## Mapeamento de Contexto

Para gerenciar a complexidade em sistemas grandes, onde múltiplos modelos coexistem, o DDD introduz o conceito de _Bounded Context_, que define as fronteiras onde um modelo específico é aplicável. O _Context Map_ é a ferramenta utilizada para visualizar e gerenciar as relações entre esses contextos. Alguns padrões de relacionamento entre contextos são:

-   **Partnership**: As equipes de dois contextos dependem uma da outra para o sucesso, exigindo cooperação no planejamento e integração.
-   **Shared Kernel**: As equipes concordam em compartilhar um pequeno subconjunto do modelo e do código, que não pode ser alterado sem consulta mútua.
-   **Customer/Supplier**: Uma equipe downstream (cliente) tem suas prioridades consideradas no planejamento da equipe upstream (fornecedor).
-   **Conformist**: A equipe downstream adota o modelo da equipe upstream para simplificar a integração, mesmo que não seja o modelo ideal.
-   **Anticorruption Layer**: A equipe downstream cria uma camada de tradução para isolar seu modelo do modelo upstream, evitando que seu próprio modelo seja corrompido.
-   **Open-Host Service**: Um subsistema define um protocolo público para que outros sistemas possam se integrar a ele como um conjunto de serviços.
-   **Published Language**: Uma linguagem de domínio bem documentada é usada como meio de comunicação comum entre contextos.
-   **Separate Ways**: Declara-se que dois contextos não têm nenhuma conexão, permitindo que evoluam de forma independente.
-   **Big Ball of Mud**: Uma parte do sistema onde os modelos são misturados e as fronteiras são inconsistentes é isolada como um contexto próprio para não contaminar o restante do sistema.

## Destilação

A destilação foca em separar os componentes essenciais do modelo para concentrar os esforços de desenvolvimento no que realmente agrega valor ao negócio. As principais estratégias são:

-   **Core Domain**: Identificar e destacar a parte mais valiosa e especializada do modelo, aplicando os melhores talentos a ela. O modelo deve ser pequeno e enxuto.
-   **Generic Subdomains**: Fatorar partes do modelo que não são a motivação principal do projeto em módulos separados, considerando o uso de soluções prontas.
-   **Domain Vision Statement**: Um documento curto que descreve o valor do domínio principal e como ele equilibra os interesses, servindo como guia para a equipe.
-   **Highlighted Core**: Tornar o domínio principal facilmente identificável para os desenvolvedores, seja através de um documento que descreve os elementos principais ou marcando-os diretamente no código.
-   **Cohesive Mechanisms**: Extrair algoritmos complexos e bem definidos para um framework leve e separado, permitindo que o resto do domínio se concentre no "o quê" em vez do "como".
-   **Segregated Core**: Refatorar o modelo para separar fisicamente os conceitos do núcleo dos elementos de suporte, fortalecendo a coesão do núcleo e reduzindo seu acoplamento.
-   **Abstract Core**: Identificar os conceitos mais fundamentais do modelo e fatorá-los em classes ou interfaces abstratas, criando um modelo de alto nível que expressa a interação entre os componentes principais.

## Estrutura em Larga Escala

Este capítulo aborda a necessidade de um princípio organizador que abranja todo o sistema, permitindo que os desenvolvedores entendam o papel de cada parte no todo. Essa estrutura deve evoluir com a aplicação, ou seja, é uma _Evolving Order_. Os padrões apresentados são:

-   **System Metaphor**: Usar uma analogia concreta e simples que capture a essência do sistema para guiar o design e se tornar parte da linguagem ubíqua.
-   **Responsibility Layers**: Identificar estratos conceituais no domínio e atribuir responsabilidades amplas a cada camada, de modo que cada objeto do modelo se encaixe em uma delas.
-   **Knowledge Level**: Criar um conjunto distinto de objetos (o nível de conhecimento) que descreve e restringe a estrutura e o comportamento do modelo básico (o nível operacional), permitindo customização.
-   **Pluggable Component Framework**: Em um modelo maduro, destilar um núcleo abstrato de interfaces e criar um framework que permita que diferentes implementações desses componentes sejam livremente substituídas e usadas por qualquer aplicação.
