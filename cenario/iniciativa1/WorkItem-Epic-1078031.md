# Análise de Ciclo de Vida — Epic #1078031

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1078031 |
| **Tipo** | Epic |
| **Título final** | 251078031 - Melhorias Resgate Senha inFlight |
| **Título original** | Internet no avião – Reset de Senha |
| **Projeto** | Portfolio Tim TI (originalmente criado em Projeto_Service_Creation!) |
| **AreaPath** | Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB |
| **TipoEpic** | Funcional |
| **ModeloGestao** | Waterfall |
| **Estado atual** | **Resolved** |
| **Criado** | 2025-08-05 16:13:30 |
| **Activated** | 2025-10-27 10:37:22 |
| **Resolved** | 2025-12-04 01:07:59 |
| **Revisões** | 43 |
| **Updates** | 51 |
| **Comentários** | 11 |
| **Parent** | #1085522 (Iniciativa) |
| **ValorEpic** | R$ 13.790,89 |
| **Macro_Valoracao** | R$ 14.000 (estimativa inicial) |

---

## 2. Hierarquia

```
Macro Portfolio #791755
  └── Iniciativa #1085522 — Melhorias Resgate Senha inFlight (Closed)
        ├── MV #1117156 — VAS (Aprovação Financeira)
        ├── MV #1117168 — FQA/ATOS (Resolved)
        └── Epic #1078031 ◄ ESTE (Resolved)
              ├── Feature #1113005 — Alteração da Fraseologia (New — zumbi)
              ├── Feature #1113128
              ├── Feature #1113105
              └── Feature #1183520 (adicionada tardiamente, 2025-11-10)
```

**Nota:** O Epic possui **4 Features** filhas, não apenas 1. Somente #1113005 foi analisada nesta iniciativa. As Features #1113128 e #1113105 foram adicionadas por Ana Maria no mesmo dia (2025-09-05); #1183520 foi adicionada 2 meses depois (2025-11-10).

---

## 3. Relações Cross-Item

| Tipo | ID | Propósito |
|------|:--:|-----------|
| Parent | #1085522 | Iniciativa (Portfolio Tim TI) |
| Child | #1113005 | Feature — Alteração da Fraseologia |
| Child | #1113128 | Feature (não analisada) |
| Child | #1113105 | Feature (não analisada) |
| Child | #1183520 | Feature (adicionada tardiamente) |
| Related | #1117156 | MV VAS (mencionado por Fernanda) |
| Related | #1117168 | MV FQA (mencionado por Fernanda) |
| Related | #1164264 | TR FQA (adicionado por Anderson/ATOS) |
| Attachment | .msg | Aprovação de Negócio (2025-10-17) |
| Attachment | .msg | Cronograma (2025-12-03) |

---

## 4. Atores

| Ator | Papel | Ações principais |
|------|-------|-----------------|
| **Danielle Da Fonseca Aguiar** (dfaguiar) | Criadora / Solicitante | Criou o Epic, preencheu campos iniciais |
| **Fernanda Soares Marelli Leite** (fleite) | Gestora de portfolio | ~22 updates, gerenciou transições, flags, StackRank, links MVs |
| **Paulo Ricardo Castellanos Souza** (pcsouza) | Tech Lead / Resolver | Aprovação Lid Tec, transições Em Valoração→Em Desenvolvimento→Resolved |
| **Ana Maria Lopes Moreira** (amlmoreira) | AssignedTo / Aprovadora 4 | Adicionou 4 Features filhas, aprovação de negócio |
| **Paulo Henrique Ferreira Costa** (pfcosta) | Aprovador 1 | Aprovação de negócio |
| **Silvio Dos Santos Junior** (sdsjunior) | Lane mapping Kanban | Ajuste de board |
| **Marcelo Henrique Costa Da Silva** (mhcdsilva) | Gestão de diretoria | Ajuste DiretoriaN2 |
| **Anderson Teixeira Abrantes** (aabrantes_atos) | Fornecedor ATOS | Link cross-project #1164264 |
| **Milton José Nogueira** | Referenciado | Comitê de discussão |
| **Diego Wanderosck Lisboa** | Referenciado | Comitê de discussão |

**10 atores** para um Epic de uma única demanda de UX.

---

## 5. Cronologia Completa — Transições de Estado

```
2025-08-05 16:13 ──── New (Danielle cria o Epic em Projeto_Service_Creation!)
       │                 Título: "Internet no avião – Reset de Senha"
       │                 AreaPath: Projeto_Service_Creation\Macro Valoracao TI
       │
       │  [24 dias — 4 renomeações de título no 1º dia]
       │
2025-08-29 21:14:36 ──── Em Design (Fernanda)
       │  59 seg
2025-08-29 21:15:35 ──── Estimativa (Fernanda)
       │  6 seg
2025-08-29 21:15:41 ──── Estimado (Fernanda)
       │              Macro_Valoracao=14.000
       │
       │  ═══════════════════════════════════════════
       │  3 TRANSIÇÕES EM 65 SEGUNDOS (ceremonial)
       │  ═══════════════════════════════════════════
       │
       │  [11 dias]
       │
2025-09-09 17:58 ──── Refinamento (Fernanda)
       │              Links: MV #1117156, MV #1117168
       │
       │  [1 dia]
       │
2025-09-10 10:52 ──── Em Valoração (Paulo Ricardo)
       │
       │  [37 dias]
       │
2025-10-17 17:33 ──── Aprovação Financeira (Fernanda)
       │              Aprovadores: Paulo Henrique (#1) + Ana Maria (#4)
       │              DataAprovacaoNegDev=2025-10-17
       │              DataAprovacaoGerLidTec=2025-10-08
       │              Attachment: email de aprovação
       │
       │  [10 dias]
       │
2025-10-27 10:37 ──── Em Desenvolvimento (Paulo Ricardo)
       │              ActivatedDate = 2025-10-27
       │
       │  [38 dias]
       │
2025-12-04 01:07 ──── Resolved (Paulo Ricardo)
       │              Attachment: email de cronograma
       │
       ▼  FIM DO CICLO
```

---

## 6. Lead Times

| Segmento | De | Até | Duração |
|----------|----|-----|---------|
| New → Em Design | 2025-08-05 | 2025-08-29 | **24 dias** |
| Em Design → Estimativa → Estimado | 2025-08-29 21:14 | 2025-08-29 21:15 | **65 seg** (ceremonial) |
| Estimado → Refinamento | 2025-08-29 | 2025-09-09 | **11 dias** |
| Refinamento → Em Valoração | 2025-09-09 | 2025-09-10 | **1 dia** |
| Em Valoração → Aprovação Financeira | 2025-09-10 | 2025-10-17 | **37 dias** |
| Aprovação Financeira → Em Desenvolvimento | 2025-10-17 | 2025-10-27 | **10 dias** |
| Em Desenvolvimento → Resolved | 2025-10-27 | 2025-12-04 | **38 dias** |
| **Ciclo total** | **2025-08-05** | **2025-12-04** | **121 dias** |

---

## 7. Evolução do Título (4 mudanças no 1º dia)

| Rev | Título |
|:---:|--------|
| 1 | Internet no avião – Reset de Senha |
| 4 | 1078031 - Internet no avião – Reset de Senha |
| 5 | 251078031 - Internet no avião – Reset de Senha |
| 8 | **251078031 - Melhorias Resgate Senha inFlight** (definitivo) |

O título mudou 4 vezes — 3 no primeiro dia (adição de IDs) e 1 sete dias depois (rename completo). O SDLC ainda não estava estabilizado quando o Epic foi criado.

---

## 8. Evolução do ValorEpic

| Data | ValorEpic | Ator |
|------|:---------:|------|
| 2025-09-10 | R$ 13.790,89 | Definido inicialmente |
| 2025-10-16 | R$ 11.790,00 | Alterado (removeu valor FQA?) |
| (posterior) | R$ 13.790,89 | Revertido ao valor correto |

O valor oscilou — temporariamente reduzido a R$ 11.790 (exatamente o valor da MV VAS sozinha), depois restaurado a R$ 13.790,89 (VAS + FQA). Isso indica confusão sobre se o Epic contabiliza apenas desenvolvimento (VAS) ou desenvolvimento + testes (VAS + FQA).

---

## 9. Problemas Identificados

### P65 — 3 transições de estado em 65 segundos (Em Design → Estimativa → Estimado)

- **Evidência:** 2025-08-29 21:14:36 → 21:15:35 → 21:15:41. Fernanda moveu o Epic por 3 estados em pouco mais de 1 minuto.
- **Impacto:** Os estados "Em Design", "Estimativa" e "Estimado" existem como etapas formais no workflow do Epic, mas foram atravessados sem qualquer atividade de design ou estimativa real. O campo `Macro_Valoracao=14.000` foi preenchido junto, mas 14.000 é um número redondo que sugere estimativa preliminar.
- **Padrão:** Idêntico ao P17 (MV VAS Macro→Valor em 1 min) e P58 (IT Task Refinamento→Valoração em 1 min). Transições ceremoniais são sistêmicas.

### P66 — Epic criado em projeto errado (Projeto_Service_Creation)

- **Evidência:** Rev 1 mostra AreaPath "Projeto_Service_Creation\Macro Valoracao TI". O Epic foi posteriormente migrado para "Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB".
- **Impacto:** O Epic nasceu no projeto de execução (Service Creation) e não no de portfolio, indicando que a separação de projetos não era clara no momento da criação. Isso é consistente com P36 (Feature migrada cross-project) — o mesmo padrão de confusão sobre onde os itens devem viver.

### P67 — ValorEpic alterado para R$ 11.790 e depois revertido

- **Evidência:** O valor foi reduzido de R$ 13.790,89 para R$ 11.790 (= valor VAS apenas) e depois restaurado.
- **Impacto:** Indica confusão sobre o perímetro do Epic — se ele cobre apenas desenvolvimento (VAS) ou também testes (FQA). Esta oscilação demonstra falta de governança sobre o campo financeiro do Epic.

### P68 — 8 transições de estado para 1 Feature ativa

- **Evidência:** O Epic passou por 8 transições (New → Em Design → Estimativa → Estimado → Refinamento → Em Valoração → Aprovação Financeira → Em Desenvolvimento → Resolved) tendo como working deliverable real apenas 1 Feature (#1113005) efetivamente utilizada.
- **Impacto:** As 4 Features filhas incluem 3 cujo estado e conteúdo não foram nem analisados (#1113128, #1113105, #1183520). O overhead de transições do Epic é proporcional a um container de alta complexidade, quando na realidade gestiona uma única alteração de UX.

### P69 — Resolved com Feature child em "New" e User Story em "Refinada"

- **Evidência:** Epic Resolved em 2025-12-04. Feature #1113005 permanece em "New" até hoje (2026-04-13). User Story #1113040 permanece em "Refinada".
- **Impacto:** O Azure DevOps não impede que um Epic seja resolvido com filhos em estados iniciais. Nenhum gate de consistência hierárquica existe. Já documentado como P38 (Feature) e P47 (User Story).

### P70 — 11 comentários com interação de comitê para UX pontual

- **Evidência:** 11 comentários incluem discussões de volumetria (122k resets em 6 meses), pedidos de aprovação, e interações de comitê com Milton Nogueira e Diego Lisboa.
- **Impacto:** O volume de deliberação formal (aprovação de negócio, aprovação de TI, comitê financeiro, cronograma) é desproporcional ao escopo técnico (adicionar um link em uma Webview).

---

## 10. Métricas Consolidadas

| Métrica | Valor |
|---------|-------|
| Lead time total | **121 dias** |
| Transições de estado | 8 |
| Transições ceremoniais (<1 min) | 3 (37,5%) |
| Revisões | 43 |
| Updates | 51 |
| Comentários | 11 |
| Atores | 10 (8 ativos + 2 referenciados) |
| Features filhas | 4 (mas apenas 1 analisada) |
| Aprovações formais | 3 (Lid Tec + Negócio x2) |
| Attachments | 2 (emails .msg) |

---

*Análise gerada a partir dos arquivos WorkItem-Epic-1078031.json, WorkItem-Epic-Revisoes-1078031.json e WorkItem-Epic-Updates-1078031.json.*
