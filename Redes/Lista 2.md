## Qual a diferença entre [[Comutação de circuitos|comutação]] e [[Roteamento de Circuitos|roteamento]] de circuitos?

Comutação e roteamento de circuitos diferem no sentido de que comutação trata-se do uso do caminho traçado pelo roteamento de circuitos. Ou seja, o roteamento define o caminho a ser seguido por pacotes na rede, enquanto a comutação trata-se do pacote de fato percorrendo este caminho através dela.

## Qual a diferença entre endereçamento físico e lógico? Quando eles são usados? Dê um exemplo de endereço físico e endereço lógico.

Endereçamento físico é aquele relativo diretamente ao dispositivo com o qual se comunica, um exemplo cotidiano é o [[Endereços físicos - MAC|endereço MAC]] das placas de rede, que é único e relativo a placa de rede, já o endereço lógico pode é um endereço relativo ao posicionamento do dispositivo na rede em que se encontra e pode variar. Um exemplo de endereço lógico é o IP.

## O que são [[Redes de circuitos virtuais|circuitos virtuais]]? E [[Canais Lógicos|canais lógicos]]? Para quê são usados?

Circuitos virtuais são os caminhos definidos dentro de uma rede para se chegar de um ponto A ao ponto B. Eles não representam necessariamente dispositivos físicos, mas sim o conjunto de dispositivos em uma rede para se chegar de um ponto ao outro. Canais lógicos são as conexões ponto a ponto. Um circuito virtual é formado por um conjunto de canais lógicos **concatenados**.
Canais lógicos são utilizados para definir qual o próximo nó da rede a ser seguido. Já circuitos virtuais são utilizados para garantir qualidade de serviço de acordo com o critério desejado

## Suponha uma rede de comutação de pacotes como o da figura abaixo. Mostre como devem ser construídas as [[Tabela de comutação|tabelas de comutação]] dos switches SP, RJ, BSB, RE e VT, no caso de existir pelo menos um circuito virtual entre cada par de estações.
![[Imagem do WhatsApp de 2023-07-11 à(s) 10.50.48.jpg]]
### SP

| Interface física de entrada | Canal lógico de entrada | Interface física de saída | Canal lógico de saída |
| --------------------------- | ----------------------- | ------------------------- | --------------------- |
| 1                           | 10                      | 2                         | 11                    |
| 1                           | 20                      | 3                         | 21                    |
| 1                           | 30                      | 3                         | 31                    |
| 2                           | 71                      | 1                         | 70                    |
| 3                           | 81                      | 1                         | 80                    |
| 3                           | 91                      | 1                         | 90                    |

### RJ 

Não vou fazer tudo pq é só repetição, mas a receta de bolo é fazer o desenho, atribuir número pra tudo e partir pro abraço.

## Substitua as estações por redes locais e mostre:
- ### Como as redes locais devem ser ligadas a uma rede de comutação de pacotes?
	Os endereços das estações agora são relacionados a uma rede inteira, portanto para inserir uma LAN no lugar das estações, é necessário que haja algum tipo de forma de detecção do destinatário dentro da LAN, para que os pacotes possam ser gerenciados e entregues de forma correta. Isto é feito utilizando um roteador, que será considerado o [[Roteadores|roteador]] da rede local como dispositivo final da rede de comutação. Ele será responsável por empacotar e encaminhar os pacotes da rede de comutação aos dispositivos de destino.
- ### Como ficam as tabelas de roteamento e comutação dos [[Roteadores|elementos de interconexão]] usados entre as redes locais e os switches?
	- Tabelas de comunicação de roteadores neste caso relacionam endereços de IP (lógicos) a interfaces físicas nas quais os dispositivos estão conectados. 
	- O IP substitui interfaces físicas e canais lógicos de entrada como identificadores para os canais de saída a serem utilizados, já que não existem canais lógicos internos as LANs.
	- Os roteadores de LAN possuem tabelas de relacionamento IP-MAC e quando recebem pacotes usam o protocolo ARP para conectar aquilo que receberam da rede de comutação

## Quais foram os principais impactos da fibra óptica na evolução das tecnologias de redes? Dê exemplos das mudanças ocorridas nas camadas físicas, enlace, rede e de aplicação.
A fibra óptica foi um grande salto tecnológico pois possibilitou uma capacidade maior de transferir mais dados em velocidades mais altas e com maior **confiabilidade** do que a que se tinha anteriormente. Com isso, pode-se ter um avanço considerável em várias tecnologias, um exemplo é o do streaming, possibilitando transmissões ao vivo em alta qualidade (4K, 8K). Cada camada teve que se adaptar para suportar as novas tecnologias.
Abaixo, podemos ver os principais [[impactos da fibra óptica nas camadas OSI]]:
### Física
- O paradigma de comunicação muda, sendo óptico e não elétrico.
- O meio é muito mais confiável, então correção de bits é feita apenas no campo de endereço.
### Enlace
- Camada de enlace passa a não corrigir mais erro já que o meio óptico é muito mais confiável
- Alta velocidade da fibra óptica faz com que a camada de enlace não mais realize o controle de fluxo.
- Apenas controle de congestionamento e detecção de erro
	- Se há erro -> descarte.
### Rede
- O roteamento passa a ser feito na origem
	- Evita gargalos de decisões de roteamento
### Aplicação
- Permite uso muito mais intenso de dados para aplicações com mais requisitos de QoS, como banda e confiabilidade. Como streaming de vídeo em altas qualidades, ligações, chamadas em geral.

## Monte uma tabela comparativa com as principais características entre redes LAN, MAN, WAN e PAN
| LAN                                   | MAN                                                      | WAN                                                             | PAN                                                      |
| ------------------------------------- | -------------------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------- |
| Redes locais, como dentro de uma casa | Metropolitana, como dentro de uma cidade ou universidade | Redes em uma área geral, como a RNP (rede nacional de pesquisa) | Rede pessoal, interligando os dispositivos de uma pessoa |
| Baixa latencia                        | Média latencia                                           | Alta latencia                                                   | Baixa Latencia                                           |
| Par trançado, fibra óptica e wifi     | Geralmente Fibra optica                                  | Satélite, fibra, sem fio (4G, 5G)                               | Sem fio (Bluetooth)                                      |
| Pequeno alcance                       | Médio a Grande alcance                                   | Grande alcance                                                  | Pequeno alcance                                          |
| Velocidade Alta                       | Velocidade média a alta                                  | Velocidade baixa a média                                        | Velocidade Baixa                                         |
| Operado por instituição ou pessoa     | Operado por instituição, pessoa ou operadoras            | Operadoreas                                                     | Instituição ou pessoa                                    | 


