## Sobre GPU's

- As GPUs funcionam bem somente com problemas paralelos em **nível de dados**
- Adiconar mais threads não resolve probmea de desempenho de memória suficiente
- É impossível obter um bom desempenho vetorial sem fornecer largura de banda de memória
---
## Sobre [[Arquitetura Vetorial]]

- Uma única instrução opera sobre vetores de dados, que resulta em muitas operações registrador-regristrador em elementos de dados.
- [[Arquitetura Vetorial#Encadeamento|Chaining]] não exige que a operação em um vetor espere que todos os elementos individuais do vetor origem estejam disponíveis.
- O carregamento e armazenamento vetoriais possuem estrutura em pipeline. Isso afeta a latência das operações dos vetores
- O tempo de início, fruto da latência de pipelining da operação vetorial, influencia o [[Arquitetura Vetorial#Tempo de execução vetorial|tempo de execução vetorial]]. O tempo de execução vetorial depende principalmente de três fatores:
	- Tamanho dos vetores do operando
	- Conflitos (hazards) estruturais
	- Dependência de dados
