# Clonar projeto do gitHub, criar confguração da API e testar
* Copiar url do projeto no gitHub
* Abrir o gitBash

**Clonar o repositório para sua máquina**
```
git clone URL_REPOSITORIO
```

**Acessar pasta**
```
cd NOME_REPOSITORIO
```

**Reinstalar os pacotes**
```
npm i
```
**Criar arquivo .env na raiz do projeto**
* Arquivo utilizado para armazenar as variáveis que serão reutilizadas na aplicação
```
nano .env
```
**Digitar no arquivo**
* Variável que contém a porta que o servidor estará rodando
```
PORT = 3008
```

**Adicionar arquivo .env no .gitignore**
* Informações sensíveis do sistema
```
nano .gitignore
```
```
.env
```

**Abrir o VSCode**
```
code .
```

**Criar arquivo de exemplo para as variáveis necessárias da aplicação**
* Como o arquivo .env não foi enviado para o gitHub, precisamos criar o exemplo das variáveis necessárias da aplicação
```
nano .env.example
```

**Adicionar no arquivo .env.example**
```
PORT = 
```

**Digitar no arquivo app.js**
* Importar o pacote express(servidor)
```
const express = require('express');
```

* Importar o pacote dotenv, gerenciador de variáveis de ambiente
```
const dotenv = require('dotenv').config();
```

* Instanciar o express na variável app
```
const app = express();
```

* Setar a porta do servidor a partir do arquivo .env
* O operador condicional '||' significa 'OU', caso não tenha a variável PORT, será utilizado o valor '3333'
```
app.set('port', process.env.PORT || 3333);
```

* Exportar as configurações na variável app
```
module.exports = app;
```

**Digitar no arquivo server.js**
* Importar o arquivo app
```
const app = require('./app');
```

* Importar a porta do servidor
```
const port = app.get('port');
```

* Testar API com a função listen
* 1º parâmetro: passamos a porta do servidor
* 2º parâmetro: arrow function para retornar um console informando a porta que está rodando o servidor
```
app.listen(port, () => {
    console.log(`Running on port ${ port }!`);
});
```

**Abrir o arquivo package.json e alterar a chave 'scripts'**
* Substituir o comando 'test' pelo comando 'start' na linha 7
```
"start":"nodemon src/server.js"
```

**Rodar o comando no terminal com gitBash**
```
npm run start
```

**Parar servidor e voltar**
```
Ctrl + c 
```

* Enviar os arquivos atualizados para o gitHub