# Bem-vindo!

> **Categoria:** Web Exploitation
>

### Introdução

O desafio consiste em analisar uma aplicação web e encontrar uma informação escondida em seu código-fonte. Para isso, será necessário observar a estrutura da página e verificar se existem informações que não são exibidas diretamente ao usuário.

> **Página do desafio:** http://welcome.discloud.app/

### Análise Inicial

Ao acessar a página do desafio, é apresentada uma página simples, sem nenhuma informação aparente sobre a flag.

Diante disso, uma das primeiras abordagens em desafios de **Web Exploitation** é analisar o código-fonte da página, procurando por informações ocultas, comentários ou elementos que não estejam visíveis diretamente no navegador.

Para realizar essa análise, foram utilizadas as ferramentas de desenvolvedor (**DevTools**) disponibilizadas pelo navegador.

### Interpretação

Ao inspecionar o código HTML da página, foi possível observar que existiam informações presentes no código-fonte que não eram exibidas visualmente na página.

Durante a análise do HTML, foi encontrado um **comentário HTML** contendo a flag.

![Flag encontrada no código-fonte da página](https://github.com/user-attachments/assets/1186f2e3-5122-4fbd-81f5-39e320811e07)

Comentários HTML são utilizados pelos desenvolvedores para inserir anotações dentro do código e não são renderizados diretamente na página. Dessa forma, a informação presente no comentário não podia ser visualizada normalmente, sendo necessário inspecionar o código da aplicação.

### Resolução

Após localizar o comentário no código HTML, foi possível obter diretamente a flag do desafio:

```text
FLAG{W3B_1NTR0DUCT10N}
```

Não foi necessário realizar nenhuma alteração na aplicação ou explorar alguma vulnerabilidade mais complexa. A resolução consistiu apenas em analisar o código-fonte disponibilizado pelo próprio website.

### Conclusão

Neste desafio, foi possível praticar uma técnica básica de reconhecimento em aplicações web: a análise do código-fonte da página.

Mesmo que uma informação não esteja visível para o usuário, ela pode estar presente no HTML e ser encontrada através das ferramentas de desenvolvedor do navegador.

O desafio serviu como uma introdução à análise de aplicações web e à identificação de informações expostas no lado do cliente.

> **Flag:** `FLAG{W3B_1NTR0DUCT10}`
