- Associa cada arquivo a uma estrutura chamada I-node
	- A estrutura em lista encadaeada do [[FAT]] é substituida por um vetor contendo um índice de blocos do arquivo
	- Cada item do i-node é um bloco do arquivo e aponta pra posição desse bloco no disco (tipo uma paginação)
- Os i-nodes de todos os arquivos são agrupados em uma tabela mantida em uma área reservada do disco, separada dos blocos de dados.

![[Pasted image 20230707104620.png]]

- Para aumentar o tamanho máximo dos arquivos armazenados, dá pra transformar as entradas em ponteiros indiretos
	- Apontam para blocos que contem outros ponteiros, meio que criando uma estrutura em árvore
 
![[Pasted image 20230707104751.png]]

## Características
- O i-node precisa estar na memória apenas quando o arquivo correspondente estiver aberto [+]
- Como é necessário ler os blocos com ponteiros indiretos, arquivos muito grandes podem precisar de três ou quatro acessos a disco adicionais para acessar o bloco desejado. [+]
- Defeitos em i-nodes ou em blocos de ponteiros podem danificar grandes extensões do arquivo. [-]
	- Mitigável com técnicas de redundância1.