# Testes automatizados com Cypress web e api
👋 Seja bem-vindo(a)!

git clone "url do projeto"

# Pré-requisitos

Antes de começar, garanta que os seguintes sistemas estejam instalados em seu computador.

- [git](https://git-scm.com/) (estou usando a versão `2.41.0` enquanto escrevo este readme)
- [Node.js](https://nodejs.org/en/) (estou usando a versão `v16.17.0` enquanto escrevo este readme)
- npm (estou usando a versão `9.8.1` enquanto escrevo este readme)
- [Visual Studio Code](https://code.visualstudio.com/) (estou usando a versão `1.64.0` enquanto escrevo este readme) ou alguma outra IDE de sua preferência

> **Obs.:** Recomendo utilizar as mesmas versões, ou versões mais recentes dos sistemas listados acima.
>
> **Obs. 2:** Ao instalar o Node.js o npm é instalado junto. 🎉
>
> **Obs. 3:** Para verificar as versões do git, Node.js e npm instaladas em seu computador, execute o comando `git --version && node --version && npm --version` no seu terminal de linha de comando.
>
> **Obs. 4:** Deixei links para os instaladores na lista de requisitos acima, caso não os tenha instalados ainda.

## Instalação e inicialização do [Cypress](https://cypress.io) 🌲

Dado que você já tenha realizado as configurações descritas anteriormente, agora vamos configurar o nosso projeto cypress com typescript. 

1. Crie uma pasta com um nome, para identificar onde estará alocado os seus scripts de testes.
2. Abra a pasta com o vs code, podendo clicar com o botão direito e escolhendo o editor de código mencionado ou de sua preferência.
3. Iniciamos a configuração do projeto com o comando `npm init -y`, no terminal, com esse comando o arquivo package.json será criado. 
   No campo “scripts” do arquivo vamos adicionar o comando “cypress”: “cypress open”, como demonstra o exemplo abaixo.   
{
  "name": "typescript",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "cypress": "cypress open"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}

4. Na raiz do projeto, execute o comando `npm install cypress@12.7.0 --save-dev` (ou `npm i cypress@12.7.0 -D` para a versão curta)


## Na Pasta do Projeto Instalar as dependecias padrão do Projeto de uma vez (opção).

- npm i @faker-js/faker cypress@12.7.0 cypress-plugin-api typescript -D

## Configurano o tsconfig.json

Após realizada as instalações, vamos criar um arquivo na raiz do projeto com onome tsconfig.json, e nele vamos inserir o seguinte arquivo 
{
  "compilerOptions": {
    "target": "es5",
    "lib": ["es5", "dom"],
    "types": ["cypress", "node"]
  },
  "include": ["**/*.ts"]
}

- [Link da documentação do cypress onde se econtra o arquivo ](https://docs.cypress.io/guides/tooling/typescript-support)

## Logo após, execute o comando `npx cypress open` para abrir o Cypress pela primeira vez
- Após executar esse comando, o Cypress ira ser executado e ira criar o arquivo cypress.config.ts (o .ts significa que a extensão do arquivo é typescript) 

## Executando testes em modo headless setando um navegador especifico (google chrome).

- npx cypress run --browser chrome

## Executando specs individuais, no caso o que sencontra entre " " é o caminho Xpath do arquivo/teste a ser executado.  

- npx cypress run --spec "cypress\e2e\test-web-e2e\portal-uranus\porturn-login\login-user.cy.js" --browser chrome --headless



