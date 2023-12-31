- Flynn propõe um sistema de classificação de sistemas de processamento denominado pela [[Taxonomia de Flynn]]
- Alguns dispositivos podem ser mais adequados para tipos específicos de computação
	- CPUs executam vários tipos de carga de trabalho, instruções tão genéricas quanto possível para permitir um desempenho razoável para a maioria dos aplicativos
	- Dispositivos especializados (**aceleradores**) são incorporados para permitir suporte de hardware para tipos de computação específicos
	- Ou seja, há a mistura de diferentes tipos de dispositivos para realizar tipos diferentes de trabalho dentro do mesmo sistema.
- Exemplos:
	- CPU + GPU = [[Single Instruction Single Data (SISD)|SISD]] + [[Single Instruction Multiple Data (SIMD)|SIMD]]
	- CPU + Intel Xeon Phi = [[Single Instruction Single Data (SISD)|SISD]] + [[Multiple Instruction Multiple Data (MIMD)|MIMD]]
	- Computação de alta performance - HPC
- A sincronização entre dispositivos de computação em sistemas híbridos é feita por [[APIs de processamento híbrido|APIs]] dedicadas para isso