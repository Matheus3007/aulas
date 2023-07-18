- Grupos de computadores completos trabalhando juntos
	- Nós do sistema que podem operar por si só independentemente do cluster

## Características
- Escalabilidade absoluta [+]
	- Um cluster pode ser contruido por quantas maquinas forem necessárias, cada uma sendo um [[Multiprocessadores simétricos|sistema SMP]]
- Escalabilidade incremental [+]
	- Clusters permitem a instalação de novos nós conforme for necessário
- Alta disponibilidade [+]
	- Um nó falhar não desativa os outros
	- Erros podem ser tratados a nível de software
- Melhor relação entre custo e desempenho
	- Um cluster pode ser construído com várias máquinas de baixo custo a fim de se atingir um desempenho de máquinas de custo elevado

Os principais tipos de cluster são:
- **[[Servidores separados]]**
- **[[Servidores conectados a discos]]**
- **[[Servidores conectados a discos compartilhados]]**
****
Para se aproveitar completamente uma configuração de cluster, é importante realizar aprimoramentos nos sistemas operacionais voltados para sistema únicos:

### Gerenciamento de falha
- Duas abordagens diferentes podem ser tomadas para o gerenciamento de falhas:
	- Alta disponibilidade -> Alta probabilidade de que todos os recursos estejam em funcionamento
	- Tolerância a falhas -> Garante que todos os recursos estejam sempre disponíveis

### Balanceamento de carga
- Sistema que quando um novo nó é adicionado ao cluster, o sistema operacional balanceia a carga automaticamente incluindo esse computador no agendamento de aplicações.


**[[Revisão - Que problema clássico de deadlock pode aparecer nos clusters conectados a discos?]]**