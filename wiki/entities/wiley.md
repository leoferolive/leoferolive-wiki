---
title: Wiley
tags: [empresa, ai-first, sse, rag, kubernetes]
last_updated: 2026-09-03
sources:
  - leoferolive.com.br/src/data/career.ts
  - leoferolive.com.br/src/data/cases.ts
  - leoferolive.com.br/src/i18n/pt.ts
  - conversa-direta-2026-09-03
---

# Wiley

## Resumo
Empresa onde o Leonardo atuou de dezembro de 2024 a junho de 2026, como Senior
Software Engineer na plataforma **UAXD**, que serve mais de 10 mil autores
globalmente. Foi também o palco onde concentrou liderança em iniciativas de
IA em produção antes de migrar para a CI&T.

## Período / Detalhes
- **Período:** Dez 2024 → Jun 2026 (1 ano e 6 meses).
- **Cargo:** Senior Software Engineer.
- **Escopo:** Plataforma UAXD (Author Experience), 10k+ autores globalmente.
- **Status:** concluído.

## Tecnologias
- Java 25, Spring Boot 4.
- SSE (Server-Sent Events) com Redis Pub/Sub.
- BroadcastChannel API no frontend.
- Kubernetes multi-pod.
- Spring AI, Pgvector, Azure OpenAI / GPT-4.
- Elasticsearch, Kibana.
- MCP (Model Context Protocol).

## Achievements / Highlights
- Arquitetura **SSE + Redis Pub/Sub** em K8s com **BroadcastChannel** no
  frontend — entrega assíncrona em tempo real entre múltiplos pods, com
  deduplicação de conexões por aba. Em produção na plataforma de submissões
  e publicações.
- **4 iniciativas de IA em produção:** análise de logs, plataforma RAG sobre
  artigos, revenue tracking, agentic workspace de suporte.
- **Co-fundador do Conselho de IA Wiley Research BR** — fórum interno para
  disseminação de padrões AI-First no time brasileiro.
- Workspace agêntico (skills + AGENTS.md + MCPs Jira/Kibana) **adotado pelo
  time** para support duty E2E.

## Cross-references
- [[concepts/sse]] — arquitetura SSE multi-pod desenhada aqui.
- [[concepts/rag]] — plataforma RAG MVP em produção sobre 5+ fontes de artigos.
- [[concepts/spring-ai]] — stack base das iniciativas de IA.
- [[concepts/kubernetes]] — multi-pod onde a SSE roda.
- [[skills/ai]] — skills aplicadas no dia-a-dia.
- [[skills/backend]] — Java 25 + Spring Boot 4.
- [[entities/ci-t]] — empresa seguinte (Jun 2026+).
