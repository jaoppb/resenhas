# Managing Technical Debt

Artigo: [https://www.construx.com/uploadedfiles/resources/whitepapers/Managing%20Technical%20Debt.pdf](https://www.construx.com/uploadedfiles/resources/whitepapers/Managing%20Technical%20Debt.pdf)

O artigo de Steve McConnell utiliza a metáfora de dívida financeira para explicar o conceito de "dívida técnica": o trabalho técnico adiado que surge quando atalhos são tomados para cumprir prazos. Assim como a dívida financeira, algumas dívidas técnicas podem ser estratégicas, enquanto outras são apenas resultado de um trabalho de baixa qualidade. O autor defende a tomada de decisões explícitas antes de incorrer em dívidas e o rastreamento delas para um gerenciamento eficaz.

## Tipos de Dívida

O artigo categoriza a dívida técnica para melhor compreensão e gerenciamento:

-   Não Dívida: Backlog de funcionalidades, funcionalidades adiadas ou cortadas não são consideradas dívidas, pois não exigem "pagamento de juros".
-   Dívida Não Intencional: Surge de um trabalho de baixa qualidade, como um design que se mostra propenso a erros ou código mal escrito, sem intenção estratégica.
-   Dívida Intencional: Ocorre quando uma organização decide conscientemente otimizar para o presente em detrimento do futuro, geralmente para cumprir um prazo crítico. É subdividida em:
    -   Dívida de Curto Prazo: Contraída taticamente para uma entrega específica e que se espera pagar rapidamente. Pode ser focada (atalhos grandes e identificáveis) ou não focada (inúmeros pequenos atalhos, como código "sujo", que deve ser evitado).
    -   Dívida de Longo Prazo: Contraída proativamente por razões estratégicas, como adiar o suporte a uma segunda plataforma por acreditar que não será necessário por vários anos.

## Serviço da Dívida (Juros)

Assim como uma dívida financeira, a dívida técnica incorre em juros. Isso significa que a existência de atalhos e soluções "rápidas e sujas" torna o desenvolvimento futuro mais lento e caro. Se a dívida se acumula, a equipe pode passar mais tempo "pagando juros" (corrigindo problemas e lidando com a complexidade) do que agregando novo valor ao produto.

## Tornando a Dívida Transparente

Um dos maiores problemas da dívida técnica é sua invisibilidade, o que facilita que ela seja ignorada. Para combater isso, o artigo sugere duas abordagens para rastreamento:

-   Manter uma lista de dívidas em um sistema de rastreamento de defeitos, com estimativas de esforço para quitá-las.
-   Tratar cada item de dívida como uma "história" em um backlog de produto Scrum, a ser estimada e priorizada como outras tarefas.

## Comunicação e Quitação

A comunicação sobre a dívida com stakeholders não técnicos é crucial e se beneficia do uso da terminologia financeira. É mais eficaz discutir o impacto em termos de dinheiro e tempo, como "40% do nosso orçamento de P&D está sendo gasto para suportar lançamentos anteriores".

Para a quitação, o artigo desaconselha grandes projetos focados apenas em reduzir dívidas, pois tendem a falhar. Em vez disso, recomenda-se que uma porcentagem do trabalho de redução de dívida seja integrada ao fluxo de trabalho normal da equipe. Uma prática eficaz é dedicar a primeira iteração após um lançamento para pagar as dívidas de curto prazo contraídas.

## Tomada de Decisão

Ao considerar incorrer em dívida, as equipes não devem se limitar a duas opções ("caminho bom, mas caro" vs. "caminho rápido e sujo"). É essencial considerar mais duas questões:

1.  Qual será o custo para refatorar e implementar a solução boa depois de ter seguido o caminho rápido? (Geralmente é mais caro) .
2.  Existe uma terceira opção? Um caminho que seja rápido, mas bem contido, de forma que não gere "juros" contínuos que afetem outras partes do sistema.

Frequentemente, essa terceira opção, embora um pouco mais cara no curto prazo que a "rápida e suja", é a melhor escolha estratégica, pois evita custos de juros e permite que a decisão de refatorar seja adiada indefinidamente sem penalidades contínuas
