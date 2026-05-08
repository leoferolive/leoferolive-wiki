---
type: interview
source: voice-interview
date: 2026-05
entity: Capgemini / Persist
period: 2014-2017
roles:
  - Estagiário (Capgemini)
  - Analista de Sistemas Júnior (Capgemini → Persist)
client: Bradesco Seguros
stack: [Java 7, SQL Server, DB2, JBoss]
tags: [bradesco, sinistro, sustentacao, legado]
---

# Entrevista — Capgemini / Persist (2014–2017)

## Entrada como estagiário (Capgemini, 2014)

Processo seletivo em grupo. Aproximadamente 20 estagiários entraram juntos. Os primeiros 3 meses foram de programa de estudos que cobria tanto tecnologia quanto o negócio de seguros em si — todos os estagiários iriam trabalhar em projetos da Bradesco Seguros, então entendia-se o domínio do negócio desde o início.

Após o programa, cada estagiário foi alocado em um time. Leo foi para o time do **Seguro Fiança** — um sistema de emissão que estava sendo criado. As tarefas eram pequenas: correções de PMD, ajustes de tela, regras de negócio simples. Em todas elas o feedback era positivo e as entregas eram rápidas.

**Foi o primeiro da turma de ~20 estagiários a ser efetivado**, indicado pelo próprio líder de equipe. Virou Analista de Sistemas Júnior com foco em desenvolvimento Java.

---

## Time de Sinistro RE (Júnior)

Após a efetivação, mudou para o time de **Sinistro de Ramos Elementares (Sinistro RE)** — um sistema crítico que havia acabado de subir em produção como uma migração para Java. O sistema tinha muitos erros diários de produção, o que gerava muito ruído junto à Bradesco.

**Responsabilidades no Sinistro RE:**
- Sustentação dos erros de produção (análise de logs, correção de dados, fix no código)
- O sistema fazia **reserva de sinistro** e **solicitações de pagamento** para o sistema de contabilidade
- A rotina de pagamento diário rodava em **procedures SQL Server** e era fonte frequente de problemas
- Muito da regra de negócio que não havia sido migrada para Java continuava no banco de dados

**Alocação no cliente:** Dada a confiança construída, Leo foi alocado diretamente na **Bradesco Seguros** para fazer o primeiro atendimento dos erros de produção. Sentava ao lado da área de negócio, entendia os problemas in loco e, dependendo da complexidade, resolvia na hora ou repassava ao time da Capgemini.

---

## Mudança de fornecedor: Capgemini → Persist

A Capgemini perdeu o contrato da conta Bradesco. Leo foi junto, mantendo seu papel como Analista Júnior na Persist — mesma conta, mesmo sistema, mesma lógica. O trabalho continuou igual.

Nessa fase, Leo já era referência de conhecimento de negócio para a conta. Analistas mais seniores que chegavam na Persist precisavam de sua ajuda para entender o banco de dados, as aplicações e o ecossistema do Sinistro RE.

---

## Notas técnicas

- **Stack principal:** Java 7, SQL Server (procedures), DB2
- **Servidor de aplicação:** JBoss
- **Contexto de negócio:** Sinistro de Ramos Elementares, Bradesco Seguros — sistema de reserva de sinistro + solicitações de pagamento
- Muito código legado com regras de negócio não documentadas
