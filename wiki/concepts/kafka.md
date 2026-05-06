---
title: Kafka
tags: [conceito, backend, event-driven, mensageria]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
---

# Kafka

## Resumo
Plataforma de streaming de eventos. Faz parte do stack backend declarado pelo
Leonardo, alinhado ao paradigma **event-driven** que ele cita explicitamente
junto a **microsserviços** e **BFF**.

## Onde foi aplicado
As fontes consultadas (`stack.ts`) listam Kafka entre as skills backend, mas
não detalham um case específico. Entradas mais detalhadas chegarão quando o
Leonardo adicionar transcripts, READMEs de projetos internos ou expandir
`cases.ts`.

## Cross-references
- [[skills/backend]]
- [[concepts/microservices]] — Kafka costuma ser o backbone entre serviços.
- [[concepts/sse]] — alternativa para entrega em tempo real ao frontend (na
  Wiley, a escolha foi Redis Pub/Sub + SSE; Kafka serve outros padrões).
