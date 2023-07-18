
## Quadro
### Formato
- 18B de cabeçallho (14 -4 )
- Campo de dados de 46 a 1500B

#### MTU
- Unidade máxima de transferência
- Por standard 1500B
- Maior que isso fragmenta

#### Campo de dados 
- Se dados < tamanho minimo tem padding

#### Jumbo package
- Configuração não padrão de MTU maiores que 1500
- Aumenta desempenho em alguns cenários
- Tem que ter cuidado, se algum pedaço da rede não tiver configurado pra jumbo package vai ter um "buraco negro" na rede onde nada surgiu
