---
title: Spring AI
tags: [conceito, ai, spring, java, llm, em-producao]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/stack.ts
  - leoferolive.com.br/src/data/cases.ts
---

# Spring AI

## Resumo
Framework Spring para integrar LLMs em aplicações Java. É a **base técnica das
features de IA em produção** que o Leonardo construiu na Wiley — combinando
Spring Boot tradicional com Azure OpenAI/GPT-4 e armazenamento vetorial via
Pgvector.

## Onde foi aplicado
- **[[entities/wiley]] — Log Analyzer (em produção):** Java 24 + Spring Boot 3
  + Spring AI + Azure OpenAI/GPT-4. Consulta Kibana/Elasticsearch por
  `transactionId`; LLM identifica sistema de origem e causa raiz. Reduziu
  investigação de incidentes de **dias para minutos**.
- **[[entities/wiley]] — Plataforma RAG (MVP em produção):** Spring AI +
  Pgvector + Azure OpenAI integrando 5+ fontes de artigos, com chat e MCP
  server para consultas em linguagem natural. Veja [[concepts/rag]].

## Tecnologias relacionadas
- Java 24 / 25, Spring Boot 3 / 4.
- Azure OpenAI (GPT-4).
- Pgvector (PostgreSQL).
- MCP (Model Context Protocol).
- Elasticsearch / Kibana (para o log analyzer).

## Cross-references
- [[skills/ai]]
- [[skills/backend]]
- [[concepts/rag]]
- [[concepts/mcp]]
