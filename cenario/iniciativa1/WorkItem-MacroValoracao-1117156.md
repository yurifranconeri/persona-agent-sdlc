# Análise de Ciclo de Vida — Macro Valoração #1117156 (VAS)

## 1. Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1117156 |
| **Tipo** | Macro Valoração |
| **Título** | 251078031 - Melhorias Resgate Senha inFlight - VAS |
| **Sistema** | VAS |
| **Diretoria TIN2** | IT Service Creation Solutions |
| **Diretoria TIN3** | VAS e Partnership Integration |
| **Diretoria TIN4** | Billing IT Solutions |
| **AreaPath** | Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB |
| **Tipo MV** | Original |
| **Estado atual** | **Aprovação Financeira** (NÃO Resolved) |
| **Criado** | 2025-09-09 18:01:13 |
| **Última alteração** | 2025-11-26 20:20:10 |
| **Revisões** | 29 |
| **Updates** | 30 |
| **Comentários** | 1 |

### Dados Financeiros

| Campo | Valor |
|-------|-------|
| Macro_Valoracao (FP) | 10 |
| Valoracao (FP) | 10 |
| TaxaValoracao | R$ 1.179/FP |
| ValorMacroValoracao | R$ 11.790 |
| ValorValoracao | R$ 11.790 |
| NumeroBOQ | 841919 |
| EstadoAprovacao2 | Aprovado |
| DataAprovacaoLidTec | 2025-09-30 |

---

## 2. Hierarquia

```
Macro Portfolio #791755
  └── Iniciativa #1085522 — Melhorias Resgate Senha inFlight
        ├── Macro Valoração #1117156 — VAS ◄ ESTE (Aprovação Financeira)
        ├── Macro Valoração #1117168 — FQA/ATOS (Resolved)
        └── Epic #1078031 — Melhorias Resgate Senha inFlight
              └── Feature #1113005
                    ├── User Story #1113040
                    └── IT Task #1136722
```

**Nota:** As duas MVs referem-se a fornecedores e diretorias diferentes, com BOQs distintos — #1117156 VAS (BOQ=841919, R$ 11.790) e #1117168 FQA-ATOS (BOQ=832868, R$ 2.000,89). A soma R$ 13.790,89 corresponde ao `ValorIniciativa` da #1085522.

---

## 3. Atores

| Ator | Papel | Ações principais |
|------|-------|-----------------|
| **Fernanda Soares Marelli Leite** (fleite) | Criadora / Gestora de portfolio | Criou o WI, gerenciou flags, toggle Macrovalorado/Valorado, StackRank |
| **Paulo Ricardo Castellanos Souza** (pcsouza) | Macrovalorador / Valorador / Aprovador | Transições de estado, aprovação Lid Tec, BOQ, AssignedTo |
| **Camilla Alves Da Silva** (csilva) | Gestão de prioridade | StackRank/ChangedBy (fase inicial) |
| **Denise Cruz Ferrao** (dferrao) | Gestão de prioridade | StackRank (rev 23, 2025-10-16) |
| **Priscila Dos Santos Figueiredo Marques** (pfmarques) | Gestão de prioridade | StackRank (rev 26, 2025-10-31) |

---

## 4. Cronologia Completa — Transições de Estado

```
2025-09-09 18:01 ──── New (Fernanda cria o WI)
       │  8 min
2025-09-09 18:09 ──── Macrovaloração (Paulo Ricardo: 10 FP, Taxa=1179, Valor=R$11.790)
       │  1 min  ← CEREMONIAL
2025-09-09 18:10 ──── Valoração (Paulo Ricardo: Valoracao=10, ListaBI, ResponsavelValoracao)
       │
       │  [15 dias em Valoração — StackRank/priorização]
       │
2025-09-24 11:55 ──── Macrovalorado=true (Fernanda)
2025-09-24 11:55 ──── Valorado=true (Fernanda, 3 seg depois)
       │
2025-09-30 11:15 ──── APROVAÇÃO LID TEC (Paulo Ricardo)
       │              NomeAprovador2=Paulo Ricardo, EstadoAprovacao2="Aprovado"
       │              DataAprovacaoLidTec=2025-09-30
       │
       │  [8 dias]
       │
2025-10-08 15:00 ──── FlagAjusteADM=true (Fernanda)
2025-10-08 15:00 ──── Valorado=false, Macrovalorado=false  ← RESET FLAGS
2025-10-08 15:03 ──── Macrovalorado=true, Valorado=true    ← RE-SET (3 min)
2025-10-08 15:04 ──── Valorado=false                       ← TOGGLE AGAIN (6 seg)
2025-10-08 15:11 ──── Valorado=true, FlagAjusteADM=false   ← FINAL (7 min)
       │
       │  [4x toggles em 11 minutos = overhead administrativo puro]
       │
2025-10-09 18:29 ──── StackRank (Fernanda)
2025-10-16 23:06 ──── StackRank (Denise Cruz Ferrao)
       │
2025-10-21 12:08 ──── Aprovação Financeira (Paulo Ricardo)
       │              NumeroBOQ=841919
       │              Kanban: "Aprovação Financeira (BOQ - PO)"
       │
       │  [36+ dias em Aprovação Financeira — sem progressão]
       │
2025-10-27 ──── StackRank (Fernanda)
2025-10-31 ──── StackRank (Priscila)
2025-11-04 ──── StackRank (Fernanda)
2025-11-10 ──── StackRank (Fernanda)
2025-11-26 ──── StackRank (Fernanda) ← ÚLTIMO REGISTRO
       │
       ▼  ITEM ESTAGNADO — nunca atingiu "Resolved"
```

---

## 5. Lead Times

| Segmento | De | Até | Duração |
|----------|----|-----|---------|
| New → Macrovaloração | 2025-09-09 18:01 | 2025-09-09 18:09 | **8 min** |
| Macrovaloração → Valoração | 2025-09-09 18:09 | 2025-09-09 18:10 | **1 min** (ceremonial) |
| Valoração → Aprovação Lid Tec | 2025-09-09 18:10 | 2025-09-30 11:15 | **21 dias** |
| Aprovação Lid Tec → Aprovação Financeira | 2025-09-30 11:15 | 2025-10-21 12:08 | **21 dias** |
| Aprovação Financeira → ? | 2025-10-21 12:08 | 2025-11-26+ | **36+ dias** (estagnado) |
| **Ciclo total (criação → último registro)** | 2025-09-09 | 2025-11-26 | **78 dias** (incompleto) |

---

## 6. Análise de Overhead — Flags Toggle (2025-10-08)

Em 11 minutos, Fernanda executou 4 operações de toggle nas flags `Macrovalorado` e `Valorado`:

| Hora | Macrovalorado | Valorado | FlagAjusteADM |
|------|:---:|:---:|:---:|
| 15:00:52 | (inalterado) | (inalterado) | false→**true** |
| 15:00:56 | true→**false** | true→**false** | true |
| 15:03:58 | false→**true** | false→**true** | true |
| 15:04:04 | true | true→**false** | true |
| 15:11:14 | true | false→**true** | true→**false** |

**Impacto:** 5 revisões (rev 17-21) geradas sem qualquer mudança de estado. Puro overhead administrativo para ajustar flags de controle que deveriam ser automáticas.

---

## 7. Problemas Identificados

### P15 — Item estagnado em Aprovação Financeira (36+ dias)

- **Evidência:** Estado "Aprovação Financeira" desde 2025-10-21; último registro 2025-11-26. Nunca atingiu "Resolved".
- **Contraste:** MV #1117168 (FQA) atingiu "Resolved" em 2025-10-23 (44 dias de ciclo total). A MV #1117156 (VAS) está com 78+ dias e incompleta.
- **Impacto:** Bloqueio visível no pipeline financeiro. O item está "aprovado" tecnicamente (EstadoAprovacao2="Aprovado", DataAprovacaoLidTec preenchida) mas não progrediu para Resolved.
- **Hipótese:** O BOQ 841919 pode estar aguardando aprovação financeira consolidada. **Nota:** as MVs possuem BOQs distintos (VAS: 841919, FQA: 832868).

### P16 — Toggle caótico de flags (5 revisões em 11 minutos)

- **Evidência:** Revisões 17-21 (2025-10-08 15:00-15:11) — Fernanda alternou Macrovalorado/Valorado/FlagAjusteADM 4 vezes.
- **Impacto:** 5 revisões sem mudança de estado = 17% das 29 revisões totais gastas em ajuste de flags.
- **Causa provável:** Ausência de validação/automação no formulário; flags manuais que deveriam ser derivadas do estado do workflow.

### P17 — Transição Macrovaloração → Valoração em 1 minuto (ceremonial)

- **Evidência:** Rev 6 (18:09:06) → Rev 7 (18:10:10) — mesma pessoa (Paulo Ricardo), sessão contínua.
- **Padrão recorrente:** Idêntico ao observado em #1117168 (FQA). Os dois estados existem como etapas separadas no workflow mas são processados como um único passo na prática.
- **Impacto:** Estado intermediário que não agrega valor decisório — overhead estrutural do processo.

### P18 — Assimetria de closure entre MVs irmãs

- **Evidência:** #1117168 (FQA) → Resolved em 2025-10-23. #1117156 (VAS) → Aprovação Financeira desde 2025-10-21, sem progressão.
- **Inconsistência:** Ambas são filhas da mesma Iniciativa #1085522, referem o mesmo Epic #1078031, mas possuem BOQs distintos (VAS: 841919, FQA: 832868). A divergência de estado final sugere que o processo de aprovação financeira não é uniforme entre diretorias (IT Quality Tests vs IT Service Creation Solutions).

### P19 — 5 atores para um item de R$11.790

- **Evidência:** Fernanda (criação/flags), Paulo Ricardo (valoração/aprovação), Camilla (StackRank), Denise (StackRank), Priscila (StackRank).
- **Contexto:** 3 dos 5 atores participaram apenas para alterar StackRank (priorização), sem contribuição ao conteúdo do item.
- **Impacto:** Ratio atores/valor financeiro desproporcional para uma estimativa de 10 FP.

---

## 8. Métricas Comparativas — MV VAS (#1117156) vs MV FQA (#1117168)

| Métrica | #1117156 (VAS) | #1117168 (FQA) |
|---------|:-:|:-:|
| Valor (FP) | 10 | 21,16 |
| Valor (R$) | R$ 11.790,00 | R$ 2.000,89 |
| Taxa (R$/FP) | R$ 1.179 | R$ 94,56 |
| BOQ | 841919 | 832868 |
| NumeroPO | — | 4504614557 |
| Revisões | 29 | 32 |
| Updates | 30 | 34 |
| Comentários | 1 | 5 |
| Estado final | **Aprovação Financeira** | **Resolved** |
| Ciclo total | 78+ dias (incompleto) | 44 dias (completo) |
| Transição Macro→Valor | 1 min (ceremonial) | 17 horas (real) |
| Atores envolvidos | 5 | 7 |
| Toggle flags | 5 ops / 11 min | 6 ops / 2,5 min |
| Separação de duties | Não (Paulo valora e aprova) | Sim (Meire valora, Paulo aprova) |

**Conclusão da comparação:** As duas MVs são radicalmente diferentes em estrutura financeira — a taxa VAS é 12,5x mais cara por FP que a taxa FQA, e o valor VAS é 5,9x maior. São BOQs distintos (841919 vs 832868), fornecedores diferentes (Engineering vs FQA-ATOS) e diretorias diferentes (IT Service Creation Solutions vs IT Quality Tests). A MV FQA completou seu ciclo em 44 dias com trabalho técnico real entre Macro e Valoração (17h), enquanto a MV VAS está incompleta após 78+ dias apesar de transição ceremonial de 1 minuto.

---

## 9. Overhead Consolidado — Camada Portfolio (2 MVs + Iniciativa + Epic)

| Item | Revisões | Valor (R$) | Estado |
|------|:--------:|:----------:|:------:|
| Iniciativa #1085522 | 43 | R$ 13.790,89 (ValorIniciativa = soma MVs) | Closed |
| Epic #1078031 | 43 | R$ 13.790,89 (ValorEpic = mesma soma) | Resolved |
| MV #1117156 (VAS) | 29 | R$ 11.790,00 | Aprovação Financeira |
| MV #1117168 (FQA) | 32 | R$ 2.000,89 | Resolved |
| **Total** | **147 revisões** | **R$ 13.790,89** (VAS + FQA) | **Parcial** |

Para chegar a uma valoração de R$ 13.790,89 (10 + 21,16 = 31,16 FP), o processo gerou 147 revisões em 4 work items de portfolio, envolvendo pelo menos 10 atores distintos, ao longo de 78+ dias — e a MV VAS ainda não atingiu Resolved.

---

*Análise gerada a partir dos arquivos WorkItem-MacroValoracao-1117156.json, WorkItem-MacroValoracao-1117156-Revisoes.json e WorkItem-MacroValoracao-1117156-Updates.json.*
