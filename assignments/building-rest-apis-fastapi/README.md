# 📘 Atividade: Construindo APIs REST com FastAPI

## 🎯 Objective

Nesta atividade, você vai construir uma API REST usando FastAPI e modelos do Pydantic. Ao final, será capaz de criar rotas, implementar operações CRUD e validar os dados enviados pelos clientes.

## 📝 Tasks

### 🛠️ Criando as primeiras rotas

#### Descrição
Crie uma aplicação FastAPI para gerenciar uma lista de livros. Comece configurando o projeto e implemente rotas para apresentar a API e listar os livros disponíveis.

#### Requisitos
O programa concluído deve:

- Criar uma aplicação FastAPI executável com Uvicorn
- Implementar `GET /` com uma mensagem que identifique a API
- Implementar `GET /books` para retornar a lista de livros, inicialmente vazia
- Permitir consultar a documentação interativa da API em `/docs`

### 🛠️ Implementando operações CRUD

#### Descrição
Amplie a API para permitir cadastrar, consultar, atualizar e remover livros. Nesta etapa, mantenha os dados em memória; a persistência em banco de dados não faz parte do escopo.

#### Requisitos
O programa concluído deve:

- Definir um modelo de livro com identificador, título, autor e ano de publicação
- Implementar `POST /books` para cadastrar um livro e retornar o recurso criado
- Implementar `GET /books/{book_id}` para consultar um livro pelo identificador
- Implementar `PUT /books/{book_id}` para atualizar os dados de um livro existente
- Implementar `DELETE /books/{book_id}` para remover um livro existente
- Retornar o status HTTP `404` quando o identificador não corresponder a um livro

### 🛠️ Validando e verificando a API

#### Descrição
Melhore a confiabilidade da API validando os dados de entrada e verificando as respostas das rotas. Use a documentação interativa ou um cliente HTTP para testar os casos válidos e inválidos.

#### Requisitos
O programa concluído deve:

- Usar modelos do Pydantic para validar os dados recebidos
- Rejeitar livros sem título ou autor e anos de publicação inválidos
- Retornar respostas com os status HTTP apropriados para criação, sucesso e recurso não encontrado
- Testar o fluxo completo de criação, consulta, atualização e remoção de um livro
- Verificar pelo menos um caso de entrada inválida e um caso de livro inexistente
