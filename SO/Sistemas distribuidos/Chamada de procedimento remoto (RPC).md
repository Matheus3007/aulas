- Neste modelo dois programas/processos se comunicam por meio de chamada de procedimentos remotos ao invés de troca de mensagens
	- O procedimento chamado reside em máquina diferente da sua implementação, portanto tem espaços de endereçamento diferentes
- A ideia é tornar a chamada de procedimento remota transparente de forma que pareça uma chamada de procedimento local
- Dois componentes principais
	- Apêndice de cliente
		- Empacota os parâmetros em uma mensagem e solicita o envio da mensagem para o servidor
	- Apêndice de servidor
		- Desempacota os parâmetros da mensagem e chama o procedimento do servidor (local)
- Você basicamente passa os parâmetros pro servidor e executa a função remotamente, retornando só os resultados
- O RPC é feito com uma consulta a um servidor diretório antes. 
	- A máquina consulta o servidor diretório
	- O servidor diretório fala onde está o servidor que processa a função
	- Faz o RPC
## Questões práticas:
- Como tratar ponteiros? (A memória não é compartilhada)
	- É preciso enviar toda a fatia de memória (ineficiente)
- O servidor deveria criar um processo (fork) ou thread para atender as solicitações?
	- Depende 
- O cliente deveria ficar bloqueado enquanto aguarda a comunicação?
	- Depende