## Análise do Work Item — Documents Repository #1113128 "Repositório de Documentos"

---

### 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID no Azure DevOps** | 1113128 |
| **Tipo de Work Item** | Documents Repository (tipo customizado) |
| **Título** | Repositório de Documentos |
| **Estado** | New (nunca transitou) |
| **Projeto** | Portfolio Tim TI → Projeto_Service_Creation |
| **Área** | CRO\Marketing Consumer e SMB → Waterfall |
| **Iteração** | 2025/Q3 → Waterfall |
| **Parent** | **#1078031 (Epic)** — filho direto do Epic |
| **Children** | #1113129 (Attachment - Anexo I), #1113130 (Attachment - Anexo II) |
| **Criado por** | Ana Maria Lopes Moreira |
| **Data de Criação** | 2025-09-05 21:27:43 |
| **Última Alteração** | 2026-03-23 21:57:04 (Ana Maria) |
| **Revisões** | 6 |
| **Updates** | 8 |
| **Comentários** | 0 |
| **Assigned To** | — (nunca atribuído) |
| **Descrição** | — (vazia) |
| **Kanban** | "New" (todos os boards, todo o ciclo) |

---

### 2. Relações

| Tipo | WI | Contexto |
|------|-----|----------|
| **Parent** | **#1078031** (Epic) | Filho direto do Epic — **mesmo nível hierárquico** das Features |
| **Child** | #1113129 (Attachment) | "Anexo I - Briefing de Produto" |
| **Child** | #1113130 (Attachment) | "Anexo II - Jornada inFlight" |

→ **Achado hierárquico crítico**: O Documents Repository é **irmão das Features** sob o Epic. O Epic #1078031 tem **3 filhos** (não 2 como identificado anteriormente):
1. Feature #1113005 (ativa)
2. Feature #1113105 (escopo negativo)
3. Documents Repository #1113128 (este WI)

→ **3º tipo customizado descoberto**: A hierarquia de documentos usa 3 tipos customizados: `Documents Repository` (contêiner) → `Attachment` (item) → `AttachedFile` (arquivo real). São **4 níveis de indireção** entre o Epic e os PPTXs.

---

### 3. Sessão de Criação — 44 segundos

Ana Maria criou toda a estrutura de documentos em **44 segundos**:

| Hora | WI | Ação |
|------|-----|------|
| 21:27:43 | #1113128 | Criação Documents Repository + Parent link para Epic |
| 21:28:05 | #1113129 | Child link adicionado (Anexo I criado — +22s) |
| 21:28:27 | #1113130 | Child link adicionado (Anexo II criado — +44s) |

→ A criação da estrutura completa foi instantânea. O trabalho real são os uploads dos PPTXs feitos nos minutos seguintes (a partir de #1113129 e #1113130).

---

### 4. Reconstituição Cronológica

| Data | Dias | Rev | Actor | Ação |
|------|:----:|:---:|-------|------|
| 2025-09-05 21:27:43 | 0 | 1 | Ana Maria | Criação + Parent #1078031 + Children #1113129/#1113130 |
| 2025-10-13 14:03:37 | +38 | 2 | Franco Kaufmann | **Migração cross-project**: Portfolio Tim TI → Projeto_Service_Creation |
| 2025-10-28 13:34:43 | +53 | 3 | Karyne Gallindo | StackRank |
| 2025-11-17 14:10:23 | +73 | 4 | Joanna Haslwanter | StackRank |
| — | — | — | — | **=== Iniciativa #1085522 Closed: 2025-12-04 ===** |
| 2026-02-05 12:45:48 | +153 | 5 | Tamiris Neves | StackRank (63 dias pós-fechamento) |
| 2026-03-23 21:57:04 | +200 | 6 | Ana Maria | StackRank (110 dias pós-fechamento) |

→ **Vida útil: 200 dias.** Trabalho real de Ana Maria: **~1 segundo** (criação do contêiner). Os 200 dias restantes são migração (1 rev) e StackRank (4 revs).

---

### 5. Atores

| # | Ator | Ação | Revisões |
|:-:|------|------|:--------:|
| 1 | **Ana Maria Lopes Moreira** | Criou + StackRank (110d pós-fechamento) | 1, 6 |
| 2 | **Franco Kaufmann** | Migração cross-project | 2 |
| 3 | **Karyne Vianna Carmo Gallindo** | StackRank | 3 |
| 4 | **Joanna Maria Haslwanter** | StackRank | 4 |
| 5 | **Tamiris Leandro Martins Das Neves** | StackRank | 5 |

→ **5 atores** para um contêiner vazio sem conteúdo próprio. 1 criou (trabalho real ~1s). Os outros 4 fizeram exclusivamente StackRank e migração.

---

### 6. Métricas de Overhead

| Métrica | Valor |
|---------|:-----:|
| Revisões totais | 6 |
| Transições de estado | **0** |
| Comentários | **0** |
| Atores envolvidos | **5** |
| Atores com ação substantiva | **1** (20%) |
| Revisões de StackRank | **4** (67% das revisões) |
| Revisões pós-fechamento | **2** (33% das revisões) |
| Alterações de conteúdo | **0** |
| Vida útil total | **200 dias** |
| Período de trabalho real | **~1 segundo** |

---

### 7. Overhead Consolidado: Cluster Documental (3 WIs)

| WI | Tipo | Rev | Updates | Atores | Conteúdo |
|----|------|:---:|:-------:|:------:|----------|
| #1113128 | Documents Repository | 6 | 8 | 5 | 0 campos, 0 anexos |
| #1113129 | Attachment (Anexo I) | 10 | 10 | 7 | 1 PPTX (2,24 MB) |
| #1113130 | Attachment (Anexo II) | 12 | 15 | 8 | 1 PPTX (1,05 MB) |
| **Total** | **3 WIs** | **28** | **33** | **8 únicos** | **2 PPTXs** |

→ **28 revisões, 33 updates e 8 pessoas para armazenar 2 PowerPoints.** Os PPTXs poderiam ser anexados diretamente ao Epic #1078031 — 0 WIs adicionais, 0 revisões de overhead.

---

### 8. Problemas Identificados

#### P160 — Epic tem 3 filhos (não 2): Documents Repository é irmão das Features

A análise do Epic #1078031 identificou **2 Features filhas**. Na realidade, o Epic tem **3 filhos**: 2 Features + 1 Documents Repository. O Documents Repository (tipo contêiner de documentos) ocupa o mesmo nível hierárquico que Features na árvore do Epic. Para qualquer query de "filhos do Epic", o Documents Repository aparece ao lado das Features — misturando itens de trabalho (Features) com itens de infraestrutura (contêiner de documentos). Isto distorce métricas como "% de Features concluídas do Epic" (2/3 vs 2/2).

#### P161 — 4 níveis de indireção para armazenar 1 arquivo

A cadeia entre o Epic e o PPTX do briefing é:
```
Epic #1078031 → Documents Repository #1113128 → Attachment #1113129 → AttachedFile (PPTX)
```
O Azure DevOps permite anexar arquivos diretamente ao Epic (1 nível). A organização criou 3 WIs intermediários com tipos customizados, gerando **28 revisões de overhead** para funcionalidade nativa da ferramenta.

#### P162 — Documents Repository: WI sem função executável

O "Documents Repository" não tem descrição, não tem campos customizados, não transita de estado, não é atribuído a ninguém, não recebe comentários. Sua **única função** é servir de Parent para os Attachments. O tipo poderia ser substituído por uma tag, um campo "Tipo de Documento", ou simplesmente pela funcionalidade nativa de attachments. Em 200 dias de existência, o WI consumiu 6 revisões (5 de overhead) sem produzir nenhuma informação.

#### P163 — StackRank em contêiner hierárquico vazio (4 de 6 revisões)

4 das 6 revisões (67%) são ajustes de StackRank — o WI é repriorizado no board como se fosse um item de backlog. Um "Repositório de Documentos" não tem prioridade funcional — é infraestrutura, não trabalho entregável. O board trata todos os tipos de WI igualmente, sem distinguir contêineres de itens executáveis, gerando overhead multiplicativo.

#### P164 — 2 revisões 63-110 dias após fechamento da Iniciativa

A Iniciativa foi fechada em 2025-12-04. O Documents Repository recebeu:
- Rev 5 (2026-02-05): Tamiris, 63 dias pós-fechamento
- Rev 6 (2026-03-23): Ana Maria, **110 dias pós-fechamento** — a revisão mais tardia de todos os WIs da iniciativa

Ana Maria (a criadora original do WI) reprioriza seu próprio contêiner de documentos mais de 3 meses após o fechamento da demanda. Nenhuma automação impede a ação.

#### P165 — 28 revisões × 3 WIs × 8 atores para 2 PPTXs: overhead estrutural multiplicativo

O cluster documental ilustra o efeito multiplicador do overhead: cada ação no board (StackRank, migração) se propaga para **todos os WIs do cluster**. Franco migrou 3 WIs em vez de 1. Cada repriorização gera revisão em 3 WIs. O custo operacional escala linearmente com a quantidade de WIs desnecessários. Num cenário com funcionalidade nativa (attachments direto no Epic), o overhead seria **exatamente 0**.

---

### 9. Hierarquia Completa Atualizada

```
Iniciativa #1085522 (Closed) ─── Portfolio Tim TI
├─ MV VAS #1117156 (Aprovação Financeira)
├─ MV FQA #1117168 (Resolved)
└─ Epic #1078031 (Resolved)
   ├─ Feature #1113005 (New — ativa)
   │  └─ User Story #1113040 (Refinada)
   │     └─ IT Task #1136722 (Concluída)
   │
   ├─ Feature #1113105 (Closed — escopo negativo)
   │  └─ User Story #1113109 (Concluída — escopo negativo)
   │
   └─ Documents Repository #1113128 (New) ◄━━ ESTE WI
      ├─ Attachment #1113129 (New) — "Anexo I - Briefing de Produto"
      └─ Attachment #1113130 (New) — "Anexo II - Jornada inFlight"
```

---

### 10. Tabela acumulada de problemas

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
| P137-P144 | Feature #1113105 (escopo negativo) | 8 |
| P145-P150, P152-P153 | Attachment #1113130 (Anexo II) | 8 |
| P154-P159 | Attachment #1113129 (Anexo I) | 6 |
| **P160-P165** | **Documents Repository #1113128** | **6** |
| **Total** | **21 WIs analisados** | **164 problemas** |