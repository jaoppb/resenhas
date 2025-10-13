# Documenting Architecture Decisions

Artigo: [https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions.html)

## O Problema

O artigo aborda um problema comum em projetos de software, especialmente os que seguem metodologias ágeis: a falta de documentação sobre as decisões de arquitetura. Embora o desenvolvimento ágil se oponha a documentação excessiva e sem valor, o autor argumenta que não registrar o _porquê_ de decisões importantes pode tornar o projeto frágil. Sem esse registro, novos membros da equipe podem reverter uma decisão crucial sem entender suas consequências ou aceitar cegamente as decisões existentes, sem saber o contexto por trás delas.

## A Solução: Architecture Decision Records (ADRs)

Para resolver isso, o autor propõe o uso de "Registros de Decisão de Arquitetura" (ADRs). A ideia é simples: criar um documento curto e focado para cada decisão arquitetural significativa. Cada ADR é um artefato que captura o contexto, a decisão tomada e as suas consequências. O objetivo é que esses registros sejam leves e fáceis de manter, ao contrário da documentação arquitetural tradicional, que muitas vezes é pesada e rapidamente se torna obsoleta.

## Formato e Prática

O artigo sugere um formato para os ADRs, que deve incluir as seguintes seções:

-   **Título**: Um resumo da decisão.
-   **Contexto**: As forças e o cenário que levaram à necessidade da decisão.
-   **Decisão**: A descrição da decisão tomada, de forma clara e ativa (ex: "Vamos usar...").
-   **Status**: O estado da decisão (proposta, aceita, substituída, etc.).
-   **Consequências**: Os resultados esperados da decisão, tanto os positivos quanto os negativos.

A recomendação é que esses registros sejam mantidos em um formato de texto simples, como Markdown, e versionados junto com o código-fonte do projeto. Isso os torna acessíveis a toda a equipe e garante que eles evoluam com o sistema.

## Conclusão

A prática de usar ADRs se mostra uma ferramenta valiosa para manter a clareza e o alinhamento em um projeto de software ao longo do tempo. Ela ajuda a integrar novos desenvolvedores, a justificar as escolhas de design e a preservar o conhecimento arquitetural, mesmo com a rotatividade da equipe. É uma abordagem pragmática que equilibra a necessidade de documentação com a agilidade do desenvolvimento.
