- Em arquiteturas cliente-servidor é preciso facilidades adicionais para sincronizar acesso a arquivos compartilhados
	- Um modo simples de se obter isso é usando um gerenciador de travas central
- Em NFS existem quatro tipos de travas
	- Fornece granularidade fina de trava (bytes)
	- Travamento completo de arquivos configura um mau projeto

| operação | descrição                                                   |
| -------- | ----------------------------------------------------------- |
| lock     | Cria uma trava para uma faixa de bytes                      |
| lockt    | Testa para verificar se foi concedida uma trava conflitante |
| locku    | Remove uma trava de uma faixa de bytes                      |
| renew    | Renova o arrendamento em uma trava específica               |

- Note que uma faixa é separada pois nem sempre se acessa todo o conjunto 