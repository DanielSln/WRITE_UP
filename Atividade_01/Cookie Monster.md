# Cookie Monster — Admin Access

> **Categoria:** Web Exploitation
>

### Introdução

O desafio consiste em analisar uma aplicação web e identificar uma possível falha no mecanismo responsável pelo controle de acesso de usuários.

O objetivo é conseguir acesso à área administrativa da aplicação e, posteriormente, encontrar a flag disponibilizada pelo sistema.

> **Página do desafio:** https://monster.discloud.app/

### Análise Inicial

Ao acessar a aplicação, somos apresentados ao **Cookie Monster**. Inicialmente, a página informa que o usuário atual não possui privilégios administrativos.

A mensagem apresentada pela aplicação é:

> `NOM NOM... Você não é admin!`

A partir dessa mensagem, podemos deduzir que existe algum mecanismo utilizado pela aplicação para determinar se o usuário possui ou não privilégios administrativos.

Como o desafio pertence à categoria **Web Exploitation**, uma das primeiras abordagens é verificar as informações armazenadas pelo navegador, como cookies e outros dados utilizados pela aplicação para manter informações relacionadas ao usuário.

### Interpretação

Para investigar como a aplicação determina se o usuário é administrador, foram utilizadas as ferramentas de desenvolvedor (**DevTools**) disponibilizadas pelo navegador.

Dentro das DevTools, acessamos a aba **Application**, que permite visualizar informações armazenadas pelo website, incluindo cookies e outros dados relacionados à aplicação.

Durante a análise, foi encontrada uma chave chamada:

```text
admin
```

O valor inicial dessa chave era:

```text
nao
```

![Cookie admin com valor nao](https://github.com/user-attachments/assets/c0bc61fd-67ab-498a-8fdb-ad51e18f5c20)

Esse comportamento indica que a aplicação aparentemente utiliza o valor dessa chave para determinar se o usuário possui privilégios administrativos.

Como essa informação estava armazenada no lado do cliente, foi possível verificar se o sistema confiava diretamente nesse valor para realizar o controle de acesso.

### Resolução

Após identificar a chave `admin`, foi realizado um teste alterando o seu valor.

O valor original:

```text
nao
```

foi alterado para:

```text
sim
```

![Cookie admin alterado para sim](https://github.com/user-attachments/assets/604ac570-dc1d-469f-bdbf-df3e0fe47851)

Após realizar a alteração, a página foi atualizada utilizando **F5**.

Ao carregar novamente a aplicação, o sistema reconheceu o novo valor da chave `admin` e passou a considerar o usuário como administrador.

Com o acesso administrativo obtido, a aplicação passou a disponibilizar a flag:

```text
FLAG{C00K1E_M0NST3R_MUNCH}
```

![Flag encontrada após obter acesso administrativo](https://github.com/user-attachments/assets/1cc882af-16c7-49f0-9b1e-6764ef8c3446)

### Conclusão

Neste desafio, foi possível identificar uma falha relacionada ao **controle de acesso baseado em informações armazenadas no lado do cliente**.

A aplicação confiava diretamente no valor da chave `admin` para determinar se o usuário possuía privilégios administrativos. Como esse valor podia ser alterado através das ferramentas de desenvolvedor do navegador, foi possível modificar o comportamento da aplicação e obter acesso à área administrativa.

O desafio demonstra a importância de não confiar em informações controladas pelo cliente para implementar mecanismos de autenticação ou autorização.

> **Flag:** `FLAG{C00K1E_M0NST3R_MUNCH}`
