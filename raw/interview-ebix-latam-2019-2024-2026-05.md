---
type: interview
source: voice-interview
date: 2026-05
entity: Ebix América Latina
period: 2019-2024
roles:
  - Analista de Sistemas Sênior
  - Referência Técnica
client: Bradesco Seguros
stack: [Java 7, Java 8, Spring Boot, Spring MVC, Spring Core, Struts, DB2, SQL Server, WebSphere 8, WebSphere 9, Jenkins]
tags: [bradesco, sinistro, sao, sro, p8-filenet, websphere, fortify, chatgpt, mentoria, referencia-tecnica]
---

# Entrevista — Ebix América Latina (Jun 2019 – Jul 2024)

## Contexto de entrada

Recebeu proposta da Ebix América Latina e aceitou como **Analista de Sistemas Sênior** — retornou à mesma conta Bradesco Seguros / Sinistro RE, mas com outro papel: referência técnica do time.

**Ativo estratégico:** Leo e um colega eram a principal fonte de conhecimento de negócio da conta. Isso dava à Ebix uma vantagem competitiva na renovação e manutenção do contrato — e a Leo, autonomia e poder de decisão técnica significativos.

---

## Papel como Sênior e Referência Técnica

- Tomada de decisão em questões arquiteturais e técnicas do sistema
- Mentoria de estagiários e desenvolvedores júniores — em algumas iniciativas, chegou a ter até 8 pessoas sob sua orientação
- Refinamento de tasks, revisão de código, boas práticas
- Ponto de referência para toda a equipe entender regras de negócio do Sinistro RE

---

## Projeto: Integração SAP (estabilização pós-produção)

### Contexto

O projeto SAP era uma integração multi-sistemas: o Sinistro RE precisava consumir dados dos sistemas de emissão de RE, consolidar tudo e enviar via **arquivo posicional diário** para o SAP. O SAP exigiu muito mais campos do que o layout anterior suportava.

Leo havia participado da fase de definição do projeto ainda na Persist — definindo quais integrações existiriam e como seriam feitas (consumo de serviços **COBOL/CICS** e consumo de **APIs REST**). Após isso, não acompanhou o desenvolvimento. Ao retornar para a Ebix LATAM, o projeto estava prestes a entrar em produção.

### O problema pós-produção

O projeto havia demorado muito e sofrido grande rotatividade de equipe. **Ninguém conhecia o sistema de ponta a ponta.** Quando entrou em produção, surgiram muitos erros.

O time de sustentação (Leo incluso) não tinha documentação adequada. A estratégia foi aprender com os problemas em produção, ao lado da área de negócio.

**Como foi a estabilização:**
- Análise de logs
- Correção de dados diretamente no banco
- Correção no código para evitar recorrência
- Muito contato com a área de negócio (relacionamento já construído ajudou muito)
- ~2-3 meses de horas extras até o projeto atingir estabilidade aceitável

---

## Projeto: SRO — Sistema de Registro de Operações

Demanda regulatória (similar ao SUSEP de anos anteriores). Projeto multi-áreas: diversas frentes da Bradesco precisavam entregar arquivos com **layouts CSV específicos por grupo de ramo**. Leo tocou sozinho a parte do Sinistro RE.

**O desafio:** Normalizar dados de diversas origens para gerar arquivos CSV seguindo layouts pré-estabelecidos.

**Solução técnica:**
- Criação de views específicas no banco de dados
- Endpoints REST com schedules diários para geração dos arquivos
- Job principal que chamava todos os layouts de uma vez
- Opção de regerar layouts individualmente (flexibilidade operacional)

**Stack:** Java 7, Spring Core, Spring MVC

---

## Projeto: Integração P8 FileNet (BFF documental)

### Contexto

A Bradesco utilizava o **IBM FileNet P8** para armazenamento de documentos (imagens de sinistros, etc.). A integração era feita diretamente via configuração de bindings no WebSphere — sem autenticação adequada, apontando para um object store específico.

A mudança foi para um modelo com **BFF na frente**: cada aplicação passaria a se autenticar com `system-id` + `secret-key` e consumir o BFF via API REST.

### Desafios

1. **Mapeamento de aplicações:** Identificar todas as aplicações que tinham integração com P8
2. **Entendimento do novo contrato:** O FileNet P8 não tem uma API trivial — upload de documento não é uma chamada simples; há vários métodos com parâmetros específicos por tipo de operação
3. **Java 6 ainda presente:** Algumas aplicações ainda estavam em Java 6, o que limitava as opções de client HTTP

Para entender melhor, chegaram a **baixar o código-fonte do BFF** e analisar localmente.

### Solução

- Autenticação: **OAuth2 Client Credentials Flow** (backend-to-backend)
- Criação de **templates reutilizáveis** para o fluxo de autenticação + chamada ao BFF:
  - **Template Java 6:** usando `HttpClient`
  - **Template Java 7+:** usando `RestTemplate`
- Entregaram dentro do prazo

---

## Projeto: Migração WebSphere 8 → 9 / Java 7 → Java 8

Participou de migrações de aplicações do stack WebSphere 8 + Java 7 para WebSphere 9 + Java 8.

**Perfil da migração:** Baixo impacto de compilação. Os principais ajustes foram:
- Compatibilidade de runtime
- Atualização de bibliotecas
- Adequações de configurações de infraestrutura do WebSphere 9

Não houve refatoração arquitetural significativa — foi mais uma migração de plataforma.

---

## Projeto: Análise de Vulnerabilidades com Fortify + ChatGPT

A Bradesco implementou o **Fortify** como gate de qualidade para as aplicações. Sistemas legados tinham apontamentos em todos os níveis. O objetivo era zerar vulnerabilidades **Críticas** e **Altas**.

Leo pegou múltiplas aplicações (não só as de Sinistro RE) para corrigir.

**Primeiro contato com IA no trabalho:** Foi nesse projeto que Leo usou **ChatGPT (GPT-3.5)** pela primeira vez de forma profissional — para ajudar a entender e corrigir vulnerabilidades em sistemas legados. O ChatGPT foi especialmente útil para interpretar os apontamentos do Fortify em código legado complexo e sugerir correções adequadas.

---

## Saída

Recebeu proposta da **City Connect** para atuar como Líder Técnico. Aceitou e saiu após 5 anos na Ebix LATAM.

---

## Notas técnicas

- 5 anos na mesma conta Bradesco — domínio profundo de negócio de seguros (Sinistro RE)
- Pioneiro no uso de ChatGPT/IA para análise de vulnerabilidades no contexto da conta
- Referência técnica consolidada: decisões arquiteturais, mentoria, padronização de código
- Volume do sistema: 500–1.000 sinistros/dia, indenizações individuais de até R$5M
