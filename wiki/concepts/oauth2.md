---
title: OAuth2 (na trajetória)
tags: [autenticacao, oauth2, seguranca, backend]
last_updated: 2026-05-08
sources:
  - raw/interview-lumis-2018-2019-2026-05.md
  - raw/interview-ebix-latam-2019-2024-2026-05.md
---

# OAuth2 (na trajetória)

## Resumo
Concept que organiza os pontos da carreira do Leonardo em que mecanismos
de autenticação modernos (OAuth2 e variantes) foram aplicados — começando
com **impersonação de sessão na Lumis (2018-2019)** e consolidando no
**Client Credentials Flow** do BFF P8 FileNet na Ebix LATAM.

## Detalhes
- **Lumis · Sistema de Partes Relacionadas (Compliance):** primeiro
  contato técnico com mecanismo de autenticação não-trivial.
  Implementou **impersonação de sessão** — administrador do compliance
  entrava no sistema e respondia o questionário em nome de diretores /
  superintendentes que não deveriam acessar pessoalmente. Diferente do
  padrão de autenticação proprietário da Bradesco que o Leonardo
  conhecia até então.
- **Ebix LATAM · BFF P8 FileNet:** migração da integração com IBM
  FileNet P8 de bindings de WebSphere para um BFF com autenticação
  formal. Modelo: cada aplicação consumidora se autentica com
  `system-id` + `secret-key` e usa **OAuth2 Client Credentials Flow**
  (backend-to-backend) para chamar o BFF via API REST.
  - Templates reutilizáveis criados para o time:
    - **Java 6:** usando `HttpClient` (algumas aplicações da conta
      ainda em Java 6).
    - **Java 7+:** usando `RestTemplate`.

## Por que importa para a wiki
- Marca a transição do Leonardo para o universo de autenticação moderna
  em ambientes enterprise — um tema que continua relevante em qualquer
  trabalho com IA agêntica e integrações backend-to-backend.
- Liga duas entidades distintas (Lumis e Ebix LATAM) que tratam o tema
  por ângulos diferentes (impersonação vs. machine-to-machine).

## Cross-references
- [[entities/lumis]] — primeiro contato (impersonação de sessão).
- [[entities/ebix-latam]] — Client Credentials Flow no BFF P8.
- [[skills/backend]] — autenticação OIDC / OAuth2 no stack backend.
