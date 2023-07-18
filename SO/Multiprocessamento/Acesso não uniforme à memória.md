- Em um [[Multiprocessadores simétricos|Sistema SMP]], processadores tem acesso a toda memória principal
- Sistema Non-Uniform-Memory-Access -> NUMA
	- Vários nós SMP, caca um com memórias cache e memória principal própria.
	
## Características
- Os processadores enxergam uma única memória principal
	- Mesmo assim, cada um tem a sua
	- Cada posição tem um endereço único em todo o sistema
	- O tempo de acesso à memória difere conforme a região de memória que está sendo usada
- Pode oferecer desempenho superior a [[Multiprocessadores simétricos|sistemas SMP]]. [+]
- Se houver grande número de acessos a posições localizadas fora do nó, o desempenho cai substancialmente. É necessário que programas tenham boa [[localidade espacial]]. [-]

### [[O que se pode dizer de uma arquitetura NUMA sem coerência de cache]]?