Compacted conversation# Análise do Work Item: Entrega #1178461

---

## 1. Identificação e Contexto

| Campo | Valor |
|-------|-------|
| **ID** | 1178461 |
| **Tipo** | Entrega |
| **Projeto** | **Entrega_de_Kits** ← 3º projeto Azure DevOps |
| **Título** | ENTREGA - Alteração da Fraseologia e Criação do Botão - inFlight |
| **Estado** | Armazenada pelo SCM |
| **Criado** | 2025-11-05 14:50:29 |
| **Criado por** | Rodrigo Alexandre Oliveira |
| **Parent** | #1136722 (IT Task — projeto Portfolio Tim TI) |
| **CodigoDemanda** | TIR1136722 |
| **Rev final** | 3 |
| **Origem** | Copiado de #1132619 |

---

## 2. Campos Específicos de Entrega

| Campo | Valor |
|-------|-------|
| **Vendor** | ENGINEERING |
| **VendorGroup** | Engineering - OAM |
| **BugOwner** | Mauricio Valderrama De Oliveira |
| **Sistema** | OAMVAS |
| **ShipmentTIM20** | OAM_1136722 |
| **ChangeForm** | CF_SSO-OneClickToBuy |
| **Patch** | FQA |
| **Label** | 202511051201_OAMVAS_OAM_1136722 |
| **TipoDeploy** | Manual |
| **DataPlanejada** | 2025-11-05 14:50:00 |
| **DataEntrega** | 2025-11-05 14:50:00 |
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

→ 9/11 "Sim", 2 "Não" — todos preenchidos simultaneamente na criação (cópia).

---

## 3. Relações

| Tipo | Destino | Observação |
|------|---------|------------|
| **Parent** | #1136722 (IT Task) | Cross-project: Entrega_de_Kits → Portfolio Tim TI |
| **Related** | #1132619 | Fonte da cópia (Entrega de outra demanda) |
| **ArtifactLink** | Changeset 51241 | "Label OAM_1136722_QA" |

---

## 4. Transições de Estado

```
(nenhuma)
```

**Zero transições.** O item nasceu no estado "Armazenada pelo SCM" — que é o estado terminal — e nunca mudou. A state machine do tipo Entrega é completamente ignorada.

---

## 5. Linha do Tempo (3 revisões, 4 updates — tudo em 11 minutos)

| # | Timestamp | Δt | Autor | Ação |
|---|-----------|-----|-------|------|
| Rev 1 | 2025-11-05 14:50:29 | — | Rodrigo Alexandre Oliveira | Criação (copiado de #1132619). Todos os campos preenchidos. Estado: "Armazenada pelo SCM". Link Related → #1132619 |
| Rev 2 | 2025-11-05 15:01:06 | +10min 37s | **AzDevOpsServ_PRD** (automação) | Label gerado automaticamente: "202511051201_OAMVAS_OAM_1136722" |
| Rev 3 | 2025-11-05 15:01:24 | +18s | Rodrigo Alexandre Oliveira | Associou changeset 51241 + definiu Parent=#1136722 |

**Ciclo total: 10 minutos 55 segundos.** Do início ao fim, em uma única sessão de trabalho de um único ator humano.

---

## 6. Atores

| Ator | Tipo | Papel |
|------|------|-------|
| **Rodrigo Alexandre Oliveira** | Humano (SCM) | Criou, linked parent e changeset |
| **AzDevOpsServ_PRD** | Service Account | Gerou label automaticamente |
| **Mauricio Valderrama De Oliveira** | Referenciado | BugOwner (Engineering vendor) |
| **Fellipe Pinheiro Moncayo** | Referenciado | Responsável pela entrega |

→ **2 atores ativos** (1 humano + 1 automação), **2 referenciados**. Total: 4 identidades envolvidas.

---

## 7. Análise da Descrição

A descrição do work item contém:

> **OAM_1131975_SSO**

Mas o shipment real é **OAM_1136722**. A descrição refere-se a uma demanda **diferente** — herdada da cópia de #1132619 e nunca corrigida.

---

## 8. Problemas Identificados

### P40 — 3º Projeto Azure DevOps na Iniciativa

A Entrega vive no projeto **Entrega_de_Kits** — um terceiro projeto Azure DevOps, junto com "Portfolio Tim TI" (Iniciativa, Epic, IT Task, MVs) e "Projeto_Service_Creation" (Feature, Test Request). Para uma mudança de R$2.000, há work items em **3 projetos distintos** com templates de processo, permissões e dashboards separados. Nenhuma view única mostra a árvore completa.

### P41 — Descrição herdada de demanda errada

A descrição contém "OAM_1131975_SSO" (da demanda original #1132619), mas esta entrega é para OAM_1136722. A operação de cópia transportou dados incorretos que nunca foram corrigidos, criando risco de rastreabilidade — alguém consultando a descrição chegaria à demanda errada.

### P42 — Nasceu no estado terminal (zero transições)

O item foi criado diretamente no estado "Armazenada pelo SCM" — o estado final do tipo Entrega. Há **zero transições de estado**. A state machine foi completamente ignorada. O work item funciona como um **registro de metadados retroativo**, não como instrumento de fluxo de trabalho. Não existe evidência de que o kit passou por etapas de preparação, revisão ou aprovação antes de ser "armazenado".

### P43 — Checklist preenchido simultaneamente na criação

Os 11 campos de quality gate (dir_structure, delivery_changeset, valid_change_form, etc.) foram **todos preenchidos no momento da criação** (rev 1). Não há evidência de verificação sequencial — todas as respostas foram copiadas junto com o template da entrega #1132619. A checklist, que deveria representar uma verificação independente de cada critério, é preenchida atomicamente.

### P44 — DataPlanejada = DataEntrega = momento de criação

Tanto a data planejada quanto a data de entrega foram definidas como **2025-11-05 14:50:00** — o mesmo minuto da criação do work item. Isto indica documentação retroativa: o kit já havia sido preparado/entregue antes da formalização no Azure DevOps, tornando as datas sem valor de planejamento ou rastreamento.

### P45 — Link parent cross-project sem visibilidade bidirecional

O parent #1136722 (IT Task) vive em um projeto diferente (Portfolio Tim TI / Projeto_Service_Creation). Um gestor que consulta o Entrega_de_Kits não vê o contexto de portfólio, e quem consulta o portfólio precisaria saber que existe um 3º projeto para encontrar a evidência de entrega. A hierarquia é **nominalmente conectada mas operacionalmente fragmentada**.

### P46 — Ciclo de vida de 11 minutos = overhead puro

100% das 3 revisões são administrativas: cópia, label automático, e linking. Nenhuma revisão contém decisão de negócio, mudança de estado significativa, ou registro de trabalho real. O work item inteiro existe como **burocracia de rastreamento**, custando tempo de um engenheiro SCM para copiar, ajustar links e associar changesets, sem agregar informação que não existisse já no controle de versão.

---

## 9. Métricas Consolidadas do Work Item

| Métrica | Valor |
|---------|-------|
| Revisões | 3 |
| Updates | 4 |
| Transições de estado | **0** |
| Tempo de vida | ~11 minutos |
| Atores ativos | 2 (1 humano + 1 automação) |
| Revisões com valor de negócio | **0/3 (0%)** |
| Overhead | **100%** |

---

## 10. Impacto no Panorama Consolidado da Iniciativa

Com a Entrega, a iniciativa "Melhorias Resgate Senha inFlight" agora inclui:

| # | Work Item | Tipo | Projeto | Revs | Transições |
|---|-----------|------|---------|:----:|:----------:|
| 1 | #1085522 | Iniciativa | Portfolio Tim TI | — | — |
| 2 | #1078031 | Epic | Portfolio Tim TI | — | — |
| 3 | #1113005 | Feature | Projeto_Service_Creation | 6 | 0 |
| 4 | #1136722 | IT Task | Portfolio Tim TI | — | — |
| 5 | #1117156 | Macro Valoração (VAS) | Portfolio Tim TI | — | — |
| 6 | #1117168 | Macro Valoração (FQA) | Portfolio Tim TI | — | — |
| 7 | #1164264 | Test Request | Projeto_Service_Creation | 24 | 6 |
| 8 | **#1178461** | **Entrega** | **Entrega_de_Kits** | **3** | **0** |

**Achados novos:**
- **3 projetos Azure DevOps** (antes eram 2) para uma única demanda de ~R$2.000
- **8 work items** no total, com a Entrega sendo o mais efêmero (11 min de vida, zero transições)
- A Entrega é evidência de que o processo de SCM trata o Azure DevOps como **repositório de registros retroativos**, não como ferramenta de workflow
- O nexo informacional entre a entrega física (changeset 51241) e o portfólio passa por **3 saltos cross-project**: Entrega_de_Kits → IT Task (Portfolio Tim TI) → Epic → Iniciativa