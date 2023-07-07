- Camada responsável por gerenciar o envio de dados para um nó vizinho dentro da mesma rede.
- Transfere datagramas de um nó para outro fisicamente adjacente.
- Camada de enlace só se preocupa com o vizinho.
## Funções
- **Delineamento da mensagem** (Início e fim da mensagem)
- **Detecção e correção de erros**
- **Compartilhamento de um [[Camada Física|meio físico]]**
- **Endereçamento** de camada de enlace
![[DiagramOSI.png]]
---
A camada de enlace "esconde" a camada física, o que é enviado entre camadas é apenas um <u>frame</u>. 

## Enlaces ou Links
- Canais de comunicação que conectam nós adjacentes ao longo de um caminho de comunicação
- Podem ser cabeados ou sem fio.
- A comunicação entre enlaces pode ser feita por [[Switches|switches]]

## Implementação
- É implementada nos hosts
	- Adaptador de rede/Placa de erede/NIC
	- Chipset na placa mãe
- Combinação de Hardware, Software e Firmware
	- Software -> Driver da placa de rede