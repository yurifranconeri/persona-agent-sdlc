# Análise de Ciclo de Vida — Feature #1113005

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1113005 |
| **Tipo** | Feature |
| **Título** | Alteração da Fraseologia e Criação do Botão |
| **Projeto atual** | **Projeto_Service_Creation** (migrado de Portfolio Tim TI!) |
| **AreaPath atual** | Projeto_Service_Creation\Waterfall |
| **AreaPath original** | Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB |
| **Iteration original** | Portfolio Tim TI\Portfolio Tim\2025\Q3 |
| **CodigoDemanda** | 251078031 |
| **TipoFeature** | Funcional |
| **ValueArea** | Business |
| **Estado atual** | **New** (NUNCA mudou!) |
| **Criado** | 2025-09-05 20:25:38 |
| **Última alteração** | 2026-03-23 21:57:04 |
| **Revisões** | 6 |
| **Updates** | 8 |
| **Comentários** | 0 |

---

## 2. Hierarquia — A Peça Que Faltava

```
┌─────────────────────────────────────────────────────────────┐
│  Portfolio Tim TI                                           │
│                                                             │
│  Iniciativa #1085522 (Closed)                               │
│    ├── MV #1117156 — VAS (Aprovação Financeira, estagnada)  │
│    ├── MV #1117168 — FQA (Resolved)                         │
│    └── Epic #1078031 (Resolved)                             │
│          │                                                  │
│          └─── Feature #1113005 ◄ ESTE ──────────────────┐   │
│                (New — ZOMBIE — nunca mudou de estado)    │   │
└─────────────────────────────────────────────────────────┐│   │
                                                         ││   │
┌────────────────────────────────────────────────────────┐││   │
│  Projeto_Service_Creation                             ││←───┘
│                                                       ││ migrado
│  Feature #1113005 (New) ◄ vive aqui desde 2025-10-13  ││
│    ├── Test Request #1113040 (ORIGINAL — fonte da cópia)
│    └── IT Task #1136722                                │
│                                                        │
│  Test Request #1164264 (Closed — cópia de #1113040)    │
│    (Related: #1117168, #1078031)                       │
└────────────────────────────────────────────────────────┘
```

**Revelação:** A Feature #1113005 é a camada intermediária que conecta o Epic #1078031 ao trabalho executivo. Tanto o IT Task #1136722 quanto o TR original #1113040 são **filhos da Feature**, não do Epic diretamente. A Feature é o ponto de articulação — e está permanentemente em "New".

**Conexão #1113040:** O child #1113040 é o **Test Request original** do qual o TR #1164264 foi copiado ("Copied from #1113040"). Ou seja, já existia um TR para esta demanda antes de Paulo Ricardo criar a cópia em 2025-10-23.

---

## 3. Atores

| Ator | Papel | Ação |
|------|-------|------|
| **Ana Maria Lopes Moreira** (amlmoreira) | Criadora / AssignedTo | Criou a Feature, adicionou child #1113040, StackRank final |
| **Paulo Ricardo Castellanos Souza** (pcsouza) | Links | Adicionou child #1136722 (IT Task) |
| **Franco Kaufmann Gaspar Ferreira Junior** (fkgjunior) | Migração | **Moveu a Feature de projeto** (Portfolio Tim TI → Projeto_Service_Creation) |
| **Karyne Vianna Carmo Gallindo** (kgallindo) | StackRank | Re-priorização |
| **Joanna Maria Haslwanter** (jhaslwanter) | StackRank | Re-priorização |
| **Tamiris Leandro Martins Das Neves** (talmdneves) | StackRank | Re-priorização |

**6 atores** para um item que **nunca saiu de "New"** e não tem um único comentário.

---

## 4. Cronologia Completa

```
2025-09-05 20:25 ──── New (Ana Maria cria a Feature no Portfolio Tim TI)
       │                 Parent=#1078031 (Epic)
       │  5 min
2025-09-05 20:30 ──── Ana Maria adiciona child #1113040 (TR original)
       │
       │  [24 dias]
       │
2025-09-29 11:58 ──── Paulo Ricardo adiciona child #1136722 (IT Task)
       │
       │  [14 dias]
       │
2025-10-13 14:03 ──── ███ MIGRAÇÃO DE PROJETO ███ (Franco Kaufmann)
       │                 Portfolio Tim TI → Projeto_Service_Creation
       │                 Area: CRO\Marketing Consumer e SMB → Waterfall
       │                 Iteration: 2025\Q3 → Waterfall
       │
       │  [15 dias]
       │
2025-10-28 13:34 ──── StackRank=1999994766 (Karyne)
       │
       │  [20 dias]
       │
2025-11-17 14:10 ──── StackRank=1999989334 (Joanna)
       │
       │  [80 dias]
       │
2026-02-05 12:45 ──── StackRank=1999987450 (Tamiris)
       │
       │  [46 dias]
       │
2026-03-23 21:57 ──── StackRank=1999986786 (Ana Maria) ← ÚLTIMO REGISTRO
       │
       ▼  ESTADO: AINDA "New" — 7+ MESES SEM PROGRESSÃO
```

---

## 5. Lead Times

| Segmento | Duração |
|----------|---------|
| Tempo em estado "New" | **7+ meses** (2025-09-05 → 2026-04-13, ainda ativo) |
| Tempo sem qualquer alteração | 21 dias (último update: 2026-03-23) |
| Intervalo entre updates de StackRank | 15d → 20d → 80d → 46d (acelerando esquecimento) |

---

## 6. Problemas Identificados

### P35 — Feature eternamente em "New" enquanto o trabalho foi executado e concluído

- **Evidência:** A Feature está em "New" desde 2025-09-05. Enquanto isso:
  - Seu child IT Task #1136722: executado e concluído
  - Seu child TR #1113040: serviu de fonte para cópia do TR #1164264
  - O TR #1164264 (cópia): **Closed com sucesso** em 2025-11-24
  - O Epic pai #1078031: **Resolved** em 2025-12-04
  - A Iniciativa avó #1085522: **Closed**
- **Consequência:** O trabalho inteiro foi planejado, estimado, aprovado, executado e fechado — mas a Feature que deveria representar esse trabalho nunca saiu de "New". O item é um **zumbi hierárquico**.

### P36 — Migração cross-project sem mudança de estado

- **Evidência:** Franco Kaufmann moveu a Feature de "Portfolio Tim TI" para "Projeto_Service_Creation" em 2025-10-13. Nenhuma transição de estado acompanhou a migração.
- **Impacto:** A Feature mudou de contexto organizacional (de portfolio para Service Creation/Waterfall) sem qualquer reflexão no workflow. Queries no projeto original deixam de encontrá-la; queries no novo projeto a veem como "New" sem contexto.
- **Questão:** Por que uma Feature de portfolio foi migrada para o projeto de execução de testes (Projeto_Service_Creation)? Isso sugere confusão sobre onde o item "vive".

### P37 — 6 atores para 0 conteúdo

- **Evidência:** 6 pessoas distintas tocaram este work item. 0 comentários. 0 mudanças de estado. As únicas ações substantivas foram: criação (Ana Maria), links de hierarquia (Ana Maria + Paulo Ricardo) e migração de projeto (Franco). As outras 3 pessoas (Karyne, Joanna, Tamiris) contribuíram exclusivamente com StackRank.
- **Impacto:** 4 das 6 revisões (67%) são puro ajuste de priorização num item que nunca progrediu.

### P38 — Epic Resolved com Feature child em "New" — inconsistência hierárquica

- **Evidência:** Epic #1078031 foi Resolved em 2025-12-04. Feature #1113005, que é child do Epic, continua em "New" até hoje (2026-04-13).
- **Impacto:** Um Epic "Resolved" com uma Feature child em "New" significa que:
  - Ou a Feature é órfã e deveria ser fechada/cancelada
  - Ou o Epic foi fechado prematuramente
  - Ou o sistema não valida consistência hierárquica de estados
- **Conclusão:** O Azure DevOps **não impede** que um parent seja resolvido enquanto children estão em aberto. Não há gate de consistência.

### P39 — Feature é a ponte invisível entre portfolio e execução

- **Evidência:** A Feature é o **único item** que conecta hierarquicamente o Epic (#1078031, portfolio) aos itens de execução (IT Task #1136722 e TR #1113040). Sem ela, a rastreabilidade parent-child entre portfolio e execução se perde.
- **Porém:** A Feature nunca foi usada ativamente para gerenciar o trabalho. É um nó de passagem — existe para satisfazer a estrutura hierárquica (Epic→Feature→Task/TR) mas não agrega decisão, aprovação ou controle.
- **Impacto para a tese:** A Feature é evidência de **overhead estrutural** — uma camada de hierarquia imposta pelo modelo de dados que não é utilizada para tomada de decisão.

---

## 7. Overhead Consolidado — Feature #1113005

| Tipo de atividade | Revisões | % do total (6) |
|-------------------|:--------:|:---:|
| Criação + links | 1 | 17% |
| Migração de projeto | 1 | 17% |
| StackRank / priorização | 4 | **67%** |
| Transições de estado | 0 | **0%** |
| Conteúdo / decisão | 0 | **0%** |

---

## 8. Visão Consolidada — Pipeline (snapshot no momento desta análise)

> **Nota:** Esta tabela reflete os WIs conhecidos no momento da análise da Feature #1113005. A tabela acumulada final está em WorkItem-Feature-1183520.md §8.

| Camada | Item | Rev | Upd | Atores | Estado | Dias |
|--------|------|:---:|:---:|:------:|:------:|:----:|
| Portfolio | Iniciativa #1085522 | 43 | 46 | 10+ | Closed | 114 |
| Portfolio | Epic #1078031 | 43 | 51 | 8 | Resolved | 121 |
| **Execução** | **Feature #1113005** | **6** | **8** | **6** | **New (zumbi)** | **7+ meses** |
| Execução | User Story #1113040 | 27 | 31 | 7+ | Refinada | 186+ |
| Execução | IT Task #1136722 | 20 | — | 4 | Concluída | 66 |
| Estimativa | MV #1117156 (VAS) | 29 | 30 | 5 | Aprovação Fin. | 78+ |
| Estimativa | MV #1117168 (FQA) | 32 | 34 | 7 | Resolved | 44 |
| Execução | TR #1164264 (FQA) | 24 | 25 | 6+bot | Closed | 32 |
| Testes | TC #1171260 (CY0001) | 14 | 15 | 5 | Closed | 20 |
| Testes | TC #1171261 (CY0002) | 15 | 16 | 5 | Closed | 20 |
| Testes | TC #1171262 (CY0003) | 23 | 24 | 5 | Closed | 21 |
| Execução | Entrega #1178461 | 3 | 4 | 2+bot | Armazenada SCM | <1 |