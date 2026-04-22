# Análise do Work Item: Feature #1113105

---

## 1. Identificação e Contexto

| Campo | Valor |
|-------|-------|
| **ID** | 1113105 |
| **Tipo** | Feature |
| **Projeto (inicial)** | **Portfolio Tim TI** → CRO → Marketing Consumer e SMB |
| **Projeto (final)** | **Projeto_Service_Creation** → Waterfall |
| **Título final** | Integração com a Intelsat *Escopo Negativo* |
| **Estado final** | **Closed** (Reason: "Acceptance tests pass") |
| **Criado** | 2025-09-05 21:05:41 |
| **Criado por** | Ana Maria Lopes Moreira |
| **Assigned** | Ana Maria Lopes Moreira |
| **Parent** | **#1078031** (Epic — o mesmo Epic da nossa iniciativa!) |
| **Child** | #1113109 (User Story) |
| **CodigoDemanda** | 251078031 |
| **TipoFeature** | Funcional |
| **Iteration** | Q3 2025 → Waterfall |
| **Rev final** | 6 |
| **Updates** | 7 |

> **NOTA ESTRUTURAL:** Esta é a **2ª Feature filha** do Epic #1078031 "Melhorias Resgate Senha inFlight" — irmã da Feature #1113005. Enquanto #1113005 seguiu o pipeline SDLC (IT Task, Test Request, TCs, Bug, Entregas), esta Feature foi **finalizada como escopo negativo** — deliberadamente excluída do escopo da demanda e fechada (Closed) sem desenvolvimento.

---

## 2. Campos Específicos

| Campo | Valor |
|-------|-------|
| **ValueArea** | Business |
| **INFORMATIVO** | Link para Wiki Catalogo Interfaces e Sistemas (página EPIC) |
| **TipoFeature** | Funcional |
| **Descrição** | *(vazia — nenhuma Description)* |
| **BoardColumn** | Closed |

→ **Zero campos de negócio preenchidos** além do título e tipo. Nenhuma descrição, nenhum critério de aceitação, nenhuma justificativa para a exclusão de escopo.

---

## 3. Relações

| Tipo | Destino | Observação |
|------|---------|------------|
| **Parent** | #1078031 (Epic) | Mesmo Epic da Feature #1113005 |
| **Child** | #1113109 (User Story) | User Story "Integração com a Intelsat" |

→ **2 relações** apenas. A Feature tem uma User Story filha #1113109 no estado "Concluída" (análise em WorkItem-UserStory-1113109.md) — também marcada como escopo negativo via título.

---

## 4. Transições de Estado

```
New → Closed
```

| # | De | Para | Timestamp | Ator | Reason |
|---|-----|------|-----------|------|--------|
| T1 | New | **Closed** | 2025-10-08 14:57:31 | Ana Maria Lopes Moreira | **"Acceptance tests pass"** |

**1 transição. Direta de New para Closed, sem passar por nenhum estado intermediário.** E a razão registrada é "Acceptance tests pass" — para uma feature **excluída do escopo** que nunca teve desenvolvimento, testes, nem código.

---

## 5. Linha do Tempo (6 revisões, 7 updates)

| Rev | Timestamp | Δt | Autor | Ação |
|-----|-----------|-----|-------|------|
| 1 | 2025-09-05 21:05:41 | — | Ana Maria Lopes Moreira | Criação. Título: "Integração com a Intelsat". Estado: New. Parent=#1078031. Child=#1113109 adicionado 40s depois |
| 2 | 2025-09-12 19:39:36 | +7 dias | Ana Maria Lopes Moreira | Título → "Integração com a Intelsat ***CANCELAR***" |
| 3 | 2025-09-12 19:40:42 | +66s | Ana Maria Lopes Moreira | Título → "Integração com a Intelsat ***ESCOPO NEGATIVO***" |
| 4 | 2025-10-08 14:57:31 | +26 dias | Ana Maria Lopes Moreira | State: New → **Closed**. Reason: "Acceptance tests pass". ActivatedDate = ResolvedDate = ClosedDate = mesmo timestamp |
| 5 | 2025-10-08 14:57:50 | +19s | Ana Maria Lopes Moreira | Título → "Integração com a Intelsat ***Escopo Negativo***" (apenas casing) |
| 6 | 2025-10-13 14:03:18 | +5 dias | **Franco Kaufmann Gaspar Ferreira Junior** | Moveu de **Portfolio Tim TI** para **Projeto_Service_Creation** (mudança de projeto, área e iteração) |

**Três fases:**
- **Criação** (05/09): Feature criada como item funcional do Epic
- **Decisão de escopo negativo via título** (12/09): Duas renomeações em 66 segundos — primeiro "*CANCELAR*", depois "*ESCOPO NEGATIVO*"
- **Fechamento formal** (08/10): Closed com razão incorreta, 26 dias após a decisão de escopo negativo
- **Reorganização** (13/10): Movida cross-project por Franco

---

## 6. Atores

| Ator | Tipo | Papel | Revisões |
|------|------|-------|----------|
| **Ana Maria Lopes Moreira** | Humano (PO/Gestão) | Criou, definiu escopo negativo, fechou | 1-5 |
| **Franco Kaufmann Gaspar Ferreira Junior** | Humano | Moveu entre projetos | 6 |

→ **2 atores ativos** (ambos humanos). Total: 2 identidades.

---

## 7. Evolução do Título — Comunicação por Renomeação

```
"Integração com a Intelsat"          → (05/09)
"Integração com a Intelsat *CANCELAR*"         → (12/09, 19:39)
"Integração com a Intelsat *ESCOPO NEGATIVO*"  → (12/09, 19:40 — 66s depois)
"Integração com a Intelsat *Escopo Negativo*"  → (08/10 — case fix)
```

Ana Maria refinou a marcação em **66 segundos**: primeiro "CANCELAR", depois "ESCOPO NEGATIVO". A diferença semântica é relevante: "cancelar" sugere abandono; "escopo negativo" é uma decisão de negócio deliberada — a funcionalidade foi avaliada e explicitamente excluída do escopo da demanda. Porém, a justificativa dessa decisão não foi registrada formalmente — apenas a decisão, via título.

---

## 8. Problemas Identificados

### P137 — Feature de escopo negativo fechada com razão "Acceptance tests pass"

A Feature foi deliberadamente excluída do escopo (título marcado "*Escopo Negativo*"), mas foi fechada com a razão **"Acceptance tests pass"**. Nenhum teste de aceitação existiu, nenhum desenvolvimento foi feito, nenhum critério de aceitação foi definido. A razão de fechamento é semanticamente incorreta. O processo provavelmente não oferece uma razão de fechamento para "escopo negativo", forçando a PO a usar a única razão disponível. O registro histórico afirma falsamente que esta feature passou em testes de aceitação.

### P138 — Ausência total de descrição e justificativa da decisão de escopo negativo

A Feature não tem `System.Description`. Não há nenhum comentário, nenhum campo explicando **por que** a "Integração com a Intelsat" foi excluída do escopo. Para auditoria de portfólio, alguém que consulte o Epic #1078031 verá duas Features — uma executada (#1113005) e uma finalizada como escopo negativo (#1113105) — mas não encontrará **nenhuma** justificativa documentada para a decisão. A comunicação da decisão foi feita exclusivamente via título.

### P139 — Decisão de escopo comunicada por manipulação de título (pattern organizacional)

O título foi usado como **canal de comunicação** para sinalizar a decisão de escopo negativo: "*CANCELAR*" → "*ESCOPO NEGATIVO*". Isto sugere que o Azure DevOps não possui (ou a equipe não conhece) um mecanismo formal para marcar itens como excluídos do escopo. O pattern é análogo ao Bug #1184452 "Copy - Copy" (P100) — o título carrega metadados informais porque os campos formais não atendem às necessidades.

### P140 — ActivatedDate = ResolvedDate = ClosedDate: tripla simultaneidade

Os três marcos temporais (ativação, resolução, fechamento) foram registrados no **mesmo timestamp** (2025-10-08 14:57:31). A Feature nunca foi "ativa" nem "resolvida" — foi criada em New e fechada diretamente. O Azure DevOps registrou as 3 datas porque a transição New→Closed dispara todos os marcos automaticamente, criando um registro que sugere falsamente que houve um ciclo de vida completo.

### P141 — User Story órfã: #1113109 permanece como filha de Feature de escopo negativo

A Feature tem um Child (#1113109 - User Story). Se a Feature foi finalizada como escopo negativo, a User Story filha está em que estado? Não há evidência de que #1113109 foi também marcada como escopo negativo ou fechada. A hierarquia mantém um item potencialmente ativo ligado a uma Feature encerrada.

### P142 — Migração cross-project post-mortem (Portfolio Tim TI → Projeto_Service_Creation)

Franco moveu a Feature de Portfolio Tim TI para Projeto_Service_Creation 5 dias após o fechamento. Uma Feature **já fechada como escopo negativo** foi reorganizada entre projetos. Isto sugere uma reorganização em massa (possivelmente do Epic inteiro e suas features) sem considerar o estado individual de cada item. A Feature #1113005 (ativa) também vive em Projeto_Service_Creation, então provavelmente ambas foram movidas juntas.

### P143 — 26 dias entre decisão de escopo negativo e fechamento formal

A decisão de escopo negativo foi tomada em **12/09** (titulo → "*ESCOPO NEGATIVO*"). O fechamento formal só ocorreu em **08/10** — 26 dias depois. Durante esse período, o WI ficou no estado "New" com título sinalizando a decisão. Qualquer dashboard ou board mostraria esta Feature como "New" (em backlog), não como encerrada. A comunicação via título é **invisível** para ferramentas de gestão.

### P144 — Epic #1078031 com 50% de escopo negativo: impacto na avaliação de complexidade

O Epic tem 2 Features: #1113005 (executada) e #1113105 (escopo negativo). Isto significa que **50% do escopo planejado foi excluído**. A avaliação de complexidade da Iniciativa (#1085522), as Macro Valorações (#1117156 e #1117168) e os pontos de função — todos foram calculados considerando o Epic completo ou apenas a Feature remanescente? A ausência de documentação sobre a decisão de escopo negativo impede verificar se o cálculo financeiro (R$13.790,89) reflete o escopo real executado ou o escopo originalmente planejado.

---

## 9. Métricas Consolidadas do Work Item

| Métrica | Valor |
|---------|-------|
| Revisões | 6 |
| Updates | 7 |
| Transições de estado | **1** (New → Closed) |
| Tempo de vida (criação → fechamento) | **33 dias** |
| Tempo de decisão escopo negativo → fechamento | **26 dias** (dormência administrativa) |
| Atores ativos | 2 |
| Descrição | **Vazia** |
| Justificativa documentada | **Nenhuma** |
| Reason de fechamento | **Semanticamente incorreta** ("Acceptance tests pass" para escopo negativo) |

---

## 10. Impacto na Estrutura do Epic #1078031

```
Epic #1078031 — Melhorias Resgate Senha inFlight
  ├─ Feature #1113005 — Alteração da Fraseologia e Criação do Botão (ATIVA)
  │    ├─ User Story #1113040
  │    ├─ IT Task #1136722
  │    ├─ Test Request #1164264
  │    ├─ Test Cases ×3
  │    ├─ Bug #1184452
  │    ├─ Reteste #1199583
  │    └─ Entregas ×3 (+ template)
  │
  └─ Feature #1113105 — Integração com a Intelsat *Escopo Negativo* (CLOSED)
       └─ User Story #1113109 (Concluída — escopo negativo)
```

O Epic originalmente contemplava **duas vertentes funcionais**: fraseologia/botão de reset de senha E integração com Intelsat. A integração com Intelsat foi deliberadamente excluída do escopo (escopo negativo), porém sem justificativa documentada. Toda a análise da iniciativa até agora referiu-se apenas à Feature #1113005, o que é correto — mas a existência de uma Feature de escopo negativo sem justificativa registrada é um achado de processo significativo.

---

## 11. Problemas acumulados na iniciativa

| Faixa | WI | Contagem |
|-------|-----|----------|
| P1-P14 | Iniciativa #1085522 | 14 |
| P15-P19 | MV VAS #1117156 | 5 |
| P20-P25 | MV FQA #1117168 | 6 |
| P26-P34 | TR #1164264 | 9 |
| P35-P39 | Feature #1113005 | 5 |
| P40-P46 | Entrega #1178461 | 7 |
| P47-P53 | User Story #1113040 | 7 |
| P54-P64 | IT Task #1136722 | 11 |
| P65-P70 | Epic #1078031 | 6 |
| P71-P78 | TC CY0001 #1171260 | 8 |
| P79-P83 | TC CY0002 #1171261 | 5 |
| P84-P91 | TC CY0003 #1171262 | 8 |
| P92-P99 | Reteste #1199583 | 8 |
| P100-P109 | Bug #1184452 | 10 |
| P110-P119 | Entrega Bug #1192780 | 10 |
| P120-P127 | Entrega Template #1132619 | 8 |
| P128-P136 | Entrega Bug #1188548 | 9 |
| **P137-P144** | **Feature #1113105 (escopo negativo)** | **8** |
| **Total** | | **144 problemas** |