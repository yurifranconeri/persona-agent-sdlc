# Análise Consolidada — Iniciativa #1085522 "Melhorias Resgate Senha inFlight"

> **Data da análise:** 2026-04-14
> **Fonte:** 26 work items extraídos do Azure DevOps (JSONs de campos, revisões e updates) + 9 documentos complementares (anexos do DevOps)
> **Método:** Análise factual campo-a-campo de cada WI; problemas numerados sequencialmente (P1–P218); conteúdo dos anexos cruzado com dados dos WIs

---

## 1. Escopo da Iniciativa

| Campo | Valor |
|-------|-------|
| **Iniciativa** | #1085522 — Melhorias Resgate Senha inFlight |
| **Projeto Portfolio** | Portfolio Tim TI |
| **Macro Portfolio** | #791755 |
| **Área** | CRO → Marketing Consumer e SMB |
| **Modelo de Gestão** | Waterfall |
| **Tipo** | Funcional |
| **Valor** | R$ 13.790,89 (Epic) |
| **Funcionamento** | Adicionar link de reset de senha na Webview inFlight (portal de bordo de companhias aéreas), substituindo texto orientativo por link clicável para `auth3.tim.com.br` |

---

## 2. Árvore Hierárquica Completa (26 WIs)

```
Portfolio Tim TI
├─ Iniciativa #1085522 (Closed — 2025-12-04)
│  ├─ MV VAS #1117156 (Aprovação Financeira — R$ 11.790,00) ← estagnada
│  ├─ MV FQA #1117168 (Resolved — R$ 2.000,89)
│  └─ Epic #1078031 (Resolved — 2025-12-04)
│     ├─ Feature #1113005 (New — 7+ meses sem transição)
│     │  └─ User Story #1113040 (Refinada — 7+ meses sem transição)
│     │     └─ IT Task #1136722 (Concluída — 2025-12-04)
│     │
│     ├─ Feature #1113105 (Closed — escopo negativo)
│     │  └─ User Story #1113109 (Concluída — escopo negativo)
│     │
│     ├─ Feature #1183520 (New — DM: 251070811 ⚠️ divergente)
│     │
│     └─ Documents Repository #1113128 (New)
│        ├─ Attachment #1113129 (New) — Briefing de Produto (2,24 MB PPTX)
│        └─ Attachment #1113130 (New) — Jornada inFlight (1,05 MB PPTX)

Projeto_Service_Creation
├─ Test Request #1164264 (Closed — 2025-11-24)
│  ├─ Test Case #1171260 CY0001 (Closed)
│  ├─ Test Case #1171261 CY0002 (Closed)
│  └─ Test Case #1171262 CY0003 (Closed — com falha e reteste)
│
├─ Bug #1184452 (Closed — container/proativo)
│  ├─ Entrega #1188548 (Aprovada em FQA)
│  ├─ Entrega #1192780 (Aprovada em FQA)
│  └─ Reteste #1199583 (Válido)
│
├─ Bug #1193756 (Closed — bug real OAuth/OAM)
│  ├─ Reteste #1196133 (Válido)
│  └─ [child link para Entrega #1195760]
│
Entrega_de_Kits
├─ Entrega #1178461 (Armazenada pelo SCM — feature original)
├─ Entrega #1188548 (Aprovada em FQA — bug fix)
├─ Entrega #1192780 (Aprovada em FQA — bug fix copy)
├─ Entrega #1195760 (Instalada em PROD — bug fix OAM)
└─ Entrega #1132619 (Armazenada pelo SCM — template externo à iniciativa)
```

---

## 3. Catálogo de Work Items — Métricas por WI

| # | ID | Tipo | Estado Final | Rev | Upd | Atores | Trans. Estado | Problemas | Projeto |
|:-:|:--:|:-----|:------------:|:---:|:---:|:------:|:---:|:---------:|:--------|
| 1 | 1085522 | Iniciativa | Closed | 43 | 46 | 10 | 8 | P1–P14 (14) | Portfolio Tim TI |
| 2 | 1078031 | Epic | Resolved | 43 | 51 | 10 | 8 | P65–P70 (6) | Portfolio Tim TI |
| 3 | 1113005 | Feature | New | 6 | 8 | 6 | 0 | P35–P39 (5) | Projeto_Service_Creation |
| 4 | 1113105 | Feature | Closed | 6 | 7 | 2 | 1 | P137–P144 (8) | Projeto_Service_Creation |
| 5 | 1183520 | Feature | New | 4 | 4 | 3 | 0 | P188–P194 (7) | Projeto_Service_Creation |
| 6 | 1113040 | User Story | Refinada | 27 | 31 | 7 | 1 | P47–P53 (7) | Projeto_Service_Creation |
| 7 | 1113109 | User Story | Concluída | 14 | 15 | 4 | 1 | P179–P187 (9) | Projeto_Service_Creation |
| 8 | 1136722 | IT Task | Concluída | 20 | 20 | 4 | 7 | P54–P64 (11) | Portfolio Tim TI |
| 9 | 1117156 | Macro Valoração | Aprovação Fin. | 29 | 30 | 5 | 2 | P15–P19 (5) | Portfolio Tim TI |
| 10 | 1117168 | Macro Valoração | Resolved | 32 | 34 | 7 | 7 | P20–P25 (6) | Portfolio Tim TI |
| 11 | 1164264 | Test Request | Closed | 24 | 25 | 7 | 6 | P26–P34 (9) | Projeto_Service_Creation |
| 12 | 1171260 | Test Case | Closed | 14 | 15 | 5 | 7 | P71–P78 (8) | Projeto_Service_Creation |
| 13 | 1171261 | Test Case | Closed | 15 | 16 | 5 | 7 | P79–P83 (5) | Projeto_Service_Creation |
| 14 | 1171262 | Test Case | Closed | 23 | 24 | 5 | 13 | P84–P91 (8) | Projeto_Service_Creation |
| 15 | 1199583 | Reteste | Válido | 1 | 2 | 2 | 0 | P92–P99 (8) | Projeto_Service_Creation |
| 16 | 1184452 | Bug | Closed | 20 | 23 | 6 | 7 | P100–P109 (10) | Projeto_Service_Creation |
| 17 | 1193756 | Bug | Closed | 34 | 36 | 7 | 12 | P195–P205 (11) | Projeto_Service_Creation |
| 18 | 1196133 | Reteste | Válido | 1 | 2 | 2 | 0 | P206–P210 (5) | Projeto_Service_Creation |
| 19 | 1132619 | Entrega | Armazenada SCM | 7 | 26 | 5 | 2 | P120–P127 (8) | Entrega_de_Kits |
| 20 | 1178461 | Entrega | Armazenada SCM | 3 | 4 | 3 | 0 | P40–P46 (7) | Entrega_de_Kits |
| 21 | 1188548 | Entrega | Aprovada FQA | 7 | 10 | 5 | 4 | P128–P136 (9) | Entrega_de_Kits |
| 22 | 1192780 | Entrega | Aprovada FQA | 7 | 8 | 5 | 4 | P110–P119 (10) | Entrega_de_Kits |
| 23 | 1195760 | Entrega | Instalada PROD | 7 | 10 | 6 | 3 | P211–P218 (8) | Entrega_de_Kits |
| 24 | 1113128 | Documents Repo | New | 6 | 8 | 5 | 0 | P160–P165 (6) | Projeto_Service_Creation |
| 25 | 1113129 | Attachment | New | 10 | 10 | 7 | 0 | P154–P159 (6) | Projeto_Service_Creation |
| 26 | 1113130 | Attachment | New | 12 | 15 | 8 | 0 | P145–P153 (8) | Projeto_Service_Creation |
| | **TOTAL** | **26 WIs** | | **457** | **520** | | **100** | **P1–P218 (217)** | **3 projetos** |

> **Nota:** P151 invalidado (artefato de exportação). P166–P178 gap reservado (não utilizado). Total efetivo: **217 problemas válidos**.

---

## 4. Métricas Agregadas

### 4.1. Volume

| Métrica | Valor |
|---------|:-----:|
| Work items | 26 |
| Revisões totais | 457 |
| Updates totais | ~520 |
| Transições de estado | 100 |
| Projetos Azure DevOps | 3 |
| Tipos de WI distintos | 12 |
| Problemas identificados | 217 |

### 4.2. Tipos de WI utilizados

| Tipo | Qtd | Projetos |
|------|:---:|---------|
| Iniciativa | 1 | Portfolio Tim TI |
| Epic | 1 | Portfolio Tim TI |
| Feature | 3 | Projeto_Service_Creation |
| User Story | 2 | Projeto_Service_Creation |
| IT Task | 1 | Portfolio Tim TI |
| Macro Valoração | 2 | Portfolio Tim TI |
| Test Request | 1 | Projeto_Service_Creation |
| Test Case | 3 | Projeto_Service_Creation |
| Bug | 2 | Projeto_Service_Creation |
| Reteste | 2 | Projeto_Service_Creation |
| Entrega | 5 | Entrega_de_Kits |
| Documents Repository | 1 | Projeto_Service_Creation |
| Attachment | 2 | Projeto_Service_Creation |

### 4.3. Estados finais

| Estado | Qtd | WIs |
|--------|:---:|-----|
| Closed | 8 | Iniciativa, Feature #1113105, TR, TC×3, Bug×2 |
| Resolved | 3 | Epic, MV FQA, MV VAS (parcial) |
| Concluída | 2 | IT Task, US #1113109 |
| New | 6 | Feature #1113005, Feature #1183520, DocRepo, Attachment×2, US #1113040 (Refinada) |
| Válido | 2 | Reteste×2 |
| Armazenada pelo SCM | 2 | Entrega #1178461, Entrega #1132619 |
| Aprovada em FQA | 2 | Entrega #1188548, Entrega #1192780 |
| Instalada em PROD | 1 | Entrega #1195760 |
| Aprovação Financeira | 1 | MV VAS #1117156 |

---

## 5. Timeline Consolidada — Marcos Principais

| Data | Evento | WI |
|:----:|--------|:--:|
| 2025-07-22 | Briefing de produto criado (PPTX) | — |
| 2025-08-05 | Epic criado (em Projeto_Service_Creation, projeto errado) | #1078031 |
| 2025-08-12 | Iniciativa criada | #1085522 |
| 2025-08-29 | Epic: 3 transições em 65 seg (Em Design→Estimativa→Estimado) | #1078031 |
| 2025-09-05 | Feature #1113005 + #1113105 + US×2 + DocRepo + Attachments criados por Ana Maria (sessão de ~1h) | 7 WIs |
| 2025-09-09 | MVs VAS e FQA criadas | #1117156, #1117168 |
| 2025-09-12 | Feature #1113105 marcada como "ESCOPO NEGATIVO" via título | #1113105 |
| 2025-09-23 | Entrega template #1132619 criada (externa à iniciativa, reutilizada como base) | #1132619 |
| 2025-09-29 | IT Task criado | #1136722 |
| 2025-10-08 | Feature #1113105 Closed ("Acceptance tests pass") + US #1113109 Concluída | #1113105, #1113109 |
| 2025-10-08 | Especificação Funcional v1.0 (Paulo Ricardo Castellanos Souza) | [Anexo DOCX] |
| 2025-10-13 | Migração em massa: Portfolio Tim TI → Projeto_Service_Creation (Franco Kaufmann) | 7+ WIs |
| 2025-10-17 | Epic: Aprovação Financeira (Paulo Henrique + Ana Maria) | #1078031 |
| 2025-10-17 | **E-mail de Aprovação de Negócio** enviado (Fernanda Soares → DL_CRO_GONEGOCIO, Ana Maria + 7 destinatários) | [Anexo .msg ×3] |
| 2025-10-21 | Caderno de Testes FQA v0.2 atualizado (original v0.1 de 21/06/2022) | [Anexo DOCX] |
| 2025-10-23 | MV FQA Resolved. Test Request criado (cópia de #1113040) | #1117168, #1164264 |
| 2025-10-27 | Epic: Em Desenvolvimento | #1078031 |
| 2025-10-29 | 3 Test Cases criados | #1171260–62 |
| 2025-11-05 | Entrega da feature original criada (Armazenada pelo SCM, 11 min de ciclo) | #1178461 |
| 2025-11-10 | Feature #1183520 criada (Rollout, código de demanda divergente) | #1183520 |
| 2025-11-11 | Bug #1184452 criado como container (antes da execução dos testes) | #1184452 |
| 2025-11-13 | Entrega #1188548 criada (bug fix, copiada de #1132619) | #1188548 |
| 2025-11-14 | TCs Bloqueados (dependência de ambiente) | #1171260–62 |
| 2025-11-17 | CY0001 e CY0002 executados com sucesso. CY0003: 1ª tentativa enviada | #1171260–62 |
| 2025-11-17 | Entrega #1192780 criada (bug fix, copiada de #1188548) | #1192780 |
| 2025-11-18 | **CY0003 falha** — erro OAuth OAM na página inFlight | #1171262 |
| 2025-11-18 | Bug #1193756 criado (bug real, Severity 1-Critical) | #1193756 |
| 2025-11-18 | CY0001 e CY0002 aprovados e fechados por Ana Maria/Automação | #1171260, #1171261 |
| 2025-11-19 | Bug #1193756: Severity rebaixada 1-Critical→3-Medium→4-Low (Marcio) | #1193756 |
| 2025-11-19 | Bug #1193756: 4 round-trips ping-pong FRN↔CCC em 52 min | #1193756 |
| 2025-11-19 | Bug #1193756: "correção" em burst de 45 seg, Closed por Anderson | #1193756 |
| 2025-11-19 | Entrega #1195760 criada (bug fix OAM, copiada de #1194802) | #1195760 |
| 2025-11-19 | CY0003 retestado com sucesso e fechado | #1171262 |
| 2025-11-19 | Reteste #1196133 criado (automação, child de Bug #1193756) | #1196133 |
| 2025-11-24 | Bug #1184452 finalmente ativado e fechado (5 dias após reteste) | #1184452 |
| 2025-11-24 | Test Request Closed | #1164264 |
| 2025-11-24 | **E-mail de Aprovação UAT** (Anderson Teixeira → Paulo Ricardo + Paulo Henrique). Menciona TR #1121243 (OFFERING_DEVELOPMENT_LIVE) como agrupador | [Anexo .eml] |
| 2025-11-24 | Reteste #1199583 criado (automação, child de Bug #1184452) | #1199583 |
| 2025-11-24 | Entregas #1188548 e #1192780 percorrem pipeline FQA em ~45 min | #1188548, #1192780 |
| 2025-12-01 | Entrega #1195760 Liberada para PROD (Paulo Ricardo, CHG0177576) | #1195760 |
| 2025-12-03 | Entrega #1195760 Instalada em PROD (Itsmazure-prod) | #1195760 |
| 2025-12-04 | Epic Resolved. IT Task Concluída. Iniciativa Closed. | #1078031, #1136722, #1085522 |
| 2025-12-11 | Comentário "VAS_IMROCEDENTE" nos Bugs (typo) | #1184452, #1193756 |
| 2026-02-10 | Comentário "VAS_IMPROCEDENTE" (correção do typo, 83 dias pós-closing) | #1193756 |
| 2026-03-23 | Último update da iniciativa (StackRank em Feature #1183520 e DocRepo) | #1183520, #1113128 |

---

## 6. Ciclos de Vida e Lead Times

### 6.1. Duração do pipeline completo

| Marco | Data | Δ acumulado |
|-------|:----:|:-----------:|
| Briefing de produto (PPTX) | 2025-07-22 | dia 0 |
| Epic criado | 2025-08-05 | +14 dias |
| Iniciativa criada | 2025-08-12 | +21 dias |
| Features e USs criadas | 2025-09-05 | +45 dias |
| MVs criadas | 2025-09-09 | +49 dias |
| IT Task criado | 2025-09-29 | +69 dias |
| Epic Em Desenvolvimento | 2025-10-27 | +97 dias |
| TCs criados | 2025-10-29 | +99 dias |
| CY0003 falha | 2025-11-18 | +119 dias |
| Bug corrigido + reteste OK | 2025-11-19 | +120 dias |
| Entrega instalada em PROD | 2025-12-03 | +134 dias |
| Iniciativa Closed | 2025-12-04 | +135 dias |
| Último update registrado | 2026-03-23 | +244 dias |

**Pipeline total (briefing → Closed):** 135 dias
**Trail de atividade pós-fechamento:** +109 dias

### 6.2. Lead Times por segmento

| Segmento | Duração |
|----------|:-------:|
| Briefing → Criação do Epic | 14 dias |
| Epic criado → Epic Em Desenvolvimento | 83 dias |
| Epic Em Desenvolvimento → Testes iniciados | 22 dias |
| Testes iniciados → Testes concluídos | 21 dias |
| Teste CY0003 falha → Bug corrigido + reteste OK | 28h 27min |
| Entrega feature criada → Entrega bug fix em PROD | 28 dias |
| Entrega bug fix criada → Instalada em PROD | 14 dias |
| Epic Em Desenvolvimento → Iniciativa Closed | 38 dias |

### 6.3. Fases do método Waterfall observadas

| Fase | Início | Fim | Duração | WIs envolvidos |
|------|:------:|:---:|:-------:|:--------------:|
| **Ideação/Briefing** | 2025-07-22 | 2025-08-12 | 21 dias | Briefing PPTX, Epic, Iniciativa |
| **Portfolio/Valoração** | 2025-08-12 | 2025-10-27 | 76 dias | Iniciativa, Epic, MVs, Features, USs |
| **Desenvolvimento** | 2025-10-27 | 2025-11-05 | 9 dias | IT Task, Entrega #1178461 |
| **Testes FQA** | 2025-10-29 | 2025-11-24 | 26 dias | TR, TCs, Bugs, Retestes, Entregas bug |
| **Deploy/Fechamento** | 2025-12-01 | 2025-12-04 | 3 dias | Entrega PROD, Epic, Iniciativa |
| **Trail pós-fechamento** | 2025-12-04 | 2026-03-23 | 109 dias | StackRank, comentários, CausaRaiz |

---

## 7. Catálogo de Atores

### 7.1. Atores únicos identificados (35 identidades)

| # | Nome | Tipo | WIs tocados | Papel principal observado |
|:-:|------|:----:|:-----------:|--------------------------|
| 1 | **Ana Maria Lopes Moreira** | Humano | 13 | PO/Gestão — criou Features, USs, DocRepo, Attachments, aprovou TCs |
| 2 | **Paulo Ricardo Castellanos Souza** | Humano | 12 | Tech Lead — valoração, aprovação Lid Tec, transições Epic/Bug/Entrega |
| 3 | **Fernanda Soares Marelli Leite** | Humano | 4 | Gestora de portfolio — transições Iniciativa/Epic, MVs, flags |
| 4 | **Anderson Teixeira Abrantes** | Humano | 9 | FQA/ATOS — TCs, Bugs (criou/fechou), TR |
| 5 | **AzDevOpsServ_PRD** | Automação | 9 | Sync de campos, ResponsavelDePara, CausaRaiz, Retestes |
| 6 | **Rodrigo Alexandre Oliveira** | Humano | 6 | SCM — criou/gerenciou Entregas |
| 7 | **Franco Kaufmann Gaspar Ferreira Junior** | Humano | 6 | Migração cross-project em lote |
| 8 | **Marcio Evaristo Souza** | Humano | 2 | Engineering — resolveu Bug #1193756, rebaixou severidade |
| 9 | **Carolina Ribeiro Gomes Sundin** | Humano | 4 | StackRank |
| 10 | **Joanna Maria Haslwanter** | Humano | 5 | StackRank |
| 11 | **Karyne Vianna Carmo Gallindo** | Humano | 4 | StackRank |
| 12 | **Tamiris Leandro Martins Das Neves** | Humano | 4 | StackRank |
| 13 | **Danielle Da Fonseca Aguiar** | Humano | 2 | Criadora do Epic e Iniciativa |
| 14 | **Paulo Henrique Ferreira Costa** | Humano | 2 | Aprovador de negócio |
| 15 | **Fabio Prazeres Da Silva** | Humano | 3 | StackRank |
| 16 | **Meire Goncalves Luksaitis** | Humano | 2 | FQA — macrovaloração |
| 17 | **Camilla Alves Da Silva** | Humano | 2 | Flags MVs |
| 18 | **Denise Cruz Ferrao** | Humano | 2 | Flags MVs |
| 19 | **Priscila Dos Santos Figueiredo Marques** | Humano | 2 | Flags MVs |
| 20 | **Mauricio Valderrama De Oliveira** | Humano | 5 | Engineering-OAM — BugOwnerCCC nas Entregas |
| 21 | **Fellipe Pinheiro Moncayo** | Humano | 5 | Responsável Entrega nos WIs de Entrega |
| 22 | **Thiago Gomes Marques** | Humano | 2 | Pipeline FQA de Entregas |
| 23 | **Victor Rodrigues Da Silva** | Humano | 2 | Comentário "VAS_IMPROCEDENTE" |
| 24 | **Andre Luiz Bruver** | Humano | 1 | Reclassificação CausaRaizN2 |
| 25 | **Silvio Dos Santos Junior** | Humano | 1 | Kanban lane mapping |
| 26 | **Marcelo Henrique Costa Da Silva** | Humano | 1 | Ajuste DiretoriaN2 |
| 27 | **Fernanda Rodrigues de Oliveira** | Humano | 1 | FQA — TR |
| 28 | **Carlos Eduardo de Lima Ribeiro** | Humano | 1 | TR |
| 29 | **Thiago Brito De Menezes** | Humano | 1 | Entrega template |
| 30 | **Priscilla Araujo Brandao** | Humano | 1 | Entrega template |
| 31 | **Priscila Santos da Silva** | Humano | 1 | Iniciativa |
| 32 | **Danielle Matos Martins** | Humano | 1 | Iniciativa |
| 33 | **Simone De Lacerda Sampaio** | Humano | 1 | Iniciativa |
| 34 | **Paulo Cesar Dias Lima** | Humano | 1 | Arquiteto (inativo no sistema) |
| 35 | **Itsmazure-prod** | Automação | 1 | Deploy PROD (ITSM) |

### 7.2. Distribuição de atores por papel

| Papel | Atores | % dos 35 |
|-------|:------:|:--------:|
| Gestão de portfolio/produto (PO, gestora, aprovadores) | 6 | 17% |
| Engenharia/Development (Tech Lead, Engineering, SCM) | 5 | 14% |
| Teste/FQA (ATOS, FQA, aprovação TC) | 4 | 11% |
| Valoração financeira (flags, MVs) | 3 | 9% |
| StackRank exclusivo (repriorização de board) | 4 | 11% |
| Automação (AzDevOpsServ_PRD, Itsmazure-prod) | 2 | 6% |
| Infraestrutura/Migração | 1 | 3% |
| Participação pontual (1 WI, ajustes administrativos) | 10 | 29% |

---

## 8. Padrões Recorrentes (Cross-Cutting)

### 8.1. Transições cerimoniais

Registros de estado atravessados sem atividade real correspondente.

| WI | Transições | Tempo | Dados |
|----|-----------|:-----:|-------|
| Epic #1078031 | Em Design → Estimativa → Estimado | 65 seg | P65 |
| IT Task #1136722 | Refinamento → Valoração | <1 min | P58 |
| MV VAS #1117156 | Macrovaloração → Valoração | 1 min | P17 |
| MV FQA #1117168 | PO atribuído 2 seg antes de Resolved | 2 seg | P23 |
| Bug #1184452 | Em Desenvolvimento → Correção Entregue | 29 seg | P102 |
| Bug #1193756 | Em Desenvolvimento → Correção Entregue → Em IT/UAT | 45 seg | P197 |
| TC #1171262 | Retestar → Aberto → Em Andamento | 9 seg | P85 |

### 8.2. Ping-pong de responsabilidade

Transições repetidas entre estados de triagem/responsabilidade.

| WI | Pattern | Rounds | Tempo | Dados |
|----|---------|:------:|:-----:|-------|
| Bug #1193756 | FRN ↔ Em Análise Detalhada | 4 | 52 min | P196 |
| Bug #1184452 | FQA→CCC→FRN→CCC→FQA→FECHADA | 5 | ciclo completo | P103 |
| Bug #1193756 | ResponsavelDePara: 14 transições vs 12 de estado | — | — | P204 |

### 8.3. Cópia em cascata com propagação de erros

WIs criados por cópia de outros, herdando campos incorretos.

| WI copiado | Fonte | Campos herdados errados | Dados |
|------------|-------|------------------------|-------|
| Bug #1184452 | IT Task #1136722 | Título "Copy - Copy", Description com requisitos (não defeito) | P100, P104, P105 |
| Entrega #1188548 | Entrega #1132619 | Label de outra demanda (DR841587), Description de BUG SSO | P129, P130 |
| Entrega #1192780 | Entrega #1188548 | Label + Title "- Copy" + Description errada (3ª geração) | P110, P111, P119 |
| Entrega #1195760 | Entrega #1194802 | CodigoDemanda de outro bug (BUG1192764) | P211 |
| TR #1164264 | US #1113040 | ValorPO inflado R$194.270 (9 dias), Vendor errado 3× | P27, P28, P29 |

### 8.4. Overhead de StackRank

WIs que recebem revisões exclusivamente de repriorização de board, sem mudança funcional.

| WI | Revs de StackRank | % do total de revs | Atores de StackRank |
|----|:------------------:|:------------------:|:-------------------:|
| Feature #1113005 | 4 | 67% | 3 |
| Feature #1183520 | 3 | 75% | 3 |
| DocRepo #1113128 | 4 | 67% | 4 |
| Attachment #1113129 | 7 | 70% | 5 |
| Attachment #1113130 | 7 | 58% | 5 |
| **Total** | **25** | | |

### 8.5. WIs pós-fechamento da Iniciativa

WIs com revisões registradas após 2025-12-04 (Iniciativa Closed).

| WI | Revs pós-fechamento | Última revisão | Δ pós-fechamento |
|----|:-------------------:|:--------------:|:----------------:|
| Feature #1113005 | 2 | 2026-03-23 | +109 dias |
| Feature #1183520 | 2 | 2026-03-23 | +109 dias |
| DocRepo #1113128 | 2 | 2026-03-23 | +109 dias |
| Attachment #1113129 | 4 | 2026-03-10 | +96 dias |
| Attachment #1113130 | 4 | 2026-03-10 | +96 dias |
| Bug #1193756 | 3 | 2026-02-10 | +68 dias |
| Bug #1184452 | 1 | 2025-12-11 | +7 dias |
| Iniciativa #1085522 | 3 | 2026-03-06 | +92 dias |
| US #1113040 | 2+ | 2026-03-23 | +109 dias |

### 8.6. Migração cross-project em lote

Em 2025-10-13, Franco Kaufmann migrou múltiplos WIs de Portfolio Tim TI para Projeto_Service_Creation. WIs afetados: Feature #1113005, Feature #1113105, US #1113040, US #1113109, DocRepo #1113128, Attachment #1113129, Attachment #1113130.

### 8.7. Retroatividade de registro

WIs criados ou preenchidos com datas/dados retroativos.

| WI | Evidência | Dados |
|----|-----------|-------|
| Entrega #1178461 | DataPlanejada = DataEntrega = momento de criação | P44 |
| Entrega #1188548 | DataPlanejada = DataEntrega = 33 seg antes da criação | P131 |
| Entrega #1192780 | DataPlanejada e DataEntrega 4 dias antes da criação. Confirmação textual "Instalação já realizada" | P113, P115 |
| Entrega #1195760 | DataPlanejada e DataEntrega 20h15min antes da criação | P212 |
| Bug #1193756 | EstimatedResolutionDate definida 11 seg antes da resolução | P203 |
| Reteste #1199583 | Criado 5 dias após o reteste real | P98 |

### 8.8. Inconsistência hierárquica de estados

WIs-pai fechados com WIs-filhos em estados iniciais.

| Pai | Estado pai | Filho | Estado filho | Dados |
|-----|:----------:|-------|:------------:|-------|
| Iniciativa #1085522 | Closed | MV VAS #1117156 | Aprovação Financeira | P15 |
| Epic #1078031 | Resolved | Feature #1113005 | New | P38, P69 |
| Epic #1078031 | Resolved | Feature #1183520 | New | P190 |
| Epic #1078031 | Resolved | US #1113040 | Refinada | P47, P69 |

---

## 9. Métricas Financeiras

| Item | Valor |
|------|------:|
| Macro_Valoracao (Epic) | R$ 14.000 |
| ValorEpic (final) | R$ 13.790,89 |
| MV VAS #1117156 | R$ 11.790,00 |
| MV FQA #1117168 | R$ 2.000,89 |
| MandayDevEstimado (TR) | 21,16 MD |
| MandayDevAferido (TR) | 21,15 MD |
| Custo declarado reteste (Bug #1193756) | 120 min |
| Custo declarado reteste (Reteste #1199583) | 120 min |
| Custo reteste total declarado | 240 min (4 horas) |

> **Nota sobre duplicidade:** Os 120 min aparecem tanto no Bug #1193756 quanto no Reteste #1199583, referindo-se ao mesmo evento. Total real observável: 120 min declarados, contabilizados em duplicata (P206).

---

## 10. O Ciclo do Bug — Da Falha ao Deploy

A falha do TC CY0003 (OAuth OAM redirect loop) gerou a seguinte cadeia:

```
TC #1171262 (CY0003) ─── falhou 2025-11-18 ───► Bug #1193756 (real)
                                                    │
Bug #1184452 (container, criado 7 dias antes) ◄─── sem link ────► Bug #1193756
    │                                                │
    ├── Reteste #1199583 (120 min)                   ├── Reteste #1196133 (120 min)
    ├── Entrega #1188548 (Aprovada FQA)              └── Entrega #1195760 (PROD)
    └── Entrega #1192780 (Aprovada FQA)
```

| Métrica | Bug #1184452 (container) | Bug #1193756 (real) |
|---------|:------------------------:|:-------------------:|
| Criação | 2025-11-11 (pré-teste) | 2025-11-18 (durante teste) |
| Fechamento | 2025-11-24 | 2025-11-19 |
| Revisões | 20 | 34 |
| Updates | 23 | 36 |
| Severidade | 2-High (mantida) | 1-Critical → 4-Low |
| Evidências técnicas | 0 (description = requisitos) | HAR + vídeo + System Info |
| Entregas filhas | 2 | 1 |
| Link entre eles | Nenhum | Nenhum |
| Comentário final | "VAS_IMPROCEDENTE" | "VAS_IMPROCEDENTE" |

---

## 11. Distribuição de Overhead

### 11.1. Revisões por categoria de atividade (estimativa)

| Categoria | Revisões est. | % |
|-----------|:------------:|:-:|
| Transições de estado (progresso real) | ~100 | 22% |
| StackRank / repriorização de board | ~60 | 13% |
| Automação (sync campos, ResponsavelDePara) | ~80 | 18% |
| Flags, toggles, adjustments administrativos | ~40 | 9% |
| Migração cross-project | ~20 | 4% |
| Conteúdo (description, campos funcionais) | ~50 | 11% |
| Criação de WIs | 26 | 6% |
| Links / relações | ~30 | 7% |
| Pós-fechamento (CausaRaiz, comentários, StackRank) | ~51 | 11% |
| **Total** | **~457** | **100%** |

### 11.2. O cluster documental

3 WIs (Documents Repository + 2 Attachments) para armazenar 2 arquivos PPTX:

| Métrica | Valor |
|---------|:-----:|
| WIs criados | 3 |
| Revisões totais | 28 |
| Atores únicos | 8 |
| Transições de estado | 0 |
| Conteúdo: arquivos PPTX | 2 (3,29 MB total) |
| Trabalho real | ~2 min (criação + upload) |
| Vida útil no board | 200 dias |

---

## 12. Tabela Completa de Problemas (P1–P218)

| Faixa | WI | Tipo | Qtd |
|:-----:|:--:|------|:---:|
| P1–P14 | #1085522 | Iniciativa | 14 |
| P15–P19 | #1117156 | MV VAS | 5 |
| P20–P25 | #1117168 | MV FQA | 6 |
| P26–P34 | #1164264 | Test Request | 9 |
| P35–P39 | #1113005 | Feature (ativa) | 5 |
| P40–P46 | #1178461 | Entrega (feature) | 7 |
| P47–P53 | #1113040 | User Story | 7 |
| P54–P64 | #1136722 | IT Task | 11 |
| P65–P70 | #1078031 | Epic | 6 |
| P71–P78 | #1171260 | TC CY0001 | 8 |
| P79–P83 | #1171261 | TC CY0002 | 5 |
| P84–P91 | #1171262 | TC CY0003 | 8 |
| P92–P99 | #1199583 | Reteste (container) | 8 |
| P100–P109 | #1184452 | Bug (container) | 10 |
| P110–P119 | #1192780 | Entrega (bug copy) | 10 |
| P120–P127 | #1132619 | Entrega (template) | 8 |
| P128–P136 | #1188548 | Entrega (bug) | 9 |
| P137–P144 | #1113105 | Feature (escopo neg.) | 8 |
| P145–P150, P152–P153 | #1113130 | Attachment (Anexo II) | 8 |
| ~~P151~~ | — | ~~Invalidado~~ | 0 |
| P154–P159 | #1113129 | Attachment (Anexo I) | 6 |
| P160–P165 | #1113128 | Documents Repository | 6 |
| P166–P178 | — | Gap reservado | 0 |
| P179–P187 | #1113109 | US (escopo negativo) | 9 |
| P188–P194 | #1183520 | Feature (orphan) | 7 |
| P195–P205 | #1193756 | Bug (real) | 11 |
| P206–P210 | #1196133 | Reteste (real) | 5 |
| P211–P218 | #1195760 | Entrega (PROD) | 8 |
| **Total** | **26 WIs** | | **217** |

---

## 13. Categorização dos 217 Problemas

| Categoria | Exemplos | Qtd est. | % |
|-----------|----------|:--------:|:-:|
| **Overhead processual** | Transições cerimoniais, StackRank, estados sem atividade | ~45 | 21% |
| **Inconsistência de dados** | Campos contraditórios, descrições herdadas erradas, títulos "Copy" | ~40 | 18% |
| **Inconsistência hierárquica** | Pais fechados com filhos abertos, estados divergentes | ~20 | 9% |
| **Retroatividade** | Datas preenchidas retroativamente, WIs criados após o fato | ~15 | 7% |
| **Duplicação** | Bugs sem link, Retestes duplicados, Entregas redundantes | ~15 | 7% |
| **Automação opaca** | ResponsavelDePara, CausaRaiz, RetesteComputado, campos GUID | ~20 | 9% |
| **Governança ausente** | Sem gate hierárquico, sem SLA, sem validação de campos | ~25 | 12% |
| **Fragmentação cross-project** | 3 projetos, migração em lote, visibilidade parcial | ~15 | 7% |
| **Overhead documental** | 3 WIs para 2 PPTXs, tipo Attachment customizado | ~10 | 5% |
| **Classificação/taxonomia** | Severidade rebaixada, CausaRaiz contradiz N2, tipo de erro errado | ~12 | 6% |

---

## 14. Dados de Referência para o TCC

### 14.1. Números-chave

| Dado | Valor | Contexto |
|------|:-----:|---------|
| WIs para 1 alteração de UX | 26 | Adicionar link numa Webview |
| Revisões totais | 457 | Para R$ 13.790,89 de valor |
| Atores humanos únicos | 33 + 5 | 33 nos WIs + 5 em documentos/e-mails |
| Projetos Azure DevOps | 3 | Portfolio, Execution, Deploy |
| Tipos de WI distintos | 12 | Customizados pela organização |
| Problemas observáveis nos dados | 217 | Factuais, extraídos dos JSONs |
| Documentos complementares | 9 | 2 PPTX, 2 DOCX, 1 XLSM, 1 EML, 3 MSG |
| Requisitos Funcionais na Especificação | 3 | RF001–RF003 para 26 WIs e 217 problemas |
| Feature principal em "New" | 7+ meses | Trabalho executado e fechado sem ela |
| Entregas que alcançaram PROD | 1 de 5 | Entrega #1195760 (bug fix OAM) |
| Pipeline briefing → produção | 135 dias | Para adicionar 1 link HTML |
| Bug "corrigido" em | 45 seg | 3 transições Em Desenvolvimento→Em IT/UAT |
| Reteste contabilizado em duplicata | 120 min × 2 | Mesmo evento, 2 WIs |
| Custo de overhead documental | 28 rev, 8 atores | Para 2 PPTXs (3,29 MB) |

### 14.2. Workflows observados

| Workflow | Projeto | WIs |
|----------|---------|:---:|
| Iniciativa (Fechada→Closed) | Portfolio Tim TI | 1 |
| Epic (New→Resolved) | Portfolio Tim TI | 1 |
| Feature (New→Closed ou New estagnado) | Projeto_Service_Creation | 3 |
| User Story (Refinada ou Concluída) | Projeto_Service_Creation | 2 |
| IT Task (New→Concluída) | Portfolio Tim TI | 1 |
| Macro Valoração (Macro→Resolved ou estagnada) | Portfolio Tim TI | 2 |
| Test Request (New→Closed) | Projeto_Service_Creation | 1 |
| Test Case (Criado→Closed) | Projeto_Service_Creation | 3 |
| Bug (SDN Registrada→Closed) | Projeto_Service_Creation | 2 |
| Reteste (Válido, terminal) | Projeto_Service_Creation | 2 |
| Entrega (Armazenada→PROD ou estagnada) | Entrega_de_Kits | 5 |
| Documents Repository / Attachment (New, sem workflow) | Projeto_Service_Creation | 3 |

---

## 15. Documentos Complementares (Anexos do DevOps)

9 documentos complementares foram adicionados ao corpus de análise. Abaixo, o inventário e as informações adicionais extraídas de cada um.

### 15.1. Inventário de Documentos

| # | Arquivo | Tipo | Tamanho | Data observável | Autor/Remetente |
|:-:|---------|:----:|:-------:|:---------------:|:----------------|
| 1 | TIM_Service Creation_Briefing INTELSAT Recuperação de Senha.pptx | PPTX | 2,35 MB | 2025-07-22 | Consumer SMB Marketing (Felipe Povoa) |
| 2 | Jornada Inflight_251078031.pptx | PPTX | 1,05 MB | 2025-07-22 | Mesmo conteúdo do slide 4 do Briefing |
| 3 | Especificação Funcional.docx | DOCX | 3,18 MB | 2025-10-08 (v1.0) | Paulo Ricardo Castellanos Souza |
| 4 | 03 - Caderno de Testes - Autenticação IntelSat.docx | DOCX | 3,26 MB | 2022-06-21 (v0.1) / 2025-10-21 (v0.2) | Paulo Castellanos |
| 5 | IT - Template Cenarios_catalogo_inflight (2).xlsm | XLSM | 56 KB | 2025 | Equipe VAS |
| 6 | Aprovação UAT e IT - Test Request 1121243...eml | EML | — | 2025-11-24 | Anderson Teixeira Abrantes |
| 7 | RES_ IT Business Agility - Epic 1078031...msg | MSG | 227 KB | 2025-10-17 | Fernanda Soares Marelli Leite |
| 8 | RES_ IT Business Agility...msg (2) | MSG | 227 KB | 2025-10-17 | Fernanda Soares Marelli Leite |
| 9 | RES_ IT Business Agility...msg (3) | MSG | 227 KB | 2025-10-17 | Fernanda Soares Marelli Leite |

### 15.2. Especificação Funcional (DOCX)

| Campo | Valor |
|-------|-------|
| **Título** | Especificação Funcional — DM251078031 – Melhoria Resgate de Senha INFLIGHT |
| **Área** | IT - Digital Solutions |
| **Versão** | 1.1 |
| **Aprovador** | Ana Maria Lopes Moreira (Struct. & VAS Service Creation & Proc) |
| **Gerente de Projetos** | Paulo Ricardo Castellanos Souza |
| **Líder Técnico** | Paulo Ricardo Castellanos Souza (mesma pessoa que GP) |
| **CCC Master** | TI – VAS & Partnerships |
| **Lista de distribuição** | Paulo Henrique Ferreira Costa (IT Digital Solutions), Ana Maria Lopes Moreira |

#### Requisitos Funcionais

| ID | Título | Regra |
|:--:|--------|:-----:|
| RF001 | Ajustar Mensagem Orientativa - Inflight (substituir texto por botão) | RN001 |
| RF002 | Direcionamento para Reset de Senha (`auth3.tim.com.br/webapp-resetSenha/forgotPassword`) | RN001 |
| RF003 | Retornar para a aplicação Inflight após reset | RN001 |

#### Regra de Negócio

| ID | Descrição |
|:--:|-----------|
| RN001 | Utilizar serviço de Reset de Senha – Tim Beta (IDM, as is) |

#### Caso de Uso

| Caso | Fluxo principal | Fluxo alternativo |
|:----:|----------------|-------------------|
| C01 — Resgate de Senha | 1. Usuário no Inflight → 2. Não sabe senha → 3. Seleciona "Esqueceu a senha" → 4. Tela de resgate → 5. Informa MSISDN → 6. Recebe senha via SMS → 7. Retorna ao Inflight | Erro na postagem do OMS → recuperar senha no APP TIM |

#### Requisitos Não Funcionais

- Resiliência do serviço
- Alta disponibilidade
- Rastreabilidade dos logs da aplicação

#### Campos "Não se aplica"

Escopo Negativo, SLAs, Matriz de Responsabilidade — todos marcados como "Não se aplica".

### 15.3. Caderno de Testes FQA (DOCX)

| Campo | Valor |
|-------|-------|
| **Título** | Caderno de Testes FQA — Fluxo de Autenticação e Resgate de Senha — Infligth TIM - IntelSat |
| **Criação original** | 21/06/2022 (v0.1) — **documento de 2022 reutilizado** |
| **Atualização** | 21/10/2025 (v0.2 — Reset de Senha) |
| **Autor** | Paulo Castellanos |

#### URL de Teste FQA

```
https://oamqa.internal.timbrasil.com.br:443/ms_oauth/oauth2/ui/oauthcaptiveflyservice/showconsent
  ?response_type=code
  &client_id=intelsat
  &redirect_uri=https://wifi.gogoinflight.com
  &scope=TIM.offline
  &oracle_client_name=Intelsat
```

#### Stack Técnico Revelado

| Componente | Tecnologia |
|------------|-----------|
| Autenticação | Oracle Access Management (OAM) |
| Gerenciamento de identidade | IDM (AAA: Autenticação, Autorização e Perfil) |
| Protocolo | OAuth 2.0 (Authorization Code flow) |
| Portal cativo | Intelsat → `wifi.gogoinflight.com` |
| Reset de senha | `auth3.tim.com.br/webapp-resetSenha` |
| Fluxo OAuth | Client → OAM consent → Access Code → redirect URI → Token |

#### Cenários de Teste (3)

| # | Cenário | Resultado esperado |
|:-:|---------|-------------------|
| 3.1 | Resgatar senha | SMS encaminhado com a senha |
| 3.2 | Voltar após reset | Retorna à página principal de autenticação |
| 3.3 | Autenticação usuário/senha | MSISDN + senha → Access Code para URI de redirect → Intelsat troca por Token |

### 15.4. Template de Cenários (XLSM)

| Campo | Valor |
|-------|-------|
| **Código da Demanda** | DM 251078031 |
| **Nome** | Melhorias Resgate Senha inFlight |
| **Ano** | 2025 |
| **Cenários definidos** | 3 (CY0001–CY0003) |
| **Cenários em branco** | 285 (CY0004–CY0288) — template pré-formatado |
| **Equipe** | VAS |
| **Prioridade** | Alta (todos) |

| CY | Sumário | Pré-condição | Resultado esperado |
|:--:|---------|-------------|-------------------|
| CY0001 | Autenticação com sucesso | MSISDN válido | Loga → autentica → recebe token para API |
| CY0002 | Resgate de Senha | MSISDN válido | Resgata senha → recebe senha → usa na autenticação |
| CY0003 | Retornar à página do Inflight após autenticação | MSISDN válido | Resgatou senha → recebeu confirmação → retorna ao Inflight |

> **Correspondência com TCs do DevOps:** CY0001 → TC #1171260, CY0002 → TC #1171261, CY0003 → TC #1171262. Títulos e sumários coincidem.

### 15.5. E-mail de Aprovação UAT (EML — 2025-11-24)

| Campo | Valor |
|-------|-------|
| **De** | Anderson Teixeira Abrantes (aabrantes_atos@timbrasil.com.br) |
| **Para** | Paulo Ricardo Castellanos Souza, Paulo Henrique Ferreira Costa |
| **CC** | Celso Pereira Dias Neto, Carlos Eduardo de Lima |
| **Data** | 2025-11-24 12:33 UTC |
| **Assunto** | Aprovação UAT e IT - Test Request 1121243: 25932252 - Criação de Canal Móvel APP TIM |
| **Conteúdo** | "Informo a conclusão parcial dos testes" — demanda "Encerrada no seu atual status" |
| **Ambiente** | UAT1 |

#### Dados do teste no e-mail

| TR | Teste | Código Demanda | Nome | Responsável CCC | Responsável FQA |
|:--:|:-----:|:--------------:|------|:---------------:|:---------------:|
| TR1164264 | UAT | DM251078031 | Alteração da Fraseologia e Criação do Botão - inFlight | Paulo Ricardo Castellanos Souza | Anderson Teixeira Abrantes |

| Cenário | Título | Tipo | Status |
|:-------:|--------|:----:|:------:|
| 1171260 | CY0001 - Autenticação com sucesso | UAT Delivery | Closed |
| 1171261 | CY0002 - Resgate de Senha | UAT Delivery | Closed |
| 1171262 | CY0003 - Retornar a pagina do inflight após autenticação | UAT Delivery | Closed |

#### Referência cruzada

O assunto do e-mail menciona **Test Request #1121243** no projeto **OFFERING_DEVELOPMENT_LIVE** (código de demanda 25932252 — "Criação de Canal Móvel APP TIM"). O corpo lista **TR #1164264** (nossa iniciativa) como um dos testes executados dentro desse escopo. Isso indica que a aprovação UAT dessa iniciativa foi agrupada com outra iniciativa diferente num mesmo ciclo de aprovação FQA.

### 15.6. E-mails de Aprovação de Negócio (.msg ×3 — 2025-10-17)

3 cópias da mesma thread de e-mail (provavelmente respostas sequenciais na thread).

| Campo | Valor |
|-------|-------|
| **De** | Fernanda Soares Marelli Leite (fleite@timbrasil.com.br) |
| **Para** | Diego Wanderosck Lisboa, DL_CRO_GONEGOCIO (lista de distribuição CRO), Danielle Da Fonseca Aguiar, Ana Maria Lopes Moreira |
| **CC** | Patricia Gassenferth Veloso Barreira Milet, Paulo Henrique Ferreira Costa, Paulo Ricardo Castellanos Souza, Cândida Pacheco da Cunha Neta |
| **Data** | 2025-10-17 13:19 UTC |
| **Assunto** | RES: IT Business Agility - Epic 1078031: 251078031 - Melhorias Resgate Senha inFlight - Aprovação de Negócio para Desenvolvimento |

> **Correlação:** A data deste e-mail (17/10/2025) coincide exatamente com a transição do Epic #1078031 para "Aprovação Financeira" registrada no Azure DevOps. O e-mail é a formalização fora do DevOps do gate de aprovação de negócio.

### 15.7. Atores Adicionais Identificados nos Documentos

Atores presentes nos e-mails e documentos que **não aparecem nos dados dos 26 WIs** do Azure DevOps:

| # | Nome | Canal | Papel observado |
|:-:|------|:-----:|:----------------|
| 1 | Diego Wanderosck Lisboa | E-mail (.msg) | Destinatário da aprovação de negócio |
| 2 | Patricia Gassenferth Veloso Barreira Milet | E-mail (.msg) | CC na aprovação de negócio |
| 3 | Cândida Pacheco da Cunha Neta | E-mail (.msg) | CC na aprovação de negócio |
| 4 | Celso Pereira Dias Neto | E-mail (.eml) | CC na aprovação UAT |
| 5 | Felipe Povoa | Briefing PPTX | Líder do Produto (área solicitante) |

> **Total de atores da iniciativa:** 35 (DevOps) + 5 (documentos) = **40 identidades únicas** envolvidas.

### 15.8. Observações Cruzadas entre Documentos e WIs

| # | Observação | Fontes |
|:-:|-----------|--------|
| 1 | O Caderno de Testes é um documento de **2022** (v0.1, 21/06/2022) reutilizado 3 anos depois (v0.2, 21/10/2025). Padrão de reúso documental. | Caderno de Testes DOCX |
| 2 | Paulo Ricardo Castellanos Souza acumula os papéis de Gerente de Projetos E Líder Técnico na Especificação Funcional — uma única pessoa em dois papéis. | Especificação Funcional DOCX |
| 3 | A Especificação Funcional define apenas **3 requisitos funcionais** e **1 regra de negócio** para toda a iniciativa. Contrasta com os 26 WIs e 217 problemas. | Especificação Funcional DOCX vs. WIs |
| 4 | O fluxo alternativo do caso de uso C01 ("Erro na postagem do OMS → recuperar senha no APP TIM") é exatamente o cenário AS-IS que a iniciativa busca eliminar — sugerindo que o fallback persiste. | Especificação Funcional DOCX |
| 5 | A URL de teste FQA (`oamqa.internal.timbrasil.com.br`) revela que o stack subjacente é Oracle Access Management (OAM) com OAuth 2.0. O Bug #1193756 (falha OAuth OAM redirect loop) está diretamente relacionado a esse componente. | Caderno de Testes DOCX vs. Bug #1193756 |
| 6 | Os 3 cenários do template XLSM (CY0001–CY0003) correspondem exatamente aos 3 Test Cases criados no DevOps (TC #1171260–#1171262). A rastreabilidade template→DevOps está intacta. | XLSM vs. TCs |
| 7 | O e-mail de aprovação UAT agrupa TR #1164264 (nossa iniciativa) sob o guarda-chuva de TR #1121243 (outra iniciativa: "Criação de Canal Móvel APP TIM"). A aprovação formal de testes é cross-initiative. | E-mail EML |
| 8 | O e-mail de aprovação de negócio (17/10/2025) foi enviado para 8 destinatários + 1 lista de distribuição (DL_CRO_GONEGOCIO), dos quais apenas 4 aparecem como atores nos WIs do DevOps. Parte significativa da governança ocorre fora do DevOps. | E-mails .msg vs. WIs |
| 9 | O Briefing PPTX e a Jornada PPTX são os mesmos 2 arquivos registrados nos WIs de Attachment (#1113129 e #1113130). Os tamanhos conferem: 2,35 MB ≈ 2,24 MB (Briefing) e 1,05 MB = 1,05 MB (Jornada). | PPTXs vs. Attachments |
| 10 | O campo "Seção: Integrações" no Briefing diz "A ser definido com TI" e a Especificação Funcional não detalha a integração Intelsat→OAM (apenas referencia os diagramas). O Caderno de Testes FQA é o único documento que revela o fluxo técnico completo (OAuth consent → Access Code → Token). | Briefing + Spec + Caderno |

---

*Análise produzida a partir de 26 work items (JSONs de campos, revisões e updates), sem deduções ou suposições. Todos os dados são observáveis nos registros do Azure DevOps.*
