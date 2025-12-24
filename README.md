# WorkoutAPI

Uma API assíncrona desenvolvida com **FastAPI** para gerenciamento de treinos de Crossfit. Este projeto faz parte do desafio prático da trilha de Python da **DIO (Digital Innovation One)**.

## 🛠️ Tecnologias Utilizadas

* **Python 3.11+**
* **FastAPI** (Framework Web)
* **Alembic** (Migrações de Banco de Dados)
* **SQLAlchemy** (ORM)
* **Pydantic** (Validação de Dados)
* **PostgreSQL** (Banco de Dados Principal)
* **Docker** & **Docker Compose** (Containerização)

## 🚀 Como Executar o Projeto

### Pré-requisitos
* Python instalado
* Docker e Docker Compose instalados

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/SEU_USUARIO/NOME_DO_REPO.git](https://github.com/SEU_USUARIO/NOME_DO_REPO.git)
    cd workout_api
    ```

2.  **Configure as variáveis de ambiente:**
    Crie um arquivo `.env` na raiz do projeto baseando-se no exemplo (se houver) ou configure a `DATABASE_URL` para o Postgres.

3.  **Suba o Banco de Dados com Docker:**
    ```bash
    docker-compose up -d
    ```

4.  **Aplique as migrações (Crie as tabelas):**
    ```bash
    make run-migrations
    # Ou manualmente: alembic upgrade head
    ```

5.  **Execute a API:**
    ```bash
    make run
    # Ou manualmente: uvicorn workout_api.main:app --reload
    ```

6.  **Acesse a Documentação:**
    Abra o navegador em: `http://localhost:8000/docs`

## 📚 Endpoints Principais

* `/atletas`: Criar e listar atletas.
* `/categorias`: Gerenciar categorias de treino.
* `/centro_treinamento`: Gerenciar os locais de treino.

## 📋 Estrutura do Banco de Dados
O projeto utiliza **SQLAlchemy** com **Alembic** para versionamento do esquema. As tabelas principais são `atletas`, `categorias` e `centro_treinamento`.

---
Desenvolvido por [Seu Nome] durante o Bootcamp Python da DIO.