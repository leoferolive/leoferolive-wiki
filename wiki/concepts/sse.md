---
title: SSE (Server-Sent Events) em escala
tags: [conceito, backend, real-time, sse, redis, broadcastchannel, em-producao]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/cases.ts
  - leoferolive.com.br/src/data/career.ts
---

# SSE (Server-Sent Events) em escala

## Resumo
Entrega de eventos em tempo real do backend para o frontend via canal HTTP
unidirecional. Em ambientes Kubernetes multi-pod, a entrega ingênua sofre de
**broadcast inconsistente entre instâncias** e **custo crescente de conexões
por aba**. O Leonardo desenhou E2E uma arquitetura que resolve ambos.

## Onde foi aplicado
- **[[entities/wiley]] — SSE at scale (em produção):**
  - **Problema:** entrega de eventos em tempo real para o frontend em K8s
    com múltiplos pods — broadcast inconsistente e conexões caras por aba.
  - **Solução:** SSE com **Redis Pub/Sub** para consistência entre pods,
    mais camada de **BroadcastChannel API** no frontend para deduplicar
    conexões por aba. Java 25, Spring Boot 4.
  - **Impacto:** eventos consistentes em ambiente multi-pod e redução
    significativa de carga de conexões no backend. Em produção na plataforma
    de submissões/publicações da Wiley.

## Tecnologias usadas
- Java 25, Spring Boot 4.
- Redis Pub/Sub.
- BroadcastChannel API (browser).
- Kubernetes (multi-pod).

## Cross-references
- [[skills/backend]]
- [[concepts/kubernetes]]
- [[skills/data]] — Redis Pub/Sub.
