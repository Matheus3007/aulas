- Existem 4 formas principais de comunicação cliente servidor:
	- Persisitente  
		- A mensagem é armazenada durante todo o tempo necessário até ela chegar ao receptor
		- O cliente e o servidor não precisam estar ativos durante a comunicação
	- Transiente
		- Armazenada somente durante o tempo de execução da aplicação, ou seja enquanto ambas as partes estiverem se comunicando
		- Cliente e servidor devem estar ativos durante a comunicação
	- Assíncrona
		- O remetente pode continuar o processamento sem esperar a resposta da mensagem pedida
	 - Síncrona
		 - Após enviar a mensagem para o servidor, o remetente é bloqueado até obter a resposta

## Modelos de comunicação
- [[Requisição-resposta]]
- [[Chamada de procedimento remoto (RPC)]]
- [[Comunicação orientada a mensagem]]