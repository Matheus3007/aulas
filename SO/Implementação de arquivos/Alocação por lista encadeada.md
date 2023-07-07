- Cada bloco do arquivo tem seus dados e um ponteiro para o próximo bloco.
- A tabela de diretório armazena a posição do primeiro bloco
## Caracteristicas
- Sem fragmentação externa [+]
- Arquivo fica disperso no disco, pdendo desacelerar o acesso já que a cabeça pode ter que se movimentar demais [+]
- Confiabilidade reduzida uma vez que uma danificação de um bloco pode ocasionar na corrupção de um bloco inteiro. [-]