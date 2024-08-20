<h1 align="center" style="font-weight: bold;">📃 API ToDo List</h1>
<p align="center">
 <a href="#tecnologias">Tecnologias</a> • 
<a href="#práticas-de-desenvolvimento">Práticas de Desenvolvimento</a> • 
 <a href="#executando-a-aplicação">Executando a aplicação</a> • 
  <a href="#api-endpoints">API Endpoints</a> 
</p>
<p align="center">
    <b>Esta API é projetada para gerenciar tarefas de forma eficiente e organizada. Ela suporta operações CRUD (Criar, Ler, Atualizar, Excluir) em tarefas, oferecendo uma solução abrangente para o gerenciamento de listas de tarefas.</b>
</p>

## 💻 Tecnologias
- Java
- Spring Boot
- Spring MVC
- Spring Data JPA
- SpringDoc OpenAPI 3
- MySQL

## 🛠️ Práticas de Desenvolvimento
- SOLID, DRY, YAGNI, KISS
- API REST
- Consultas com Spring Data JPA
- Injeção de Dependências
- Tratamento de Respostas de Erro
- Geração Automática de Swagger com OpenAPI 3

## 🚀 Executando a aplicação
### Clonar o repositório:

```bash
git clone your-project-url-in-github
```

### Construir o projeto:
```bash
$ ./mvnw clean package
```

### Executar a aplicação:
```bash
 java -jar target/todolist-0.0.1-SNAPSHOT.jar
```

## 📍 API Endpoints
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

