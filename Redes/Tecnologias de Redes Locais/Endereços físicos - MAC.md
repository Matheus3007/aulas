- Endereço Físico / de Hardware -> identificar um nó em um segmento de rede de [[Camada de Enlace|camada 2]]
- Tem esse nome porque fica gravado na placa de rede

## MAC 
-> Endereço físico de 48 bits gravado/configurado na placa de rede ou via [[Camada de Enlace#Implementação|driver da placa]] de rede
- 6 grupos de 1 byte em hexadecimal
- 1A:2F:BB:76:09:AD
-> Espaço de endereçamento controlado pelo IEEE
- 24 bits iniciais identificam fabricante - OUI
- 78:31:c1:c8:fa:64 -> Apple

### Unicast
- Transmissão para um único nó da rede

### Broadcast
- Transmissão para todos os nós da rede

### Multicast
- Transmissão para alguns nós da rede
	- Um exemplo é o IpV6 que não manda broadcast
	- Alguns MACs são especiais, identificando dispositivos de rede como roteadores.