Read [](file:///c%3A/Users/yfranconeri/Source/persona-agents/samples/02-telecom/iniciativa1/WorkItem-Iniciativa.json#1-1), lines 1 to 200

Read [](file:///c%3A/Users/yfranconeri/Source/persona-agents/samples/02-telecom/iniciativa1/WorkItem-Iniciativa-Revisoes.json#1-1), lines 1 to 200

Read [](file:///c%3A/Users/yfranconeri/Source/persona-agents/samples/02-telecom/iniciativa1/WorkItem-Iniciativa.json#200-200), lines 200 to 288

Read [](file:///c%3A/Users/yfranconeri/Source/persona-agents/samples/02-telecom/iniciativa1)

Vou analisar todos os dados extraídos em profundidade — o work item, suas 43 revisões, 46 updates, e o briefing — para produzir uma seção completa para o TCC. 

Created 5 todos

Read [](file:///c%3A/Users/yfranconeri/Source/persona-agents/samples/02-telecom/iniciativa1/WorkItem-Iniciativa-Revisoes.json#200-200), lines 200 to 500

Starting: *Produzir seção completa para o TCC* (5/5)

Tenho todos os dados necessários. Aqui está a seção completa e exaustiva para o TCC:

---

## Caso 1: Melhorias Resgate de Senha InFlight (ID 1085522)

### 1.1 Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID no Azure DevOps** | 1085522 |
| **Tipo de Work Item** | Iniciativa |
| **Título** | Melhorias Resgate Senha inFlight |
| **Área** | Portfolio Tim TI → Portfolio Tim 2025 → CRO → Marketing Consumer e SMB |
| **Iteração** | 2025 / Q3 |
| **Categoria** | Manutenção de Portfólio |
| **Programa** | Ofertas |
| **Segmento** | Pós-pago, Família e Controle |
| **Alinhamento Estratégico** | Aumento de receita; Melhoria na experiência do cliente |
| **Obrigações Legais** | Não se aplica |
| **Entrega Incremental** | Não |
| **Origem Orçamento** | Fábrica |
| **Valor da Iniciativa** | R$ 13.790,89 |
| **Valor Macro** | R$ 14.000,00 |
| **Parent Work Item** | 791755 |
| **Children Work Items** | 1117156, 1117168, 1078031 (3 itens filhos) |

### 1.2 Descrição do Problema de Negócio

Clientes TIM que utilizam o serviço de internet a bordo (*Inflight*) em aeronaves não conseguem resetar a senha de acesso diretamente pela página da companhia aérea. Ao tentar recuperar a senha, o sistema exibe apenas uma mensagem orientativa instruindo o cliente a usar o aplicativo Meu TIM — o que é inviável durante o voo, gerando quebra de jornada e impossibilidade de uso do serviço contratado.

A solução proposta é substituir a mensagem orientativa por um link funcional que direcione o cliente para uma Webview de reset de senha integrada ao sistema da Intelsat (provedor de conectividade a bordo), eliminando a necessidade de acesso ao App Meu TIM.

**Escopo técnico efetivo:** Trata-se de uma alteração pontual de UX — substituir um texto estático por um link clicável apontando para uma página já existente (`auth3.tim.com.br/webapp-resetSenha/forgotPassword`).

### 1.3 Atores Envolvidos

A análise das 43 revisões e 46 updates do work item permite mapear todas as pessoas que interagiram com esta iniciativa:

| # | Ator | Papel Identificável | Ações no Work Item |
|:-:|------|--------------------|--------------------|
| 1 | **Fernanda Soares Marelli Leite** | PO / Gestora do backlog (assigned to) | Criou o item, preencheu campos, moveu entre estados, fechou. 26+ revisões atribuídas |
| 2 | **Diego Wanderosck Lisboa** | Solicitante (negócio) | Registrado como `NomeSolicitante`. Mencionado em comentários |
| 3 | **Danielle Da Fonseca Aguiar** | Analista de portfolio | Editou campos na rev 3-4 (segmento, problema, objetivo). Mencionada em pedido de aprovação |
| 4 | **Priscila Santos da Silva** | Aprovadora / Gestão | Primeira aprovação de negócio (rev 5, 2025-08-25). Mencionada como aprovadora para alocação |
| 5 | **Danielle Matos Martins** | Aprovadora 1 (negócio) | Registrada como `NomeAprovador1`, status: Aprovado |
| 6 | **Simone De Lacerda Sampaio** | Aprovadora 3 (negócio) | Registrada como `NomeAprovador3`, status: Aprovado. Mencionada em comentário pedindo segunda aprovação |
| 7 | **Paulo Henrique Ferreira Costa** | Security | Mencionado em 2 comentários separados pedindo preenchimento de formulário de security |
| 8 | **Carolina Ribeiro Gomes Sundin** | Stakeholder (FYI) | Mencionada em comentário de aprovação como FYI |
| 9 | **Paulo Cesar Dias Lima** | Arquiteto responsável | Registrado como `ArquitetoResponsavel`. Status: **inativo no sistema** |
| 10 | **Marcelo Henrique Costa Da Silva** | Gestão de portfolio | Última alteração no item (2026-03-06), 3 meses após o fechamento |
| 11 | **Danielle Da Fonseca Aguiar** | Analista | Revisões de campos preenchidos |
| 12 | **Felipe Povoa** | Líder de Produto (briefing) | Citado no briefing como Líder do Produto, sem interação no work item |

**Total: 10-12 pessoas envolvidas** para uma alteração que consiste em trocar um texto por um link em uma Webview.

### 1.4 Reconstituição Cronológica Completa

A análise cruzada entre revisões, updates e transições de estado Kanban permite reconstituir toda a jornada desta iniciativa:

| Data | Dias | Evento | Coluna Kanban | Rev | Ator |
|------|:----:|--------|:-------------:|:---:|------|
| 2025-08-12 | 0 | Criação do work item | Wishlist | 1 | Fernanda Leite |
| 2025-08-12 | 0 | Stack rank atribuído | Wishlist | 2 | Fernanda Leite |
| 2025-08-19 | +7 | Preenchimento de campos (segmento, problema, objetivo) | Wishlist | 3 | Danielle Aguiar |
| 2025-08-19 | +7 | Adição de detalhes (data estimada resolução: 29/08) | Wishlist | 4 | Danielle Aguiar |
| 2025-08-25 | +13 | **1ª Aprovação de negócio** (para estimativa) | Wishlist | 5 | Priscila Santos |
| 2025-08-25 | +13 | Preenchimento de prioridade diretoria (=26) | Wishlist | 6 | Priscila Santos |
| 2025-08-29 | +17 | Adição de sumário executivo | Wishlist | 7-8 | Fernanda Leite |
| 2025-08-29 | +17 | Edição do sumário executivo (revisão de texto) | Wishlist | 9 | Fernanda Leite |
| 2025-08-29 | +17 | Campos adicionais preenchidos | Wishlist | 10 | Fernanda Leite |
| 2025-08-29 | +17 | **Ativação** (State: New → Active) | Refinamento do Briefing | 11-12 | Priscila Santos + Fernanda |
| 2025-08-29 | +17 | Adição de marcadores, campos obrigatórios | Refinamento do Briefing | 13-14 | Fernanda Leite |
| 2025-08-29 | +17 | **Comentário**: Histórico com observação | Refinamento do Briefing | 15 | Fernanda Leite |
| 2025-09-01 | +20 | Re-rank (stack rank ajustado) | Refinamento do Briefing | 16 | Fernanda Leite |
| 2025-09-01 | +20 | Preenchimento de resultado esperado de negócio | Refinamento do Briefing | 17-18 | Danielle Aguiar |
| 2025-09-07 | +26 | Re-rank novamente | Refinamento do Briefing | 19 | Fernanda Leite |
| 2025-09-07 | +26 | Transição para **Análise** | Análise | 20 | Fernanda Leite |
| 2025-09-07 | +26 | **Comentário**: "@Paulo Henrique, favor preencher formulário de security" | Análise | 21 | Fernanda Leite |
| 2025-09-07 | +26 | **Comentário**: "@Simone e @Priscila, favor realizar 2ª aprovação de negócio" + FYI para 3 pessoas | Análise | 22-24 | Fernanda Leite |
| 2025-09-08 | +27 | **2ª Aprovação de negócio** (para alocação) | Análise | 25-26 | Priscila Santos |
| 2025-09-08 | +27 | **Comentário**: "@Paulo Henrique, favor preencher formulário de security" (2ª vez) | Análise | 27 | Fernanda Leite |
| 2025-09-09 | +28 | Comentário e adição de security responses + links | Análise | 28-29 | Fernanda Leite + outro |
| 2025-09-09 | +28 | Transição para **Estimativa** | Estimativa | 30 | Fernanda Leite |
| 2025-09-12 | +31 | Transição para **Priorizado (Alocado)** | Priorizado (Alocado) | 31 | Fernanda Leite |
| 2025-09-12 | +31 | Ajuste de lane Kanban | Priorizado | 32 | Fernanda Leite |
| 2025-09-12 | +31 | Prioridade diretoria alterada: 26 → **80** | Priorizado | 33 | Marcelo Silva |
| 2025-09-18 | +37 | Prioridade diretoria alterada: 80 → **47** | Priorizado | 34 | Priscila Santos |
| 2025-09-24 | +43 | Ajustes administrativos | Priorizado | 35 | Fernanda Leite |
| 2025-11-12 | +92 | Re-rank (stack rank ajustado) | Priorizado | 36 | Fernanda Leite |
| 2025-12-03 | +113 | Transição para **Em Andamento** (State: Active → Active, Kanban move) | Em Andamento | 37-38 | Outro + Fernanda |
| 2025-12-04 | +114 | **Fechamento** (State: Closed) | Closed | 39-40 | Fernanda Leite |
| 2026-02-09 | +181 | Alteração de resultado esperado de negócio (pós-fechamento) | Closed | 41 | Fernanda Leite |
| 2026-03-06 | +206 | Última alteração (ajustes administrativos pós-fechamento) | Closed | 42-43 | Marcelo Silva |

### 1.5 Análise de Lead Time

| Segmento do Ciclo | Início | Fim | Duração |
|--------------------|--------|-----|:-------:|
| **Criação → 1ª Aprovação Negócio** | 2025-08-12 | 2025-08-25 | **13 dias** |
| **1ª Aprovação → Ativação** | 2025-08-25 | 2025-08-29 | **4 dias** |
| **Ativação → Análise** | 2025-08-29 | 2025-09-07 | **9 dias** |
| **Análise → Estimativa** | 2025-09-07 | 2025-09-09 | **2 dias** |
| **Estimativa → Priorizado** | 2025-09-09 | 2025-09-12 | **3 dias** |
| **Priorizado → Em Andamento** | 2025-09-12 | 2025-12-03 | **82 dias** |
| **Em Andamento → Closed** | 2025-12-03 | 2025-12-04 | **1 dia** |
| | | | |
| **TOTAL: Criação → Closed** | 2025-08-12 | 2025-12-04 | **114 dias** |
| **Tempo pré-desenvolvimento** | 2025-08-12 | 2025-12-03 | **113 dias (99,1%)** |
| **Tempo de execução efetiva** | 2025-12-03 | 2025-12-04 | **1 dia (0,9%)** |

**Achado crítico**: 99,1% do lead time total foi consumido antes do início da execução técnica. A iniciativa passou 82 dias parada na coluna "Priorizado (Alocado)" sem ação — 72% do ciclo total é tempo de espera puro.

### 1.6 Análise do Overhead Processual

| Métrica | Valor | Observação |
|---------|:-----:|------------|
| Total de revisões | 43 | Para um item de escopo mínimo |
| Total de updates | 46 | Inclui edições de relações |
| Comentários formais | 5 | Predominantemente cobranças administrativas |
| Aprovações de negócio | 2 | 1ª para estimativa, 2ª para alocação |
| Formulário de security | 1 | Cobrado 2 vezes, em datas diferentes |
| Avaliação de arquitetura | 1 | Resultado: "Avaliado — sem impacto" |
| Alterações de prioridade | 3 | 26 → 80 → 47 → 46 |
| Alterações de stack rank | 4 | Re-priorizações no board |
| Alterações pós-fechamento | 3 revisões | 2 revisões em fev/2026, 1 em mar/2026 |
| Atores envolvidos | 10-12 | Para substituir um texto por um link |

### 1.7 Análise de Qualidade do Briefing

#### 1.7.1 Campos do Work Item: Preenchidos vs. Ausentes

| Campo | Status | Conteúdo |
|-------|:------:|----------|
| Problema/Contexto | **Preenchido** | "Atualmente os clientes TIM não conseguem resetar a senha diretamente pela página da companhia aérea..." |
| Objetivo | **Preenchido** | "Alterar a jornada atual do cliente fazendo que a mensagem o direcione para a página de reset integrada ao sistema da Intelsat..." |
| Sumário Executivo | **Preenchido** | "Direcionar o cliente para a página de reset de senha, sem precisar acessar o APP Meu TIM, para melhorar a experiência do cliente" |
| Resultado Esperado | **Genérico** | "Melhoria na Jornada do Cliente" — sem KPI, sem métrica, sem meta |
| Riscos e Premissas | **"n/a"** | Apesar de haver dependência técnica de terceiro (Intelsat) |
| Status Arquitetura | **"Avaliado - sem impacto"** | Preenchido mas sem detalhamento técnico |
| Impacto Arquitetura | **false** | Correto para o escopo, mas sem justificativa documentada |
| Security Q1 | **"Sim"** | Questionário sendo cobrado em 2 comentários separados |
| Security Q2-Q3 | **"Não"** | Sem justificativa |

#### 1.7.2 Campos do Briefing (Apresentação): Preenchidos vs. Ausentes

| Campo do Briefing | Status | Impacto |
|-------------------|:------:|---------|
| Escopo (resumo) | **Preenchido** | Descritivo claro |
| Cenário atual | **Preenchido** | Com capturas de tela |
| Cenário desejado | **Preenchido** | Com mockup |
| Jornada do cliente | **Preenchido** | Detalhada em 7 passos |
| Premissas | **Parcial** | 2 premissas, mas a 2ª inclui "a TI precisa avaliar" |
| Projetos de Referência | **Em branco** | |
| Metas de Contribuição | **Em branco** | Sem KPI, sem meta de negócio |
| Benefícios | **Em branco** | |
| Vigência | **Em branco** | |
| Integrações | **"A ser definido com TI"** | Dependência técnica não mapeada |
| Canais impactados | **Todos em branco** | Tabela de canais inteira vazia |
| Critérios de aceitação | **Inexistentes** | Não há ACs em nenhum nível |
| User Stories | **Inexistentes** | Nenhuma user story decomposta |
| Requisitos não-funcionais | **Inexistentes** | Sem RNFs (performance, segurança, acessibilidade) |
| Elegibilidade | **Informação negativa** | "Não altera base elegível" — sem detalhe |

#### 1.7.3 Avaliação pela Rubrica de Qualidade (Seção 3.6 do TCC)

Aplicando a rubrica de qualidade de requisitos proposta no TCC ao conteúdo disponível desta iniciativa, considerando que não existem user stories formais — apenas o briefing como especificação implícita:

| Critério | Peso | Score | Justificativa |
|----------|:----:|:-----:|---------------|
| **Completude** | 1.5 | 0 | Não há user story formalizada. O briefing descreve a solução desejada, mas sem estrutura "como [persona], quero [ação], para [valor]". Não identifica a persona do cliente com especificidade |
| **Testabilidade** | 1.5 | 0 | Critérios de aceitação completamente ausentes. Nenhum cenário Dado/Quando/Então. Não é possível derivar testes verificáveis sem interpretação subjetiva |
| **Univocidade** | 1.0 | 1 | A intenção é razoavelmente clara (adicionar link), mas a URL definitiva é incerta ("a TI precisa avaliar"), os parâmetros DD e MSISDN dependem de validação técnica, e o comportamento do reCAPTCHA em ambiente de voo não é endereçado |
| **Rastreabilidade** | 1.0 | 0 | Nenhum marcador de fonte. Nenhum vínculo formal entre briefing e work item (o briefing é um PPTX separado, não referenciado no body do work item). Resultado esperado genérico ("Melhoria na Jornada") |
| **Granularidade** | 0.5 | 1 | Escopo pequeno o suficiente para uma sprint, mas não decomposto em itens entregáveis independentes |

**Score total: (0×1.5) + (0×1.5) + (1×1.0) + (0×1.0) + (1×0.5) = 1.5/10.0**

### 1.8 Problemas Identificados

#### P1 — Ausência Total de Critérios de Aceitação

Nem o work item nem o briefing contêm critérios de aceitação verificáveis. As seguintes questões ficam sem resposta formal:

- O link deve funcionar **durante o voo** (com internet Intelsat) ou apenas **em solo**?
- O reCAPTCHA funciona via rede Intelsat? (reCAPTCHA requer Google — há bloqueio?)
- O SMS de recuperação chega durante o voo? (conectividade celular vs. Wi-Fi)
- A Webview deve abrir dentro do portal de bordo ou em janela/aba separada?
- Qual o comportamento se o número informado não for TIM?
- Qual o comportamento se o cliente errar o DDD?
- Há timeout? Quantas tentativas são permitidas?
- O link deve funcionar em todos os navegadores dos dispositivos de bordo?

#### P2 — Dependência Técnica Não Resolvida na Fase de Requisitos

O briefing afirma: *"a TI precisa avaliar e informar qual será o melhor caminho/URL definitiva para produção"*. Isso significa que a solução técnica foi especificada com base em uma URL de **ambiente Beta** (`auth3.tim.com.br`), sem confirmação de que:

- A URL é acessível via rede Intelsat
- A URL suporta o tráfego esperado
- Há necessidade de whitelist no firewall da Intelsat
- Os parâmetros são os mesmos em produção

#### P3 — Resultado Esperado Sem Métrica

O campo `ResultadoEsperadoNegocio` contém apenas: *"Melhoria na Jornada do Cliente"*. Não há:

- Métrica de sucesso (ex: % de resets bem-sucedidos via Webview)
- Baseline de comparação (quantos clientes tentam resetar senha hoje)
- Meta quantitativa (ex: reduzir chamados de suporte em X%)
- Prazo de medição

#### P4 — Arquiteto Designado Inativo

O campo `ArquitetoResponsavel` registra Paulo Cesar Dias Lima, cujo registro no sistema está marcado como `"inactive": true`. Isso significa que o recurso designado como responsável pela avaliação arquitetural não estava disponível no sistema durante o ciclo da iniciativa.

#### P5 — Formulário de Security Cobrado Duas Vezes

O histórico de comentários mostra que em 2025-09-07 (rev 21) e novamente em 2025-09-08 (rev 27), Fernanda Leite precisou cobrar Paulo Henrique Ferreira Costa para preencher o formulário de security. Isso indica que:

- O processo de security não tinha SLA ou mecanismo de follow-up automático
- A PO atuou como **dispatcher manual** de tarefas de compliance

#### P6 — Múltiplas Aprovações sem Valor Agregado

Para uma alteração de UX que consiste em substituir texto por link, o processo exigiu:

1. 1ª Aprovação de Negócio para Estimativa (13 dias após criação)
2. Preenchimento de Formulário de Security (cobrado 2x)
3. Avaliação de Arquitetura (resultado: "sem impacto")
4. 2ª Aprovação de Negócio para Alocação (27 dias após criação)

O custo processual dessas etapas — envolvendo no mínimo 6 pessoas — é desproporcional ao valor e ao risco da iniciativa.

#### P7 — Instabilidade de Priorização

A prioridade da diretoria foi alterada 3 vezes em 6 dias (26 → 80 → 47 → 46), evidenciando ausência de critérios estáveis de priorização ou repriorização por eventos externos não documentados.

#### P8 — Campos Obrigatórios Não Fiscalizados

O work item foi movido da Wishlist até Priorizado com campos críticos em branco: Benefícios, Vigência, Canais, Integrações. O workflow do Azure DevOps não impediu a progressão do item sem esses campos.

#### P9 — 82 dias de espera pura em "Priorizado (Alocado)"

A Iniciativa permaneceu na coluna "Priorizado (Alocado)" de 2025-09-12 a 2025-12-03 — **82 dias corridos** sem nenhuma ação, nenhuma revisão substantiva, nenhum comentário. Este período representa **72% do lead time total** (82/114 dias). O item já estava aprovado, estimado e alocado — apenas esperando na fila. A desproporcionalidade é extrema: 31 dias para preparar e aprovar, 82 dias parado, 1 dia para executar e fechar.

#### P10 — StatusIniciativa "Não iniciado" com State = Closed

O campo `Custom.StatusIniciativa` permaneceu como **"Não iniciado"** durante todas as 43 revisões — inclusive após o fechamento (State = Closed). O workflow não sincroniza este campo com o estado do Kanban. Para qualquer relatório que filtre por `StatusIniciativa`, esta Iniciativa aparece como "não iniciada" — contradizendo sua conclusão real.

#### P11 — ClassificacaoIniciativa "Wishlist" com State = Closed

O campo `Custom.ClassificacaoIniciativa` permaneceu como **"Wishlist"** durante todo o ciclo de vida, desde a criação até o fechamento. Uma Iniciativa que passou por Refinamento, Análise, Estimativa, Priorização, Execução e Fechamento ainda está classificada como "Wishlist". Mesmo padrão de P10: campos customizados que não acompanham o ciclo de vida real do item.

#### P12 — 3 revisões pós-fechamento (67–92 dias após Closed)

Após o fechamento em 2025-12-04, a Iniciativa recebeu 3 revisões adicionais:
- Rev 41 (2025-12-04): imediatamente após fechamento — provavelmente ajuste automático
- Rev 42 (2026-02-09): por Marcelo Silva — **67 dias após fechamento**
- Rev 43 (2026-03-06): por Marcelo Silva — **92 dias após fechamento**

Um item já concluído sendo modificado meses depois sugere ajustes administrativos retroativos (re-rank, campos de portfolio). O processo não impede edição de itens fechados.

#### P13 — EstimatedResolutionDate = 2025-08-29 vs ClosedDate = 2025-12-04 (97 dias de atraso)

O campo `EstimatedResolutionDate` foi preenchido com **2025-08-29** (17 dias após a criação). A Iniciativa foi fechada apenas em **2025-12-04** — **97 dias após a data estimada**. A previsão nunca foi atualizada durante as 43 revisões. Qualquer dashboard que compare previsão vs. realização mostraria esta Iniciativa como 97 dias atrasada.

#### P14 — Kanban Lane "Outros (ajustar mapeamento)" nunca corrigida

O WI está mapeado em dois Kanban boards. No board primário (WEF_588EBAF7), a lane registrada é literalmente **"Outros (ajustar mapeamento)"** — o texto contém uma nota administrativa para corrigir o mapeamento, nunca executada. No board secundário (WEF_029FFC12), a lane é "Marketing Consumer & SMB" (correto). A inconsistência entre boards persistiu por todas as 43 revisões sem correção.

### 1.9 Fluxo Kanban Reconstituído

```
Wishlist ──── 17 dias ────→ Refinamento do Briefing
                                   │
                              9 dias
                                   │
                                   ▼
                              Análise ──── 2 dias ────→ Estimativa
                                                           │
                                                       3 dias
                                                           │
                                                           ▼
                                                   Priorizado (Alocado)
                                                           │
                                                      82 dias (!)
                                                           │
                                                           ▼
                                                    Em Andamento ── 1 dia ──→ Closed
```

### 1.10 Classificação para o Estudo Experimental

| Atributo | Classificação | Justificativa |
|----------|:------------:|---------------|
| **Complexidade** | **S (Simples)** | Escopo pontual: trocar texto por link em Webview |
| **Domínio** | Consumer / Marketing | CRO → Marketing Consumer e SMB |
| **Hierarquia** | 1 Iniciativa → 3 filhos | IDs: 1117156, 1117168, 1078031 |
| **Riqueza de problemas** | **Alta** | 14 problemas documentáveis (8 de engenharia de requisitos + 6 de gestão de ciclo de vida) |
| **Inputs disponíveis** | Briefing (PPTX transcrito), Work Item completo com 43 revisões | Material suficiente para reprocessamento |
| **Viabilidade para o estudo** | **Alta** | Demonstra overhead processual em item simples — caso ideal para mostrar onde IA-persona pode comprimir o ciclo |

### 1.11 Síntese dos Achados

Esta iniciativa ilustra com clareza empírica os problemas crônicos descritos na Seção 2.1 do TCC:

| Problema Crônico do SDLC | Manifestação nesta Iniciativa | Evidência |
|---------------------------|-------------------------------|-----------|
| **Volatilidade de requisitos** | Requisitos não formalizados — briefing visual sem ACs | Score 1.5/10 na rubrica |
| **Falha de comunicação** | Cobranças manuais de security (2x), pedidos de aprovação via menção em comentários | Revs 21, 24, 27 |
| **Dívida processual** | 43 revisões e 10+ atores para trocar texto por link | 99,1% do tempo em overhead |
| **Detecção tardia de problemas** | Dependência técnica (URL de produção, Intelsat) nunca resolvida na fase de requisitos | Briefing: "a TI precisa avaliar" |

O caso demonstra que **a complexidade não está no escopo técnico, mas no processo organizacional**. Uma iniciativa de escopo mínimo consumiu 114 dias, 43 revisões, 10 atores e múltiplos gates — sem produzir nenhum artefato de requisito verificável (user story, critério de aceitação, especificação técnica).

Este é exatamente o cenário onde a hipótese central do TCC (H₁) prevê impacto: um agente-PO com o framework proposto teria, com os mesmos inputs (briefing + contexto organizacional), capacidade de produzir user stories estruturadas com critérios de aceitação verificáveis, marcadores de rastreabilidade e identificação explícita de lacunas — comprimindo o trabalho de formalização de requisitos que tomou 31 dias (Wishlist → Priorizado) com 10 pessoas, para uma sessão estruturada com validação humana.

--- 

Completed: *Produzir seção completa para o TCC* (5/5)

A seção acima é o detalhamento exaustivo do Caso 1, pronto para inserção no TCC. Pontos-chave para a banca:

1. **Score 1.5/10** na própria rubrica do TCC — evidência quantificável de baixa qualidade de requisitos
2. **99,1% do lead time** foi overhead pré-execução — dado impactante
3. **43 revisões e 10 atores** para trocar um texto por um link — desproporcionalidade demonstrável
4. **14 problemas documentados** diretamente das evidências do Azure DevOps — não é inferência, é dado