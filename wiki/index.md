---
title: Index
tags: [index, catalogo]
last_updated: 2026-05-08
sources:
  - wiki/entities/*
  - wiki/projects/*
  - wiki/concepts/*
  - wiki/skills/*
---

# Index — catálogo da LLM Wiki

Catálogo completo. Lido pelo backend `chat-api` em query-time para selecionar
páginas relevantes a cada consulta. Cada linha:
`- [Title](path) — one-line summary`.

## Perfil
- [Sobre Leonardo](about.md) — Leonardo Ferreira Oliveira, 35 anos (nasc. 29/11/1990); resumo profissional e identidade.

## Entidades
- [Wiley](entities/wiley.md) — empresa atual (Dez 2024+); plataforma UAXD com 10k+ autores; Senior SE liderando 4 iniciativas de IA em produção.
- [City Connect](entities/city-connect.md) — Ago–Dez 2024, Líder de Projetos no contrato TCE-PR (Lumis Portal + app mobile), squad de 8 devs.
- [Ebix América Latina](entities/ebix-latam.md) — Jun 2019 → Jul 2024, Sênior / referência técnica no Bradesco · Sinistro RE; SAP, SRO, BFF P8 FileNet, primeiro uso profissional de IA (ChatGPT/Fortify).
- [Lumis](entities/lumis.md) — Out 2018 → Mai 2019, SulAmérica; primeiro contato com micro-frontend (Vue.js), OpenShift e OAuth2 (impersonação).
- [Ebix (1ª passagem)](entities/ebix-2017.md) — 2017-2018, promoção a Pleno; célula ágil de Salvados (Bradesco) com Novo Portal do Recuperador.
- [Capgemini / Persist](entities/persist.md) — 2014-2017, estágio → Pleno na conta Bradesco · Sinistro RE; primeiro da turma de estagiários a ser efetivado.

## Projetos
- [nossalista](projects/nossalista.md) — listas colaborativas em tempo real (Java 25 + Spring Boot 4 + React + WebSocket); construído via Claude Code + Codex (BMAD).
- [nossagrana](projects/nossagrana.md) — PWA offline-first de finanças familiares (Node/TS + React + PostgreSQL); construído via Claude Code + Codex.
- [homelab](projects/homelab.md) — Raspberry Pi 4B com K3s, Traefik, Cloudflare Tunnel e administração via OpenClaw + Telegram.

## Conceitos
- [Spring AI](concepts/spring-ai.md) — base técnica das features de IA em produção na Wiley (Log Analyzer, plataforma RAG).
- [RAG (Retrieval-Augmented Generation)](concepts/rag.md) — plataforma RAG MVP em produção integrando 5+ fontes de artigos com Spring AI + Pgvector + Azure OpenAI + MCP.
- [MCP (Model Context Protocol)](concepts/mcp.md) — protocolo usado tanto na plataforma RAG quanto no agentic workspace de support duty.
- [SSE em escala](concepts/sse.md) — arquitetura SSE multi-pod com Redis Pub/Sub e BroadcastChannel desenhada E2E na Wiley.
- [Microservices](concepts/microservices.md) — paradigma central, aplicado de BFF legacy (Ebix) a multi-pod cloud-native (Wiley).
- [Kubernetes](concepts/kubernetes.md) — três escalas: AWS EKS (Wiley), OpenShift (Lumis), K3s (homelab).
- [Kafka](concepts/kafka.md) — listado no stack backend, alinhado ao paradigma event-driven; cases específicos a serem expandidos.
- [Sinistro RE](concepts/sinistro-re.md) — domínio de negócio Bradesco que atravessa Capgemini → Persist → Ebix (2017-2018) → Ebix LATAM (2019-2024).
- [OAuth2](concepts/oauth2.md) — trajetória de autenticação moderna: impersonação (Lumis) e Client Credentials (BFF P8 FileNet, Ebix LATAM).

## Skills
- [Skills · ai/](skills/ai.md) — Spring AI, Pgvector, Azure OpenAI, MCP, Claude Code, Cursor, ChatGPT, Codex, BMAD, RAG.
- [Skills · backend/](skills/backend.md) — Java 8-25, Spring Boot 4, Microservices, BFF, Event-driven, Kafka, REST + SSE, OIDC.
- [Skills · data/](skills/data.md) — PostgreSQL, MongoDB, Redis, SQL Server, Oracle, DB2.
- [Skills · devops/](skills/devops.md) — AWS EKS, Kubernetes, K3s, Helm, Docker, GitHub Actions, Jenkins, Cloudflare Tunnel, Tailscale, Traefik.
