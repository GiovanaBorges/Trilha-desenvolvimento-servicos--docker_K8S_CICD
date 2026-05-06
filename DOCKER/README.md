# 🐳 Docker: Criando e Gerenciando Containers

Anotações básicas do curso de "Docker: criando e gerenciando containers" da Alura, abordando desde a criação de containers até a orquestração com Docker Compose.

---

## 📦 O que aprendi

* Subir containers com Docker
* Criar e personalizar imagens
* Trabalhar com persistência de dados usando volumes
* Configurar redes para comunicação entre containers
* Utilizar Docker Compose para gerenciar múltiplos containers

---

## 🚀 Comandos básicos do Docker

### 🔹 Verificar versão

```bash
docker --version
```

Mostra a versão do Docker instalada.

---

### 🔹 Baixar uma imagem

```bash
docker pull nome-da-imagem
```

Faz o download de uma imagem do Docker Hub.

---

### 🔹 Listar imagens

```bash
docker images
```

Exibe todas as imagens disponíveis localmente.

---

### 🔹 Rodar um container

```bash
docker run nome-da-imagem
```

Cria e inicia um container com base na imagem.

Exemplo com porta:

```bash
docker run -p 8080:80 nginx
```

Mapeia a porta 8080 da máquina para a 80 do container.

---

### 🔹 Listar containers

```bash
docker ps
```

Mostra containers em execução.

```bash
docker ps -a
```

Mostra todos, inclusive os parados.

---

### 🔹 Parar um container

```bash
docker stop ID_DO_CONTAINER
```

---

### 🔹 Remover um container

```bash
docker rm ID_DO_CONTAINER
```

---

## 🛠️ Criando imagens personalizadas

### 🔹 Build de uma imagem

```bash
docker build -t nome-da-imagem .
```

Cria uma imagem a partir de um Dockerfile.

---

## 💾 Persistência com Volumes

Volumes permitem salvar dados mesmo após o container ser removido.

```bash
docker volume create meu-volume
```

```bash
docker run -v meu-volume:/app nginx
```

---

## 🌐 Redes no Docker

Permitem que containers conversem entre si.

```bash
docker network create minha-rede
```

```bash
docker run --network minha-rede nome-da-imagem
```

---

## 🧩 Docker Compose

Usado para gerenciar múltiplos containers com um único arquivo (`docker-compose.yml`).

### 🔹 Subir serviços

```bash
docker-compose up
```

### 🔹 Rodar em segundo plano

```bash
docker-compose up -d
```

### 🔹 Parar serviços

```bash
docker-compose down
```

---

## 📌 Conclusão

Docker facilita muito a criação de ambientes isolados, reproduzíveis e portáveis. Com containers, você consegue rodar aplicações de forma consistente em qualquer lugar.

---
