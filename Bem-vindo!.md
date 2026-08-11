# WriteUp — Bem-vindo!

## Descrição

Ao acessar a página fornecida pelo desafio:

```text
http://welcome.discloud.app/
```

é apresentada uma mensagem indicando que devemos analisar a página para obter a flag.

## Análise da página

Primeiramente, acessei a página normalmente pelo navegador.

Em seguida, utilizei a ferramenta de **Inspecionar Elemento** (`F12`) para analisar o código HTML da página.

Durante a análise, procurei por elementos e comentários presentes no código-fonte. No HTML, foi possível encontrar a flag escondida dentro de um comentário.

<img width="867" height="314" alt="Captura de tela 2026-08-10 225240" src="https://github.com/user-attachments/assets/1186f2e3-5122-4fbd-81f5-39e320811e07" />


Como comentários HTML não são exibidos diretamente na página para o usuário, a flag não aparecia visualmente, sendo necessário analisar o código da página.

## Resultado

Após localizar o comentário no HTML, encontrei diretamente a flag do desafio:

```text
FLAG{W3B_1NTR0DUCT10N}
```

## Conclusão

O objetivo do desafio era identificar uma informação escondida no código-fonte da página.

A resolução consistiu em:

1. Acessar a página fornecida;
2. Abrir as ferramentas de desenvolvedor do navegador;
3. Inspecionar o código HTML;
4. Localizar o comentário contendo a flag;
5. Copiar a flag encontrada.

Não foi necessário realizar nenhuma exploração ou alteração na aplicação, apenas analisar o código-fonte disponibilizado pelo próprio site.
