---
title: Microservices
tags: [conceito, backend, arquitetura, kubernetes]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
  - leoferolive.com.br/src/data/career.ts
---

# Microservices

## Resumo
Paradigma arquitetural central no perfil do Leonardo. Aparece tanto em
contexto **enterprise legacy** (BFF + P8 FileNet na Ebix/Bradesco) quanto em
**deploys cloud-native modernos** (OpenShift na Lumis/SulAmérica, Kubernetes
multi-pod na Wiley).

## Onde foi aplicado
- [[entities/lumis]] (2018-2019): microsserviços em **OpenShift** para
  SulAmérica.
- [[entities/ebix-latam]] (2019-2024): BFF (Backend for Frontend) sobre P8 FileNet,
  integrações distribuídas com SAP e WebSphere 8/9.
- [[entities/wiley]] (2024+): plataforma multi-pod em Kubernetes com SSE +
  Redis Pub/Sub.

## Tecnologias relacionadas
- Java + Spring Boot.
- Kubernetes / OpenShift / K3s.
- Kafka, Redis (mensageria entre serviços).
- BFF como padrão de borda.

## Cross-references
- [[skills/backend]]
- [[concepts/kubernetes]]
- [[concepts/kafka]]
- [[concepts/sse]]
