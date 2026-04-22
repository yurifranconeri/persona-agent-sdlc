# Análise de Ciclo de Vida — User Story #1113109

## 1. Ficha Técnica

| Campo | Valor |
|:------|:------|
| **ID** | 1113109 |
| **Tipo** | User Story |
| **Título** | Integração com a Intelsat *Escopo Negativo* |
| **Projeto (atual)** | Projeto_Service_Creation |
| **Area Path** | Projeto_Service_Creation\Waterfall |
| **Iteration Path** | Projeto_Service_Creation\Waterfall |
| **State** | Concluída |
| **Reason** | Moved out of state Nova História |
| **Board Column** | TIR em Produção |
| **Assigned To** | Ana Maria Lopes Moreira |
| **Created By** | Ana Maria Lopes Moreira |
| **Created Date** | 2025-09-05 |
| **Changed By** | Franco Kaufmann Gaspar Ferreira Junior |
| **Changed Date** | 2025-10-13 |
| **Closed Date** | 2025-10-08 |
| **Closed By** | Ana Maria Lopes Moreira |
| **Finish Date** | 2025-10-08 |
| **State Change Date** | 2025-10-08 |
| **Priority** | — (não definida) |
| **Value Area** | Business |
| **Código Demanda** | 251078031 |
| **Bug Vendor** | .NÃO IDENTIFICADO |
| **Percentual Automação** | 0% |
| **User Story Testável** | false |
| **Revisada PO** | false |
| **Sem Impacto** | false |
| **IdMacroValoracao** | 0 |
| **StackRank** | 1999996906 |
| **Comment Count** | 2 |
| **Revisões** | 14 |
| **Updates** | 15 |
| **Parent** | #1113105 (Feature — Integração, escopo negativo) |

### Escopo Negativo — Justificativa Técnica

> "A página de reset de senha é inviável na Intelsat, pois a Intelsat não autoriza o captcha que é recomendação de segurança da TIM nesse processo de autenticação do cliente."

Campo: `EscopoNegativoStory.TIMDM`, preenchido por Paulo Ricardo Castellanos Souza em 2025-09-09.

### Descrição (resumo semântico)

**EU COMO** Marketing  
**DESEJO QUE** seja implementada integração da página de reset de senha da TIM ao sistema da Intelsat, via Webview, conforme jornada indicada no #1113130  
**PARA** eliminar quebras de jornada e redirecionamentos desnecessários (obrigação de acessar APP Meu TIM)

URL de referência: `auth3.tim.com.br/webapp-resetSenha/forgotPassword?layout=meutimapp&loginType=USER&channel=4&msisdn=DD%"MSISDN"`

---

## 2. Relações

| Tipo | WI | Nome/Observação | Projeto |
|:-----|:---|:-----------------|:--------|
| **Parent** | #1113105 | Feature — Integração (escopo negativo, Closed) | Projeto_Service_Creation |
| Related | #1113130 | Attachment — "Anexo II - Jornada inFlight" (auto-link por menção na description) | Projeto_Service_Creation |

**Nota:** Apenas 2 relações. Nenhum filho (IT Task), nenhum link com Test Request ou Entrega. A US é uma folha isolada da árvore de execução.

---

## 3. Migração de Projeto

| Período | Projeto | Area Path |
|:--------|:--------|:----------|
| Criação (rev 1–12) | Portfolio Tim TI | Portfolio Tim TI\Portfolio Tim 2025\CRO\Marketing Consumer e SMB |
| Final (rev 13–14) | Projeto_Service_Creation | Projeto_Service_Creation\Waterfall |

A US foi criada em Portfolio Tim TI (projeto de governança) e migrada para Projeto_Service_Creation (projeto de execução) nas revisões finais — **direção oposta** à do Epic pai #1078031, que fez Projeto_Service_Creation → Portfolio Tim TI.

---

## 4. Cronologia de Estados

| # | Estado | Entrada | Saída | Duração | Ator da Transição |
|:-:|:-------|:--------|:------|:-------:|:------------------|
| 1 | Nova História | 2025-09-05 | 2025-10-08 | **33 dias** | Ana Maria Lopes Moreira |
| 2 | Concluída | 2025-10-08 | — | — | Ana Maria Lopes Moreira |

**Ciclo total: 33 dias** (2025-09-05 → 2025-10-08)

Transição direta: Nova História → Concluída. Todos os estados intermediários do workflow (Refinada, Em Desenvolvimento, Em Teste, etc.) foram saltados.

---

## 5. Cronologia Detalhada de Revisões

| Rev | Data | Ator | Ação |
|:---:|:----:|:-----|:-----|
| 1 | 2025-09-05 21:06 | Ana Maria | Criação. Título: "Integração com a Intelsat". Parent: #1113105 |
| 2 | 2025-09-05 21:14 | Ana Maria | Description adicionada |
| 3 | 2025-09-05 21:27 | Ana Maria | Description revisada |
| 4 | 2025-09-05 21:55 | Ana Maria | Description revisada novamente |
| — | 2025-09-05 21:55 | Ana Maria | Related link adicionado (#1113130) |
| 5 | 2025-09-05 22:05 | Ana Maria | Description revisada (4ª versão) |
| 6 | 2025-09-09 18:18 | Paulo Ricardo | Campo EscopoNegativoStory preenchido |
| 7 | 2025-09-09 18:19 | Paulo Ricardo | Comentário #1 |
| 8 | 2025-09-09 22:07 | Ana Maria | Comentário #2 |
| 9 | 2025-09-10 21:28 | Ana Maria | IdMacroValoracao definido |
| 10 | 2025-09-11 17:59 | Fabio Prazeres | StackRank definido |
| 11 | 2025-09-12 19:40 | Ana Maria | Título alterado → "Integração com a Intelsat *Escopo Negativo*" |
| 12 | 2025-10-08 14:57 | Ana Maria | State: Nova História → Concluída. Board: TIR em Produção. ClosedDate/FinishDate definidos |
| 13 | 2025-10-08 14:58 | Ana Maria | Campos adicionais |
| 14 | 2025-10-13 14:03 | Franco Kaufmann | Última revisão (provável migração de projeto) |

---

## 6. Atores (4)

| # | Ator | Papel Observado | Revs |
|:-:|:-----|:----------------|:----:|
| 1 | Ana Maria Lopes Moreira | Criadora, redatora, fechamento | 1–5, 8–9, 11–13 |
| 2 | Paulo Ricardo Castellanos Souza | Decisão técnica (escopo negativo), comentário | 6–7 |
| 3 | Fabio Prazeres Da Silva | StackRank (classificação) | 10 |
| 4 | Franco Kaufmann Gaspar Ferreira Junior | Revisão final / migração | 14 |

---

## 7. Problemas Identificados

### P179 — "Concluída" + "TIR em Produção" para US escopo negativo
**Severidade:** Alta | **Categoria:** Semântica de estados

A US está em estado "Concluída" e board column "TIR em Produção" — termos que implicam trabalho entregue em produção. Nenhum trabalho foi executado — o escopo foi negado por inviabilidade técnica (Intelsat não autoriza captcha). O workflow de User Story não possui estado dedicado para escopo negativo, forçando o uso de "Concluída" como fechamento genérico. Qualquer relatório que conte USs "Concluídas" como entregues computará esta US falsamente como throughput.

---

### P180 — Título como metadado informal ("*Escopo Negativo*")
**Severidade:** Média | **Categoria:** Modelagem de dados

O status de escopo negativo foi codificado no título com asteriscos: `"Integração com a Intelsat *Escopo Negativo*"`. O campo dedicado `EscopoNegativoStory.TIMDM` existe e está preenchido com a justificativa técnica. Mas o título é o principal sinal visual — filtragem e reporting dependem de pattern matching em texto livre em vez de campo estruturado.

---

### P181 — Skip de todos os estados intermediários
**Severidade:** Média | **Categoria:** Integridade do workflow

A US transitou diretamente de "Nova História" para "Concluída" em um único update (rev 12), saltando todos os estados intermediários (Refinada, Em Desenvolvimento, Em Teste, etc.). Embora justificável para escopo negativo, o Reason "Moved out of state Nova História" é auto-gerado e não documenta o motivo real da transição.

---

### P182 — 29 dias entre decisão técnica e fechamento formal
**Severidade:** Alta | **Categoria:** Lead time

| Marco | Data | Lag |
|:------|:----:|:---:|
| EscopoNegativoStory preenchido (decisão técnica) | 2025-09-09 | — |
| Título atualizado com "*Escopo Negativo*" | 2025-09-12 | +3 dias |
| State → Concluída (fechamento formal) | 2025-10-08 | +29 dias |

A decisão de inviabilidade técnica era conhecida desde 2025-09-09 (justificativa documentada por Paulo Ricardo). A US permaneceu em "Nova História" por mais 29 dias após a decisão, gerando atividade editorial desnecessária (revs 9–11: IdMacroValoracao, StackRank, título).

---

### P183 — 14 revisões e 4 atores para zero entregas
**Severidade:** Média | **Categoria:** Overhead operacional

Uma user story que não produziu nenhum deliverable acumulou:
- 14 revisões + 15 updates
- 4 atores distintos
- 4 versões da description (revs 2–5, todas em 1 hora)
- 2 comentários
- 33 dias de ciclo

Todo o esforço editorial é overhead puro — a US já era inviável antes da primeira revisão da description.

---

### P184 — Migração bidirecional inversa ao Epic
**Severidade:** Média | **Categoria:** Governança de dados

| WI | Direção da migração |
|:---|:--------------------|
| Epic #1078031 | Projeto_Service_Creation → Portfolio Tim TI |
| US #1113109 | Portfolio Tim TI → Projeto_Service_Creation |

A US migra na direção **oposta** à do Epic avô. Não existe padrão ou regra documentada sobre qual projeto deve hospedar cada nível da hierarquia. O resultado é que a US reside em um projeto diferente do seu avô Epic.

---

### P185 — RevisadaPO=false e UserStoryTestavel=false
**Severidade:** Baixa | **Categoria:** Completude de campos

A US foi fechada como "Concluída" sem revisão do PO (`RevisadaPO=false`) e marcada como não testável (`UserStoryTestavel=false`). Para escopo negativo, a decisão de inviabilidade **é** a revisão — mas o campo não reflete esse fato. O PO (ou equivalente funcional) participou ativamente (Ana Maria fez 10 das 14 revisões) mas o flag formal permanece false.

---

### P186 — Description referencia Attachment WI (#1113130) como requisito
**Severidade:** Baixa | **Categoria:** Acoplamento estrutural

A description da US contém hyperlink para `#1113130` ("Anexo II - Jornada inFlight") — um work item do tipo Attachment que contém um PPTX. O requisito da user story depende de um documento armazenado em um WI customizado que por sua vez está 3 níveis de indireção abaixo do Epic (Epic → Documents Repository → Attachment). Se qualquer WI intermediário for excluído ou movido, a referência de requisito se quebra.

---

### P187 — Description iterada 4 vezes em 1 hora sem controle de versão semântico
**Severidade:** Baixa | **Categoria:** Overhead editorial

A description foi criada e revisada 4 vezes nas revs 2–5, entre 21:14 e 22:05 de 2025-09-05 (51 minutos). Cada revisão gerou um update completo com snapshot de campos. O Azure DevOps não oferece diff nativo entre versões de description — as 4 versões são opacas. Para uma US que seria negada 4 dias depois, o polimento da description é overhead sem retorno.

---

## 8. Árvore Hierárquica (posição deste WI)

```
Iniciativa #1085522 (Closed)
└─ Epic #1078031 (Resolved)
   ├─ Feature #1113005 (New — ativa)
   │  └─ User Story #1113040 (Refinada)
   │     └─ IT Task #1136722 (Concluída)
   ├─ Feature #1113105 (Closed — escopo negativo)
   │  └─ User Story #1113109 (Concluída — escopo negativo) ← ESTE WI
   ├─ Documents Repository #1113128 (New)
   │  ├─ Attachment #1113129 (New)
   │  └─ Attachment #1113130 (New) ← referenciado na description desta US
   └─ Feature #1183520 (New) — Rollout e Pós Rollout [DM: 251070811 ⚠️]
```

---

## 9. Tabela Acumulada de Problemas

| WI | Tipo | Problemas | Qtd |
|:---|:-----|:----------|:---:|
| #1085522 | Iniciativa | P1–P14 | 14 |
| #1078031 | Epic | P166–P178 | 13 |
| #1113005 | Feature (ativa) | P15–P38 | 24 |
| #1113105 | Feature (escopo neg.) | P137–P144 | 8 |
| #1113040 | User Story | P39–P56 | 18 |
| **#1113109** | **User Story (escopo neg.)** | **P179–P187** | **9** |
| #1136722 | IT Task | P57–P68 | 12 |
| #1117156 | MV VAS | P69–P80 | 12 |
| #1117168 | MV FQA | P81–P88 | 8 |
| #1164264 | Test Request | P89–P96 | 8 |
| #1173498 | Test Case | P97–P102 | 6 |
| #1173533 | Test Case | P103–P108 | 6 |
| #1173534 | Test Case | P109–P114 | 6 |
| #1179903 | Entrega | P115–P120 | 6 |
| #1184452 | Bug | P121–P128 | 8 |
| #1199583 | Reteste | P129–P136 | 8 |
| #1193756 | Entrega | (nos .md existentes) | — |
| #1132619 | Entrega (template) | (nos .md existentes) | — |
| #1113128 | Documents Repository | P160–P165 | 6 |
| #1113129 | Attachment | P154–P159 | 6 |
| #1113130 | Attachment | P145–P150, P152–P153 | 8 |
| **Total** | | **P1–P187 (P151 inval.)** | **186** |

**Próximo P-number disponível: P188**