# Análise de Ciclo de Vida — Feature #1183520

## 1. Ficha Técnica

| Campo | Valor |
|:------|:------|
| **ID** | 1183520 |
| **Tipo** | Feature |
| **Título** | Rollout e Pós Rollout |
| **Projeto** | Projeto_Service_Creation |
| **Area Path** | Projeto_Service_Creation\Waterfall |
| **Iteration Path** | Projeto_Service_Creation\Waterfall |
| **State** | New |
| **Reason** | New |
| **Board Column** | New |
| **Assigned To** | Ana Maria Lopes Moreira |
| **Created By** | Ana Maria Lopes Moreira |
| **Created Date** | 2025-11-10 |
| **Changed By** | Ana Maria Lopes Moreira |
| **Changed Date** | 2026-03-23 |
| **State Change Date** | 2025-11-10 (nunca mudou) |
| **Priority** | — (não definida) |
| **Value Area** | Business |
| **Código Demanda** | **251070811** |
| **Tipo Feature** | Funcional |
| **StackRank** | 1999992162 |
| **Comment Count** | 0 |
| **Revisões** | 4 |
| **Updates** | 4 |
| **Description** | — (vazia) |
| **INFORMATIVO** | Link para Wiki Catálogo de Interfaces e Sistemas (página "EPIC") |
| **Parent** | #1078031 (Epic — Melhorias Resgate Senha inFlight) |

---

## 2. Relações

| Tipo | WI | Nome/Observação | Projeto |
|:-----|:---|:-----------------|:--------|
| **Parent** | #1078031 | Epic — 251078031 - Melhorias Resgate Senha inFlight | Portfolio Tim TI |

**Uma única relação.** Nenhum filho, nenhum Related, nenhum link com Test Request, Entrega, Bug ou qualquer outro WI. Feature completamente isolada — é apenas um nó pendurado no Epic.

---

## 3. Cronologia de Estados

| # | Estado | Entrada | Saída | Duração |
|:-:|:-------|:--------|:------|:-------:|
| 1 | New | 2025-11-10 | — (atual) | **155+ dias** (até 2026-04-13) |

**Zero transições de estado.** A Feature foi criada em "New" e permanece em "New" há mais de 5 meses. Nenhum trabalho foi iniciado.

---

## 4. Cronologia Detalhada de Revisões

| Rev | Data | Ator | Ação |
|:---:|:----:|:-----|:-----|
| 1 | 2025-11-10 | Ana Maria Lopes Moreira | Criação. Título: "Rollout e Pós Rollout". Parent: #1078031. CodigoDemanda: 251070811 |
| 2 | 2025-11-17 | Joanna Maria Haslwanter | StackRank definido (1999997418) |
| 3 | 2026-02-05 | Tamiris Leandro Martins Das Neves | StackRank ajustado (→ 1999993466) |
| 4 | 2026-03-23 | Ana Maria Lopes Moreira | StackRank ajustado (→ 1999992162) |

As 4 revisões são exclusivamente: criação (1) + StackRank re-classificação (3). Nenhum campo funcional foi preenchido em nenhuma revisão. Nenhum comentário, nenhuma description, nenhum conteúdo.

---

## 5. Atores (3)

| # | Ator | Papel Observado | Revs |
|:-:|:-----|:----------------|:----:|
| 1 | Ana Maria Lopes Moreira | Criadora, re-ranking | 1, 4 |
| 2 | Joanna Maria Haslwanter | StackRank | 2 |
| 3 | Tamiris Leandro Martins Das Neves | StackRank | 3 |

**Dois atores novos** na iniciativa (Joanna e Tamiris), que não participam de nenhum outro WI desta árvore. Ambos fizeram apenas re-ranking.

---

## 6. Problemas Identificados

### P188 — Código de Demanda divergente do Epic pai
**Severidade:** Alta | **Categoria:** Integridade referencial

| WI | Código Demanda |
|:---|:---------------|
| Epic #1078031 | **251078031** |
| Feature #1113005 | 251078031 |
| Feature #1113105 | 251078031 |
| **Feature #1183520** | **251070811** |

A Feature usa código de demanda `251070811` — diferente do código `251078031` compartilhado por todos os outros WIs da iniciativa. Isso indica que **esta Feature pertence a outra demanda** e foi vinculada ao Epic #1078031 por engano, ou que é uma Feature compartilhada entre demandas sem que isso esteja documentado.

---

### P189 — Feature sem description, sem acceptance criteria, sem conteúdo
**Severidade:** Alta | **Categoria:** Completude

Em 4 revisões e 155+ dias de existência, a Feature nunca recebeu:
- Description
- Acceptance criteria
- Qualquer campo funcional além de título e StackRank

O título "Rollout e Pós Rollout" é genérico e não descreve o que será feito. Nenhum participante da iniciativa adicionou contexto à Feature.

---

### P190 — Feature em "New" enquanto Epic pai está "Resolved"
**Severidade:** Alta | **Categoria:** Inconsistência de estados

| WI | State | State Change Date |
|:---|:------|:------------------|
| Iniciativa #1085522 | Closed | 2025-12-05 |
| Epic #1078031 | Resolved | 2025-12-04 |
| **Feature #1183520** | **New** | **2025-11-10** |

A Iniciativa está Closed, o Epic está Resolved, mas esta Feature filha permanece em "New". O Epic foi resolvido em 2025-12-04 sem que esta Feature fosse concluída ou cancelada. Nenhuma ação foi tomada no WI — ele foi simplesmente ignorado na resolução do Epic.

---

### P191 — 3 revisões exclusivamente para StackRank (overhead puro)
**Severidade:** Média | **Categoria:** Overhead operacional

Das 4 revisões, 3 (revs 2–4) alteraram exclusivamente o campo StackRank:
- Rev 2: `null → 1999997418` (Joanna, 2025-11-17)
- Rev 3: `1999997418 → 1999993466` (Tamiris, 2026-02-05)
- Rev 4: `1999993466 → 1999992162` (Ana Maria, 2026-03-23)

Cada re-ranking gera um update completo com snapshot de todos os campos. 3 atores, 3 revisões, 3 entradas de auditoria — para alterar um número de priorização relativa de uma Feature que nunca saiu de "New" e não tem conteúdo.

---

### P192 — Feature criada 97 dias após o Epic, ativa 134 dias após Epic Resolved
**Severidade:** Média | **Categoria:** Ciclo de vida anômalo

| Marco | Data | Referência |
|:------|:----:|:-----------|
| Epic criado | 2025-08-05 | — |
| Feature criada | 2025-11-10 | +97 dias |
| Epic Resolved | 2025-12-04 | +24 dias após Feature criada |
| Última revisão da Feature | 2026-03-23 | **+109 dias após Epic Resolved** |
| Hoje (data da análise) | 2026-04-13 | **+130 dias após Epic Resolved** |

A Feature foi criada quando o Epic já estava em fase "Em Desenvolvimento" (rev 41, 2025-10-27). O Epic foi resolvido 24 dias depois, mas a Feature continua recebendo ajustes de StackRank 4+ meses após a resolução do pai. Nenhum processo a "limpa" do backlog.

---

### P193 — 2 atores exclusivos desta Feature, ausentes do restante da iniciativa
**Severidade:** Baixa | **Categoria:** Governança de acesso

Joanna Maria Haslwanter e Tamiris Leandro Martins Das Neves não aparecem em nenhum outro WI da iniciativa. Ambas alteraram apenas StackRank — possivelmente via reordenação de backlog board, sem consciência de que estão operando nesta iniciativa específica. Evidência de que a Feature está em um backlog genérico misturado com outras demandas.

---

### P194 — Link INFORMATIVO para Wiki genérica, não para conteúdo da demanda
**Severidade:** Baixa | **Categoria:** Qualidade da informação

O campo `Custom.INFORMATIVO` contém link para a Wiki de Catálogo de Interfaces e Sistemas (página "EPIC") — uma página genérica de referência, não documentação específica desta Feature ou da demanda 251070811. O link não agrega informação ao WI.

---

## 7. Árvore Hierárquica (revisada — final)

```
Iniciativa #1085522 (Closed) — Portfolio Tim TI
├─ MV VAS #1117156 (Aprovação Financeira) — R$ 11.790,00
├─ MV FQA #1117168 (Resolved) — R$ 2.000,89
└─ Epic #1078031 (Resolved) — R$ 13.790,89
   ├─ Feature #1113005 (New) — Alteração Fraseologia e Botão [DM: 251078031]
   │  └─ User Story #1113040 (Refinada)
   │     └─ IT Task #1136722 (Concluída)
   ├─ Feature #1113105 (Closed) — Integração / escopo negativo [DM: 251078031]
   │  └─ User Story #1113109 (Concluída — escopo negativo)
   ├─ Feature #1183520 (New) — Rollout e Pós Rollout [DM: 251070811 ⚠️] ← ESTE WI
   ├─ Documents Repository #1113128 (New)
   │  ├─ Attachment #1113129 (New) — Briefing de Produto
   │  └─ Attachment #1113130 (New) — Jornada inFlight
   │
   ├─ [Related] TR #1164264 → TC #1171260, TC #1171261, TC #1171262
   ├─ [Related] MV VAS #1117156
   ├─ [Related] MV FQA #1117168
   │
   └─ [pipeline de teste e entregas]
      ├─ Entrega #1178461 (Armazenada pelo SCM)
      ├─ Entrega #1188548 (Aprovada em FQA) → copiada de #1132619
      ├─ Entrega #1192780 (Aprovada em FQA) → copiada de #1188548
      ├─ Entrega #1195760 (Instalada em PROD) → fix Bug #1193756
      ├─ Entrega (template) #1132619 (Armazenada pelo SCM)
      ├─ Bug #1184452 (Closed) → Reteste #1199583
      └─ Bug #1193756 (Closed) → Reteste #1196133
```

---

## 8. Tabela Acumulada de Problemas

| WI | Tipo | Problemas | Qtd |
|:---|:-----|:----------|:---:|
| #1085522 | Iniciativa | P1–P14 | 14 |
| #1117156 | MV VAS | P15–P19 | 5 |
| #1117168 | MV FQA | P20–P25 | 6 |
| #1164264 | Test Request | P26–P34 | 9 |
| #1113005 | Feature (ativa) | P35–P39 | 5 |
| #1178461 | Entrega (feature) | P40–P46 | 7 |
| #1113040 | User Story | P47–P53 | 7 |
| #1136722 | IT Task | P54–P64 | 11 |
| #1078031 | Epic | P65–P70 | 6 |
| #1171260 | Test Case (CY0001) | P71–P78 | 8 |
| #1171261 | Test Case (CY0002) | P79–P83 | 5 |
| #1171262 | Test Case (CY0003) | P84–P91 | 8 |
| #1199583 | Reteste | P92–P99 | 8 |
| #1184452 | Bug (container) | P100–P109 | 10 |
| #1192780 | Entrega (bug) | P110–P119 | 10 |
| #1132619 | Entrega (template) | P120–P127 | 8 |
| #1188548 | Entrega (bug) | P128–P136 | 9 |
| #1113105 | Feature (escopo neg.) | P137–P144 | 8 |
| #1113130 | Attachment (Anexo II) | P145–P150, P152–P153 | 8 |
| #1113129 | Attachment (Anexo I) | P154–P159 | 6 |
| #1113128 | Documents Repository | P160–P165 | 6 |
| #1113109 | User Story (escopo neg.) | P179–P187 | 9 |
| **#1183520** | **Feature (orphan)** | **P188–P194** | **7** |
| **Total** | | **P1–P194 (P151 inval., P166–P178 reservados)** | **193** |

**Próximo P-number disponível: P195**

> **Nota:** P166–P178 estão reservados (gap). P151 foi invalidado (era artefato da exportação de JSONs). WIs analisados após este arquivo: Bug #1193756 (P195–P205), Reteste #1196133 (P206–P210), Entrega #1195760 (P211–P218) — total geral: 217 problemas válidos (P218 sendo o último).

### Resumo da descoberta

A Feature #1183520 é essencialmente um **WI fantasma**: sem conteúdo, sem filhos, sem transição de estado, com código de demanda de outra iniciativa, e ativa 130+ dias após o Epic pai ter sido resolvido. É o caso mais extremo de overhead identificado nesta análise — 3 atores manipulando StackRank de um contêiner vazio.