# No Silver Bullet

Artigo: [https://worrydream.com/refs/Brooks*1986*-\_No_Silver_Bullet.pdf](https://worrydream.com/refs/Brooks_1986_-_No_Silver_Bullet.pdf)

## O Lobisomem

Assim como se procurou uma forma de matar lobisomens no mundo mágico e se descobriu a bala de prata, as pessoas que trabalham com software buscam uma maneira de resolver, de forma mágica, os problemas que surgem durante o desenvolvimento e a manutenção de um sistema. O artigo trata desse assunto e faz comparações com o mundo do hardware, que passou por diversas melhorias nos últimos anos.

## Essências

Se a parte mais complicada de desenvolver um software é criar boas especificações, então o trabalho de modelá-lo é inerentemente complexo. Em seguida, são discutidas quatro essências de um sistema: complexidade, conformidade, mutabilidade e invisibilidade.

### Complexidade

Nas ciências exatas, problemas complexos são frequentemente reduzidos a problemas mais simples ao se ignorarem partes não essenciais do fenômeno. Ao tentar trazer essa mesma abordagem para o software, concluímos que isso não é possível, pois a complexidade de um programa faz parte de sua essência e, se a removermos, não teremos mais aquele programa. Isso também nos permite enxergar uma das diferenças entre hardware e software: o hardware possui estados finitos, enquanto o software possui estados infinitos, o que demonstra que a carga de complexidade é muito maior no software.

### Conformidade

Aqui, novamente, é feito um paralelo entre os físicos e os engenheiros de software. Os primeiros acreditam que sempre há uma lei unificadora e simples para todos os fenômenos. No entanto, para os engenheiros, a complexidade é sempre arbitrária, podendo ser tão simples quanto um problema de física ou tão complexa quanto um problema de física quântica ainda não estudado. Em muitos casos, essa complexidade vem do fato de que o software precisa se conformar a interfaces já definidas ou a tendências de mercado.

### Mutabilidade

Como a alteração de um software é muito mais barata que a de um hardware, foram desenvolvidos sistemas de hardware genéricos e simples que permitem uma gama limitada de operações, mas que, através dos programas, tornam muitas coisas possíveis. Portanto, o propósito de um programa é ser maleável.

### Invisibilidade

Comparando novamente com outras engenharias, desta vez com os modelos que representam algo, seja o projeto de arquitetura de uma casa ou algo mais próximo, como um diagrama de hardware, percebemos um desafio. Quando tentamos modelar o software, seja por fluxo de dados, hierarquia, etc., sempre chegamos a uma estrutura complexa que atrapalha a visualização completa do sistema.

## Tecnologias

### Linguagens de Alto Nível

Essa tecnologia nos permite abstrair boa parte da complexidade de como o hardware funciona, permitindo que softwares sejam feitos com muito menos esforço. Contudo, quando combinada com muitas abstrações fornecidas pela linguagem, a tarefa pode se tornar mais complicada.

### Unificação de Ambientes

Uma forma pela qual a complexidade foi reduzida foi a padronização de ambientes, o que permite que o engenheiro de software se preocupe mais com seu sistema do que com o que precisa ser feito para que ele funcione corretamente em todos os cenários possíveis de um computador.

## Esperanças

### Orientação a Objetos

Permitindo que cada estrutura de dados se autogerencie, a separação de responsabilidades torna-se muito mais alcançável, reduzindo assim a complexidade geral de um software.

### Sistemas Inteligentes

Assim como na técnica de _pair programming_, a ideia é ter inteligências artificiais atuando como suporte aos programadores, lembrando de pontos importantes, sugerindo otimizações, apontando casos de teste, etc.

### Testes

Ainda que os testes permitam que um software se mantenha operacional, não é possível garantir que todos os cenários foram testados, nem que isso se tornará a salvação para os nossos problemas.

## Ataques Promissores

### Prototipação

Como a especificação de um software se torna a base para tudo o que será construído, ela é a parte mais vital do processo. Porém, nem sempre o cliente ou o usuário sabe o que quer que o programa faça. Logo, a prototipação surge para garantir que as partes mais importantes funcionem como desejado, permitindo que o feedback rápido refine os requisitos.
