---
title: homelab
tags: [projeto, infra, raspberry-pi, k3s, self-hosted, openclaw, telegram]
last_updated: 2026-05-06
sources:
  - leoferolive.com.br/src/data/projects.ts
---

# homelab

## Resumo
Infraestrutura self-hosted do Leonardo: **tudo em um Raspberry Pi 4B (8GB)**
rodando K3s, Traefik e Cloudflare Tunnel. Usa **OpenClaw + Telegram** para
administração remota — provisiona bancos, faz deploys e troubleshoot direto
pelo chat.

## Período / Detalhes
- **Tipo:** infraestrutura.
- **Hardware:** Raspberry Pi 4B (8GB RAM).
- **Hospeda:** site `leoferolive.com.br`, [[projects/nossalista]],
  [[projects/nossagrana]] e (planejado) o backend `chat-api` da LLM Wiki.

## Tecnologias
- Raspberry Pi 4B.
- K3s (Kubernetes leve).
- Traefik (ingress).
- Cloudflare Tunnel (exposição sem abrir portas).
- OpenClaw (controle agêntico do cluster).
- Tailscale (acesso à rede interna).

## Achievements / Highlights
- Cluster K3s estável em ARM com múltiplos serviços de produção.
- **Operação remota via Telegram + OpenClaw**: sem precisar de SSH manual no
  fluxo comum (provisionamento de banco, deploy, troubleshoot).

## Cross-references
- [[concepts/kubernetes]] — K3s é a distribuição usada.
- [[skills/devops]] — toda a stack de operação.
- [[projects/nossalista]] — hospedado aqui.
- [[projects/nossagrana]] — hospedado aqui.
