Entendido — espero as Macro Valorações e IT Task. Enquanto isso, aqui vai a camada User Story com o que já temos:

---

## 1.3 Camada User Story: Work Item 1113040

### 1.3.1 Ficha Técnica

| Campo | Valor |
|-------|-------|
| **ID** | 1113040 |
| **Tipo** | User Story |
| **Título Final** | Alteração da Fraseologia e Criação do Botão - inFlight |
| **Estado Final** | **Refinada** |
| **Projeto** | Projeto_Service_Creation → Waterfall |
| **Iteração** | Projeto_Service_Creation → Waterfall |
| **Código Demanda** | 251078031 |
| **Criada por** | Ana Maria Lopes Moreira |
| **Assigned To** | Ana Maria Lopes Moreira |
| **Revisões** | 27 |
| **Updates** | 31 |
| **Comentários** | 4 |
| **Parent** | 1113005 (Feature) |
| **Related** | 1113130, 1136722, 1164264, 1171260, 1171261, 1171262 (6 itens) |
| **Revisada pelo PO** | **false** |
| **User Story Testável** | true |
| **Percentual Automação** | 0% |
| **Análise Security** | Não |
| **IdMacroValoracao** | 1117156 |

### 1.3.2 Conteúdo da User Story

**Título:** Alteração da Fraseologia e Criação do Botão - inFlight

**Descrição (campo Description, decodificado do HTML):**

> **EU COMO** Marketing
>
> **DESEJO QUE** no produto **inFlight**, a atual mensagem orientativa exibida na opção **"Esqueci minha senha"** seja substituída por um **"botão"** que redirecione o cliente à página de reset de senha da TIM (Webview), conforme jornada indicada no **#1113130**
>
> Como referência, segue abaixo a URL atualmente utilizada pelo APP Beta para reset de senha. No entanto, é necessário que a área de TI valide e nos informe o caminho mais adequado:
> `https://auth3.tim.com.br/webapp-resetSenha/forgotPassword?layout=meutimapp&loginType=USER&channel=4&msisdn=DD%"MSISDN"`
>
> **PARA** eliminar quebras de jornada como a obrigação de acessar o APP Meu TIM, garantindo uma experiência mais fluida e sem interrupções.

**Critérios de Aceitação (campo AcceptanceCriteria):**

> Evidenciar que, no lugar da frase orientativa para o cliente recuperar a senha pelo **"APP Meu TIM"**, exista um **botão "CLICANDO AQUI"** que redirecione o usuário para a **página de reset de senha da TIM (Webview)**

**Definition of Done (campo DefinionOfDone [sic]):**

> Detalhamento funcional que será entregue esta contido na Task abaixo
> https://dev.azure.com/timbrasil/Portfolio%20Tim%20TI/_workitems/edit/1136722

**Premissas Acordadas:**

> Este projeto NÃO altera a base elegível.

### 1.3.3 Cronologia da User Story

| Data | Dias | Evento | Estado | Rev | Ator |
|------|:----:|--------|:------:|:---:|------|
| 2025-09-05 20:30 | 0 | Criada | Nova História | 1 | Ana Maria |
| 2025-09-05 20:32 | 0 | Edição de Description (1ª vez) | Nova História | 2 | Ana Maria |
| 2025-09-05 21:04 | 0 | Edição de Description (2ª vez) | Nova História | 3 | Ana Maria |
| 2025-09-05 21:21 | 0 | Título renomeado + Description (3ª vez) | Nova História | 4 | Ana Maria |
| 2025-09-05 21:23 | 0 | Premissas preenchidas | Nova História | 5 | Ana Maria |
| 2025-09-05 22:05 | 0 | Título ajustado ("Inflight" → "inFlight") + Description (4ª vez) | Nova História | 6 | Ana Maria |
| **2025-09-09** | +4 | **→ Refinada** + AnaliseSecurity = Não | Refinada | 7 | Paulo Ricardo |
| 2025-09-09 | +4 | Edições (Ana Maria) | Refinada | 8 | Ana Maria |
| 2025-09-11 | +6 | Edições | Refinada | 9 | Ana Maria |
| 2025-09-12 | +7 | Alterações + relação adicionada | Refinada | 10-12 | Novo ator + Ana Maria |
| 2025-09-17 | +12 | Edições | Refinada | 13 | Ana Maria |
| 2025-09-29 | +24 | Relação adicionada | Refinada | — | Paulo Ricardo |
| 2025-10-08 | +33 | Edições | Refinada | 14-15 | Ana Maria + Paulo Ricardo |
| 2025-10-13 | +38 | Edições | Refinada | 16 | Paulo Ricardo |
| 2025-10-23 | +48 | Relação adicionada | Refinada | — | Paulo Ricardo |
| 2025-11-11 | +67 | Edições | Refinada | 17 | Novo ator |
| **2025-11-12** | +68 | StartDate definido + DataInicioRefinamento | Refinada | 18-20 | Ana Maria |
| 2025-11-17 | +73 | Edições | Refinada | 21 | Ana Maria |
| 2025-11-18 | +74 | Edições + relação adicionada | Refinada | 22 | Carolina Sundin |
| **2025-12-04** | — | ***Epic resolvido + Iniciativa fechada*** | — | — | — |
| 2026-01-28 | +145 | Edições (pós-fechamento pais) | Refinada | 23 | Novo ator |
| 2026-02-05 | +153 | Edições | Refinada | 24 | Carolina Sundin |
| 2026-03-02 | +178 | Edições | Refinada | 25 | Novo ator |
| 2026-03-10 | +186 | Última alteração | **Refinada** | 26-27 | Karyne Gallindo |

### 1.3.4 Achado Crítico: Inconsistência de Estado na Hierarquia

| Nível | ID | Estado Final | Data Encerramento |
|-------|:--:|:------------:|:-----------------:|
| Iniciativa | 1085522 | **Closed** | 2025-12-04 |
| Epic | 1078031 | **Resolved** | 2025-12-04 |
| User Story | 1113040 | **Refinada** | ***Nunca encerrada*** |

**Achado P47 — O Epic foi resolvido e a Iniciativa foi fechada, mas a User Story nunca saiu do estado "Refinada".** Isso significa que os itens-pai foram encerrados sem que o item-filho tivesse sequer entrado em desenvolvimento. A User Story permanece ativa com edições até março de 2026 — **3 meses** após o fechamento dos pais. O workflow não impede que pais sejam fechados com filhos em estados anteriores.

### 1.3.5 Avaliação pela Rubrica de Qualidade (Seção 3.6 do TCC)

Agora temos uma User Story formalizada — aplicável diretamente à rubrica:

| Critério | Peso | Score | Justificativa |
|----------|:----:|:-----:|---------------|
| **Completude** | 1.5 | **1** | Formato "EU COMO / DESEJO QUE / PARA" presente, mas a persona é **"Marketing"** (área organizacional, não persona de uso). Não é possível testar do ponto de vista do usuário final. A ação está razoavelmente descrita. O valor é genérico ("experiência fluida") |
| **Testabilidade** | 1.5 | **1** | Existe critério de aceitação, mas é **único e impreciso**: "Evidenciar que exista um botão 'CLICANDO AQUI'". Não usa formato Dado/Quando/Então. Não cobre: cenário de erro, campo inválido, reCAPTCHA, SMS não recebido, timeout, browser do avião. Critério é de existência visual, não de comportamento |
| **Univocidade** | 1.0 | **1** | Ambiguidade residual: "botão" vs "link" (o briefing diz link sublinhado, a story diz botão). URL marcada como "TI precisa validar". "Conforme jornada indicada no #1113130" — referência externa não inlineada, interpretação depende de outro item |
| **Rastreabilidade** | 1.0 | **1** | Referencia #1113130 (jornada) e URL. Mas sem marcadores `[Fonte:]`. A story não cita o briefing original. A Description contém informação técnica (URL) misturada com requisito de negócio. Vínculo com objetivo estratégico ("Melhoria na experiência do cliente") é implícito |
| **Granularidade** | 0.5 | **2** | Escopo pequeno — substituir texto por botão/link. Entregável em 1 sprint se as dependências estivessem resolvidas |

**Score: (1×1.5) + (1×1.5) + (1×1.0) + (1×1.0) + (2×0.5) = 6.0/10.0**

**Comparação com o score do briefing (nível Iniciativa):**

| Nível | Score | Δ |
|-------|:-----:|:-:|
| Briefing / Iniciativa (sem User Story) | 1.5/10 | — |
| User Story formalizada | 6.0/10 | +4.5 |

A formalização em User Story melhorou significativamente a completude. Porém, 6.0/10 ainda é insuficiente em três dimensões: **persona errada** ("Marketing" em vez de persona de uso), **critério de aceitação único e superficial**, e **ambiguidade técnica não resolvida** ("botão" vs "link", URL de produção).

### 1.3.6 Análise Detalhada dos Problemas de Requisitos (P47–P53)

#### P47 — Inconsistência de Estado Parent-Child (redetalhado acima)

O Epic e a Iniciativa foram encerrados em 2025-12-04, mas a User Story permanece em "Refinada" com alterações até 2026-03-10. O workflow permite que pais sejam fechados com filhos ativos.

#### P48 — Persona Incorreta na User Story

A persona é "**Marketing**" — uma área organizacional, não uma persona de uso. Quem se beneficia da funcionalidade é o **cliente TIM usuário do serviço Inflight**, não o Marketing. O formato correto seria:

> "**EU COMO** cliente TIM que utiliza o serviço de internet a bordo"

Usar "Marketing" como persona confunde o **solicitante da demanda** com o **beneficiário da funcionalidade**. Isso viola o princípio fundamental de personas em user stories (Cooper, 1999) e reduz a testabilidade — não é possível validar critérios de aceitação da perspectiva do "Marketing".

#### P49 — Critério de Aceitação Único e Superficial

O AC é uma única frase: *"Evidenciar que exista um botão 'CLICANDO AQUI' que redirecione o usuário para a página de reset de senha"*. Problemas:

| Aspecto | Status | Impacto |
|---------|:------:|---------|
| Formato Dado/Quando/Então | **Ausente** | Não automatizável como teste |
| Cenário de sucesso (happy path) | **Parcial** | Descreve existência visual, não fluxo completo |
| Cenário de erro | **Ausente** | Número inválido? DDD errado? Cliente não-TIM? |
| Cenário de borda | **Ausente** | reCAPTCHA em rede Intelsat? SMS em 30.000 pés? |
| Número mínimo de ACs (≥3) | **Não atende** | 1 AC vs. mínimo 3 da rubrica |
| Verificabilidade | **Fraco** | "Evidenciar" é ambíguo — screenshot? Teste automatizado? Log? |

#### P50 — Definition of Done Delegada a Outro Work Item

O campo `DefinionOfDone` [nota: typo no nome do campo — "Definion" em vez de "Definition"] contém:

> "Detalhamento funcional que será entregue esta contido na Task abaixo"
> → link para #1136722

Isso significa que a DoD da User Story **não está na User Story**. Está num outro work item (Task). A rastreabilidade depende de seguir um link externo, e a completude da especificação só é visível ao cruzar múltiplos itens.

#### P51 — Description Editada 4 Vezes em 90 Minutos

| Rev | Horário | Intervalo | Alteração |
|:---:|---------|:---------:|-----------|
| 1 | 20:30 | — | Versão inicial |
| 2 | 20:32 | 2 min | Edit 1 |
| 3 | 21:04 | 32 min | Edit 2 |
| 4 | 21:21 | 17 min | Edit 3 + título renomeado |
| 5 | 21:23 | 2 min | Premissas adicionadas |
| 6 | 22:05 | 42 min | Edit 4 + título ajustado (capitalização) |

6 revisões em 95 minutos no mesmo dia, pela mesma pessoa. Isso indica que a story foi sendo "descoberta" durante a escrita — não havia clareza prévia do que escrever. Cada revisão do Description é uma iteração de refinamento que poderia ter sido evitada com extração estruturada dos inputs do briefing.

#### P52 — Campo `RevisadaPO = false`

Apesar de a story existir há 6+ meses, com 27 revisões e 31 updates, o campo `RevisadaPO` permanece **false**. Isso indica que:

- A story nunca passou por validação formal do Product Owner, **ou**
- O campo não é utilizado consistentemente no processo

Em qualquer caso, a rastreabilidade da aprovação de negócio da story é inexistente.

#### P53 — Ambiguidade "Botão" vs. "Link"

| Fonte | Termo Usado |
|-------|-------------|
| Briefing (PPTX) | "link sublinhado" / "CLICANDO AQUI" sublinhado em azul |
| Iniciativa (work item) | "botão que leve para a página de reset" |
| Epic (Description) | "botão que leve para a página de reset de senha da TIM (Webview)" |
| User Story (Description) | "botão" que redirecione |
| User Story (AC) | "botão 'CLICANDO AQUI'" |
| Briefing (cenário desejado visual) | Texto sublinhado clicável (não é um botão, é um link inline) |

O briefing visual mostra claramente um **link de texto sublinhado** dentro de um parágrafo. Mas todos os work items referem-se a um **"botão"**. São elementos de UI distintos. Um desenvolvedor pode implementar um botão (elemento `<button>`) quando o esperado era um link (`<a href>`). Essa ambiguidade nunca foi resolvida em 186 dias.

### 1.3.7 Quadro Consolidado Atualizado (3 Camadas)

| Métrica | Iniciativa | Epic | User Story | **Total** |
|---------|:----------:|:----:|:----------:|:---------:|
| Revisões | 43 | 43 | 27 | **113** |
| Updates | 46 | 51 | 31 | **128** |
| Comentários | 5 | 11 | 4 | **20** |
| Atores distintos | 10 | 8 | 7+ | **17+ únicos** |
| Lead time | 114 dias | 121 dias | 186+ dias (aberto) | — |
| Estado final | Closed | Resolved | **Refinada** | Inconsistente |
| Score rubrica | 1.5/10 | — | 6.0/10 | — |

### 1.3.8 Itens Relacionados Pendentes de Análise

| ID | Relação | O que espero encontrar |
|:--:|---------|----------------------|
| **1113005** | Parent (Feature) | Feature correspondente à F1 do briefing |
| **1113130** | Related (mencionado na Description) | Work item de "jornada" referenciado como especificação |
| **1136722** | Related (mencionado na DoD) | **IT Task** — onde está o detalhamento funcional real |
| 1164264 | Related | Work item cross-referenciado |
| 1171260, 1171261, 1171262 | Related | Possivelmente Test Cases |
| **1117156, 1117168** | Children da Iniciativa | **Macro Valorações** de estimativa de custo |
| **1183520** | Child do Epic (4ª Feature) | Feature adicionada tardiamente sem registro |

---

Quando tiver os dados da IT Task (1136722), das Features/Macro Valorações e dos Test Cases, complemento. A IT Task é especialmente importante — é onde a DoD está delegada, então é ali que a especificação real deve viver.