---
title: RAG (Retrieval-Augmented Generation)
tags: [conceito, ai, rag, pgvector, llm, em-producao, mvp]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/cases.ts
  - leoferolive.com.br/src/data/stack.ts
---

# RAG (Retrieval-Augmented Generation)

## Resumo
Padrão de IA onde o LLM consulta uma base de conhecimento em tempo de query
em vez de "saber" tudo nos pesos. O Leonardo aplicou RAG em produção na
Wiley para resolver fragmentação de informação de artigos espalhada em 5+
sistemas internos.

## Onde foi aplicado
- **[[entities/wiley]] — Plataforma RAG (MVP em produção):**
  - **Problema:** informação de artigos espalhada em 5+ sistemas internos.
  - **Solução:** Spring AI + Pgvector + Azure OpenAI integrando 5+ fontes.
    Interfaces de chat e servidor MCP para consultas em linguagem natural.
  - **Impacto:** MVP em produção. Suporte e produto consultam em linguagem
    natural.

## Tecnologias usadas
- [[concepts/spring-ai]] — orquestração no Java.
- Pgvector — vetores em PostgreSQL (ver [[skills/data]]).
- Azure OpenAI — modelo de embeddings + geração.
- [[concepts/mcp]] — MCP server expondo as consultas.

## Cross-references
- [[skills/ai]]
- [[concepts/spring-ai]]
- [[concepts/mcp]]
