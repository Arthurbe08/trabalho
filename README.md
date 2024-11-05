# trabalho
trabalho, senac3000talentos 04/11/2024

```js
// Importa o módulo 'express', que é um framework para construir aplicações web e APIs em Node.js.
const express = require('express');

// Cria uma instância do aplicativo Express, permitindo que você configure e manipule rotas e responda a solicitações.
const app = express();

// Define uma rota para o endpoint raiz ('/'). 
// Quando uma solicitação GET é feita para '/', essa função é executada.
app.get('/', function(request, response) {
    // Retorna uma resposta no formato JSON com uma mensagem de boas-vindas.
    return response.json({
        message: 'Olá Dev! Bem vindo ao curso!'
    });
});

// Define uma rota para o endpoint '/projects'.
// Quando uma solicitação GET é feita para '/projects', essa função é executada.
app.get('/bookshelf', function(request, response) {
    // Retorna uma resposta JSON com uma lista de projetos.
    return response.json([
        'livro 1',
        'livro 2'
    ]);
});

// Define uma rota para criar um novo projeto.
// Quando uma solicitação POST é feita para '/projects', essa função é executada.
app.post('/bookshelf', function(request, response) {
    // Retorna uma resposta JSON com uma lista de projetos, incluindo o novo projeto.
    return response.json([
        'livro 1',
        'livro 2',
        'livro 3'
    ]);
});

// Define uma rota para atualizar um projeto específico.
// O ':id' é um parâmetro de rota, que será substituído pelo ID do projeto na URL.
app.put('/bookshelf/:id', function(request, response) {
    // Retorna uma resposta JSON com a lista de projetos atualizada.
    return response.json([
        'livro 4',
        'livro 2',
        'livro 3'
    ]);
});

// Define uma rota para deletar um projeto específico.
// O ':id' permite especificar qual projeto deletar pelo ID.
app.delete('/bookshelf/:id', function(request, response) {
    // Retorna uma resposta JSON com a lista de projetos após a exclusão de um deles.
    return response.json([
        'livro 2',
        'livro 3'
    ]);
});

app.get('/bookshelf/:id' , function(request, response) {
    return response.json([
        'catchei the vision'
    ])
})
// Inicia o servidor na porta 3000 e exibe uma mensagem no console.
// O servidor ficará "ouvindo" solicitações HTTP nessa porta.
app.listen(3455, () => {
    console.log('Server started on port 3000! 🏆');
});
```
