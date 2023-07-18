## Salto
![[Pasted image 20230713135904.png]]

##  ALU
![[Pasted image 20230713135930.png]]

## Barrel Shifter
![[Pasted image 20230713135946.png]]

## Load/Store Half
![[Pasted image 20230713140157.png]]

## Load store com offset imediato
![[Pasted image 20230713140036.png]]

## Load store com registrador de índice
![[Pasted image 20230713140058.png]]

## Load store multiple
![[Pasted image 20230713140253.png]]

## Move Coprocessor
![[Pasted image 20230713140422.png]]

## Load store coprocessor
![[Pasted image 20230713140430.png]]

## Lógica de tradução
![[Untitled-2023-07-13-1406 1.svg]]
***
## Tabela de possibilidades

| 27  | 26  | 25  | Tipo                             |
| --- | --- | --- | -------------------------------- |
| 0   | 0   | 0   | Barrel Shift - Load/Store Half   |
| 0   | 0   | 1   | ALU                              |
| 0   | 1   | 0   | -                                |
| 0   | 1   | 1   | Load store registrador de índice |
| 1   | 0   | 0   | Load store multiple              |
| 1   | 0   | 1   | Salto                            |
| 1   | 1   | 0   | Load store coprocessador         |
| 1   | 1   | 1   | Move coprocessador               |
 
### Desambiguição shift - load/store half

| 11  | 10  | 9   | 8   | 7   | Tipo       |
| --- | --- | --- | --- | --- | ---------- |
| 0   | 0   | 0   | 0   | 1   | Load/Store |
| X   | X   | X   | X   | X   | Shift           |

![[Untitled-2023-07-13-1406(2).svg]]