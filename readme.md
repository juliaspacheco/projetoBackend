# Criando pasta e organizando estrutura do projeto
* Abrir gitBash

Criar pasta para a aplicação
```
mkdir NOME PASTA
```
Acessar pasta
```
cd NOME PASTA
```
Criar arquivo para documentar projeto
```
touch readme.md
```
Iniciar o gerenciador de pacotes Node
```
npm init -y
```
Instalar os pacotes
```
npm i express nodemon dotenv
```
Abrir o VSCode
```
code .
```
Criar arquivo .gitignore
```
nano .gitignore
```
* Ctrl + o: Salvar o arquivo
* Enter: Confirmar
* Ctrl + x: Fechar o arquivo

Adicionar no arquivo .gitignore o nome da pasta criada após instalação dos pacotes
```
node_modules
```
Criar estrutura de arquivos e pastas
```
mkdir src
```
Criar arquivos dentro da pasta src
```
touch src/app.js
```
```
touch src/server.js
```
Criar pastas dentro da pasta src
```
mkdir src/config
```
```
mkdir src/controllers
```
```
mkdir src/routes
```
* Enviar estrutura do projeto para o gitHub