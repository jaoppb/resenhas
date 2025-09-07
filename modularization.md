# On The Criteria To Be Used in Decomposing Systems into Modules

Artigo: [https://dl.acm.org/doi/10.1145/361598.361623](https://dl.acm.org/doi/10.1145/361598.361623)

## Modularização

O artigo define o termo como um alinhamento de responsabilidades, que inclui as decisões de design do sistema que devem ser feitas antes da implementação.

## A KWIC Index Production System

Dois projetos para o sistema foram propostos: um baseado no fluxo de dados e o outro no princípio de _"information hiding"_. Cada um dos modelos se comporta melhor ou pior dependendo do tipo de mudança necessária. Por exemplo, ambos reagem bem à mudança no formato de entrada, devido ao módulo de entrada separado. Porém, caso a entrada seja muito grande e o processamento precise ser feito em disco em vez de em memória, seria mais interessante um reprojeto do sistema, pois todos os módulos esperam o acesso imediato às linhas.

Devido à separação feita no segundo modelo, o autor considera o custo computacional de chamadas de função frequentes. Acredito que isso deva ser considerado, mas as tecnologias recentes permitem que não precisemos nos preocupar tanto com esse tipo de _overhead_.

Por fim, o autor conclui com a proposta de que é melhor iniciar um modelo de sistema a partir de uma lista de dificuldades de design, na qual cada módulo esconde um item da lista dos outros módulos. Essa abordagem se contrapõe à do primeiro modelo, que foi criado a partir do fluxo de dados.
