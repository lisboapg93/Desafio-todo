# TODO List

Desafio baseado no teste de vaga backend junior da Simplify

API para gerenciar tarefas (CRUD) que faz parte desse desafio para pessoas desenvolvedoras backend júnior, que se candidatam para a Simplify.

## Tecnologias

Spring Boot
Spring MVC
Spring Data JPA
SpringDoc OpenAPI 3
Mysql

## Práticas adotadas

SOLID, DRY, YAGNI, KISS
API REST
Consultas com Spring Data JPA
Injeção de Dependências
Tratamento de respostas de erro
Geração automática do Swagger com a OpenAPI 3
C

### Como Executar

Clonar repositório git
Construir o projeto:
```sh
./mvnw clean package
```
Executar a aplicação:
```sh
$ java -jar target/todolist-0.0.1-SNAPSHOT.jar
```
A API poderá ser acessada em localhost:8080. O Swagger poderá ser visualizado em 
```sh
localhost:8080/swagger-ui.html
```

API Endpoints

Para fazer as requisições HTTP abaixo, foi utilizada a ferramenta httpie:

Criar Tarefa
```sh
http POST :8080/todos nome="Todo 1" descricao="Desc Todo 1" prioridade=1
```

[
{
"descricao": "Desc Todo 1",
"id": 1,
"nome": "Todo 1",
"prioridade": 1,
"realizado": false
}
]
Listar Tarefas
```sh
http GET :8080/todos
```

[
{
"descricao": "Desc Todo 1",
"id": 1,
"nome": "Todo 1",
"prioridade": 1,
"realizado": false
}
]
Atualizar Tarefa
```sh
http PUT :8080/todos/1 nome="Todo 1 Up" descricao="Desc Todo 1 Up" prioridade=2
```

[
{
"descricao": "Desc Todo 1 Up",
"id": 1,
"nome": "Todo 1 Up",
"prioridade": 2,
"realizado": false
}
]
Remover Tarefa
```sh
http DELETE :8080/todos/1
```

[ ]
