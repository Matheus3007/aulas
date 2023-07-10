- Modelos de comunicação requisição-resposta e chamada de procedimento remoto requerem como premissa que o receptor esteja executando durante a comunicação
	- [[Comunicação Cliente-Servidor|Comunicação transiente]]
	- Assíncrona, persistente e orientada a mensagem
	- A iideia é que cada aplicação tenha sua fila própria para a qual outras aplicações podem enviar mensagens
		- Uma fila só pode ser lida por sua aplicação associada
		- Várias aplicações podem compartilhar a mesma fila
- Um remetente só tem a garantia de que sua mensagem será inserida na fila do receptor em algum momento
	- Não há garantia se a mensagem será lida; esse comportamento ´e determinado pelo receptor
- O remetente e destinatário podem estar com estado passivo em execução
	- Passivo: a entrega da mensagem não é possível
## Primitivas de comunicação
- put
	- Coloca mensagem na fila
- get
	- Obtém mensagem da fila
- poll
	- Verifica se a fila possui elemento, e se sim tira o primeiro
- notify

---
