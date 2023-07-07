Scheduling é o ato de alocar recursos para realizar tarefas. Os recursos podem variar, como por exemplo:
- Processadores
- Links de rede
- Cartões de expansão
Já as tarefas em jeral são processos, threads, ou fluxos de dados.
---
O escalonamento tem como alguns de seus objetivos:
- Maximizar a quantidade total de trabalho completa por unidade de tempo
- Minimizar o tempo de espera para o trabalho ficar pronto 
- Minimizar a latencia, ou seja o tempo que o trabalho fica pronto desde que está terminado
- Tornar justo o tempo gasto por cada processo alocando melhor os recursos.

Um exemplo de escalonador é o dispatcher, que é responsável por realizar mudanças de contexto entre processos ou threads que estão sendo executados em um SO.