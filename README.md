API RESTful de Afazeres com Flask
API simples para gerenciamento de tarefas/afazeres desenvolvida com Flask, implementando operações CRUD completas e testes unitários.
📋 Sobre o Projeto
Este projeto é uma API RESTful para gerenciamento de tarefas (to-do list), permitindo criar, listar, atualizar e excluir tarefas. A API foi construída usando o microframework Flask e armazena os dados em memória, com testes unitários implementados usando pytest e requests.
🛠️ Tecnologias Utilizadas

Python
Flask (2.3.0)
Werkzeug (2.3.0)
Requests (2.31.0)
Pytest (7.4.3)

⚙️ Funcionalidades

Criar novas tarefas
Listar todas as tarefas
Buscar tarefa por ID
Atualizar tarefas existentes
Excluir tarefas
Marcar tarefas como concluídas/não concluídas

🚀 Instalação
Siga os passos abaixo para configurar o projeto em sua máquina local:
bash# Clone o repositório
git clone https://github.com/GuilhermeVicenteFigueira/Api-RestFull-de-Afazeres-com-CRUD-e-teste-unit-rios-.git

# Entre no diretório do projeto
cd Api-RestFull-de-Afazeres-com-CRUD-e-teste-unit-rios-

# Crie um ambiente virtual
python -m venv venv

# Ative o ambiente virtual
# No Windows:
venv\Scripts\activate
# No macOS/Linux:
source venv/bin/activate

# Instale as dependências
pip install -r requirements.txt

# Inicie o servidor de desenvolvimento
python app.py
🔄 API Endpoints
MétodoRotaDescriçãoPOST/tasksCria uma nova tarefaGET/tasksLista todas as tarefasGET/tasks/<id>Busca uma tarefa específica por IDPUT/tasks/<id>Atualiza uma tarefa existenteDELETE/tasks/<id>Remove uma tarefa
Exemplos de Uso
Criar uma nova tarefa
POST /tasks
Body:
json{
  "title": "Nova tarefa",
  "description": "Descrição da nova tarefa"
}
Resposta:
json{
  "message": "Nova tarefa criada com sucesso",
  "id": 1
}
Listar todas as tarefas
GET /tasks
Resposta:
json{
  "tasks": [
    {
      "id": 1,
      "title": "Nova tarefa",
      "description": "Descrição da nova tarefa",
      "completed": false
    }
  ],
  "total_tasks": 1
}
Buscar uma tarefa específica
GET /tasks/1
Resposta:
json{
  "id": 1,
  "title": "Nova tarefa",
  "description": "Descrição da nova tarefa",
  "completed": false
}
Atualizar uma tarefa
PUT /tasks/1
Body:
json{
  "title": "Título atualizado",
  "description": "Nova descrição",
  "completed": true
}
Resposta:
json{
  "message": "Tarefa atualizada com sucesso"
}
Deletar uma tarefa
DELETE /tasks/1
Resposta:
json{
  "message": "Tarefa deletada com sucesso"
}
📂 Estrutura do Projeto
.
├── app.py                # Arquivo principal da aplicação
├── models/
│   └── task.py           # Modelo da entidade Task
├── requirements.txt      # Dependências do projeto
└── test_app.py           # Testes unitários
✅ Testes
O projeto inclui testes unitários para validar o funcionamento correto da API:
bash# Para executar os testes, primeiro certifique-se de que a aplicação está rodando em http://127.0.0.1:5000
# Em um terminal separado, execute:
pytest
Os testes validam as seguintes operações:

Criação de tarefas
Listagem de todas as tarefas
Busca de uma tarefa específica
Atualização de tarefas
Exclusão de tarefas

💡 Notas Adicionais

A aplicação usa armazenamento em memória (lista Python) para as tarefas, portanto os dados são perdidos quando o servidor é reiniciado
O controle de ID é feito através de uma variável global incrementada a cada nova tarefa

👨‍💻 Autor
Guilherme Vicente Figueira

GitHub: @GuilhermeVicenteFigueira

🤝 Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

Faça um Fork do projeto
Crie sua Feature Branch (git checkout -b feature/AmazingFeature)
Commit suas mudanças (git commit -m 'Add some AmazingFeature')
Push para a Branch (git push origin feature/AmazingFeature)
Abra um Pull Request

📜 Licença
Este projeto está licenciado sob a licença MIT - consulte o arquivo LICENSE para obter detalhes.
