É uma abordagem que leva várias portas diferentes para os processadores e para as entradas e saídas ao invés de utilizar um barramento único:

![[Pasted image 20230706183913.png]]

## Características
- Com um caminho dedicado a memória para cada processador é possível um melhor desempenho. [+]
- Com caminhos diferentes por processador e para entrada e saída, é possível definir com mais granularidade porções dedicadas da memória para o uso de um ou mais processos e IO, garantindo mais segurança contra acessos não autorizados. [+]
- A complexidade é muito mais alta [-]
- Requer uma grande quantidade de circuitos lógicos [-]

## Pergunta de revisão:
### Qual a facilidade para adicionar novos processadores na abordagem com múltiplas portas?
Para adicionar novos processadores basta expandir a memória de forma que os CI's necessários para acessar o processador sejam adicionados e então colocar o novo processador.