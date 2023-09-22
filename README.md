<h2>Desafio referente ao módulo: Fundamentos do Node.js</h2> 

<h3>Sobre</h3>

Criar uma API para realizar o CRUD de tarefas. A aplicação contem as seguintes funcionalidades:

- [x] Criação de task.
- [x] Listagem de todas as tasks.
- [x] Atualização de uma task pelo `id`.
- [x] Remoção uma task pelo `id`.
- [x] Marcar pelo `id` uma task como completa.
- [x] Importação de tasks em massa por um arquivo CSV.

As tasks possuem as seguintes propriedades:

- **_id_** - Identificador único de cada task.
- **_title_** - Título da task.
- **_description_** - Descrição detalhada da task.
- **_completed_at_** - Data de quando a task foi concluída. O valor inicial deve ser `null`.
- **_created_at_** - Data de quando a task foi criada.
- **_updated_at_** - Deve ser sempre alterado para a data de quando a task foi atualizada.

<h3>Rotas da aplicação</h3>

<details>
  <summary>GET - <code>/tasks</code></summary>
  <br>
    Lista todas as tasks salvas no banco de dados. Também é possível realizar uma busca, filtrando as tasks pelo <code>title</code> e <code>description</code>.
</details>

<details>
  <summary>POST - <code>/tasks</code></summary>
  <br>
  Cria uma task no banco de dados com os campos <code>title</code> e <code>description</code> recebidos por meio do <code>body</code> da requisição.
  Ao criar uma task, os campos: <code>id</code>, <code>created_at</code>, <code>updated_at</code> e <code>completed_at</code> são preenchidos automaticamente, conforme a descrição das propriedades de uma task acima.
</details>

<details>
  <summary>PUT - <code>/tasks/:id</code></summary>
  <br>
  Rota para atualizar uma task pelo <code>id</code>.
  O <code>body</code> da requisição, deve conter somente o <code>title</code> e/ou <code>description</code> para serem atualizados. Se for enviado somente o <code>title</code>, significa que o <code>description</code> não será atualizado e vice-versa.
</details>

<details>
  <summary>DELETE - <code>/tasks/:id</code></summary>
  <br>
  Remove uma task pelo <code>id</code>.
</details>

<details>
  <summary>PATCH - <code>/tasks/:id/complete</code></summary>
  <br>
  Marca uma task como completa ou incompleta.
</details>

