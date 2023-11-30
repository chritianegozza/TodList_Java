## API de Gerenciamento de Tarefas


Esta é uma API simples de gerenciamento de tarefas desenvolvida em Java com Spring Boot, que oferece operações padrão de CRUD para tarefas. A API utiliza enums para representar status e prioridade, e emprega LocalDate para lidar com datas.

## Sumário

Pré-requisitos
Configuração
Modelo de Dados
Endpoints
Uso
Exemplos de Requisições
Contribuição
Licença
Pré-requisitos
Java 8 ou superior
Maven
MySQL (ou outro banco de dados compatível)


## Configuração

1 Clone este repositório:
git clone https://github.com/chritianegozza/TodList_Java.git
cd api-gerenciamento-tarefas

2 Configure o banco de dados no arquivo src/main/resources/application.properties.

Configure o banco de dados no arquivo src/main/resources/application.properties.



## Modelo de Dados

A entidade Task é definida com os seguintes atributos:

id (Long): Identificador único da tarefa.
title (String): Título da tarefa.
description (String): Descrição da tarefa.
status (Enum [TODO, IN_PROGRESS, DONE]): Status atual da tarefa.
priority (Enum [LOW, MEDIUM, HIGH]): Prioridade da tarefa.
dueDate (LocalDate): Data de vencimento da tarefa.
Endpoints
GET /api/tasks: Retorna todas as tarefas.
GET /api/tasks/{id}: Retorna uma tarefa específica pelo ID.
POST /api/tasks: Cria uma nova tarefa.
DELETE /api/tasks/{id}: Exclui uma tarefa pelo ID.
PUT /api/tasks/{id}: Atualiza todas as informações de uma tarefa pelo ID.
PATCH /api/tasks/{id}: Atualiza parcialmente uma tarefa pelo ID.
Uso

## Inicie o aplicativo:

mvn spring-boot:run

Acesse a documentação Swagger para interagir com a API:

http://localhost:8080/swagger-ui.html

## Exemplos de Requisições

Criar uma nova tarefa (POST):

curl -X POST -H "Content-Type: application/json" -d '{"title": "Estudar Spring Boot", "description": "Concluir tutorial sobre Spring Boot", "status": "TODO", "priority": "HIGH", "dueDate": "2023-12-31"}' http://localhost:8080/api/tasks

Atualizar uma tarefa existente (PUT):

curl -X PUT -H "Content-Type: application/json" -d '{"title": "Estudar Spring Boot Avançado", "description": "Explorar recursos avançados do Spring Boot", "status": "IN_PROGRESS", "priority": "HIGH", "dueDate": "2024-01-15"}' http://localhost:8080/api/tasks/1


Obter todas as tarefas (GET):

curl http://localhost:8080/api/tasks


## Contribuição
Se você encontrar problemas ou melhorias possíveis, sinta-se à vontade para abrir um problema ou enviar uma solicitação pull.

## Licença
Este projeto está licenciado sob a Licença MIT.

### Imagens da Equipe

<table>
  <tr>
         <td align="center"><a href="https://github.com/chritianegozza"><img src="https://avatars.githubusercontent.com/u/72118415?v=4" width="100px;" alt=""/><br /><sub><b>Christiane Gozza</b></sub></a><br /><a href="https://github.com/chritianegozza">👩🏻‍💻</a></td>
         <br>
         <td align="center"><a href="https://github.com/flavia45"><img src="https://avatars.githubusercontent.com/u/147008248?v=4" width="100px;" alt=""/><br /><sub><b>Flávia</b></sub></a><br /><a href="https://github.com/flavia45">👩🏻‍💻</a></td> 
        <br>
         <td align="center"><a href="https://github.com/robconceicao"><img src="https://avatars.githubusercontent.com/u/97703445?v=4" width="100px;" alt=""/><br /><sub><b>Roberto Tadeu</b></sub></a><br /><a href="https://github.com/robconceicao">👩🏻‍💻</a></td> 
    </tr>
</table>
