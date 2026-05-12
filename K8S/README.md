# Kubernetes: Pods, Services, ConfigMaps, Deployments e Autoscaling ☸️

Projeto desenvolvido durante a trilha de "Docker e Kubernetes" da Alura.

Este repositório reúne diversos laboratórios práticos utilizados para estudar desde os fundamentos do Kubernetes até recursos mais avançados como:

- Deployments
- ReplicaSets
- StatefulSets
- Persistent Volumes
- Horizontal Pod Autoscaler (HPA)
- Liveness e Readiness Probes

O projeto funciona como uma trilha prática de evolução no Kubernetes 🚀

---

# 📚 Conteúdos estudados

## Fundamentos Kubernetes

- Arquitetura do Kubernetes
- Funcionamento do cluster
- Pods
- Services
- ConfigMaps
- Comunicação entre aplicações
- kubectl

## Exposição de aplicações

- Services `NodePort`
- Services `ClusterIP`

## Gerenciamento de aplicações

- ReplicaSets
- Deployments
- Estratégias de atualização

## Persistência de dados

- Volumes
- PersistentVolumeClaim (PVC)
- Storage Classes
- Provisionamento dinâmico de volumes

## Alta disponibilidade e escalabilidade

- StatefulSets
- Horizontal Pod Autoscaler (HPA)

## Monitoramento de saúde da aplicação

- Liveness Probe
- Readiness Probe

---

# 📁 Estrutura do projeto

```bash
.
├── exemplo-svc
│   ├── portal-noticias.yml
│   └── svc-portal-noticias.yml
├── nginx-deployment.yml
├── pod-1.yml
├── pod-2.yml
├── portal-noticias-replicaset.yaml
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
├── refactor-project-k8s
│   ├── db-noticias-deployment.yml
│   ├── imagens-pvc.yml
│   ├── pod-volume.yml
│   ├── portal-noticias-deployment.yml
│   ├── portal-noticias-hpa.yml
│   ├── sessao-pvc.yml
│   ├── sistema-noticias-deployment.yml
│   └── sistema-noticias-statefulset.yml
├── svc-pod-1.yml
└── svc-pod-2.yml
```

---

# 🧪 Laboratórios do projeto

# 📦 Pods básicos

Arquivos utilizados para aprender os fundamentos do Kubernetes:

- `primeiro-pod.yml`
- `pod-1.yml`
- `pod-2.yml`
- `portal-noticias.yml`

Exemplos:

```bash
kubectl apply -f primeiro-pod.yml

kubectl get pods

kubectl describe pod nome-do-pod
```

---

# 🌐 Services

## NodePort

Exposição externa das aplicações.

Arquivos:

- `svc-pod-1.yml`
- `svc-pod-2.yml`
- `svc-portal-noticias.yml`

---

## ClusterIP

Comunicação interna entre aplicações dentro do cluster.

Arquivo:

- `svc-db-noticias.yaml`

---

# ⚙️ ConfigMaps

Utilizados para centralizar variáveis de ambiente e configurações.

Arquivos:

- `db-configmap.yml`
- `portal-configmap.yml`
- `sistema-configmap.yml`

---

# 🚀 Projeto intermediário

A pasta `project-k8s-alura` contém uma arquitetura simples baseada em:

- Portal de notícias
- Sistema de notícias
- Banco de dados

Recursos utilizados:

- Pods
- Services
- ConfigMaps

---

# 🏗️ Refatoração avançada Kubernetes

A pasta `refactor-project-k8s` contém a evolução do projeto utilizando recursos mais avançados do Kubernetes.

## Recursos implementados

### Deployments

Gerenciamento declarativo das aplicações.

Arquivos:

- `portal-noticias-deployment.yml`
- `sistema-noticias-deployment.yml`
- `db-noticias-deployment.yml`

---

### ReplicaSets

Controle de réplicas e alta disponibilidade.

Arquivo:

- `portal-noticias-replicaset.yaml`

---

### StatefulSet

Gerenciamento de aplicações stateful com identidade persistente.

Arquivo:

- `sistema-noticias-statefulset.yml`

---

### Volumes e Persistência

Persistência de dados utilizando PVCs.

Arquivos:

- `imagens-pvc.yml`
- `sessao-pvc.yml`
- `pod-volume.yml`

Conceitos praticados:

- PersistentVolumeClaim
- StorageClass
- Provisionamento dinâmico

---

### Health Checks

Monitoramento da saúde da aplicação utilizando:

- Liveness Probe
- Readiness Probe

Exemplo:

```yaml
livenessProbe:
  httpGet:
    path: /
    port: 80

readinessProbe:
  httpGet:
    path: /
    port: 80
```

---

### Autoscaling

Escalabilidade automática utilizando Horizontal Pod Autoscaler.

Arquivo:

- `portal-noticias-hpa.yml`

Exemplo:

```bash
kubectl get hpa

kubectl top pods

kubectl describe hpa portal-noticias-hpa
```

---

# ⚙️ Principais comandos utilizados

## Aplicar recursos

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

## Listar Deployments

```bash
kubectl get deployments
```

## Listar StatefulSets

```bash
kubectl get statefulsets
```

## Listar HPA

```bash
kubectl get hpa
```

## Ver consumo de recursos

```bash
kubectl top pods

kubectl top nodes
```

## Remover recursos

```bash
kubectl delete -f arquivo.yml
```

---

# 🛠️ Tecnologias utilizadas

- Kubernetes
- Docker
- kubectl
- Minikube
- YAML

---

# 🎯 Objetivo do projeto

Este projeto teve como foco praticar na prática os principais recursos do Kubernetes, desde os fundamentos até funcionalidades avançadas de escalabilidade e persistência.

---

# ☁️ Conceitos praticados

| Recurso | Objetivo |
|---|---|
| Pod | Executar containers |
| Service | Comunicação entre aplicações |
| NodePort | Exposição externa |
| ClusterIP | Comunicação interna |
| ConfigMap | Configuração de aplicações |
| ReplicaSet | Controle de réplicas |
| Deployment | Gerenciamento declarativo |
| StatefulSet | Aplicações stateful |
| PVC | Persistência de dados |
| HPA | Escalabilidade automática |
| Liveness Probe | Verificar saúde da aplicação |
| Readiness Probe | Verificar disponibilidade |
| kubectl | Gerenciamento do cluster |

---

# 📌 Observação

Projeto desenvolvido para fins de estudo, prática e aprofundamento em Kubernetes ☸️