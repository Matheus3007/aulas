## Geral

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

---
## Sobre GPU's
- O modelo de programação CUDA é classificado pela NVIDIA como [[Single Instruction Multiple Data (SIMD)#Single Instruction Multiple Thread (SIMT)|SIMT]]
- O programador determina o paralelismo em CUDA explicitamente, especificando as dimensões do [[grid]] e o número de threads por processador [[Single Instruction Multiple Data (SIMD)|SIMD]]
- O hardware da GPU suporta execução em paralelo e o gerenciamento de threads
- Os primeiros ancestrais das GPU's são os aceleradores gráficos. Uma linguagem de programação para as GPU's foi essencial para aumentar o seu uso em computação de alto desempenho

---

## Sobre conjunto de instruções [[Single Instruction Multiple Data (SIMD)|SIMD]] para multimídia
- As extensões SIMD não oferecem os modos de endereçamento mais sofisticados das arquiteturas vetoriais, especificamente acessos por passo e [[Acesso Gather-Scatter|acessos gather-scatter]]
- Estas extensões são motivadas pela observação de que muitas aplicações de mídia operam com tipos de dados mais restritos que os tamanhos de palavra nativos.
- Como as instruções vetoriais, uma instrução de extensão SIMD especifica a mesma operação em vetores de dados
- Não existe um registrador de comprimento vetorial que especifica o número de operandos para a operação atual como em arquiteturas vetoriais
	- A quantidade de operandos é codificada no OPCode

---

## Calculo de parâmetros
![[Pasted image 20230710105347.png]]
### Características:
| Item                                       | quantidade |
| ------------------------------------------ | ---------- |
| Pistas precisão simples                    | 8          |
| Processadores SIMD                         | 10         |
| Largura instrução SIMD                     | 32b        |
| % dos threads threads ativos               | 80         |
| % de instruções simd de aritmética simples | 70         |
| % de instruções simd de load store         | 20         |
| Taxa média de despacho de instruções SIMD  | 0.85       |
| Clock da GPU                               | 1.5GHz     |

---
##### Ao aumentar o número de pistas de precisão simples para 16, calcule o ganho.
Considerando ganho linear $$Ganho=\frac{nPistasNovo}{nPistasOriginal}=\frac{16}{8}=2$$ 

---
##### Adicionar um cache que vai efetivamente reduzir a latência de memória em 40%, aumenta a taxa de despacho de instruções para 0.95. Desta forma, o ganho é?
$$Ganho = \frac{taxaDespachoNova}{taxaDespachoAntiga}=\frac{0.95}{0.85}=1.117$$

---
###### Ao aumentar o número de processadores SIMD para 15, calcule o ganho. Essa mudança não afeta outras medidas de desempenho e o código está em proporção com os processadores adicionais.
