# 🚀 CI/CD com Go e GitHub Actions

Projeto desenvolvido durante o curso **"Integração Contínua: pipelines e testes automatizados com GitHub Actions"** da Alura.

O objetivo deste projeto foi praticar a criação de uma pipeline de CI utilizando GitHub Actions em uma aplicação Go com PostgreSQL e Docker Compose.

---

# 🛠️ Tecnologias utilizadas

- Go 1.22
- PostgreSQL
- Docker
- Docker Compose
- GitHub Actions
- GolangCI-Lint

---

# ⚙️ Pipeline de CI

A pipeline realiza automaticamente:

✅ Checkout do código  
✅ Configuração do ambiente Go  
✅ Inicialização do PostgreSQL com Docker Compose  
✅ Build da aplicação  
✅ Execução do linter  
✅ Execução dos testes automatizados  
✅ Upload do artefato compilado  

---

# 🔐 Uso de Secrets

As variáveis sensíveis utilizadas nos testes são armazenadas com segurança utilizando **GitHub Secrets**.

Secrets utilizados:

- `DB_HOST`
- `DB_USER`
- `DB_PASSWORD`
- `DB_NAME`

---

# 📂 Estrutura do projeto

```bash
.
├── .github/
│   └── workflows/
│       └── ci.yml
├── CI-CD/
│   ├── controllers/
│   ├── database/
│   ├── models/
│   ├── routes/
│   ├── docker-compose.yml
│   ├── go.mod
│   └── main.go