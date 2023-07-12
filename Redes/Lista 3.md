## Quais as diferenças entre friba óptica [[Fibra Monomodo|Monomodo]] e [[Fibra Multimodo|multimodo]]? Explique como são construídas

A diferença entre fibra monomodo e multimodo encontra-se na quantidade de fibras contidas dentro do fio. A multimodo possuí várias fibras passando dentro do fio e faixas de operação menores, na casa de 850nm, enquanto a monomodo possui apenas menos fibras interna e uma faixa de operação um pouco mais alta, de cerca de 1310nm
A construção da fibra óptica é feita através de um núcleo feito com vidro, a fibra óptica propriamente dita, cercado por um material isolante e protetor denominado casca e por fim uma capa feita de plástico, que tem como propósito proteger todo o conjunto. A diferença de construção de ambas reside apenas na diferença do diâmetro do núcleo, que é maior na multimodo.

## Quais são as principais gerações de evolução da fibra óptica e seu uso?

### 1ª Geração
- Usada puramente como meio de transmissão em substituição ao cabo de cobre
- Todas as funções de amplificação/repetição, comutação e roteamentos são realizadas eletronicamente.
- Aumento da capacidade de transmissão da fibra

### 2ª Geração
- Aumento da taxa de transmissão através de multiplexação (OTDM - Optical Time Division Multiplexing)
	- Taxa de transmissão de até 250Gbps
- [[WDM|Wavelenght Division Multiplexing - WDM]]

## O que são redes [[WDM]]? Como são diferenciadas as redes [[Coarse Wavelength Division Multiplexing - CWDM|CWDM]], [[Dense Wavelength Division Multiplexing - DWDM|DWDM]] e UWDM?

Redes WDM tratam-se de uma tecnologia desenvolvida a partir da segunda geração de fibra óptica que utiliza uma tecnologia de multiplexação de comprimento de onda (cores diferentes no mesmo fio) para utilizar a mesma fibra óptica para transmitir dados diferentes de uma vez só, apenas se aproveitando da multiplexação.
[[Coarse Wavelength Division Multiplexing - CWDM|Redes CWDM]], ou Coarse Wavelenght Division Multiplexing, são redes onde os comprimentos de onda contidos no fio são tem espaços relativamente grandes entre sí, com cerca de 4 a 16 comprimentos de onda diferentes, então diminuindo a quantidade de comprimentos de onda diferentes e simplificando um pouco o processo de multiplexação e demultiplexação de ondas. São utilizados geralmente em redes MAN e tem um custo um pouco menor do que o seu comparativo, as redes [[Dense Wavelength Division Multiplexing - DWDM|DWDM]].
[[Dense Wavelength Division Multiplexing - DWDM|Redes DWDM]] (Dense wavelenght division multiplexing), são redes onde os comprimentos de onda no fio estão bastante próximos, com cerca de , garantindo então uma variedade maior de comprimentos de onda diferentes e consequentemente uma quantidade maior de fluxos de dados independentes a serem transmitidos no mesmo canal. As redes DWDM podem atingir até 400Gbps e tendem a ser mais caras, com processos de multiplexação mais complicados e requerimentos de garantia dos comprimentos de onda mais estritos. Ideal para transmissão de dados em longas distâncias, porém também muito mais caras.
[[Ultra-dense Wavelenght Division Multiplexing|Redes UWDM]] são ultra densas, então tem mais de 128 comprimentos de onda.

## Quais são os principais componentes de uma rede DWDM e suas funções?

Uma rede DWDM precisa ter inicialmente os transponders, que são comuns a todas as redes ópticas, transformando os sinais elétricos em ópticos, mas também é necessário que haja um multiplexador, que vai transformar todos os sinais independentes a serem transmitidos em uma rede em um único sinal composto com diferentes comprimentos de onda que serão transmitidos simultaneamente através da fibra óptica. A depender da rede, é possível que haja amplificadores de fibra (EDFA's) que amplificam o sinal óptico sem necessitar convertê-lo para elétrico. Ao final da transmissão, é necessário também um demultiplexador que vai converter cada faixa de comprimento de onda em seu próprio sinal e os enviar para os receptores respectivos, realizando assim a comunicação de maneira adequada.

## O que é [[janela de transmissão]] de uma fibra? Qual o critério de seleção da faixa de comprimentos de onda de uma janela de transmissão?

Determina-se janela de transmissão a faixa de comprimentos de onda selecionadas para a transmissão de dados utilizando fibras ópticas. Para garantir uma maior confiabilidade do sinal enviado, janelas de transmissão são comprimentos de onda especificamente selecionados por sua baixa atenuação.

## O ITU-T definiu dentro do contexto do G694.1 dois padrões para redes [[Dense Wavelength Division Multiplexing - DWDM|DWDM]], [[Dense Wavelength Division Multiplexing - DWDM#Grade fixa|grade fixa]] e [[Dense Wavelength Division Multiplexing - DWDM#Grade flexível|grade flexível]]. Qual a diferença entre estes padrões? Quais são as suas vantagens e desvantagens?

O padrão de grade fixa limita a rede a utilizar espaçamentos fixos entre os comprimentos de onda do canal, espaçamentos estes que podem variar de 12.5 a 100GHz, isso é vantajoso por ser mais simples de se implementar, portanto em redes onde não há tanta variação de necessidades entre os canais de comunicação pode ser mais vantajoso implementar um DWDM de grade fixa. Já o padrão de grade variável, permite a variação do espaçamento entre cada comprimento de onda utilizado na multiplexação, podendo aumentar ou diminuir o espaço de cada canal de acordo com suas necessidades e portanto utilizando o canal de comunicação de uma forma vastamente mais eficiente, no entanto, com uma implementação muito mais complexa e custosa que a de grade fixa, portanto só deve ser utilizado em aplicações onde sua presença é necessária, por exemplo, onde há uma disparidade grande de requisitos de banda por canal de transmissão e uma grande variação destes requisitos.

## Quais são os diferentes tipos de topologias de redes ópticas? Quais suas vantagens e desvantagens?

Os principais tipos são a [[Arquitetura Ponto-a-Ponto]], onde os dois pontos são conectados diretamente por uma fibra, o que é bom por ser simples e de fácil implementação, porém tem robustez reduzida e baixa flexibilidade, uma vez que aquele link de fibra é a única forma desses dois pontos se comunicarem através da fibra óptica. Depois da ponto a ponto, tem-se a [[Arquitetura Anel]], onde todos os pontos da rede são conectados de forma circular através de um optical add-drop multiplexers, o que é bom por ser altamente flexível e robusto, permitindo até mesmo anéis duplos trabalhando em paralelo, ou o uso da rede em um sentido oposto caso um de seus ramos seja rompido, mas com a desvantagem de se precisar de equipamentos específicos para sua implementação. Frequentemente utilizadas em MANs. Por fim, a [[Arquitetura Malha]] é constituida por um conjunto de pontos todos interligados entre sí formando uma malha de caminhos diferentes. Essa rede é a melhor em termos de disponibilidade e robustez, garantindo que mesmo com a falha de algumas conexões, a transmissão ainda vai ser mantida, mantendo sempre a disponibilidade do sistema, porém vale notar que nem sempre vai ser uma implementação barata, aumentando assim sua barreira de implementação com desafios de roteamento também.

## Quais os tipos de comutação óptica que existem? Quais são os desafios existentes?

Os principais tipos de comutação são [[Add Drop Multiplexing]], [[Optical Cross Connect]] e [[Multicast Optical Cross Connect]]. O primeiro faz uso de um multiplexador para definir o que entra e o que sai da rede, podendo desviar fluxos ópticos diferentes através do comprimento de onda, enquanto o segundo e o terceiro utilizam switches ópticos capazes de chavear o sinal na entrada para qualquer porta de saída a depender de seu destino. O terceiro é muito similar ao segundo, porém com um spliter ou amplificador na saída, permitindo que o sinal de entrada seja transmitido para quantas portas forem necessárias, possibilitando a [[comunicação multicast]] com o switch óptico. Todas estas tecnologias são excelentes, porém apresentam grandes desafios de implementação, especialmente no que trata de manter a qualidade do sinal, uma vez que ele será manipulado diretamente e também em como realizar o controle de forma adequada e eficiente sem perder a eficiência da comunicação, que é muito rápida por se tratar de um canal óptico.

## Quais são os principais desafios para puxar cabos submarinos? O que representa a malha de cabos submarinos existentes hoje?

Para se puxar cabos submarinos, primeiro é preciso considerar a dificuldade de se posicionar a fibra sem danifica-la, uma vez que é extremamente sensível por natureza. Além disso, trata-se de um único cabo atravessando extensões oceânicas, portanto é necessário garantir que nenhum de seus trechos se danifique no processo, que já é lento. Para garantir a qualidade do sinal, é importante que junto ao cabo sejam instalados repetidores capazes de manter a transmissão de maneira saudável, por fim, vale também ressaltar que por se tratarem de serviços de comunicação base, sua localização é conteudo sensível e deve ser mantida em segredo para evitar problemas de segurança. Hoje em dia, alguns dos principais cabos submarinos internacionais são:
- SACS -> Atlântico Sul, fortaleza a Luanda
- SAIL -> Fortaleza a camarões
- BRUSA -> Brasil a porto rico e aos eua
- Tannat -> Praia grande a Maldonado
- Junior -> Rio de janeiro à Praia grande, apenas dados do google.

