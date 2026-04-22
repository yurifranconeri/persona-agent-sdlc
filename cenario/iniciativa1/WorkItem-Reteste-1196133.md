# Análise de Ciclo de Vida — Reteste #1196133

---

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1196133 |
| **Tipo** | Reteste |
| **Título** | Reteste do Bug #1193756 |
| **Projeto** | Projeto_Service_Creation |
| **AreaPath** | Projeto_Service_Creation\Waterfall |
| **Estado final** | **Válido** (nasceu neste estado — terminal) |
| **Reason** | Moved to state Válido |
| **Criado** | 2025-11-19 18:27:53 |
| **Criado por** | **AzDevOpsServ_PRD** (automação — nenhum humano tocou este WI) |
| **ChangedBy** | AzDevOpsServ_PRD |
| **Parent** | Bug #1193756 |
| **Revisões** | 1 |
| **Updates** | 2 |
| **Comentários** | 0 |
| **Transições de estado** | **0** |

---

## 2. Campos Customizados — Métricas de Reteste

| Campo | Valor |
|-------|-------|
| **CodigoDemanda.TIMDM** | 251078031 |
| **CodigoFQA.TIMDM** | TR1164264 |
| **BugProject.TIMDM** | CANAIS DIGITAIS |
| **BugSubProject.TIMDM** | APP Meu TIM |
| **BugEnviroment.TIMDM** | IT / UAT |
| **BugVendor.TIMDM** | ENGINEERING |
| **Custom.VendorGroup** | Engineering - VAS |
| **Custom.KPIProdutividade** | FQA - Atos |
| **MotivoReteste.TIMDM** | ENTREGA DE KIT |
| **TipoReteste.TIMDM** | Reteste OK |
| **WorkItemOrigemReteste.TIMDM** | Bug |
| **IdOrigemReteste.TIMDM** | 1193756 |
| **QtdMinPerdidosReteste.TIMDM** | **120** (2 horas declaradas como "perdidas") |
| **QtdCenariosReteste.TIMDM** | **1** (1 cenário retestado) |
| **SistemaAreaReteste.TIMDM** | VAS |
| **CreatedByReteste.TIMDM** | Anderson Teixeira Abrantes |

---

## 3. Hierarquia e Relações

```
┌─────────────────────────────────────────────────────────────┐
│  PROJETO: Projeto_Service_Creation                          │
│                                                             │
│  Bug #1193756 (Parent)                                      │
│    └── Reteste #1196133 ◄ ESTE (Child)                      │
│                                                             │
│  Bug #1193756 ── TestedBy ── TC #1171262 (CY0003)           │
│                                                             │
│  Bug #1184452 (outro bug, mesma falha)                      │
│    └── Reteste #1199583 (Child — outro reteste, mesma falha)│
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

| # | Tipo de Relação | Destino | Nome |
|---|----------------|---------|------|
| 1 | System.LinkTypes.Hierarchy-Reverse | Bug #1193756 | Parent |

---

## 4. Atores

| # | Nome | E-mail | Papel |
|---|------|--------|-------|
| 1 | AzDevOpsServ_PRD | AzDevOpsServ_PRD_usr@timbrasil.com.br | CreatedBy, ChangedBy, AuthorizedAs (100% automação) |
| 2 | Anderson Teixeira Abrantes | aabrantes_atos@timbrasil.com.br | **CreatedByReteste** (referenciado — o humano que fez o reteste) |

> **0 atores humanos ativos**. O work item foi inteiramente criado e preenchido por automação. Anderson aparece apenas como campo referencial (quem fez o reteste na prática).

---

## 5. Cronologia (2 Updates, 1 Revisão — tudo no mesmo segundo)

| Upd | Rev | Timestamp (UTC) | Ator | Ação |
|:---:|:---:|:---------------:|:----:|------|
| 1 | 1 | 2025-11-19 18:27:53 | AzDevOpsServ_PRD | **Criação completa**. Estado: Válido. Todos os campos preenchidos atomicamente pela automação |
| 2 | 1 | 2025-11-19 18:27:53 | AzDevOpsServ_PRD | **Relação**: Parent → Bug #1193756 (mesma revisão, ~0 seg depois) |

**Ciclo total: 0 segundos.** O item nasceu completo no estado terminal.

> Criado **12 segundos** após o Bug #1193756 ser fechado (18:27:41 → 18:27:53). A automação é imediata — não há delay de batch.

---

## 6. Transições de Estado

```
(nenhuma)
```

Zero transições. O item foi criado diretamente no estado "Válido" — estado terminal do tipo Reteste. Padrão idêntico ao Reteste #1199583 e à Entrega #1178461.

---

## 7. Comparação com Reteste #1199583 — Dois retestes para a mesma falha

| Campo | Reteste #1196133 (este) | Reteste #1199583 |
|-------|:-----------------------:|:----------------:|
| **Parent** | Bug #1193756 | Bug #1184452 |
| **Criado** | 2025-11-19 18:27:53 | 2025-11-24 13:14:48 |
| **Δ Criação** | — | +5 dias depois |
| **QtdMinPerdidosReteste** | **120 min** | **120 min** |
| **QtdCenariosReteste** | **1** | **3** |
| **SistemaAreaReteste** | VAS | APP_MeuTim |
| **BugProject** | CANAIS DIGITAIS | VAS |
| **BugSubProject** | APP Meu TIM | VAS |
| **MotivoReteste** | ENTREGA DE KIT | ENTREGA DE KIT |
| **TipoReteste** | Reteste OK | Reteste OK |
| **BugVendor** | ENGINEERING | ENGINEERING |
| **VendorGroup** | Engineering - VAS | Engineering - VAS |
| **CodigoDemanda** | 251078031 | 251078031 |
| **CodigoFQA** | TR1164264 | TR1164264 |

> **Ambos os Reteste WIs referem-se à mesma falha do TC CY0003 (#1171262), ao mesmo vendor (ENGINEERING), e ao mesmo motivo (ENTREGA DE KIT).** A diferença é que cada um é filho de um bug diferente — #1193756 (bug real) e #1184452 (bug container).

---

## 8. Problemas Identificados

### P206 — 120 minutos contabilizados em DUPLICATA — mesmo reteste cobrado 2×

O Reteste #1196133 declara `QtdMinPerdidosReteste=120` (2h). O Reteste #1199583 também declara `QtdMinPerdidosReteste=120` (2h). Ambos referem-se à mesma falha (TC CY0003), ao mesmo vendor (ENGINEERING/VAS), e ao mesmo motivo (ENTREGA DE KIT). O reteste real aconteceu uma única vez em 2025-11-19.

**Total contabilizado: 240 minutos (4 horas).** Trabalho real: um único reteste de 1 cenário.

**Impacto**: O vendor ENGINEERING é penalizado com 4 horas de reteste quando houve apenas 1 evento de reteste. Se o custo de reteste é faturado ou usado para SLA contratual, há duplicação financeira. Métricas de "minutos perdidos" da iniciativa #1085522 estão infladas em 100%.

---

### P207 — Dois reteste WIs para a mesma falha — sem deduplicação

O processo gerou dois WIs de Reteste automaticamente: #1196133 (ao fechar Bug #1193756 em 2025-11-19) e #1199583 (ao fechar Bug #1184452 em 2025-11-24). A automação é disparada pelo fechamento de cada bug individualmente — não verifica se já existe um reteste para a mesma CodigoDemanda/CodigoFQA.

**Impacto**: A ausência de regra de deduplicação permite que múltiplos bugs para o mesmo defeito gerem múltiplos WIs de reteste. Cada bug é tratado como evento independente, quando na realidade Bug #1184452 e #1193756 cobrem a mesma falha (P200). Os problemas se compõem: duplicação de bugs (P200) → duplicação de retestes (P207) → duplicação de custos (P206).

---

### P208 — Dados divergentes entre os dois retestes — métricas inconsistentes

Os dois Reteste WIs para a mesma falha divergem em campos críticos:

| Campo | #1196133 | #1199583 | Inconsistência |
|-------|----------|----------|----------------|
| QtdCenariosReteste | **1** | **3** | Quantos cenários foram retestados? |
| SistemaAreaReteste | **VAS** | **APP_MeuTim** | Qual sistema foi afetado? |
| BugProject | **CANAIS DIGITAIS** | **VAS** | Qual projeto? |
| BugSubProject | **APP Meu TIM** | **VAS** | Qual subprojeto? |

Cada reteste herdou os campos de seu bug pai — e os dois bugs tinham classificações diferentes para o mesmo defeito.

**Impacto**: Relatórios por projeto/sistema produzem resultados diferentes dependendo de qual reteste é consultado. Se filtrado por BugProject="VAS", apenas o #1199583 aparece. Se por "CANAIS DIGITAIS", apenas o #1196133. A mesma falha aparece em silos diferentes.

---

### P209 — Reteste #1196133 referencia corretamente o Bug #1193756 — mas o #1199583 não

O Reteste #1196133 aponta para o Bug #1193756 via `IdOrigemReteste=1193756` e Parent=#1193756. Este é o bug correto — o bug real criado durante a falha do CY0003 em 2025-11-18 14:03. O Reteste #1199583, por outro lado, aponta para o Bug #1184452 (o bug container criado proativamente em 2025-11-11, antes dos testes).

**Impacto**: Dos dois retestes, este (#1196133) tem rastreabilidade correta: Reteste → Bug #1193756 → TC #1171262 (CY0003). O #1199583 aponta para o bug genérico que não tem link direto com o TC que falhou. Paradoxalmente, o reteste com rastreabilidade incorreta (#1199583) foi o que já havia sido analisado como o "reteste da iniciativa".

---

### P210 — Campo GUID opaco (Custom.59bfa7e3-...) sem nome legível

O campo `Custom.59bfa7e3-23eb-496f-9a9a-f4299caf5e79` contém o timestamp de criação (2025-11-19T18:27:53.483Z), com nome representado por GUID em vez de label funcional. Idêntico ao problema P99 do Reteste #1199583.

**Impacto**: Campo técnico sem semântica documentada. Dificulta auditoria fora do contexto da automação.

---

## 9. Métricas Consolidadas

| Métrica | Valor |
|---------|-------|
| **Revisões** | 1 |
| **Updates** | 2 |
| **Transições de estado** | 0 |
| **Ciclo total** | 0 segundos (nasceu terminal) |
| **Atores humanos** | 0 (100% automação) |
| **Relações** | 1 (Parent → Bug #1193756) |
| **Custo declarado reteste** | 120 min / 1 cenário |
| **Custo duplicado com Reteste #1199583** | 120 min (mesmo evento) |
| **Problemas** | P206–P210 (5) |

---

## 10. Conclusão Executiva

O Reteste #1196133 é o segundo WI de reteste gerado para a mesma falha do TC CY0003. O primeiro foi o Reteste #1199583 (filho do Bug #1184452), analisado anteriormente com os problemas P92-P99.

**Descoberta central**: a duplicação de bugs (P200) propagou-se para duplicação de retestes, resultando em **240 minutos de "tempo perdido" contabilizados ao vendor ENGINEERING por um único evento de reteste**. A cadeia causal é:

```
1 falha TC CY0003
  → 2 bugs (#1184452 + #1193756) — sem link entre si (P200)
    → 2 retestes (#1199583 + #1196133) — sem deduplicação (P207)
      → 240 min contabilizados — duplicação de custo (P206)
        → métricas divergentes entre si (P208)
```

Ironicamente, este reteste (#1196133) tem a rastreabilidade correta (Bug #1193756 → TC CY0003), enquanto o #1199583 aponta para o bug container errado. Mas ambos existem, ambos contabilizam 120 minutos, e a automação não detecta a duplicação.

---

## 11. Cadeia Completa de WIs para a Falha CY0003

| # | Tipo | ID | Criado | Fechado | Estado | Papel |
|:-:|------|----|--------|---------|:------:|-------|
| 1 | Bug (container) | #1184452 | 2025-11-11 | 2025-11-24 | Closed | Pré-fabricado antes dos testes |
| 2 | Bug (real) | #1193756 | 2025-11-18 | 2025-11-19 | Closed | Criado durante falha CY0003 |
| 3 | Reteste (real) | **#1196133** | 2025-11-19 | — | Válido | Filho do Bug real. Rastreabilidade correta |
| 4 | Reteste (container) | #1199583 | 2025-11-24 | — | Válido | Filho do Bug container. Rastreabilidade incorreta |
| 5 | Entrega | #1195760 | 2025-11-19 | — | ? | Kit de correção (Child do Bug #1193756) |

> **5 work items** para rastrear uma única falha de teste de um erro de configuração OAuth no ambiente QA. Custo processual total: 2 bugs + 2 retestes + 1 entrega = 5 WIs, 35 revisões, 38 updates, 14 transições de estado, e 240 minutos de reteste contabilizados.
