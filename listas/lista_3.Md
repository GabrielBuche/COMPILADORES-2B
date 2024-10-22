# Lista 03

1. **Explique sobre os conflitos que ocorrem em um analisador Shift-Reduce quando a gramática não é LR.**
    Um conflito shift-Reduce ocorre quando meu analisador se depara com uma derivação com dois caminhos, podendo tanto ser um deslocamento para o proximo estado (Shift) ou se reduz (reduce).

2. **Gere a gramática estendida da gramática abaixo, construa o autômato LR(0) com a coleção LR(0) canônica e a tabela para análise SLR(1).**

    E → E v T | T  
    T → T & F | F  
    F → !F | id

3. **Verifique se as linguagens abaixo pertencem à gramática do exercício anterior, utilizando o Analisador SLR(1):**

    a. `id v id`  
    b. `! & id v id`  
    c. `id & !id`
