<img src="https://hermes.dio.me/tracks/169e3d0f-263a-4efb-86c5-244bdf1ce8d6.png" width=100>

# Lista de Tarefas

A proposta deste desafio é construir um sistema gerenciador de tarefas, onde o usuário poderá cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

A aplicação é um CRUD do tipo `webapi` do .NET e utiliza o `Entity Framework`.

## Sobre o projeto

**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

## Schema das tarefas

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```

## Como testar

1. Substitua a string de conexão do seu banco de dados no arquivo [`appsettings.Development.json`](appsettings.Development.json);

2. Com o `.NET` e o `Entity Framework` já instalados no seu pc e o SQL Server iniciado, execute o comando:

    ```bash
      dotnet-ef migrations add TabelaTarefas
    ```

3. Atualize o seu banco

    ```bash
      dotnet-ef database update
    ```

4. Por último, basta rodar o comando abaixo e acessar o link fornecido no terminal:

    ```bash
      dotnet watch run
    ```

## Contribuição

Caso você encontrei algum erro ou queira fazer alguma melhoria, sinta-se à vontade para abrir um Pull Request ou uma issue!

---
Obrigada por visitar meu repositório e não esquece de visitar meus outros projetos! 💜
