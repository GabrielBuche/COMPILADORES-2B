# Lista 03

1. **Explique sobre os conflitos que ocorrem em um analisador Shift-Reduce quando a gramática não é LR.**

    *Resposta:*
    Um conflito shift-Reduce ocorre quando meu analisador se depara com uma derivação com dois caminhos, podendo tanto ser um deslocamento para o proximo estado (Shift) ou se reduz (reduce).

2. **Gere a gramática estendida da gramática abaixo, construa o autômato LR(0) com a coleção LR(0) canônica e a tabela para análise SLR(1).**

    E → E v T (1)
    E → T (2)
    T → T & F (3)
    T → F  (4)
    F → !F (5)
    F → id (6)

tabela dos follows

| S | FOLLOW     |
|---|------------|
| E | { V }      |
| F | { V, & }   |
| T | { V, & }   |

> o autômato LR(0) com a coleção LR(0) canônica
> a tabela foi criado com base no arquivo [resposta2.pdf](./resposta_2.pdf)
> foi criado no draw.io e exportado no formato pdf para facilitar a visualização e criação

tabela para análise SLR(1)

| I | ID | V  |  ! | &  | E | T | F |
|---|----|----|----|----|---|---|---|
| 0 | S5 |    | s4 |    | 1 | 2 | 3 |
| 1 |    | S6 |    |acc |   |   |   |
| 2 |    | R2 |    | S7 |   |   |   |
| 3 |    | R4 |    | R4 |   |   |   |
| 4 | S5 |    | S4 |    |   |   | 8 |
| 5 |    | R6 |    | R6 |   |   |   |
| 6 | S5 |    | s4 |    |   |10 | 3 |
| 7 | S5 |    | S4 |    |   |   | 9 |
| 8 | S5 | R5 |    | R5 |   |   |   |
| 9 |    | R3 |    | R3 |   |   |   |
| 10|    | R1 |    | s7 |   |   |   |

1. **Verifique se as linguagens abaixo pertencem à gramática do exercício anterior, utilizando o Analisador SLR(1):**

    a. `id v id`  
    b. `! & id v id`  
    c. `id & !id`
