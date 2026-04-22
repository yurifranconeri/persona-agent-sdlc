# Análise do Work Item: Entrega #1132619

---

## 1. Identificação e Contexto

| Campo | Valor |
|-------|-------|
| **ID** | 1132619 |
| **Tipo** | Entrega |
| **Projeto** | **Entrega_de_Kits** |
| **Título** | ENTREGA - BUG [OCTB] [IDM] - IDM mantém cookie por sessão |
| **Estado final** | Armazenada pelo SCM ← **revertida de "Liberada para PROD"** |
| **Criado** | 2025-09-23 19:13:32 |
| **Criado por** | Rodrigo Alexandre Oliveira |
| **Assigned (final)** | Mauricio Valderrama De Oliveira |
| **Parent** | **Nenhum** (sem hierarquia) |
| **CodigoDemanda** | BUG1131975 ← **bug de OUTRA iniciativa** |
| **ChangeNumber** | CHG0171485 (change de PROD) |
| **Rev final** | 7 |
| **Updates** | 26 |
| **Relação com a iniciativa** | **WI-template** — fonte de cópias para #1178461 e #1188548→#1192780 |

> **NOTA:** Este WI **NÃO pertence** à iniciativa "Melhorias Resgate Senha inFlight". Ele pertence ao BUG1131975 "[OCTB] [IDM] - IDM mantém cookie por sessão" — um bug completamente diferente. Sua relevância é ser o **template-fonte** que propagou metadados errôneos para todas as Entregas da nossa iniciativa.

---

## 2. Campos Específicos de Entrega

| Campo | Valor |
|-------|-------|
| **Vendor** | ENGINEERING |
| **VendorGroup** | Engineering - OAM |
| **BugOwner** | Mauricio Valderrama De Oliveira |
| **Sistema** | OAMVAS |
| **ShipmentTIM20** | OAM_1131975_SSO |
| **ChangeForm** | CF_SSO-OneClickToBuy |
| **Patch** | FQA |
| **Label (rev 1)** | `202507221553_OAMVAS_OAM_20250605_DR841587_v6_QA` ← **herdado de julho/2025** |
| **Label (rev 2)** | `OAM_1131975_SSO` |
| **Label (rev 4, final)** | `202509231624_OAMVAS_OAM_1131975_SSO` |
| **TipoDeploy** | Manual |
| **DataPlanejada** | 2025-09-23 19:11:00 ← **2 min antes da criação do WI** |
| **DataEntrega** | 2025-09-23 19:11:00 ← idem |
| **Responsável entrega** | Fellipe Pinheiro Moncayo |
| **EvidenciaSystemTest** | Sim |
| **Áreas** | VAS |

### Checklist de Qualidade de Entrega (11 campos booleanos)

| Campo | Valor |
|-------|-------|
| dir_structure | Sim |
| delivery_changeset | Sim |
| delivery_change_form | Sim |
| correct_content_cf | Sim |
| info_change_form_param | Sim |
| last_delivery_change_form_install_env | **Não** |
| change_form_schema_system | **Não** |
| b_change_form_schema_system | Sim |
| redelivery_changeform | Sim |
| valid_change_form | Sim |
| VendorouVendorGroupInvalido | Valido |

→ 9/11 "Sim", 2 "Não". **Este é o padrão-fonte** — os mesmos valores exatos foram copiados para #1178461 e #1192780.

---

## 3. Relações (estado final)

| Tipo | Destino | Observação |
|------|---------|------------|
| **Affects** | #1131975 (Bug) | Único link semântico ao bug original |
| **ArtifactLink** | Changeset 49994 | "Label OAM_1131975_SSO" |
| **Related** | #1178461 | **Nossa** Entrega da demanda (cópia filha) |
| **Related** | #1161225 | Outra entrega (cópia) |
| **Related** | #1161622 | Outra entrega (cópia) |
| **Related** | #1134181 | Outra entrega (cópia) |
| **Related** | #1139422 | Outra entrega (cópia) |
| **Related** | #1173781 | Outra entrega (cópia) |
| **Related** | #1200055 | Outra entrega (cópia) |
| **Related** | #1203236 | Outra entrega (cópia) |

→ **8 links Related** — cada um representando uma entrega criada por cópia deste template. Este WI funciona como **registro-mestre reutilizável**.

---

## 4. Transições de Estado

```
Armazenada pelo SCM → Liberada para PROD → Armazenada pelo SCM (revertida)
```

| # | De | Para | Timestamp | Δt | Ator |
|---|-----|------|-----------|-----|------|
| T1 | Armazenada pelo SCM | Liberada para PROD | 2025-11-01 21:42:48 | — | Thiago Brito De Menezes |
| T2 | Liberada para PROD | **Armazenada pelo SCM** | 2025-11-01 21:53:58 | +11min 10s | Thiago Brito De Menezes |

**2 transições, resultado líquido = zero.** O WI foi promovido a PROD e revertido 11 minutos depois, pelo mesmo ator. O estado final é idêntico ao inicial. Nenhum comentário ou justificativa registrada para a reversão.

---

## 5. Linha do Tempo (7 revisões, 26 updates — 3 fases distintas)

### Fase 1 — Setup (23/09, ~13 minutos)

| Rev | Timestamp | Δt | Autor | Ação |
|-----|-----------|-----|-------|------|
| 1 | 2025-09-23 19:13:32 | — | Rodrigo Alexandre Oliveira | Criação. Label herdado de demanda anterior: "202507221553_OAMVAS_OAM_20250605_**DR841587**_v6_QA" |
| 2 | 2025-09-23 19:14:15 | +43s | Rodrigo Alexandre Oliveira | Label corrigido para "OAM_1131975_SSO" |
| 3 | 2025-09-23 19:24:04 | +9min 49s | Rodrigo Alexandre Oliveira | Associou changeset 49994. Comment: "Associated with changeset 49994." |
| 4 | 2025-09-23 19:24:07 | +3s | AzDevOpsServ_PRD | Label formatado → "202509231624_OAMVAS_OAM_1131975_SSO" |
| 5 | 2025-09-23 19:26:23 | +2min 16s | Rodrigo Alexandre Oliveira | AssignedTo → Mauricio Valderrama. Adicionou link ArtifactLink (changeset) |

### Fase 2 — Template passivo (25/09 → 31/10, ~37 dias)

| Upd | Timestamp | Autor | Ação |
|-----|-----------|-------|------|
| 7 | 2025-09-25 | Rodrigo | +Related link (cópia #1134181) |
| 8 | 2025-09-30 | Rodrigo | +Related link |
| 9 | 2025-10-20 | Rodrigo | +Related link |
| 10 | 2025-10-20 | **Priscilla Araujo Brandao** | +Related link (única ator externo) |
| 11 | 2025-10-30 | Rodrigo | +Related link |
| 12 | 2025-10-30 | Rodrigo | -Related link (removeu) |
| 13 | 2025-10-31 | Rodrigo | +Related link |

→ 7 updates de relações, zero mudanças de campo. O WI acumula links passivamente conforme novas entregas são criadas a partir dele.

### Fase 3 — State flip e mais template (01/11 → 26/11, ~25 dias)

| Rev | Timestamp | Δt | Autor | Ação |
|-----|-----------|-----|-------|------|
| 6 | 2025-11-01 21:42:48 | — | Thiago Brito De Menezes | State → "Liberada para PROD". Adicionou ChangeNumber=CHG0171485 |
| 7 | 2025-11-01 21:53:58 | +11min 10s | Thiago Brito De Menezes | State → **DE VOLTA** "Armazenada pelo SCM" |

Após rev 7, mais 11 updates de relações (cópias #1178461 em 05/11, #1188548 em 13/11 e 18/11, #1192780, etc.) até 26/11.

---

## 6. Atores

| Ator | Tipo | Papel | Atividade |
|------|------|-------|-----------|
| **Rodrigo Alexandre Oliveira** | Humano (SCM) | Criou, configurou, gerenciou todas as cópias | Rev 1-5, updates 7-13, 16-26 |
| **AzDevOpsServ_PRD** | Service Account | Formatou label | Rev 4 |
| **Thiago Brito De Menezes** | Humano (Engineering) | State flip PROD → revertido | Rev 6-7 |
| **Priscilla Araujo Brandao** | Humano | Adicionou 1 link Related | Update 10 |
| **Mauricio Valderrama De Oliveira** | Referenciado (Assigned final) | BugOwner | — |
| **Fellipe Pinheiro Moncayo** | Referenciado | Responsável pela entrega | — |

→ **4 atores ativos** (3 humanos + 1 automação), **2 referenciados**. Total: 6 identidades.

---

## 7. Análise da Descrição

A descrição contém:
> **OAM_1131975_SSO**

Neste WI, a descrição é **coerente** com o CodigoDemanda (BUG1131975) — este é o **único** WI da cadeia onde a descrição corresponde ao conteúdo. A partir das cópias (#1178461, #1188548, #1192780), a descrição se torna errônea porque os WI-filhos pertencem a demandas diferentes.

---

## 8. Genealogia do Label — Descoberta de 4ª Geração

O label na rev 1 foi:
```
202507221553_OAMVAS_OAM_20250605_DR841587_v6_QA
```

| Componente | Significado |
|------------|------------|
| `20250722` | Data: **22 de julho de 2025** |
| `1553` | Hora: 15:53 |
| `OAMVAS` | Sistema |
| `OAM_20250605` | Referência a **05 de junho de 2025** |
| `DR841587` | Demanda **DR841587** — demanda anterior |
| `v6_QA` | Versão 6, ambiente QA |

**Revelação:** Este WI é ele mesmo uma cópia de um WI ainda mais antigo (DR841587 de junho/julho 2025). A cadeia completa de cópias é:

```
DR841587 (Jun/Jul 2025) → #1132619/BUG1131975 (Set 2025) → #1178461/TIR1136722 (Nov 2025)
                                                            → #1188548/BUG1184452 (Nov 2025) → #1192780/BUG1184452 (Nov 2025)
```

**Quatro gerações** de cópias. A descrição "OAM_1131975_SSO" e a checklist 9/2 propagaram-se por 3 das 4.

---

## 9. Problemas Identificados

### P120 — WI-template: entrega de BUG externo reutilizada como modelo genérico

Este WI (BUG1131975 - IDM cookie) foi copiado **pelo menos 8 vezes** para criar entregas de demandas completamente diferentes: TIR1136722 (feature), BUG1184452 (reset senha), e pelo menos 6 outras. Não existe um mecanismo de "New from template" — o processo é copiar um WI antigo, herdando todos os campos (inclusive os errados), e corrigir manualmente o que for lembrado. A prática cria **propagação sistêmica de metadados incorretos**.

### P121 — State flip: Liberada para PROD → revertida em 11 minutos, sem justificativa

Thiago Brito moveu para "Liberada para PROD" às 21:42 e reverteu para "Armazenada pelo SCM" às 21:53 em 01/11. Nenhum comentário, nenhuma history entry, nenhuma explicação. Possíveis causas: erro operacional, deploy cancelado, ou confusão de WI. A reversão sem registro viola G2 (toda decisão com justificativa) e cria ambiguidade no estado do deploy.

### P122 — Label herdado de 4ª geração (DR841587 de julho 2025)

O label na criação era `202507221553_OAMVAS_OAM_20250605_DR841587_v6_QA` — um identificador de uma demanda de **junho/julho 2025**, 3 meses antes. Rodrigo corrigiu manualmente em 43 segundos (rev 2), mas o fato de o label original vir de DR841587 prova que a cadeia de cópias tem **pelo menos 4 gerações**. Cada geração herda o DNA da anterior.

### P123 — Zero parent: entrega órfã sem hierarquia

O WI não tem `System.Parent`. A única ligação semântica ao bug original é um link "Affects → #1131975". Para auditoria de portfólio, esta entrega **não aparece na árvore** de nenhum outro WI. É um nó solto no grafo do Azure DevOps, conectado apenas por Related links (que são bidirecionais mas semanticamente fracos).

### P124 — 26 updates vs. 7 revisões: 19 updates fantasma

19 dos 26 updates são mudanças de relação (add/remove link) que não incrementam o número de revisão. Isto cria uma discrepância entre o "tamanho visível" do WI (7 revisões, parece simples) e sua atividade real (26 updates). Os updates de relação documentam 2 meses de reuso como template, mas são invisíveis num audit baseado em revisões.

### P125 — DataPlanejada = DataEntrega = 2 minutos antes da criação

DataPlanejada = DataEntrega = **19:11:00**, WI criado às **19:13:32**. Esta é a origem da prática herdada por todas as cópias: definir a data de entrega **antes** do WI existir. Na Entrega #1178461, as datas foram para o mesmo minuto da criação; na #1192780, foram 4 dias antes. O pattern origina-se aqui.

### P126 — Checklist como DNA de template: padrão 9/2 propagado por 3 gerações

Os exatos mesmos 9 "Sim" + 2 "Não" (last_delivery_change_form_install_env + change_form_schema_system) aparecem em #1132619 (Set/25), #1178461 (Nov/25, demanda diferente) e #1192780 (Nov/25, bug diferente). São demandas com escopos diferentes (cookie session, fraseologia de UI, reset de senha interpretando 3 tipos de artefatos diferentes) — mas a "verificação de qualidade" é idêntica. A checklist é **hereditária, não verificatória**.

### P127 — ChangeNumber (CHG0171485) adicionado na ida a PROD mas preservado após reversão

Ao mover para "Liberada para PROD", Thiago adicionou CHG0171485 (número de change management). Após reverter o estado, o CHG permaneceu no WI. Se o change foi de fato executado, o WI está no estado errado ("Armazenada pelo SCM" quando já foi a PROD). Se não foi executado, o CHG é um phantom reference.

---

## 10. Métricas Consolidadas do Work Item

| Métrica | Valor |
|---------|-------|
| Revisões | 7 |
| Updates | 26 |
| Transições de estado | **2** (ida + volta = resultado líquido 0) |
| Tempo de vida | ~64 dias (23/09 → 26/11) |
| Tempo ativo humano | **~24 minutos** (13 min setup + 11 min state flip) |
| Atores ativos | 4 (3 humanos + 1 automação) |
| Related links (cópias) | **8** |
| Revisões com valor de negócio | **0/7 (0%)** |
| Overhead do template | Propagou erros para ≥3 WI-filhos |

---

## 11. Papel Estrutural: O Template-Raiz

```
DR841587 (Jun/Jul 2025)
  └─ cópia → #1132619 / BUG1131975 (Set 2025) ← ESTE WI
                ├─ cópia → #1178461 / TIR1136722 (Nov 2025) — Entrega da Demanda
                ├─ cópia → #1188548 / BUG1184452 (Nov 2025) — Entrega do Bug (1ª)
                │            └─ cópia → #1192780 / BUG1184452 (Nov 2025) — Entrega do Bug (2ª)
                ├─ cópia → #1161225, #1161622, #1134181, #1139422, #1173781, #1200055, #1203236
                └─ (Affects → Bug #1131975)
```

Este WI é o **Patient Zero** da propagação de metadados errôneos. Dele originaram-se:
- A descrição "OAM_1131975_SSO" que aparece em WI's de demandas diferentes
- A checklist 9/2 aplicada indiscriminadamente a todos os tipos de entrega
- O título "- Copy" / "- Copy - Copy" nunca corrigido
- As datas retroativas (DataPlanejada = momento da cópia)

**Para a tese:** A prática de "template por cópia manual" sem validação de campos herdados é a causa-raiz de pelo menos **6 problemas documentados** em análises anteriores (P41, P43, P44, P111, P112, P118, P119). Este WI é a evidência empírica de como a ausência de templates formais no Azure DevOps gera dívida de metadados cumulativa e rastreabilidade degradada.

---

## 12. Problemas acumulados na iniciativa

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
| **P120-P127** | **Entrega Template #1132619** | **8** |
| **Total** | | **127 problemas** |