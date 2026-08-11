# Brainfuck

> **Categoria:** Misc
>
> **Autor:** M3SSAG3_MAN

### Introdução

O desafio apresenta um conjunto de símbolos aparentemente aleatórios e informa que esse conteúdo é, na verdade, um programa funcional.

O objetivo é descobrir como interpretar o código e, a partir da sua execução, obter a flag.

O código fornecido pelo desafio é:

```text
+++++++[<++++++++++>-]<.[-]>+++++++[<++++++++++>-]<++++++.[-]>++++++[<++++++++++>-]<+++++.[-]>+++++++[<++++++++++>-]<+.[-]>++++++++++++[<++++++++++>-]<+++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++[<++++++++++>-]<.[-]>++++[<++++++++++>-]<+++++++++.[-]>++++++++++[<++++++++++>-]<+++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++[<++++++++++>-]<+++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<+++++.[-]>++++[<++++++++++>-]<++++++++.[-]>+++++++++++[<++++++++++>-]<++++++.[-]>+++++[<++++++++++>-]<+.[-]>+++++++++++[<++++++++++>-]<++++.[-]>++++[<++++++++++>-]<+++++++++.[-]>+++++++++[<++++++++++>-]<+++++++++.[-]>++++[<++++++++++>-]<++++++++.[-]>++++++++++++[<++++++++++>-]<+++++.
```

### Análise Inicial

Ao observar o código, é possível perceber que ele é composto praticamente apenas por símbolos como `+`, `-`, `<`, `>`, `[` , `]` e `.`.

A princípio, esses caracteres não parecem representar um código convencional. Porém, essa combinação específica de símbolos é característica da linguagem de programação esotérica **Brainfuck**.

Dessa forma, em vez de tentar interpretar o conteúdo manualmente, o próximo passo foi identificar a linguagem e utilizar uma ferramenta capaz de executar o programa.

### Interpretação

O **Brainfuck** possui apenas oito comandos básicos, cada um responsável por uma operação específica sobre a memória:

* `+` — incrementa o valor da célula atual;
* `-` — decrementa o valor da célula atual;
* `>` — move o ponteiro para a próxima célula;
* `<` — move o ponteiro para a célula anterior;
* `[` — inicia um loop;
* `]` — encerra um loop;
* `.` — imprime o valor da célula atual como um caractere;
* `,` — recebe um caractere de entrada.

Ao comparar esses comandos com o código fornecido pelo desafio, fica evidente que estamos diante de um programa escrito em **Brainfuck**.

### Resolução

Para interpretar o programa, foi utilizado o [dCode — Brainfuck Language](https://www.dcode.fr/brainfuck-language).

<img width="441" height="216" alt="Captura de tela 2026-08-10 224359" src="https://github.com/user-attachments/assets/730a222c-a879-414b-ae5b-e3198a5f8f3d" />

O código fornecido pelo desafio foi inserido no interpretador e executado.

Durante a execução, o programa manipula os valores das células de memória utilizando os comandos da linguagem. Os comandos `[` e `]` são utilizados para realizar os loops, enquanto o comando `.` é responsável por enviar os valores calculados para a saída.

Após a execução completa do programa, o interpretador exibiu diretamente a flag do desafio:

<img width="339" height="134" alt="Captura de tela 2026-08-10 224410" src="https://github.com/user-attachments/assets/f29f5ec9-5b03-4ddf-b34c-1eb7e3fda7f7" />

```text
FLAG{c0d1g0_3s0t3r1c0}
```

### Conclusão

O desafio consistia principalmente em reconhecer a linguagem utilizada pelo código.

A presença dos caracteres `+`, `-`, `<`, `>`, `[`, `]` e `.` permitiu identificar o programa como **Brainfuck**. Após essa identificação, foi utilizado um interpretador para executar o código, obtendo diretamente a flag.

Não foi necessária uma etapa adicional de decodificação, pois a própria execução do programa já produziu a resposta esperada.

> **Flag:** `FLAG{c0d1g0_3s0t3r1c0}`
