---
title: Ebix América Latina
tags: [empresa, senior, referencia-tecnica, bradesco, sinistro-re, websphere, fortify, chatgpt]
last_updated: 2026-05-08
sources:
  - leoferolive.com.br/src/data/career.ts
  - raw/interview-ebix-latam-2019-2024-2026-05.md
---

# Ebix América Latina

## Resumo
Retorno do Leonardo à conta Bradesco Seguros / Sinistro RE como **Analista
Sênior e referência técnica do time** — papel sustentado por 5 anos. Junto
a um colega, era a principal fonte de conhecimento de negócio da conta, o
que dava à Ebix vantagem competitiva na renovação do contrato e ao
Leonardo autonomia técnica significativa. Foi também o lugar onde teve
seu primeiro uso profissional de IA (ChatGPT GPT-3.5) — predecessor
histórico do trabalho AI-First na Wiley.

## Período / Detalhes
- **Período:** Jun 2019 → Jul 2024 (5 anos).
- **Cargo:** Analista de Sistemas Sênior / Referência Técnica.
- **Cliente:** Bradesco Seguros — Sinistro de Ramos Elementares.
- **Mentoria:** até **8 pessoas** sob orientação em iniciativas
  específicas (estagiários e juniores).

## Tecnologias
- Java 7 e Java 8 (migração).
- Spring Boot, Spring MVC, Spring Core; Struts em sistemas legados.
- DB2, SQL Server (procedures).
- WebSphere 8 / 8.5 → 9 (migração); Tomcat 8 / 9 em alguns sistemas.
- IBM FileNet P8.
- COBOL/CICS (consumo de serviços legados na integração SAP).
- Jenkins.
- ChatGPT (GPT-3.5) — uso profissional pioneiro na conta.
- Fortify (gate de qualidade da Bradesco).

## Achievements / Highlights
- **Volume operacional:** sistema processando **500–1.000 sinistros/dia**
  com indenizações individuais de até **R$ 5 milhões**.
- **Estabilização do projeto SAP em produção:** projeto multi-sistemas que
  consolidava dados via arquivo posicional diário. Time de sustentação sem
  documentação adequada — ~2-3 meses de horas extras + análise de logs +
  correção de dados e código + relacionamento próximo com a área de
  negócio até atingir estabilidade aceitável.
- **SRO (Sistema de Registro de Operações):** demanda regulatória.
  Tocou sozinho a frente do Sinistro RE — views específicas no banco,
  endpoints REST com schedule diário, job principal chamando todos os
  layouts CSV + opção de regerar individualmente.
- **Integração P8 FileNet (BFF documental):** mapeamento de aplicações
  consumidoras, novo contrato com **OAuth2 Client Credentials Flow** e
  templates reutilizáveis — um para Java 6 (`HttpClient`) e outro para
  Java 7+ (`RestTemplate`). Entregue no prazo apesar do FileNet ter API
  não-trivial.
- **Migração WebSphere 8 → 9 e Java 7 → 8** em múltiplas aplicações —
  baixo impacto de compilação, foco em compatibilidade de runtime,
  bibliotecas e configurações de infra.
- **Fortify + ChatGPT (GPT-3.5):** correção de vulnerabilidades Críticas
  e Altas em sistemas legados, com ChatGPT auxiliando interpretação dos
  apontamentos e sugestão de correções. **Primeiro uso profissional de
  IA do Leonardo.**
- Tomada de decisão arquitetural, mentoria contínua, refinamento de
  tasks e revisão de código como referência consolidada do time.

## Cross-references
- [[entities/persist]] — primeira passagem na mesma conta, ainda como
  Júnior.
- [[entities/ebix-2017]] — primeira passagem na própria Ebix (2017-2018,
  Salvados).
- [[entities/city-connect]] — empresa seguinte (saída em Jul 2024 para
  papel de liderança).
- [[concepts/sinistro-re]] — domínio de negócio onde acumulou 9 anos no
  total.
- [[concepts/oauth2]] — Client Credentials Flow no BFF P8.
- [[concepts/microservices]] — BFF documental sobre P8 FileNet.
- [[skills/backend]] — Java/Spring legacy + integrações enterprise.
- [[skills/data]] — DB2, SQL Server enterprise.
- [[skills/ai]] — primeiro uso profissional de IA (ChatGPT/Fortify).
