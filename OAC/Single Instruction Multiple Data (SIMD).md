## Single Instruction Multiple Data (SIMD)
- Se refere a um modelo onde uma única instrução opera em múltiplos elementos de dados simultaneamente.
	- Cada operação em qualquer momento é a mesma realizada em diferentes argumentos de dados
- Exemplo: GPU
![[Pasted image 20230717134046.png]]
### Single Instruction Multiple Thread (SIMT)
- É um termo utilizado especificamente sob o contexto da arquitetura de GPU da NVIDIA. Descreve a forma como o core da GPU executa instruções em paralelo.
- Um grupo de threads (*Warp*) executa a mesma instrução de forma concorrente, mas cada thread opera sobre seu próprio conjunto de dados.