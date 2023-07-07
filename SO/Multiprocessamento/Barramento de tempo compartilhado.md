[[Multiprocessadores simétricos|Voltar]]

Em um barramento de tempo compartilhado, todos os processadores se comunicam com a memória principal e a interface de IO utilizando um barramento único de tempo compartilhado. 
- Implica em barramento bloqueado quando utilizado por outro processador
- Processadores aguardam o liberamento

![[Diagrama barramento compartilhado.png]]

## Características
- **Simplicidade**: Com um barramento único, a simplicidade é garantida, uma vez que a interfase física e as lógicas de endereçamento são as mesmas que um sistema com um único processador. A diferença básica fica na função de [[escalonamento]]. [+]
- **Flexibilidade**: Expandir o sistema é fácil, já que basta conectar mais processadores ao barramento. [+]
- **Desempenho**: 
	- Uma vez que todo o acesso a memória precisa passar pelo barramento comum, o desempenho é comprometido já que quando um processador está usando a memória, todos os outros precisam esperar. [-]
	 - Além de ficar bloqueado durante a operação dos processadores, o barramento é a única forma de comunicar os sinais de controle e protocolos [-]
	 - Eventualmente, adicionar mais processadores degrada o desempenho

### Otimizações
É possível melhorar o desempenho é possível utilizar a memória cache para acelerar os acessos a memória e diminuir os bloqueios, porém, com novas questões de projeto:
- Cada cache possui uma imagem diferente (porção) da memória principal. A alteração de um dos caches pode invalidar as copias na memória principal.
- A coerência deve ser mantida.

Aqui é possível notar uma arquitetura de barramento compartilhado com cache:

![[TempoCompartilhadoCache.png]]

