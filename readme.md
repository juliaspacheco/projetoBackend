# Testar rotas da API com o Insomnia
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
**Recriar o arquivo .env**
* Definir as variáveis no arquivo .env a partir das chaves definidas no arquivo .env.example
```
PORT = 3000
```

**Testar os endpoints (rotas) da API:**

## Insomnia
* Programa open source feito em javascript. O programa é um testador de rotas para APIs, como todos os outros (por exemplo o postman), você coloca a url da API e o caminho da rota

* Abrir o Insomnia no computador

* Criar um novo projeto, clicando no símbolo de '+'

* Dar um nome ao projeto e clicar no botão 'Create'

* Com o projeto criado, clicar no botão 'New Collection'

* Dar um nome para a coleção e clicar no botão 'Create'

* Criar a primeira requisição para a API clicando no botão 'New HTTP Request'

* Todas as requisições desta coleção ficam listadas no quadro da esquerda

* Por padrão a requisição é criada no método GET, mas podemos alterar o método da requisição clicando no ícone de seta para baixo ao lado do nome 'GET'

* Descrever a url da API com a porta que foi definida
```
http://localhost:3000
```

* e as rotas (/api/listar) que criamos no arquivo rotas.js do passo anterior. Ficará assim:
```
http://localhost:3000/api/listar
```
* Antes de clicar no botão 'Send' para executar a ação da rota, execute o comando 'npm start' no gitBash e  verifique se o retorno estará rodando na porta definida para o servidor

* Exemplo:

```
'Running on port 3000!'
```

* Após validar que a API esta rodando, execute a ação da rota clicando no botão 'Send'

* O Insomnia deverá retornar a mensagem descrita no método GET do arquivo de rotas

### Método GET
<img src="img/Método GET.png">

## Fazer o mesmo processo com os próximos métodos (POST, PUT e DELETE)

### Método POST
<img src="img/Método POST.png">

### Método PUT
<img src="img/Método PUT.png">

### Método DELETE
<img src="img/Método DELETE.png">

**Enviar os arquivos atualizados para o gitHub**