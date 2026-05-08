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
`- [Title](path) — one-line summary [tag1, tag2, ...]`. As tags inline são
consumidas pelo retriever (peso 2× no scoring) e espelham o frontmatter
de cada página.

## Perfil
- [Sobre Leonardo](about.md) — Leonardo Ferreira Oliveira, 35 anos (nasc. 29/11/1990); resumo profissional e identidade. [perfil, sobre, identidade, leonardo, ferreira, oliveira]

## Entidades
- [Wiley](entities/wiley.md) — empresa atual (Dez 2024+); plataforma UAXD com 10k+ autores; Senior SE liderando 4 iniciativas de IA em produção. [empresa, atual, ai-first, sse, rag, kubernetes, uaxd, senior]
- [City Connect](entities/city-connect.md) — Ago–Dez 2024, Líder de Projetos no contrato TCE-PR (Lumis Portal + app mobile), squad de 8 devs. [empresa, lideranca, lumis-portal, tce-pr, governo, transicao]
- [Ebix América Latina](entities/ebix-latam.md) — Jun 2019 → Jul 2024, Sênior / referência técnica no Bradesco · Sinistro RE; SAP, SRO, BFF P8 FileNet, primeiro uso profissional de IA (ChatGPT/Fortify). [empresa, senior, referencia-tecnica, bradesco, sinistro-re, websphere, fortify, chatgpt]
- [Lumis](entities/lumis.md) — Out 2018 → Mai 2019, SulAmérica; primeiro contato com micro-frontend (Vue.js), OpenShift e OAuth2 (impersonação). [empresa, microservicos, micro-frontend, openshift, sulamerica, oauth2]
- [Ebix (1ª passagem)](entities/ebix-2017.md) — 2017-2018, promoção a Pleno; célula ágil de Salvados (Bradesco) com Novo Portal do Recuperador. [empresa, pleno, bradesco, salvados, celula-agil]
- [Capgemini / Persist](entities/persist.md) — 2014-2017, estágio → Pleno na conta Bradesco · Sinistro RE; primeiro da turma de estagiários a ser efetivado. [empresa, estagio, primeira-experiencia, bradesco, sinistro-re, java]

## Projetos
- [nossalista](projects/nossalista.md) — listas colaborativas em tempo real (Java 25 + Spring Boot 4 + React + WebSocket); construído via Claude Code + Codex (BMAD). [projeto, app, colaborativo, websocket, ai-built, em-producao]
- [nossagrana](projects/nossagrana.md) — PWA offline-first de finanças familiares (Node/TS + React + PostgreSQL); construído via Claude Code + Codex. [projeto, pwa, financas, offline-first, ai-built, em-producao]
- [homelab](projects/homelab.md) — Raspberry Pi 4B com K3s, Traefik, Cloudflare Tunnel e administração via OpenClaw + Telegram. [projeto, infra, raspberry-pi, k3s, self-hosted, openclaw, telegram]

## Conceitos
- [Spring AI](concepts/spring-ai.md) — base técnica das features de IA em produção na Wiley (Log Analyzer, plataforma RAG). [conceito, ai, spring, java, llm, em-producao]
- [RAG (Retrieval-Augmented Generation)](concepts/rag.md) — plataforma RAG MVP em produção integrando 5+ fontes de artigos com Spring AI + Pgvector + Azure OpenAI + MCP. [conceito, ai, rag, pgvector, llm, em-producao, mvp]
- [MCP (Model Context Protocol)](concepts/mcp.md) — protocolo usado tanto na plataforma RAG quanto no agentic workspace de support duty. [conceito, ai, mcp, agentic, em-producao]
- [SSE em escala](concepts/sse.md) — arquitetura SSE multi-pod com Redis Pub/Sub e BroadcastChannel desenhada E2E na Wiley. [conceito, backend, real-time, sse, redis, broadcastchannel, em-producao]
- [Microservices](concepts/microservices.md) — paradigma central, aplicado de BFF legacy (Ebix) a multi-pod cloud-native (Wiley). [conceito, backend, arquitetura, kubernetes]
- [Kubernetes](concepts/kubernetes.md) — três escalas: AWS EKS (Wiley), OpenShift (Lumis), K3s (homelab). [conceito, devops, infra, k8s, k3s, openshift]
- [Kafka](concepts/kafka.md) — listado no stack backend, alinhado ao paradigma event-driven; cases específicos a serem expandidos. [conceito, backend, event-driven, mensageria]
- [Sinistro RE](concepts/sinistro-re.md) — domínio de negócio Bradesco que atravessa Capgemini → Persist → Ebix (2017-2018) → Ebix LATAM (2019-2024). [dominio, seguros, bradesco, sustentacao, regulatorio]
- [OAuth2](concepts/oauth2.md) — trajetória de autenticação moderna: impersonação (Lumis) e Client Credentials (BFF P8 FileNet, Ebix LATAM). [autenticacao, oauth2, seguranca, backend]

## Skills
- [Skills · ai/](skills/ai.md) — Spring AI, Pgvector, Azure OpenAI, MCP, Claude Code, Cursor, ChatGPT, Codex, BMAD, RAG. [skills, ai, llm, rag, mcp, agentic]
- [Skills · backend/](skills/backend.md) — Java 8-25, Spring Boot 4, Microservices, BFF, Event-driven, Kafka, REST + SSE, OIDC. [skills, backend, java, spring, microservicos, kafka, sse]
- [Skills · data/](skills/data.md) — PostgreSQL, MongoDB, Redis, SQL Server, Oracle, DB2. [skills, data, postgres, mongodb, redis, sql-server, oracle, db2]
- [Skills · devops/](skills/devops.md) — AWS EKS, Kubernetes, K3s, Helm, Docker, GitHub Actions, Jenkins, Cloudflare Tunnel, Tailscale, Traefik. [skills, devops, kubernetes, k3s, aws-eks, helm, docker, ci-cd]
