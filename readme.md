# Documentação da API

* Escolher um local do computador apra criar o projeto
* Abrir o gitBash nesta pasta

Com o gitBash aberto executar o comando para criar a raiz do projeto: (mkdir: make diretorio = criar pasta)
```
mkdir NOME_PROJETO
```
Acessar a pasta
```
cd NOME_PROJETO
```
Comando para abrir o VSCode
```
code .
```
Criar o arquivo gerenciador de pacotes node
```
npm init -y
```
Criar arquivo .gitignore na raiz do projeto
```
touch .gitignore
```
Criar arquivo .env (arquivo para reservar variaveis do projeto)
```
touch .env
```
## Instalar os pacotes do projeto

### Testes

#### Teste

##### Teste

Instalar os pacotes para o projeto
```
npm i express nodemon dotenv
```
* express: sera o servidor da api
* nodemon: atualiza os arquivos alterados sem para o servidor
* dotenv: gerenciador de variaveis de ambiente

Criar pasta src
```
mkdir src
```
Criar arquivo server.js dentro da pasta src
```
touch src/server.js
```
Adicionar arquivos e pastas no gitigonre
```
node_modules.env
```
adicionar a porta do servidor no arquivo .env
```
PORT = 3004
```
Configurção básica da  da API com express
```
// Importar o pacote express
const express = require('express');

// Instanciar o express na variavel app
const app = express();

// Recuperar o pacote dotenv
const dotenv = require('dotenv').config();

// Importando variavel do arquivo .env
const PORT = process.env.PORT;

// Testando o servidor
app.listen(PORT, () => console.log(`Running at port ${PORT}!`));
```
Criar comando para criar o servidor do arquivo package.json
```
"start":"nodemon src/server.js"
```
|Rodar o servidor
```
npm start
```