# Microserviços

Artigo: [https://martinfowler.com/articles/microservices.html](https://martinfowler.com/articles/microservices.html)

## Resenha

O artigo começa com uma pequena introdução ao conceito de microserviços, definindo como vários programas, ou módulos, que se comunicam por protocolos de comunicação leves e rápidos. Também é comparado aos sistemas monolíticos que resolvem o problema de escalabilidade horizontalmente.

Um ótimo paralelo que sempre vem à minha mente quando se fala de microserviços é a separação de classes em POO, principalmente com a responsabilidade única envolvida.

### Características

#### Componentes

O ponto sobre componentização é trazido novamente, desta vez citando bibliotecas e diferenciando os serviços por sua chamada remota. A principal vantagem do serviço é sua capacidade de ser _deployable_ independentemente de outras partes do sistema, como sempre existem exceções mas esse tópico não é explorado muito a fundo. Em seguida vem a principal desvantagem em comparação com as bibliotecas que são o custo de cada chamada remota, que trazem um peso muito maior do que umas simples _system call_.

#### _Boundaries_

Outro ponto trago pelo autor é o quão grande deve ser cada time cuidando de um serviço, e atualmente nas _BIG Techs_ existem variações mas no geral são times de 6 à 12 pessoas.

#### Projetos X Produtos

Mais uma comparação traga são projetos e produtos, onde projetos são desenvolvidos por um time e mantidos por outro, e produtos o mesmo time que o desenvolveu o mantém durante todo o seu período de vida útil. Esta última é mais adotada pelos times que implementam a arquitetura de micro serviço e ajuda o time a ter uma relação mais próxima com seus usuários.

#### Comunicação

Neste momento o princípio da comunicação são _smart endpoints and dump pipes_, _smart endpoints_ por causa da lôgica aplicada pelos serviços e _dump pipes_ por agirem como um simples roteamento de mensagens. Outra complicação que surgem na refatoração do sistema monolíto para microserviços são as comunicações, que em memória são muito rápidas e não são ótimizadas usualmente, porém quando transformadas em requisições HTTP, por exemplo, se tornam inviáveis, tendo que serem repensadas em chamadas que buscam mais conteúdo de uma vez.

#### Multi-linguagem

Mais uma consequências da arquitetura discutida é a capacidade de se utilizar várias linguagens de programação no mesmo _software_, apesar de que você não deve fazer isso somente por poder, mas sim com um objetivo bem definido e clara na sua mente do motivo da escolha.

#### _Data Independency_

Como cada componente pode ter seus dados desacoplados dos outros, fica mais coerente cada visão que faça sentido para o contexto sendo lidado, em contrapartida se não gerido adequadamente pode surgir redundâncias.

#### Testes

Como as "interfaces publicadas" definem como aquela parte do sistema se comunica externamente, é vital que testes sejam escritos e executados para garantir que os times não quebrem o sistema descuidadamente.

#### _Downtimes_

Com o baixo nível de acoplamento entre os serviços surge a complexidade de se lidar com a indisponibilidade de cada um, se tornando uma desvantagem em comparação com o monolíto. Além da necessidade de monitoramento que deve ser implementada na infraestrutura para alertar o time em casos de erro no serviço.

### Conclusão

O autor finaliza com as perspectivas futuras da arquitetura de microserviços, citando que já utilizou do padrão em alguns projetos e também que algumas grandes empresas estão utilizando-a, mesmo que por outro nome. Além disso, a complexidade trazida pela arquitetura pode não fazer sentido a escolha, onde o problema é movido da parte interna para a comunicação entre os contextos.
