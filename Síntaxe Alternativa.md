# WriteUp — Desafio Brainfuck

## Descrição

O desafio apresenta um conjunto de símbolos aparentemente aleatórios:

```text
+++++++[<++++++++++>-]<.[-]>+++++++[<++++++++++>-]<++++++.[-]>++++++[<++++++++++>-]<+++++.[-]>+++++++[<++++++++++>-]<+.[-]>++++++++++++[<++++++++++>-]<+++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++[<++++++++++>-]<.[-]>++++[<++++++++++>-]<+++++++++.[-]>++++++++++[<++++++++++>-]<+++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++[<++++++++++>-]<+++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<+++++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++++[<++++++++++>-]<++++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<++++.[-]>++++[<++++++++++>-]<+++++++++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++++[<++++++++++>-]<+++++.
```

A própria descrição informa que o conteúdo é um programa funcional e que é necessário descobrir como interpretá-lo.

## Identificando a linguagem

Analisando os caracteres utilizados, é possível perceber que o código utiliza principalmente:

* `+` — incrementa o valor da célula atual;
* `-` — decrementa o valor da célula atual;
* `<` — move o ponteiro uma posição para a esquerda;
* `>` — move o ponteiro uma posição para a direita;
* `[` e `]` — estruturas de repetição;
* `.` — imprime o caractere correspondente ao valor da célula.

Esses são justamente os comandos básicos da linguagem **Brainfuck**.

Portanto, o próximo passo foi executar o código utilizando um interpretador de Brainfuck.

<img width="441" height="216" alt="Captura de tela 2026-08-10 224359" src="https://github.com/user-attachments/assets/52dfc1ba-7aa2-48a3-8760-48e2fff8a328" />

## Execução

Utilizei um interpretador de Brainfuck e inseri o código fornecido pelo desafio.

Após executar o programa, o interpretador realizou todas as operações e converteu os valores das células em caracteres por meio do comando `.`.

A saída do programa foi diretamente a flag do desafio.

<img width="339" height="134" alt="Captura de tela 2026-08-10 224410" src="https://github.com/user-attachments/assets/9be32b3e-d035-49ce-98d7-be4f307ed842" />

## Conclusão

O desafio consistia em reconhecer que o conjunto de símbolos representava um programa escrito em **Brainfuck**.

Depois de identificar a linguagem, bastou utilizar um interpretador compatível para executar o código. A própria execução revelou diretamente a flag, não sendo necessário realizar uma segunda etapa de decodificação.

**Flag:** `[FLAG ENCONTRADA]`
