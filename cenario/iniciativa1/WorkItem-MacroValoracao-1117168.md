# Análise de Ciclo de Vida — Macro Valoração #1117168 (FQA / ATOS)

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1117168 |
| **Tipo** | Macro Valoração |
| **Título** | 251078031 - Melhorias Resgate Senha inFlight - FQA - ATOS |
| **Sistema** | TEST FACTORY |
| **BugVendor** | FQA - ATOS |
| **Diretoria TIN2** | IT Planning e Projects |
| **Diretoria TIN3** | IT Quality Tests e Control |
| **AreaPath** | Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB |
| **Tipo MV** | Original |
| **Estado atual** | **Resolved** |
| **Criado** | 2025-09-09 18:05:13 |
| **Resolved** | 2025-10-23 17:25:06 |
| **Última alteração** | 2025-11-26 20:20:10 |
| **Revisões** | 32 |
| **Updates** | 34 |
| **Comentários** | 5 |

### Dados Financeiros

| Campo | Valor |
|-------|-------|
| Macro_Valoracao (FP) | 21,16 |
| Valoracao (FP) | 21,16 |
| TaxaValoracao | R$ 94,56/FP |
| ValorMacroValoracao | R$ 2.000,89 |
| ValorValoracao | R$ 2.000,89 |
| NumeroBOQ | 832868 |
| NumeroPO | 4504614557 |
| EstadoAprovacao2 | Aprovado |
| DataAprovacaoLidTec | 2025-09-30 |

---

## 2. Hierarquia

```
Macro Portfolio #791755
  └── Iniciativa #1085522 — Melhorias Resgate Senha inFlight
        ├── Macro Valoração #1117156 — VAS (Aprovação Financeira — estagnada)
        ├── Macro Valoração #1117168 — FQA/ATOS ◄ ESTE (Resolved)
        └── Epic #1078031 — Melhorias Resgate Senha inFlight
              └── User Story → IT Task #1136722
```

**Links:** Parent=#1085522 (Iniciativa), Related=#1078031 (Epic), Related=#1164264 (cross-project, adicionado por Anderson Teixeira Abrantes da ATOS).

**Nota:** Ao contrário do que a análise da MV #1117156 (VAS) afirmou, as duas MVs **NÃO compartilham o mesmo BOQ**. FQA tem BOQ=832868 e PO=4504614557; VAS tem BOQ=841919 e nenhum PO. Cada diretoria tem alocação orçamentária separada.

---

## 3. Atores

| Ator | Papel | Ações principais |
|------|-------|-----------------|
| **Fernanda Soares Marelli Leite** (fleite) | Criadora / Gestora de portfolio | Criou o WI, flags Macrovalorado/Valorado, FlagAjusteADM, comentários, StackRank |
| **Meire Goncalves Luksaitis** (mluksaitis) | Macrovaloradora / Valoradora / Resolver | Macrovaloração (c/ tabela FQA), Valoração, Aprovação Financeira + BOQ, NumeroPO, Resolved. AssignedTo. |
| **Paulo Ricardo Castellanos Souza** (pcsouza) | Aprovador (Lid Tec) | NomeAprovador2, EstadoAprovacao2="Aprovado", DataAprovacaoLidTec |
| **Camilla Alves Da Silva** (csilva) | Gestão de prioridade | StackRank (2 updates, fase inicial) |
| **Denise Cruz Ferrao** (dferrao) | Gestão de prioridade | StackRank (rev 25, 2025-10-16) |
| **Priscila Dos Santos Figueiredo Marques** (pfmarques) | Gestão de prioridade | StackRank (rev 29, 2025-10-31) |
| **Anderson Teixeira Abrantes** (aabrantes_atos) | Fornecedor ATOS | Adicionou link cross-project #1164264 (2025-10-27) |

---

## 4. Cronologia Completa — Transições de Estado

```
2025-09-09 18:05 ──── New (Fernanda cria o WI)
       │  68 min
2025-09-09 19:13 ──── Macrovaloração (Meire: 21,16 FP, Taxa=94,56, Valor=R$2.000,89)
       │              Comentário com tabela FQA: 3 cenários de teste, R$2.000, 1 reteste aceitável
       │
       │  ~17 horas ← SEPARAÇÃO REAL entre macro e valoração
       │
2025-09-10 12:16 ──── Valoração (Meire: Valoracao=21,16, ListaBI, ResponsavelValoracao=Meire)
       │
       │  19 min
       │
2025-09-10 12:35 ──── Valorado=true (Fernanda — flag de controle)
       │
       │  [Fase dormência: 9-12 → 9-22 = StackRank/priorização por Camilla, Fernanda]
       │
2025-09-29 20:01 ──── COMENTÁRIO: Meire pede aprovação
       │              "@Fernanda @Paulo Ricardo preciso que o workitem seja aprovado" + screenshot
       │
2025-09-29 22:01 ──── COMENTÁRIO: Fernanda responde
       │              "O Paulo Ricardo vai aprovar. Peço aguardar o comitê financeiro de TI
       │               para prosseguir com a BOQ."
       │
2025-09-30 11:17 ──── APROVAÇÃO LID TEC (Paulo Ricardo)
       │              NomeAprovador2=Paulo Ricardo, EstadoAprovacao2="Aprovado"
       │              DataAprovacaoLidTec=2025-09-30
       │
2025-09-30 14:03 ──── Aprovação Financeira (Meire)
       │              NumeroBOQ=832868
       │              Kanban: "Aprovação Financeira (BOQ - PO)"
       │
       │  [8 dias]
       │
2025-10-08 15:01 ──── FlagAjusteADM=false→true, Macrovalorado=true→false (Fernanda)
2025-10-08 15:01 ──── Valorado=true→false                        (Fernanda, +2seg)
2025-10-08 15:03 ──── FlagAjusteADM=true→false                   (Fernanda, +2min)
2025-10-08 15:03 ──── Macrovalorado=false→true                    (Fernanda, +5seg)
2025-10-08 15:03 ──── Valorado=false→true                        (Fernanda, +3seg)
       │
       │  [6 operações de toggle em 2,5 minutos — overhead administrativo]
       │
2025-10-09 ──── StackRank (Fernanda)
2025-10-16 ──── StackRank (Denise Cruz Ferrao)
       │
2025-10-23 17:25:04 ──── NumeroPO=4504614557 (Meire)
2025-10-23 17:25:06 ──── Resolved (Meire, 2 segundos depois)
       │
       │  [Atividade pós-Resolved: StackRank por Fernanda, Priscila, Fernanda]
       │
2025-10-27 ──── Link cross-project #1164264 (Anderson/ATOS)
2025-10-27 ──── StackRank (Fernanda)
2025-10-31 ──── StackRank (Priscila)
2025-11-04 ──── StackRank (Fernanda)
2025-11-10 ──── StackRank (Fernanda)
2025-11-26 ──── StackRank (Fernanda) ← ÚLTIMO REGISTRO
```

---

## 5. Lead Times

| Segmento | De | Até | Duração |
|----------|----|-----|---------|
| New → Macrovaloração | 2025-09-09 18:05 | 2025-09-09 19:13 | **68 min** |
| Macrovaloração → Valoração | 2025-09-09 19:13 | 2025-09-10 12:16 | **17 horas** |
| Valoração → Aprovação Lid Tec | 2025-09-10 12:16 | 2025-09-30 11:17 | **20 dias** |
| Aprovação Lid Tec → Aprovação Financeira | 2025-09-30 11:17 | 2025-09-30 14:03 | **2h46** (mesmo dia) |
| Aprovação Financeira → Resolved | 2025-09-30 14:03 | 2025-10-23 17:25 | **23 dias** |
| **Ciclo total (criação → Resolved)** | 2025-09-09 | 2025-10-23 | **44 dias** |
| Atividade pós-Resolved | 2025-10-23 | 2025-11-26 | **34 dias** (StackRank) |

---

## 6. Análise de Overhead — Flags Toggle (2025-10-08)

Em 2,5 minutos, Fernanda executou 6 operações de toggle nas flags `Macrovalorado`, `Valorado` e `FlagAjusteADM`:

| Hora | Macrovalorado | Valorado | FlagAjusteADM |
|------|:---:|:---:|:---:|
| 15:01:03 | true→**false** | (inalterado) | false→**true** |
| 15:01:05 | false | true→**false** | true |
| 15:01:07 | false | false | true |
| 15:03:32 | false | false | true→**false** |
| 15:03:37 | false→**true** | false | false |
| 15:03:40 | true | false→**true** | false |

**Impacto:** 6 revisões (rev 18-23) geradas sem qualquer mudança de estado. Puro overhead administrativo.

**Padrão cruzado:** A mesma sequência de toggles ocorreu simultaneamente na MV irmã #1117156 (VAS) no mesmo dia/horário (15:00-15:11), indicando que Fernanda processou ambas as MVs em lote — ajuste administrativo em massa.

---

## 7. Análise de Comentários — Dinâmica de Aprovação

A MV #1117168 possui uma interação de comentários que revela a friction no processo de aprovação:

| # | Data | Autor | Conteúdo |
|---|------|-------|----------|
| 1 | 2025-09-09 18:05 | Fernanda | (menção ao Epic #1078031) |
| 2 | 2025-09-09 19:13 | Meire | Tabela FQA: "Valoração de 2k", 3 cenários, R$2.000, 1 reteste aceitável |
| 3 | 2025-09-10 01:09 | Fernanda | "@Meire Favor seguir com a valoração. FYI @Paulo Ricardo" |
| 4 | 2025-09-29 20:01 | Meire | "@Fernanda @Paulo Ricardo preciso que o workitem seja aprovado" + screenshot |
| 5 | 2025-09-29 22:01 | Fernanda | "O Paulo Ricardo vai aprovar. Peço aguardar o comitê financeiro de TI para prosseguir com a BOQ." |

**Ciclo de aprovação:**
- Meire completa a valoração em 2025-09-10
- 19 dias depois (2025-09-29), Meire precisa pedir explicitamente que o WI seja aprovado
- Fernanda responde que Paulo Ricardo vai aprovar, mas pede "aguardar o comitê financeiro"
- Paulo Ricardo aprova no dia seguinte (2025-09-30 11:17)
- Meire transita para Aprovação Financeira 2h46 depois

**Conclusão:** O gargalo de 19 dias entre a valoração e a solicitação de aprovação indica que o processo não tem mecanismo de notificação/SLA — a valoradora precisa cobrar manualmente a aprovação.

---

## 8. Problemas Identificados

### P20 — Gargalo de 19 dias entre Valoração e solicitação de aprovação

- **Evidência:** Meire completou a valoração em 2025-09-10 12:16. Somente em 2025-09-29 20:01 (19 dias depois) pediu explicitamente que o WI fosse aprovado.
- **Causa:** Ausência de mecanismo automático de notificação/SLA que alerte o aprovador quando a valoração é concluída.
- **Impacto:** 19 dos 44 dias de ciclo total (43%) foram gargalo de handoff entre papéis.

### P21 — Aprovação Lid Tec como comitê financeiro (gating desnecessário?)

- **Evidência:** Fernanda menciona "comitê financeiro de TI" como pré-requisito para BOQ (comentário 5). Paulo Ricardo aprova no dia seguinte.
- **Questão:** Para um item de R$2.000,89, qual é o threshold de aprovação pelo comitê financeiro? O processo aplica o mesmo gate para itens de R$2k e R$12k (VAS)?
- **Impacto:** Overhead de governança potencialmente desproporcional ao valor.

### P22 — Toggle caótico de flags (6 revisões em 2,5 minutos)

- **Evidência:** Revisões 18-23 (2025-10-08 15:01-15:03) — mesma Fernanda, operação em lote com MV #1117156.
- **Impacto:** 6 das 32 revisões (19%) gastas em ajuste de flags sem mudança de estado.
- **Causa provável:** Mesma da MV VAS — flags manuais que deveriam ser derivadas automaticamente.

### P23 — PO atribuído 2 segundos antes de Resolved (ceremonial)

- **Evidência:** Update 27: NumeroPO=4504614557 em 2025-10-23 17:25:04. Update 28: Resolved em 17:25:06.
- **Padrão:** O NumeroPO é pré-requisito formal para Resolved, mas atribuído no mesmo instante — indicando que a aprovação financeira real já ocorreu fora do sistema.
- **Impacto:** O campo NumeroPO funciona como checkbox de compliance, não como controle efetivo.

### P24 — 7 atores para um item de R$2.000

- **Evidência:** Fernanda (criação/flags), Meire (valoração/resolução), Paulo Ricardo (aprovação), Camilla (StackRank), Denise (StackRank), Priscila (StackRank), Anderson (link).
- **Contexto:** 3 atores participaram apenas para StackRank, 1 para adicionar um link cross-project.
- **Impacto:** Ratio atores/valor financeiro ainda mais desproporcional que a MV VAS (7 atores para R$2k vs 5 atores para R$12k).

### P25 — 34 dias de atividade pós-Resolved

- **Evidência:** Resolved em 2025-10-23. Último registro em 2025-11-26. 5 updates de StackRank + 1 link pós-resolução.
- **Impacto:** Item "concluído" continua gerando revisões por 34 dias — overhead de re-priorização num item já encerrado.

---

## 9. Diferenças Significativas vs MV VAS (#1117156)

### 9.1 Macrovaloração → Valoração: trabalho real vs ceremonial

- **FQA (#1117168):** 17 horas entre os estados. Meire (especialista FQA) fez a macrovaloração às 19:13 e voltou no dia seguinte às 12:16 para completar a valoração. Sugere que houve análise técnica real entre os dois passos.
- **VAS (#1117156):** 1 minuto entre os estados. Paulo Ricardo fez ambos os passos sequencialmente na mesma sessão. Transição puramente ceremonial.

### 9.2 Separação de papéis

- **FQA:** Meire (especialista FQA/ATOS) faz a valoração técnica; Paulo Ricardo aprova. Separação de duties.
- **VAS:** Paulo Ricardo faz a valoração E aprova o item. Conflito de papéis.

### 9.3 Dinâmica de comentários

- **FQA:** 5 comentários com interação real (Meire cobrando aprovação, Fernanda mediando, valoração técnica documentada).
- **VAS:** 1 comentário. Processo mais opaco.

### 9.4 Estrutura financeira radicalmente diferente

| Métrica | FQA (#1117168) | VAS (#1117156) |
|---------|:-:|:-:|
| FP | 21,16 | 10 |
| Taxa (R$/FP) | R$ 94,56 | R$ 1.179,00 |
| Valor total | R$ 2.000,89 | R$ 11.790,00 |
| BOQ | 832868 | 841919 |
| NumeroPO | 4504614557 | — (ausente) |

A taxa VAS é **12,5x mais cara** por FP que a taxa FQA. Mesmo tendo o dobro de function points, a MV FQA custa **6x menos** que a MV VAS. Isso reflete contratos e taxas diferentes por fornecedor/diretoria.

---

## 10. Métricas Comparativas Corrigidas — MV FQA (#1117168) vs MV VAS (#1117156)

| Métrica | #1117168 (FQA) | #1117156 (VAS) |
|---------|:-:|:-:|
| Valor (FP) | 21,16 | 10 |
| Valor (R$) | R$ 2.000,89 | R$ 11.790 |
| Taxa (R$/FP) | R$ 94,56 | R$ 1.179 |
| BOQ | 832868 | 841919 |
| NumeroPO | 4504614557 | — |
| Revisões | 32 | 29 |
| Updates | 34 | 30 |
| Comentários | 5 | 1 |
| Estado final | **Resolved** | **Aprovação Financeira** |
| Ciclo total | 44 dias (completo) | 78+ dias (incompleto) |
| Transição Macro→Valor | 17 horas (real) | 1 min (ceremonial) |
| Atores envolvidos | 7 | 5 |
| Toggle flags | 6 ops / 2,5 min | 5 ops / 11 min |
| Separação de duties | Sim (Meire valora, Paulo aprova) | Não (Paulo valora e aprova) |

**Correção importante:** A análise anterior da MV VAS (seção 8) comparava incorretamente as duas MVs como idênticas em valor (10 FP, R$11.790, BOQ=841919). Na realidade, as MVs referem fornecedores diferentes (FQA-ATOS vs VAS), com taxas radicalmente distintas (R$94,56 vs R$1.179/FP) e BOQs separados.

---

## 11. Overhead Consolidado — Revisões sem Valor

| Tipo de atividade | Revisões | % do total (32) |
|-------------------|:--------:|:---:|
| Transições de estado (4 transições) | 4 | 12,5% |
| Flags de controle manuais | 8 | 25% |
| StackRank / priorização | 12 | 37,5% |
| Comentários / aprovação | 5 | 15,6% |
| Link / relações | 1 | 3,1% |
| Criação | 1 | 3,1% |
| Outros (campo minor) | 1 | 3,1% |

**Conclusão:** Apenas 28% das revisões (transições + aprovação) representam progresso no workflow. 62,5% são overhead puro (flags + StackRank).

---

*Análise gerada a partir dos arquivos WorkItem-MacroValoracao-1117168.json, WorkItem-MacroValoracao-1117168-Revisoes.json e WorkItem-MacroValoracao-1117168-Updates.json.*