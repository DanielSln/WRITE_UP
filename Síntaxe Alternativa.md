# WriteUp — Desafio Brainfuck

## Descrição

O desafio apresenta um conjunto de símbolos aparentemente aleatórios:

```text
+++++++[<++++++++++>-]<.[-]>+++++++[<++++++++++>-]<++++++.[-]>++++++[<++++++++++>-]<+++++.[-]>+++++++[<++++++++++>-]<+.[-]>++++++++++++[<++++++++++>-]<+++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++[<++++++++++>-]<.[-]>++++[<++++++++++>-]<+++++++++.[-]>++++++++++[<++++++++++>-]<+++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++[<++++++++++>-]<+++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<+++++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++++[<++++++++++>-]<++++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<++++.[-]>++++[<++++++++++>-]<+++++++++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++++[<++++++++++>-]<+++++.
```

A descrição informa que esse conjunto de símbolos é um programa funcional e que é necessário descobrir como interpretá-lo.

## Identificando a linguagem

Analisando os caracteres utilizados no código, é possível perceber a presença dos principais comandos da linguagem **Brainfuck**:

* `+` — incrementa o valor da célula atual;
* `-` — decrementa o valor da célula atual;
* `<` — move o ponteiro uma posição para a esquerda;
* `>` — move o ponteiro uma posição para a direita;
* `[` e `]` — delimitam estruturas de repetição;
* `.` — imprime o valor da célula atual como um caractere.

A combinação desses símbolos é uma forte indicação de que o programa está escrito em **Brainfuck**.

Após identificar a linguagem, o próximo passo foi utilizar um interpretador para executar o código.

![Identificação do código como Brainfuck](https://github.com/user-attachments/assets/52dfc1ba-7aa2-48a3-8760-48e2fff8a328)

## Execução

Para interpretar o código, utilizei o [dCode — Brainfuck Language](https://www.dcode.fr/brainfuck-language).

O código fornecido pelo desafio foi inserido no interpretador e executado.

Durante a execução, as operações realizadas pelo programa manipulam os valores armazenados nas células de memória. Ao encontrar o comando `.`, o valor da célula atual é convertido em um caractere e enviado para a saída.

Dessa forma, após a execução completa do programa, o interpretador exibiu diretamente a flag do desafio.

![Saída do interpretador contendo a flag](https://github.com/user-attachments/assets/9be32b3e-d035-49ce-98d7-be4f307ed842)

## Conclusão

O desafio consistia em reconhecer que o conjunto de símbolos representava um programa escrito em **Brainfuck**.

Após identificar a linguagem, foi utilizado um interpretador compatível para executar o código. A execução revelou diretamente a flag, não sendo necessária uma segunda etapa de decodificação.

**Flag:**

```text
FLAG{c0d1g0_3s0t3r1c0}
```
