## Base
- Lê conjunto de elementos de dados e armazena em registradores vetoriais
- Opera nestes registradores
- Dispersa os resultados de volta a memória
- **Registradores são controlados por compilador**
- Aproveitar a largura de banda da memória

## Tempo de execução vetorial
São três os fatores que definem o tempo de execução vetorial:
- Tamanho dos vetores operandos
- Hazards estruturais entre operações
- Dependências de dado
---

## Comboio
- O conjunto de instruções vetoriais que potencialmente poderiam iniciar sua execução juntas define-se comboio
- Sequências com dependências RAW podem estar no mesmo comboio devido ao [[#Encadeamento|encadeamento]]

### Encadeamento 
- Permite que uma operação vetorial comece assim que os elementos  individuais de seu vetor operando origem esteja disponível

## Chime
- Unidade de tempo para executar um [[#Comboio]]
- <u>m</u> comboios executam em <u>m</u> chimes para um vetor de tamanho <u>n</u>
- Um vetor de tamanho <u>n</u> requer <u>m</u> x <u>n</u> ciclos de clock