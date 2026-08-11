# Cookie Monster — Admin Access

> **Categoria:** Web Exploitation

## Introdução

Este desafio consiste em analisar o funcionamento de uma aplicação web e identificar uma falha relacionada ao controle de acesso de usuários. O objetivo é encontrar uma forma de obter acesso à área administrativa e, consequentemente, recuperar a flag escondida na aplicação.

**Desafio:** https://monster.discloud.app/

## Análise Inicial

Ao acessar o website, somos apresentados à aplicação **Cookie Monster**. Inicialmente, a página informa que o usuário não possui privilégios administrativos.

A mensagem apresentada pela aplicação é:

> `NOM NOM... Você não é admin!`

A partir dessa mensagem, podemos interpretar que existe algum mecanismo responsável por determinar se o usuário possui ou não privilégios de administrador.

Como o desafio é relacionado à exploração de uma aplicação web, uma das primeiras coisas a serem verificadas são as informações armazenadas pelo navegador, principalmente cookies e outros dados utilizados pela aplicação para manter informações sobre o usuário.

## Interpretação

Para investigar como a aplicação determina se o usuário é administrador, utilizamos as ferramentas de desenvolvedor (**DevTools**) disponibilizadas pelo navegador.

Dentro das DevTools, acessamos a aba **Application**, responsável por apresentar informações armazenadas pelo website, como cookies e outros dados relacionados à aplicação.

Durante a análise, foi encontrada uma chave chamada:

`admin`

O valor inicial dessa chave era:

`nao`

Isso indicava que a aplicação aparentemente utilizava esse valor para determinar se o usuário possuía privilégios administrativos.

Como essa informação estava armazenada no lado do cliente, foi possível testar se a aplicação confiava diretamente nesse valor para realizar o controle de acesso.

## Resolução

Com a chave `admin` identificada, alteramos seu valor de:

`nao`

para:

`sim`

Após realizar a alteração, atualizamos a página utilizando **F5**.

Ao carregar novamente a aplicação, o sistema reconheceu o novo valor da chave `admin` e passou a considerar o usuário como administrador.

Com o acesso administrativo obtido, foi possível visualizar a flag do desafio:

```text
FLAG{C00K1E_M0NST3R_MUNCH}
```

## Conclusão

Este desafio demonstrou uma falha relacionada ao **controle de acesso baseado em informações armazenadas no lado do cliente**.

A aplicação confiava em um valor controlado pelo usuário para determinar se ele possuía privilégios administrativos. Como esse valor podia ser alterado diretamente através das ferramentas de desenvolvedor do navegador, foi possível modificar o comportamento da aplicação e obter acesso administrativo.

Durante a resolução, foram utilizados principalmente os **DevTools**, através da aba **Application**, para identificar e modificar a chave `admin`.

Esse tipo de vulnerabilidade demonstra a importância de não confiar em informações fornecidas ou controladas pelo cliente para decisões de autorização. Em uma aplicação segura, a permissão de administrador deve ser validada no lado do servidor, evitando que o usuário consiga simplesmente modificar um valor local e obter privilégios elevados.
