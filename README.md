## Sobre

Neste repositório há o resultado do projeto prático implementado no seminário de **Introdução ao Vue.js e Nuxt.js** apresentado por Samuel Lucas, membro do Programa Educação Tutorial do Curso de Ciência da Computação da Universidade Federal do Rio Grande do Norte.

## Requisitos

 - Node
 - Yarn (_ou NPM_ )

## Como instalar o projeto

Em seu computador execute os seguintes comandos para clonagem do repositório localmente e instalação das dependências do projeto:
```bash
# install dependencies

$ git clone https://github.com/Samuellucas97/Introducao-Nuxtjs 
$ cd Introducao-Nuxtjs

$ yarn install ## Ou npm install
```
Em seguida, crie dentro do projeto um arquivo chamado `.env` que conterá o endereço URL da API.

```
API_URL=https://jsonplaceholder.typicode.com/
```

## Como executar o projeto

### Modo Desenvolvimento

Para facilitar o desenvolvimento, aconselha-se a usar o programa no modo de desenvolvedor onde ocorre atualização automática em tela das mudanças feitas em código. Diante disso, execute o seguinte comando:

``` bash
$ yarn dev # Ou npm run dev
```

Em seguida, abra o navegador e acesse o seguinte endereço [http://localhost:3000](http://localhost:3000).

### Modo Produção

Em estágio de produção, aconselha-se a usar o programa no modo de produção. Diante disso, execute os seguintes comandos:



| Modo de deploy: | Comando:  |    
| :---------- | :------------- |
|Server Side Rendering	| `$ yarn build && yarn start` |  
|Site Static Generated 	| `$ yarn generate` |  

## Referências

 - [Nuxt.js - Documentação (inglês) ](https://nuxtjs.org/docs/2.x/get-started/installation)
 - [Awesome Nuxt - Lista de conteúdos ](https://github.com/nuxt-community/awesome-nuxt)
