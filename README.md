# Flask API Project

Este projeto consiste em uma API simples construída com **Flask**, permitindo operações CRUD (Create, Read, Update, Delete) em uma coleção de itens.

## Install Flask 
python -m venv venv
source venv/bin/activate 
pip3 install Flask



## 🚀 Tecnologias Utilizadas

- **Python**
- **Flask**
- **Flask-JSONify** (para respostas JSON)

## 📌 Como Executar o Projeto

### 1️⃣ Pré-requisitos
Antes de executar o projeto, certifique-se de ter instalado:
- [Python 3.x](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/)

### 2️⃣ Instalação
Clone o repositório e navegue até a pasta do projeto:

```bash
git clone https://github.com/seu-repo/nome-do-projeto.git
cd nome-do-projeto
```

Crie e ative um ambiente virtual:

```bash
# No macOS/Linux
python3 -m venv venv
source venv/bin/activate

# No Windows
python -m venv venv
venv\Scripts\activate
```

Instale as dependências:

```bash
pip install flask
```

### 3️⃣ Executando a API

Para rodar a aplicação, execute o seguinte comando:

```bash
python app.py
```

A API será iniciada e estará acessível em:

```
http://127.0.0.1:5000
```

## 📡 Endpoints Disponíveis

### 🔹 **Obter todos os itens**
**GET** `/items`

Resposta:
```json
[
    {"id": 1, "name": "Item 1"},
    {"id": 2, "name": "Item 2"}
]
```

### 🔹 **Adicionar um novo item**
**POST** `/items`

Corpo da requisição (JSON):
```json
{
    "name": "Novo Item"
}
```

Resposta:
```json
{
    "id": 3,
    "name": "Novo Item"
}
```

### 🔹 **Obter um item específico**
**GET** `/items/{id}`

Resposta:
```json
{
    "id": 1,
    "name": "Item 1"
}
```

### 🔹 **Atualizar um item existente**
**PUT** `/items/{id}`

Corpo da requisição (JSON):
```json
{
    "name": "Item Atualizado"
}
```

Resposta:
```json
{
    "id": 1,
    "name": "Item Atualizado"
}
```

### 🔹 **Deletar um item**
**DELETE** `/items/{id}`

Resposta:
```json
{
    "message": "Item deleted"
}
```

## 📌 Considerações Finais
- O servidor está configurado para rodar em **modo de desenvolvimento** (`debug=True`).
- Para deploy em produção, utilize um servidor WSGI como **Gunicorn**.

---

🔹 **Autor:** Seu Nome  
🔹 **Contato:** [seu-email@example.com](mailto:seu-email@example.com)

