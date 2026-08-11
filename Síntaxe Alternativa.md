# Brainfuck

> **Categoria:** Misc
>

### Introdução

O desafio apresenta um conjunto de símbolos aparentemente aleatórios e informa que esse conteúdo é, na verdade, um programa funcional.

O objetivo é descobrir como interpretar o código e, a partir da sua execução, obter a flag.

O código fornecido pelo desafio é:

```text id="8r7k2p"
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

Ao comparar esses comandos com o código fornecido pelo desafio, fica evidente que estamos diante de um programa escrito em Brainfuck.

### Resolução

Para interpretar o programa, foi utilizado o [dCode — Brainfuck Language](https://www.dcode.fr/brainfuck-language).

O código fornecido pelo desafio foi inserido no interpretador e executado.

Durante a execução, o programa manipula os valores das células de memória utilizando os comandos da linguagem. Os comandos `[` e `]` são utilizados para realizar os loops, enquanto o comando `.` é responsável por enviar os valores calculados para a saída.

Após a execução completa do programa, o interpretador exibiu diretamente a flag do desafio:

```text id="n5k1vb"
FLAG{c0d1g0_3s0t3r1c0}
```

### Conclusão

O desafio consistia principalmente em reconhecer a linguagem utilizada pelo código.

A presença dos caracteres `+`, `-`, `<`, `>`, `[` , `]` e `.` permitiu identificar o programa como **Brainfuck**. Após essa identificação, foi utilizado um interpretador para executar o código, obtendo diretamente a flag.

Não foi necessária uma etapa adicional de decodificação, pois a própria execução do programa já produziu a resposta esperada.

> **Flag:** `FLAG{c0d1g0_3s0t3r1c0}`
