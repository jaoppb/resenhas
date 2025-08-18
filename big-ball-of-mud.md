# Big Ball of Mud

Artigo: [http://www.laputan.org/mud](http://www.laputan.org/mud)

## Resenha

Assim como em tudo na Engenharia de _software_ o artigo traz um ponto muito importante sobre contexto. Pois, apesar de discorrer e justificar a definição da **Grande Bola de Lama** como um _anti-pattern_ também é afirmado que não é errado enxergar esse padrão como um padrão, devido ao fato que em certos momentos é necessário o seu uso, como em uma prototipagem ou em um teste de mercado.

### _Throwaway Code_

Assim como seu nome diz, é aquele código que o programador sabe que não está bom quando o fez, mas teve seus motivos para fazé-lo. Por exemplo: a equipe precisava testar a viabilidade de uma ideia e para isso fez um prototipo, porém quando chegou o momento de se fazer a [reconstrução](#reconstruction) do protótipo, o cliente, a gerência ou até mesmo a própria equipe decide que é bom o suficiente e a aplicação é levada a produção.

### _Piecemeal Growth_

Esse princípio é bem parecido com o que é aplicado atualmente no _SCRUM_ no sentido que o mantra principal é o incremento do _software_ e que as **mudanças** sempre vão ocorrer. Além disso, outro problema que pode gerar a **Grande Bola de Lama** é a inercia do "_if it works, don't touch it_", e o fato de que o _software_ foi pensado para ser incremental encoraja seu crescimento.

### _Keep It Working_

Nesta parte é discutido que apesar de que a **Grande Bola de Lama** deve ser "limpa", todo cuidado é pouco, pois empresas e pessoas podem depender de seu _software_ e isso limita as ações que podem ser tomadas. Então, é trazido do _Extreme Programming_ a prática de testes unitários, que são escritos antes mesmos de qualquer linha de código.

Outro fato interessante trago nesta seção são as práticas de algumas empresas em sempre garantir que uma _working build_ seja feita, seja diária ou semanalmente.

### _Shearing Layers_

Comparando-se as camadas de uma construção com as camadas de um _software_ fica mais fácil de entender onde é mais necessário focar em fazer uma implementação mais passível de mudanças ou algo mais concreto e bem definido. As camadas citadas da costrução são: _Site_, _Structure_, _Skin_, _Services_, _Space Play_ e _Stuff_. E a contrapartida no software são: _Data_, _Code_ e a partir daqui **depende** do seu contexto.

### _Sweeping It Under Rug_

Aqui é descrito mais uma forma de se lidar com a **Grande Bola de Lama**, com sua ideia principal sendo fazer como um lagarto corta sua cauda: isolando a parte identificada como um problema para a arquitetura do software e posteriormente cortando-a fora. Caso não seja possível esse isolamento o que te resta é a [reconstrução](#reconstruction).

### _Reconstruction_

Por fim, se você chegou na situação: "quando eu fiz esse código só eu e deus sabiamos o que ele fazia, agora só deus sabe.". É necessário a reconstrução completa do software, desta vez seguindo uma arquitetura bem pensada, definida e adequada para seu contexto, em conjunto com boas práticas, como testes unitários e _clean code_.

### Conclusão

Aqui afirmo novamente que tudo na engenharia de software **depende** e dessa vez não foi diferente, por isso ter conhecimento sobre as diversas atividades que envolvem a produção de um software é importante, por que você vai conseguir saber como lidar de uma boa forma com o contexto de desenvolvimento e de uso.
