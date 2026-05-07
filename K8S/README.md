# Kubernetes: Pods, Services e ConfigMaps ☸️

Projeto desenvolvido durante o curso **“Kubernetes: Pods, Services e ConfigMaps”** da alura.  
Neste repositório estão os exemplos e exercícios práticos utilizados para entender a arquitetura do Kubernetes, gerenciamento de Pods, exposição de aplicações com Services e configuração utilizando ConfigMaps.

O projeto funciona como um pequeno laboratório Kubernetes para praticar os principais recursos básicos da plataforma ☁️

---

# 📚 Conteúdos estudados

Durante o curso foram abordados os seguintes conceitos:

- Arquitetura do Kubernetes
- Funcionamento do cluster Kubernetes
- Gerenciamento de containers com Kubernetes
- Criação e gerenciamento de Pods
- Uso do `kubectl`
- Exposição de aplicações com Services
- Services do tipo:
  - `NodePort`
  - `ClusterIP`
- Configuração de variáveis de ambiente com ConfigMaps
- Comunicação entre Pods e Services

---

# 📁 Estrutura do projeto

```bash
.
├── exemplo-svc
│   ├── portal-noticias.yml
│   └── svc-portal-noticias.yml
├── pod-1.yml
├── pod-2.yml
├── portal-noticias.yml
├── primeiro-pod.yml
├── project-k8s-alura
│   ├── db-configmap.yml
│   ├── db-noticias.yaml
│   ├── portal-configmap.yml
│   ├── portal-noticias.yml
│   ├── sistema-configmap.yml
│   ├── sistema-noticias.yml
│   ├── svc-db-noticias.yaml
│   ├── svc-portal-noticias.yml
│   └── svc-sistema-noticias.yml
├── svc-pod-1.yml
└── svc-pod-2.yml
```

---

# 🧩 Organização dos arquivos

## 📦 Pods básicos

Arquivos utilizados para aprender a criação e gerenciamento de Pods:

- `primeiro-pod.yml`
- `pod-1.yml`
- `pod-2.yml`
- `portal-noticias.yml`

Exemplos de comandos utilizados:

```bash
kubectl apply -f primeiro-pod.yml

kubectl get pods

kubectl describe pod nome-do-pod

kubectl delete pod nome-do-pod
```

---

# 🌐 Services

## Exemplo simples de Service

A pasta `exemplo-svc` contém um exemplo básico de exposição de aplicação utilizando `NodePort`.

Arquivos:

- `portal-noticias.yml`
- `svc-portal-noticias.yml`

Exemplo de aplicação:

```bash
kubectl apply -f portal-noticias.yml
kubectl apply -f svc-portal-noticias.yml
```

---

## Services dos Pods

Os arquivos:

- `svc-pod-1.yml`
- `svc-pod-2.yml`

são responsáveis por expor os Pods:

- `pod-1.yml`
- `pod-2.yml`

utilizando Services no Kubernetes.

---

# 🚀 Projeto final

A pasta `project-k8s-alura` representa o projeto final do curso.

Nela foi criada uma pequena arquitetura com múltiplos Pods, Services e ConfigMaps.

## Estrutura do projeto final

### Aplicações

- Portal de notícias
- Sistema de notícias
- Banco de dados de notícias

### ConfigMaps

Arquivos responsáveis pelas variáveis de ambiente/configurações:

- `db-configmap.yml`
- `portal-configmap.yml`
- `sistema-configmap.yml`

### Services

#### NodePort

Utilizados para expor aplicações externamente:

- `svc-portal-noticias.yml`
- `svc-sistema-noticias.yml`

#### ClusterIP

Utilizado para comunicação interna do banco de dados:

- `svc-db-noticias.yaml`

O Pod do banco (`db-noticias.yaml`) utiliza um Service `ClusterIP`, permitindo acesso apenas dentro do cluster Kubernetes 🔒

---

# ⚙️ Principais comandos kubectl utilizados

## Criar recursos

```bash
kubectl apply -f arquivo.yml
```

## Listar Pods

```bash
kubectl get pods
```

## Listar Services

```bash
kubectl get svc
```

## Descrever recurso

```bash
kubectl describe pod nome-do-pod
```

## Remover recurso

```bash
kubectl delete -f arquivo.yml
```

---

# 🛠️ Tecnologias utilizadas

- Kubernetes
- kubectl
- Docker
- YAML

---

# 🎯 Objetivo do projeto

Este projeto teve como foco praticar os fundamentos do Kubernetes, principalmente:

- Criação de Pods
- Exposição de aplicações com Services
- Comunicação entre containers
- Configuração de aplicações com ConfigMaps
- Gerenciamento básico de aplicações Kubernetes

---

# ☁️ Conceitos praticados

| Recurso | Objetivo |
|---|---|
| Pod | Executar containers |
| Service | Expor aplicações e permitir comunicação |
| NodePort | Exposição externa |
| ClusterIP | Comunicação interna |
| ConfigMap | Configurações e variáveis de ambiente |
| kubectl | Gerenciamento do cluster |

---

# 📌 Observação

Projeto desenvolvido para fins de estudo e aprendizado sobre Kubernetes ☸️