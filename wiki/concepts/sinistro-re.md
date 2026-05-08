---
title: Sinistro de Ramos Elementares (Sinistro RE)
tags: [dominio, seguros, bradesco, sustentacao, regulatorio]
last_updated: 2026-05-08
sources:
  - raw/interview-capgemini-persist-2014-2017-2026-05.md
  - raw/interview-ebix-2017-2018-2026-05.md
  - raw/interview-ebix-latam-2019-2024-2026-05.md
---

# Sinistro de Ramos Elementares (Sinistro RE)

## Resumo
Domínio de negócio da Bradesco Seguros que atravessa praticamente toda a
primeira década de carreira do Leonardo — Capgemini → Persist → Ebix
(2017-2018) → Ebix LATAM (2019-2024). Sistema crítico que faz reserva de
sinistro e solicitações de pagamento para o sistema de contabilidade,
processando volumes operacionais altos com criticidade financeira por
operação.

## Detalhes
- **Sigla:** RE = Ramos Elementares (linhas patrimoniais — automóvel,
  residencial, empresarial, etc., excluindo vida e saúde).
- **Função:** reserva de sinistro + solicitações de pagamento ao sistema
  de contabilidade.
- **Volume:** 500–1.000 sinistros processados por dia (referência
  Ebix LATAM, 2019-2024).
- **Criticidade:** indenizações individuais de até **R$ 5 milhões**.
- **Características técnicas:**
  - Migração inicial para Java vinda de plataforma anterior — gerou
    muitos erros em produção nos primeiros anos pós-migração.
  - **Muita regra de negócio em procedures SQL Server** que não havia
    sido migrada para Java; rotina de pagamento diário rodava no banco.
  - Convivência DB2 + SQL Server.
  - Aplicações sobre **WebSphere 8 / 8.5 / 9** e **Tomcat 8 / 9**.
- **Áreas adjacentes:** Salvados (recuperação de itens sinistrados,
  foco veículos) — entrou no escopo do Leonardo na primeira passagem
  pela Ebix.

## Por que importa para a wiki
- É o domínio em que o Leonardo se tornou **referência de conhecimento**,
  ainda como Júnior na Persist — e que sustentou sua autonomia e poder
  de decisão técnica como Sênior na Ebix LATAM.
- Atravessa quatro entities, então cross-references para cá evitam
  duplicação de contexto de negócio.

## Cross-references
- [[entities/persist]] — primeiro contato, ainda como Júnior; alocação
  dentro da Bradesco para atendimento de erros de produção.
- [[entities/ebix-2017]] — sustentação inicial antes da célula de
  Salvados.
- [[entities/ebix-latam]] — domínio principal por 5 anos como
  referência técnica; projetos SAP, SRO, P8 FileNet, migrações.
