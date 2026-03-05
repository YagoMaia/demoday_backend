
# 🚀 Simulador de Investimentos - Back-end

Este é o back-end da aplicação de simulação de investimentos, responsável por processar os cálculos de juros compostos e projeção patrimonial. A API foi construída utilizando **Python** com o framework **FastAPI**.

## 🛠️ Tecnologias Utilizadas

* **Python 3.12+**
* **FastAPI**: Framework web de alta performance.
* **Uvicorn**: Servidor ASGI para produção e desenvolvimento.
* **Pydantic**: Validação de dados e schemas.
* **UV**: Gerenciador de pacotes e ambientes Python ultrarápido.

## 📋 Pré-requisitos

Antes de começar, você precisará ter instalado em sua máquina:

* [Python](https://www.python.org/)
* [UV](https://github.com/astral-sh/uv) (Recomendado) ou `pip`.

## 🔧 Instalação e Configuração

1. **Clone o repositório:**
```bash
git clone <url-do-seu-repositorio>
cd demoday_backend

```


2. **Crie o ambiente virtual e instale as dependências:**
```bash
uv sync

```


3. **Certifique-se de que a estrutura de pastas está correta:**
```text
demoday_backend/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── routes.py
│   ├── schemas.py
│   └── services.py
├── pyproject.toml
└── .venv/

```



## 🚀 Executando o Servidor

Para iniciar o servidor de desenvolvimento com *hot-reload*:

```bash
uv run python -m uvicorn app.main:app --reload --port 8000

```

O servidor estará disponível em: `http://localhost:8000`

## 🛣️ Endpoints da API

| Método | Endpoint | Descrição |
| --- | --- | --- |
| `POST` | `/api/simular` | Recebe dados do investimento e retorna o array para o gráfico. |

### Exemplo de Payload (JSON):

```json
{
  "valorInicial": 10000,
  "aporteMensal": 500,
  "taxaAnual": 12,
  "periodo": 10
}

```
## 🔐 Configuração de CORS

O projeto está configurado para aceitar requisições do front-end rodando em `http://localhost:3000`. Caso o endereço do seu front-end mude, ajuste a lista de origins no arquivo `app/main.py`.