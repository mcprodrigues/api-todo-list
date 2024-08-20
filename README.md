<h1 align="center" style="font-weight: bold;">📃 API ToDo List</h1>
<p align="center">
 <a href="#tech">Tecnologias</a> • 
<a href="#practices">Práticas de Desenvolvimento</a> • 
 <a href="#started">Executando a aplicação</a> • 
  <a href="#routes">API Endpoints</a> 
</p>
<p align="center">
    <b>Esta API é projetada para gerenciar tarefas de forma eficiente e organizada. Ela suporta operações CRUD (Criar, Ler, Atualizar, Excluir) em tarefas, oferecendo uma solução abrangente para o gerenciamento de listas de tarefas.</b>
</p>

<h2 id="technologies">💻 Tecnologias</h2>
- Java
- Spring Boot
- Spring MVC
- Spring Data JPA
- SpringDoc OpenAPI 3
- MySQL

<h2 id="practices">🛠️ Práticas de Desenvolvimento</h2>
- SOLID, DRY, YAGNI, KISS
- API REST
- Consultas com Spring Data JPA
- Injeção de Dependências
- Tratamento de Respostas de Erro
- Geração Automática de Swagger com OpenAPI 3

<h2 id="started">🚀 Executando a aplicação</h2>
<h3>Clonar o repositório:</h3>

```bash
git clone your-project-url-in-github
```

<h3>Construir o projeto:</h3>
```bash
$ ./mvnw clean package
```

<h3>Executar a aplicação:</h3>
```bash
$ java -jar target/todolist-0.0.1-SNAPSHOT.jar
```

<h2 id="routes">📍 API Endpoints</h2>
Para fazer as requisições HTTP, foi utilizada a ferramenta [httpie](https://httpie.io):
- Criar Tarefa
```
$ http POST :8080/todos nome="Todo 1" descricao="Desc Todo 1" prioridade=1

[
  {
    "descricao": "Desc Todo 1",
    "id": 1,
    "nome": "Todo 1",
    "prioridade": 1,
    "realizado": false
  }
]
```

- Listar Tarefas
```
$ http GET :8080/todos

[
  {
    "descricao": "Desc Todo 1",
    "id": 1,
    "nome": "Todo 1",
    "prioridade": 1,
    "realizado": false
  }
]
```

- Atualizar Tarefa
```
$ http PUT :8080/todos/1 nome="Todo 1 Up" descricao="Desc Todo 1 Up" prioridade=2

[
  {
    "descricao": "Desc Todo 1 Up",
    "id": 1,
    "nome": "Todo 1 Up",
    "prioridade": 2,
    "realizado": false
  }
]
```

- Remover Tarefa
```
http DELETE :8080/todos/1

[ ]
```

