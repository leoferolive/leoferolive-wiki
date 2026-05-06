---
title: Kubernetes
tags: [conceito, devops, infra, k8s, k3s, openshift]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
  - leoferolive.com.br/src/data/career.ts
  - leoferolive.com.br/src/data/projects.ts
---

# Kubernetes

## Resumo
Plataforma de orquestração de containers. Aparece em **três escalas distintas**
no perfil do Leonardo: AWS EKS na Wiley (produção corporativa), OpenShift na
Lumis (Kubernetes Red Hat), e K3s no homelab pessoal (ARM, Raspberry Pi).

## Onde foi aplicado
- [[entities/wiley]] — produção em K8s (presumivelmente AWS EKS, listado em
  `stack.ts`). Plataforma multi-pod com SSE + Redis Pub/Sub.
- [[entities/lumis]] — OpenShift na conta SulAmérica.
- [[projects/homelab]] — K3s em Raspberry Pi 4B (8GB), Traefik como ingress.

## Tecnologias relacionadas
- AWS EKS, OpenShift, K3s.
- Helm.
- Traefik (ingress).
- Cloudflare Tunnel (exposição sem abrir portas).

## Cross-references
- [[skills/devops]]
- [[concepts/microservices]]
- [[concepts/sse]] — arquitetura SSE da Wiley assume multi-pod.
