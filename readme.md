# Clonar projeto do gitHub, criar a configuração do arquivo de rotas
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
**Criar pasta dentro da pasta src**
```
mkdir src/routes
```

**Criar arquivo dentro da pasta routes**
* Responsável pelas rotas que serão acessadas na API
```
touch src/routes/rotas.js
```

**Abrir o VSCode**
```
code .
```

**Digitar no arquivo rotas.js**
```
// Importar o modulo de Router do express
const { Router } = require('express');

// Instanciar o Router na variável router
const router = Router();

router.get('/listar', (request, response) => {
    response.send('Método GET: listar informações');
});
router.post('/cadastrar', (request, response) => {
    response.send('Método POST: salvar informações');
});
router.put('/user/:id', (request, response) => {
    response.send('Método PUT: atualizar informações');
});
router.delete('/user/:id', (request, response) => {
    response.send('Método DELETE: remover informações');
});

module.exports = router;
```

**Digitar no arquivo app.js**
* Importar o arquivo de rotas nas configurações da API
* Habilitar as rotas na aplicação
```
const router = require('./routes/rotas');
```
```
app.use('/api', router);
```
* Esta linha deve inserida depois da criação da variável app



* Enviar os arquivos atualizados para o gitHub