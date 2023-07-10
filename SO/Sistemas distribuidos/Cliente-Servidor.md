- Processos são clientes ou servidores
- Existe uma hierarquia
- Os clientes solicitam informações e serviços apenas ao servidor/servidores
- Os servidores simplesmente aguardam requisições dos clientes
- Cliente -> Faz solicitação -> Servidor Processa -> Responde ao cliente
- Um exemplo de arquitetura cliente servidor é uma página web.
	- O cliente faz a requisição, o servidor processa e retorna a página contina na base de dados.
	- Pode ser feito com três camadas, onde o servidor faz request para uma terceira camada
- Possível ter servidores com e sem estado
| Servidor com estado                                       | Servidor sem Estado                                         |
| --------------------------------------------------------- | --------- |
| Armazenam informações sobre os cliente | Não mantém informações sobre o estado dos clientes        |
| Operações podem ser implementadas de forma mais eficiente | Requisições precisam conter toda a informação necessária para o processamento |
| Mensagens com pedidos são menores                         | Mensagens maiores uma vez que precisam conter toda a informação               |
|                    -                                       |Implementação mais simples e mais escalável           |
|-|Clientes e servidores podem retomar a execução após uma falha, sem a necessidad de quaisquer procedimento de recuperação                                                                              |


