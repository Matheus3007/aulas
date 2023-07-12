Abordagem de transmissão de dados em uma rede que busca transmitir vários pacotes de mensagens diferentes ao longo do mesmo percurso na rede, separando-as em pacotes diferentes.

![[Pasted image 20230711215056.png]]

- Várias conexões lógicas multiplexando uma única conexão física.
- Tráfego agregado estatisticamente
- [[Store and forward]]
- Tráfego em rajadas
- Permite rotas alternativas
- Não suporta aplicações sensíveis a atraso (**Pode produzir latência**)
- Perda de pacotes devido ao congestionamento da rede
- Perda de sequencia dos pacotes requer reordenação no destino