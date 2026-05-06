---
title: Skills · devops/
tags: [skills, devops, kubernetes, k3s, aws-eks, helm, docker, ci-cd]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
  - leoferolive.com.br/src/data/projects.ts
---

# Skills · devops/

## Resumo
Stack de infraestrutura e entrega contínua. Cobre **AWS EKS** em ambiente
corporativo (Wiley) e **K3s em ARM** no homelab pessoal — mesmo paradigma
Kubernetes em escalas opostas. Pipelines em GitHub Actions e Jenkins.

## Itens (do `stack.ts`)
- AWS EKS
- Kubernetes
- K3s
- Helm
- Docker
- GitHub Actions
- Jenkins
- Cloudflare Tunnel
- Tailscale
- Traefik

## Onde foram aplicadas
- [[entities/wiley]] — Kubernetes em produção (SSE multi-pod com Redis Pub/Sub).
- [[entities/lumis]] — OpenShift (Kubernetes Red Hat) em projetos SulAmérica.
- [[projects/homelab]] — Raspberry Pi 4B + K3s + Traefik + Cloudflare Tunnel
  + Tailscale, hospedando todos os projetos pessoais.

## Cross-references
- [[concepts/kubernetes]] — paradigma central.
- [[concepts/microservices]] — usualmente entregues via K8s.
- [[projects/homelab]] — playground self-hosted onde a stack devops vive.
