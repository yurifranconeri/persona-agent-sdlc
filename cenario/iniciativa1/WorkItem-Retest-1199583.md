# Análise de Ciclo de Vida — Reteste #1199583

---

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1199583 |
| **Tipo** | **Reteste** ← 6º tipo de work item na iniciativa |
| **Título** | Reteste do Bug #1184452 |
| **Projeto** | Projeto_Service_Creation |
| **AreaPath** | Projeto_Service_Creation\Waterfall |
| **Estado final** | **Válido** (nasceu neste estado — terminal) |
| **Reason** | Moved to state Válido |
| **Criado** | 2025-11-24 13:14:48 |
| **Criado por** | **AzDevOpsServ_PRD** (automação — nenhum humano tocou este WI) |
| **ChangedBy** | AzDevOpsServ_PRD |
| **Parent** | Bug #1184452 |
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
| **BugProject.TIMDM** | VAS |
| **BugSubProject.TIMDM** | VAS |
| **BugEnviroment.TIMDM** | IT / UAT |
| **BugVendor.TIMDM** | ENGINEERING |
| **Custom.VendorGroup** | Engineering - VAS |
| **Custom.KPIProdutividade** | FQA - Atos |
| **MotivoReteste.TIMDM** | ENTREGA DE KIT |
| **TipoReteste.TIMDM** | Reteste OK |
| **WorkItemOrigemReteste.TIMDM** | Bug |
| **IdOrigemReteste.TIMDM** | 1184452 |
| **QtdMinPerdidosReteste.TIMDM** | **120** (2 horas declaradas como "perdidas") |
| **QtdCenariosReteste.TIMDM** | **3** (3 cenários retestados) |
| **SistemaAreaReteste.TIMDM** | APP_MeuTim |
| **CreatedByReteste.TIMDM** | Anderson Teixeira Abrantes |

---

## 3. Hierarquia e Relações

```
┌─────────────────────────────────────────────────────────────┐
│  PROJETO: Projeto_Service_Creation                          │
│                                                             │
│  Bug #1184452 (Parent)                                      │
│    └── Reteste #1199583 ◄ ESTE (Child)                      │
│                                                             │
│  Bug #1184452 ── TestedBy ── TC #1171260, #1171261, #1171262│
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

| # | Tipo de Relação | Destino | Nome |
|---|----------------|---------|------|
| 1 | System.LinkTypes.Hierarchy-Reverse | Bug #1184452 | Parent |

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
| 1 | 1 | 2025-11-24 13:14:48 | AzDevOpsServ_PRD | **Criação completa**. Estado: Válido. Todos os campos preenchidos atomicamente pela automação |
| 2 | 1 | 2025-11-24 13:14:48 | AzDevOpsServ_PRD | **Relação**: Parent → Bug #1184452 (mesma revisão, ~0 seg depois) |

**Ciclo total: 0 segundos.** O item nasceu completo no estado terminal.

---

## 6. Transições de Estado

```
(nenhuma)
```

Zero transições. O item foi criado diretamente no estado "Válido" — que é o estado terminal do tipo Reteste. Padrão idêntico à Entrega #1178461 (que nasceu em "Armazenada pelo SCM").

---

## 7. Análise — O que é um "Reteste" neste processo?

O tipo "Reteste" é um **artefato de métricas/KPI**, não um instrumento de workflow. Ele existe para:

1. **Registrar o custo do reteste**: `QtdMinPerdidosReteste = 120` (2 horas "perdidas")
2. **Atribuir responsabilidade ao fornecedor**: `BugVendor = ENGINEERING`, `VendorGroup = Engineering - VAS`
3. **Contar cenários impactados**: `QtdCenariosReteste = 3`
4. **Classificar o resultado**: `TipoReteste = Reteste OK`
5. **Vincular ao bug de origem**: `IdOrigemReteste = 1184452`, Parent = #1184452

O campo "QtdMinPerdidosReteste = 120" é particularmente revelador: declara que o reteste dos 3 cenários custou 2 horas. Porém, os dados reais dos Test Cases mostram que o reteste efetivo do CY0003 (o único que falhou e foi retestado) durou **~34 segundos** de transições + ~20 minutos de gravação de vídeo. Os 120 minutos provavelmente incluem toda a análise do bug, reprodução, regravação de evidência e overhead administrativo — atribuídos como "custo do fornecedor ENGINEERING".

---

## 8. Cronologia cruzada — Reteste vs Test Cases vs Bug

| Data | Evento | WI |
|------|--------|-----|
| 2025-11-17 20:18 | CY0003 → Enviado para Usuário (1ª tentativa) | TC #1171262 |
| 2025-11-18 11:48 | CY0003 → rejeitado, volta para Em Andamento | TC #1171262 |
| 2025-11-18 14:03 | CY0003 → **Falhado** + Bug #1193756 vinculado | TC #1171262 |
| 2025-11-19 18:27-18:28 | CY0003 retestado (3 transições em 9 seg) | TC #1171262 |
| 2025-11-19 21:30 | CY0003 → Closed | TC #1171262 |
| 2025-11-24 13:14 | **Reteste #1199583 criado por automação** (5 dias depois) | **Reteste** |

> O Reteste WI foi criado **5 dias após** o reteste real ter sido concluído. É um registro retroativo puro.

---

## 9. Problemas Identificados

### P92 — 14º work item na iniciativa — novo tipo "Reteste"

O Reteste #1199583 introduz o **6º tipo de work item** na iniciativa (Iniciativa, Epic, Feature, User Story, IT Task, Macro Valoração, Test Request, Test Case, Entrega, Bug, e agora **Reteste**). Para uma alteração de UX de R$ 13.790,89, a organização utiliza 6 tipos distintos de work items em 3 projetos Azure DevOps.

**Impacto**: Cada tipo tem seu próprio workflow, campos, e regras de automação. A fragmentação torna impossível uma visão unificada do pipeline sem consultar múltiplos schemas.

---

### P93 — 100% automação — zero interação humana

O work item foi inteiramente criado, preenchido e finalizado pela service account AzDevOpsServ_PRD. Nenhum humano nunca abriu, editou ou visualizou este item. Anderson aparece apenas como campo referencial (`CreatedByReteste.TIMDM`).

**Impacto**: O WI existe exclusivamente para alimentar dashboards/relatórios de KPI. Se nenhum humano interage com ele, seu valor depende inteiramente da qualidade da automação que o gera — e dos dados que herda.

---

### P94 — Nasceu no estado terminal "Válido" — zero transições

Padrão idêntico à Entrega #1178461. O estado "Válido" é o estado final do tipo Reteste. Não existe workflow a percorrer — o item é um **snapshot retroativo** de um evento que já aconteceu.

**Impacto**: A state machine do tipo Reteste é decorativa. O item poderia ser uma linha em uma tabela de métricas em vez de um work item completo com campos de identidade, watermark e auditoria.

---

### P95 — 120 minutos "perdidos" vs 34 segundos de reteste real

O campo `QtdMinPerdidosReteste = 120` (2 horas) contrasta dramaticamente com os dados observáveis:
- O reteste real do CY0003 durou ~20 minutos de trabalho efetivo (gravação de vídeo) + 34 segundos de transições de estado
- Os CY0001 e CY0002 **não foram retestados** (passaram na 1ª tentativa)

Os 120 minutos provavelmente representam o custo total atribuído ao fornecedor (ENGINEERING), incluindo análise de causa raiz, correção, re-deploy e validação — não apenas o ato de retestar no Azure DevOps.

**Impacto**: O campo `QtdMinPerdidosReteste` mistura trabalho de engenharia de correção com trabalho de reteste de FQA. A métrica é usada para gestão contratual (penalização/compensação do vendor) mas não reflete o esforço real de teste.

---

### P96 — 3 cenários contabilizados mas apenas 1 retestado

`QtdCenariosReteste = 3` indica que 3 cenários foram "impactados" pelo reteste. Porém, os dados dos Test Cases mostram que **apenas o CY0003** falhou e foi retestado. CY0001 e CY0002 passaram na primeira tentativa e foram fechados normalmente.

**Impacto**: Inflação da métrica de impacto. Se os 3 cenários são contabilizados como retestados, o custo de 120 minutos é dividido por 3 para calcular KPI de produtividade (40 min/cenário), quando na realidade todo o custo foi de 1 cenário.

---

### P97 — Título referencia Bug #1184452 mas o bug que causou a falha é #1193756

O Reteste tem título "Reteste do Bug #1184452" e Parent = #1184452. Porém, a análise do TC #1171262 mostra que o Bug #1193756 foi vinculado no momento da falha (update 12 do TC). O Bug #1184452 está vinculado a **todos os 3 TCs** como relação genérica (TestedBy-Reverse), enquanto #1193756 é específico do CY0003.

**Impacto**: Ambiguidade na rastreabilidade. O Reteste WI aponta para o bug genérico (#1184452) e não para o bug que efetivamente causou a falha (#1193756). Não é possível, a partir do Reteste, determinar qual defeito específico foi corrigido.

---

### P98 — Criado 5 dias após o reteste real — registro retroativo

O reteste do CY0003 foi concluído em 2025-11-19 (TC fechado às 21:30). O Reteste WI foi criado em 2025-11-24 13:14 — **5 dias calendário depois**. O WI não acompanhou o trabalho em tempo real; foi gerado retroativamente pela automação, provavelmente como parte de um batch de consolidação de métricas.

**Impacto**: Os timestamps do Reteste WI não refletem quando o reteste aconteceu. Para análise de lead time, o Reteste WI é inútil — é necessário consultar os Test Cases para obter as datas reais.

---

### P99 — Campo GUID opaco (Custom.59bfa7e3-...) sem nome legível

O campo `Custom.59bfa7e3-23eb-496f-9a9a-f4299caf5e79` contém o timestamp de criação (2025-11-24T13:14:48.63Z), mas seu nome é um GUID em vez de um label funcional. Isso indica que o campo foi criado por extensão/automação sem proper naming.

**Impacto**: Campo técnico sem semântica documentada. Dificulta auditoria e análise de dados fora do contexto da automação que o gerou.

---

## 10. Métricas Consolidadas

| Métrica | Valor |
|---------|-------|
| **Revisões** | 1 |
| **Updates** | 2 |
| **Transições de estado** | 0 |
| **Ciclo de vida** | 0 segundos |
| **Atores humanos ativos** | 0 |
| **Atores automação** | 1 (AzDevOpsServ_PRD) |
| **Parent** | Bug #1184452 |
| **Custo declarado** | 120 min (2h) |
| **Cenários declarados** | 3 |
| **Cenários efetivamente retestados** | 1 (CY0003) |
| **Problemas** | P92–P99 (8) |

---

## 11. Pipeline Atualizado da Iniciativa

| # | Tipo | ID | Projeto | Rev | Estado |
|:-:|------|----|---------|:---:|:------:|
| 1 | Iniciativa | #1085522 | Portfolio Tim TI | 51 | Closed |
| 2 | Epic | #1078031 | Portfolio Tim TI | 51 | Resolved |
| 3 | MV VAS | #1117156 | Portfolio Tim TI | 38 | Aprovação Financeira |
| 4 | MV FQA | #1117168 | Portfolio Tim TI | 34 | Resolved |
| 5 | Feature | #1113005 | Projeto_Service_Creation | 6 | New |
| 6 | User Story | #1113040 | Projeto_Service_Creation | 27 | Refinada |
| 7 | IT Task | #1136722 | Projeto_Service_Creation | 20 | Concluída |
| 8 | Test Request | #1164264 | Projeto_Service_Creation | 24 | Closed |
| 9 | Test Case | #1171260 | Projeto_Service_Creation | 14 | Closed |
| 10 | Test Case | #1171261 | Projeto_Service_Creation | 15 | Closed |
| 11 | Test Case | #1171262 | Projeto_Service_Creation | 23 | Closed |
| 12 | Entrega | #1178461 | Entrega_de_Kits | 3 | Armazenada SCM |
| **13** | **Reteste** | **#1199583** | **Projeto_Service_Creation** | **1** | **Válido** |
| — | Bug | #1184452 | Projeto_Service_Creation | ? | ? |
| — | Bug | #1193756 | Projeto_Service_Creation | ? | ? |
| | | **TOTAL: 13 WIs + 2 Bugs** | **3 projetos** | **277+** | |