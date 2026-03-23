# Documentacao API Be Compliance

Repositorio de documentacao interativa das APIs do sistema Be Compliance para integracoes de terceiros.

## O que este projeto faz

Fornece uma página web com [Swagger UI](https://swagger.io/tools/swagger-ui/) que permite aos clientes visualizar e testar os endpoints das APIs:

- **Third Party Analysis API** — Due Diligence de Pessoas Juridicas
- **BeNP API** — Due Diligence de Pessoas Fisicas (Background Check)

A página exibe automaticamente os endpoints corretos de acordo com o servidor (API) selecionado pelo usuario.

## Estrutura do projeto

```
docs/
├── index.html                 # Página principal com Swagger UI
├── swagger.json               # Especificacao OpenAPI (arquivo principal)
├── api-swagger.json           # Especificacao da API Third Party Analysis
├── benp-swagger.json          # Especificacao da API BeNP
└── swagger-ui/                # Arquivos do Swagger UI (CSS e JS)
```

## Como rodar localmente

Sirva a pasta `docs/` com qualquer servidor HTTP. Exemplos:

```bash
# Com Python
python3 -m http.server 8080 -d docs

# Com PHP
php -S localhost:8080 -t docs

# Com Node.js
npx serve docs
```

Acesse `http://localhost:8080` no navegador.


## Instrucoes para o time de Infra

### Requisitos

Este projeto e composto **apenas por arquivos estaticos** (HTML, CSS, JS e JSON). Nao necessita de:
- Runtime (Node.js, Python, PHP, etc.)
- Banco de dados
- Backend ou servidor de aplicacao

Basta servir os arquivos da pasta `docs/` via um servidor web com HTTPS.
O `Dockerfile` já está na raiz do repositorio.

### Configuracao do dominio

Disponibilizar em uma URL acessivel aos clientes.
