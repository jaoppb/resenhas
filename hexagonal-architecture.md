# Arquitetura Hexagonal

Artigo: [https://alistair.cockburn.us/hexagonal-architecture](https://alistair.cockburn.us/hexagonal-architecture)

## O Problema

Alistair Cockburn introduz a arquitetura hexagonal, ou "Portas e Adaptadores", como uma solução para problemas comuns em arquiteturas de software tradicionais, como a arquitetura em camadas. O principal problema abordado é o acoplamento da lógica de negócios com componentes externos, como interfaces de usuário (UI), bancos de dados e sistemas de teste. Esse acoplamento dificulta a evolução do software, a realização de testes automatizados e a substituição de tecnologias. Em sistemas tradicionais, a lógica de negócios acaba se misturando com a lógica da UI e do banco de dados, tornando o sistema rígido e frágil.

## A Solução: Portas e Adaptadores

A ideia central da arquitetura hexagonal é criar uma clara separação between o "interior" e o "exterior" da aplicação. O "interior" contém a lógica de negócios pura, sem conhecimento de tecnologias externas. O "exterior" é composto por "adaptadores" que interagem com o mundo externo. A comunicação entre o interior e o exterior é feita através de "portas", que são interfaces que definem um contrato de comunicação.

-   **Portas**: Definem a API da aplicação. Existem portas para os "atores primários" (que iniciam a interação, como um usuário através de uma UI) e para os "atores secundários" (que são acionados pela aplicação, como um banco de dados).
-   **Adaptadores**: São a implementação das portas. Por exemplo, um adaptador de UI traduz as ações do usuário em chamadas para as portas da aplicação. Um adaptador de banco de dados implementa a interface de uma porta de repositório, traduzindo as chamadas da aplicação em queries SQL.

O termo "hexagonal" é uma metáfora para ilustrar que não há apenas "topo" e "base" como na arquitetura em camadas, mas sim múltiplos pontos de entrada e saída (portas) na aplicação.

## Vantagens

A principal vantagem dessa arquitetura é a flexibilidade e a testabilidade. Como a lógica de negócios é isolada, ela pode ser testada em total isolamento, usando adaptadores de teste (mocks ou stubs) no lugar de um banco de dados real ou de uma UI. Isso permite testes mais rápidos e confiáveis. Além disso, a aplicação pode ser facilmente adaptada a novas tecnologias ou requisitos, bastando criar novos adaptadores sem alterar a lógica central. Por exemplo, uma aplicação pode ser controlada tanto por um usuário, quanto por um sistema de testes automatizados, ou por outro programa, simplesmente trocando-se os adaptadores.

## Conclusão

A arquitetura hexagonal promove a construção de sistemas mais manuteníveis e resilientes a mudanças tecnológicas. Ao impor uma separação estrita entre a lógica de negócios e as preocupações externas, ela permite que a aplicação evolua de forma mais sustentável. A complexidade é gerenciada isolando as dependências externas em adaptadores, o que torna o núcleo do sistema mais coeso e focado no domínio do problema.
