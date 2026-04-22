## IT Task #1136722 — Análise Completa

### 1. Identidade

| Campo | Valor |
|-------|-------|
| ID | 1136722 |
| Tipo | IT Task |
| Título | Alteração da Fraseologia e Criação do Botão - inFlight - Copy |
| Parent | #1113005 |
| Copiado de | #1113040 |
| Código Demanda | 251078031 |
| Prioridade | 2 |
| Story Points | 1 |
| Estimativa Original | 10h |
| Effort | 10h |

---

### 2. Timeline Kanban Completa

| Data | Rev | Estado | Ator | Ação |
|------|-----|--------|------|------|
| 2025-09-29 11:58 | 1 | **Nova História** | Paulo Ricardo CS | Criado (cópia de #1113040); assigned Ana Maria |
| 2025-09-29 11:58 | 2 | Nova História | Paulo Ricardo CS | BugVendor → "ENGINEERING" |
| 2025-09-29 12:02 | 3 | Nova História | Paulo Ricardo CS | Reassigned: Ana Maria → Paulo Ricardo |
| 2025-10-08 14:11–14:47 | 4–12 | Nova História | Paulo Ricardo CS | **9 revisões em 36 min**: reescrita da Description com RF001/RF002/RF003, AS IS/TO BE, URL, DoD, AC. VendorGroup → "Engineering - VAS" |
| 2025-10-08 14:47 | 13 | Nova História | **Ana Maria LM** | **RevisadaPO = true** (aprovação PO) |
| 2025-10-13 14:03 | 14 | Nova História | **Franco Kaufmann** | AreaPath → Projeto_Service_Creation\\Waterfall |
| 2025-10-20 18:48 | 15 | Nova História | Paulo Ricardo CS | VendorGroup → "Engineering - OAM" |
| 2025-10-20 18:56 | 16 | **Em Refinamento** | Paulo Ricardo CS | StoryPoints = 1 |
| 2025-10-20 18:57 | 17 | **Em Valoração** | Paulo Ricardo CS | OriginalEstimate = 10h |
| 2025-10-27 10:39 | 18 | **Liberado p/ Dev** | Paulo Ricardo CS | — |
| 2025-10-27 10:42 | 19 | **Em Desenvolvimento** | Paulo Ricardo CS | StartDate 27/10, FinishDate 02/12, EntregaDev 10/11 |
| 2025-11-05 19:05 | — | — | **Rodrigo A. Oliveira** | Adicionou child #1178461 |
| 2025-11-11 11:54 | — | — | Paulo Ricardo CS | Linked Related #1184452 |
| 2025-12-04 15:24 | 20 | **Concluída** | Paulo Ricardo CS | ClosedDate, Effort = 10h |

---

### 3. Atores Mapeados

| Ator | Papel | Ações |
|------|-------|-------|
| **Paulo Ricardo C. Souza** (pcsouza) | Criador, especificador, executor | Criou, reassignou, escreveu 100% da especificação, operou todas as transições de estado, fechou |
| **Ana Maria L. Moreira** (amlmoreira) | PO / Revisora | Assignee inicial (herdada da cópia), marcou RevisadaPO = true |
| **Franco Kaufmann G. F. Junior** (fkgjunior) | Gestor de Projeto | Moveu para Projeto_Service_Creation\\Waterfall |
| **Rodrigo Alexandre Oliveira** (T3671925) | Desenvolvedor | Adicionou child WI #1178461 (presumivelmente task de implementação) |

---

### 4. Evolução do Conteúdo — Description, DoD e Acceptance Criteria

#### Description (3 versões):

| Versão | Conteúdo |
|--------|----------|
| Rev 1 (cópia) | User Story format: "EU COMO Marketing, DESEJO QUE no produto inFlight… PARA eliminar quebras de jornada" + URL de referência |
| Rev 4–8 | Reescrita completa com **RF001** (Ajustar Mensagem Orientativa — botão "CLICANDO AQUI"), **RF002** (Direcionamento para Reset de Senha — URL `auth3.tim.com.br`), **RF003** (Retornar para Inflight), screenshots AS IS/TO BE |
| Rev 13 (final) | Mesma estrutura RF001/RF002/RF003, com imagens movidas para attachments do Azure DevOps |

#### Definition of Done:

| Versão | Texto |
|--------|-------|
| Inicial (cópia) | "Sera substituida a fraseologia na jornada de reset de senha da aplicação inFlight" |
| **Final** | "Implementação deverá ser executada conforme contido no campo descrição" |

#### Acceptance Criteria:

| Versão | Texto |
|--------|-------|
| Inicial (cópia) | "Evidenciar que… exista um botão 'CLICANDO AQUI' que redirecione o usuário para a página de reset de senha da TIM (Webview)" |
| **Final** | "Documento Completo de Especificação funcional anexo" |

---

### 5. Problemas Identificados

#### P54 — Criação por cópia sem rastreabilidade formal
A IT Task foi criada como "Copy" manual de #1113040, não como decomposição hierárquica. Não há link de predecessor/sucessor — apenas "Related". A rastreabilidade do porquê da duplicação é nula.

#### P55 — Gap de 9 dias entre criação e especificação
Criada em 29/09, especificada em 08/10. Durante 9 dias, o item existia com uma Description em formato de user story herdada da cópia, sem requisitos funcionais.

#### P56 — Especificação concentrada em um único ator, sessão única de 36 minutos
Paulo Ricardo produziu individualmente 9 revisões (rev 4-12) entre 14:11 e 14:47 de 08/10. Toda a engenharia de requisitos (RF001-RF003, screenshots, URL, DoD, AC) foi produzida por **uma pessoa em meia hora**. Não há evidência de revisão técnica, design review, ou validação de stakeholder.

#### P57 — Revisão PO instantânea e sem profundidade
Ana Maria marcou `RevisadaPO = true` (rev 13) **dentro da mesma sessão** do Paulo — 14:47 no mesmo dia. A revisão PO de uma especificação com 3 requisitos funcionais + mockups levou no máximo minutos, sugerindo aprovação cerimonial.

#### P58 — Transições de estado cerimoniais
- **Nova História → Em Refinamento**: 21 dias parado, transição sem evidência de refinamento de equipe
- **Em Refinamento → Em Valoração**: **1 minuto** (18:56 → 18:57)
- **Em Valoração → Liberado p/ Dev**: 7 dias
- **Liberado → Em Desenvolvimento**: **3 minutos** (10:39 → 10:42)

As etapas de refinamento e valoração foram passadas em minutos. Não há evidência de estimativa coletiva, planning poker, ou qualquer cerimônia ágil real.

#### P59 — Acumulação de papéis
Paulo Ricardo simultaneamente: criou o item, escreveu a especificação, definiu DoD/AC, estimou (1 SP / 10h), operou todas as transições de estado, e fechou o item. Uma mesma pessoa é requisitante, especificador, gestor e encerrador.

#### P60 — DoD e AC enfraquecidos ao longo do tempo
- DoD original era específico ("substituir fraseologia") → final genérico ("conforme contido no campo descrição")
- AC original era verificável ("botão CLICANDO AQUI + redirect Webview") → final delegado ("documento anexo")

Ambos perderam testabilidade e verificabilidade, tornando impossível uma validação objetiva do completamento.

#### P61 — Sem etapa de teste/validação
O workflow foi `Em Desenvolvimento → Concluída` direto. Nenhum estado de QA, UAT, homologação, ou validação. A funcionalidade (substituição de fraseologia + botão com redirect WebView) foi considerada "concluída" sem evidência de teste.

#### P62 — Atraso na entrega vs. estimativa
DataEntregaDev era 10/11/2025. A task foi concluída em 04/12/2025 — **24 dias de atraso**. Considerando que a estimativa original era 10h, os 38 dias de ciclo (27/10 → 04/12) sugerem ou subestimação, ou bloqueios não documentados.

#### P63 — Mudança de vendor sem justificativa documentada
VendorGroup mudou de "Engineering - VAS" para "Engineering - OAM" (rev 15) — sem comentário ou justificativa registrada. Indica incerteza sobre qual equipe deveria executar.

#### P64 — Premissa não validada
O campo `PremissasAcordadas` diz "Este projeto NÃO altera a base elegível" — mas o requisito RF002 adiciona um redirect para uma WebView de reset de senha que **potencialmente** altera o fluxo de autenticação. A premissa não foi revalidada após a especificação detalhada.

---

### 6. Métricas

| Métrica | Valor |
|---------|-------|
| Lead Time (criação → conclusão) | **66 dias** (29/09 → 04/12) |
| Cycle Time (desenvolvimento) | **38 dias** (27/10 → 04/12) |
| Tempo em especificação | ~36 minutos (sessão única 08/10) |
| Tempo em "Nova História" | 21 dias (29/09 → 20/10) |
| Tempo Em Refinamento | 1 minuto |
| Tempo Em Valoração | 7 dias |
| Revisões de Description | 9 (todas no mesmo dia, mesmo autor) |
| Atores envolvidos | 4 |
| Atraso vs. DataEntregaDev | +24 dias |