# Gerenciador de Tarefas

Aplicação web para gerenciamento de tarefas, desenvolvida como atividade da disciplina de **Desenvolvimento Frontend**. O sistema permite cadastrar, consultar, atualizar e excluir tarefas, com persistência de dados em MySQL e comunicação entre frontend e backend por meio de uma API HTTP.

## Objetivo

Aplicar os conceitos de desenvolvimento web em uma aplicação com operações de **CRUD (Create, Read, Update e Delete)**, integrando uma interface construída com HTML, CSS e JavaScript a um servidor Node.js com Express e a um banco de dados MySQL.

## Funcionalidades

- Cadastro de tarefas com nome e horário.
- Consulta e listagem das tarefas cadastradas.
- Alteração do estado de conclusão das tarefas.
- Filtros de visualização: todas, pendentes e concluídas.
- Exclusão de tarefas.
- Persistência das informações no banco de dados.

## Tecnologias utilizadas

- **HTML5:** estrutura da interface.
- **CSS3:** estilização da aplicação.
- **JavaScript:** manipulação do DOM e requisições à API.
- **Node.js e Express:** servidor e rotas HTTP.
- **MySQL:** armazenamento dos dados.
- **MySQL2:** comunicação entre o servidor e o banco.
- **body-parser:** interpretação dos corpos JSON recebidos pela API.

## Estrutura do projeto

```text
projeto/
├── public/          # Arquivos HTML, CSS e JavaScript do frontend
├── cript.sql   # Criação do banco de dados e da tabela tarefas
├── db.js            # Configuração da conexão com o MySQL
├── server.js        # Servidor Express e rotas CRUD
├── package.json     # Dependências do projeto
├── package-lock.json # Versões das dependências instaladas
└── README.md        # Documentação
```


## Rotas da API

| Método | Endpoint | Descrição | Resposta de sucesso |
| --- | --- | --- | --- |
| `GET` | `/tarefas` | Retorna as tarefas cadastradas | `200 OK` |
| `POST` | `/tarefas` | Cadastra uma tarefa | `201 Created` |
| `PATCH` | `/tarefas/:id` | Altera o status de conclusão | `200 OK` |
| `DELETE` | `/tarefas/:id` | Remove uma tarefa | `204 No Content` |

### Exemplos de requisições

**Cadastro — `POST /tarefas`:**

```json
{
  "nome": "Estudar Node.js",
  "horario": "18:00"
}
```

**Atualização — `PATCH /tarefas/1`:**

```json
{
  "concluido": 1
}
```

O campo `concluido` utiliza `0` para pendente e `1` para concluída.

## Instalação e execução

### Pré-requisitos

- Node.js e npm.
- MySQL Server.
- MySQL Workbench ou outro cliente MySQL (para executar o script SQL).

### Passos

1. Clone o repositório:

   ```bash
   git clone URL_DO_REPOSITORIO
   cd NOME_DA_PASTA
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Abra o arquivo **`script.sql`** no MySQL Workbench (ou em outro cliente MySQL) e execute os comandos para criar o banco de dados e a tabela `tarefas`. Confira se o nome do banco no script corresponde ao utilizado no `db.js`.
4. Configure o arquivo `db.js` com os dados de conexão do seu ambiente. Não utilize credenciais reais versionadas no Git.
5. Inicie a aplicação:

   ```bash
   node server.js
   ```

6. Abra `http://localhost:3000` no navegador.

## Requisitos acadêmicos atendidos

- Interface web em HTML, CSS e JavaScript.
- Backend desenvolvido com Node.js e Express.
- Integração com banco de dados MySQL.
- Operações de inclusão, consulta, alteração e exclusão.
- Documentação de instalação e execução.

## Integrantes


- Roberto Rosado - roberto-ros4do - 47938439
- Rafael Oliveira - ROS757 -
- Matheus Mendes - mendesmatheus846 -
- Julia Rodrigues - juliarodriguesbezerra02-cell -
- Nicole Albuquerque - nicolealbuquerque2006 -

## Disciplina

**Desenvolvimento Front-End para Web**
