# Trabalho de Conclusão de Curso

MBA USP / ESALQ

## Folha de Rosto

Trabalho de Conclusão de Curso apresentado para obtenção do título de especialista em  
**Engenharia de Software** – **2026**

---

### Título do trabalho de conclusão de curso

**Agentes de inteligência artificial assumindo personas no ciclo de vida de desenvolvimento de software**

---

### Autores

Yuri Franconeri¹\*; Jorge Carlos Valverde Rebaza²

¹ [Empresa ou Instituição]. [Titulação ou função ou departamento].  
[Endereço completo] – [Bairro]; [CEP] [Cidade], [Estado], Brasil

² [Empresa ou Instituição]. [Titulação ou função ou departamento].  
[Endereço completo] – [Bairro]; [CEP] [Cidade], [Estado], Brasil

\* autor correspondente: [email@email.com]

---

## Agentes de inteligência artificial assumindo personas no ciclo de vida de desenvolvimento de software

---

## Resumo

A engenharia de requisitos é uma das fases mais críticas do Ciclo de Vida de Desenvolvimento de Software (SDLC), pois falhas nessa etapa se refletiram em retrabalho, defeitos e perda de previsibilidade das entregas. Este trabalho investigou o impacto da introdução de um agente de inteligência artificial assumindo o papel de Product Owner (PO) na fase inicial do SDLC, com foco na elicitação, validação e estruturação de requisitos em itens de trabalho hierarquicamente organizados, da especificação funcional aos critérios de teste. A pesquisa adotou abordagem aplicada com delineamento exploratório-descritivo, conduzida por meio de estudo de caso único em ambiente corporativo de grande porte do setor de telecomunicações, caracterizado por alta complexidade organizacional e elevada variabilidade de requisitos, com análise documental comparativa dos artefatos produzidos. O agente foi construído em plataforma de agentes de inteligência artificial, dotado de recuperação contextual de informação a partir de bases documentais corporativas e integração operacional com a plataforma de gestão do SDLC. A caracterização do cenário pré-intervenção evidenciou concentração dos gargalos nas etapas anteriores ao desenvolvimento, especialmente na transição entre o entendimento de negócio e a formalização dos requisitos. Na comparação qualitativa dos artefatos antes e depois da intervenção, observaram-se maior padronização das histórias de usuário, critérios de aceitação mais explícitos e maior completude inicial dos artefatos produzidos, reforçando um modelo de colaboração humano-máquina sem eliminar a supervisão humana. Os resultados do caso analisado indicaram potencial de qualificação dos artefatos de requisitos, condicionado à existência de governança clara e processos previamente definidos.

**Palavras-chave:** engenharia de requisitos; product owner; histórias de usuário; sistemas agênticos; colaboração humano-máquina

---

## Introdução

O Ciclo de Vida de Desenvolvimento de Software (*Software Development Life Cycle*, SDLC) constitui uma estrutura metodológica central da Engenharia de Software, cuja finalidade é impor disciplina estruturada e previsível a um processo intrinsecamente complexo (ALAZZAWI; YAS; RAHMATULLAH, 2023). Esse modelo de governança decompõe o projeto em fases interdependentes (análise de requisitos, arquitetura, implementação, testes, implantação e manutenção), com o objetivo de otimizar a alocação de recursos, garantir a qualidade do produto e mitigar riscos ao longo de todo o ciclo.

Apesar da consolidação dessas estruturas metodológicas, a engenharia de software enfrenta desafios crônicos que transcendem soluções puramente técnicas e residem na natureza sistêmica e processual do desenvolvimento. Requisitos incompletos, ambíguos ou em constante mudança, aliados a comunicação deficiente entre partes interessadas e equipes técnicas, configuram uma problemática recorrente. A pressão por velocidade frequentemente resulta em atalhos que geram dívida técnica, código de difícil manutenção e ciclos de retrabalho, nos quais defeitos descobertos tardiamente elevam exponencialmente os custos de correção. Estudos empíricos demonstram que uma parcela significativa dos projetos de software não é concluída dentro do prazo e orçamento estipulados, com relatórios indicando que mais da metade enfrenta estouros orçamentários e que entre 19% e 31% são cancelados antes da conclusão (STANDISH GROUP, 2020).

Dentre as fases do SDLC, a engenharia de requisitos é reconhecida como uma das mais críticas e, simultaneamente, uma das mais suscetíveis a falhas. Deficiências nessa etapa propagam-se ao longo de todo o ciclo, manifestando-se em retrabalho, defeitos funcionais e divergências de escopo que comprometem a previsibilidade das entregas. Revisões sistemáticas recentes mapearam o potencial da IA generativa para apoiar atividades de engenharia de requisitos, incluindo elicitação, classificação e formalização de requisitos (CHENG et al., 2024). Contudo, a maior parte dos estudos concentra-se em aplicações assistivas pontuais, como geração de texto ou classificação automatizada, sem investigar empiricamente a atuação de agentes autônomos assumindo papéis completos no processo. Pesquisas sobre a perspectiva de praticantes quanto à aplicação de IA agêntica no SDLC reforçam a percepção de que há distância significativa entre o potencial teórico dessas abordagens e sua validação empírica em ambientes reais (AKBAR et al., 2025).

A inteligência artificial tem sido apontada como uma das principais alavancas para superar ineficiências históricas do desenvolvimento de software. Contudo, pesquisas sobre o estado do desenvolvimento assistido por IA revelam um cenário de impacto complexo. Embora a adoção tenha se tornado quase universal, a IA atua como um amplificador que potencializa tanto as capacidades das organizações de alto desempenho quanto as disfunções daquelas com processos frágeis (DORA, 2025). A simples aplicação de ferramentas de IA em processos deficientes não resolve os problemas subjacentes e pode intensificá-los, uma vez que o aumento de *throughput* (vazão de entregas por unidade de tempo) observado é frequentemente acompanhado de maior instabilidade na entrega.

Nesse contexto, distingue-se a IA assistiva da IA agêntica. Enquanto a IA assistiva opera em tarefas discretas sob direcionamento humano direto, os sistemas agênticos são projetados para atuar com autonomia em processos complexos, por meio de ciclos contínuos de percepção, planejamento, ação e reflexão (ACHARYA; KUPPAN; DIVYA, 2025). Esses sistemas transcendem a interação conversacional baseada em *Large Language Models* ao incorporar duas capacidades complementares. A primeira é a Geração Aumentada por Recuperação (*Retrieval-Augmented Generation*, RAG), que permite ancorar respostas em bases documentais específicas do domínio. A segunda é a integração com sistemas externos por meio de conectores padronizados, viabilizando a execução autônoma de ações em plataformas de gestão do SDLC (BORGHOFF; BOTTONI; PARESCHI, 2025). Essa combinação de autonomia, fundamentação contextual e capacidade de ação posiciona os agentes de IA como potenciais colaboradores ativos nos processos de engenharia de software.

Apesar do reconhecimento crescente desse potencial, a literatura apresenta uma lacuna relevante: não foram identificados estudos empíricos que avaliem, de forma estruturada e com critérios objetivos, o impacto de agentes de IA agêntica assumindo o papel de *Product Owner* (PO) na engenharia de requisitos. As pesquisas existentes abordam predominantemente a aplicação de IA generativa em atividades isoladas ou reportam percepções de praticantes sem mensuração comparativa dos artefatos produzidos. Essa lacuna é especialmente relevante diante da evidência de que a eficácia da IA está condicionada à qualidade dos processos organizacionais preexistentes, demandando investigações que considerem tanto as capacidades técnicas dos agentes quanto o contexto de governança e maturidade processual em que são inseridos.

O objetivo deste trabalho foi investigar, por meio de pesquisa aplicada com estudo de caso, o impacto da introdução de um agente de inteligência artificial assumindo o papel de PO na fase de engenharia de requisitos do SDLC. Especificamente, buscou-se avaliar a contribuição do agente (construído em plataforma de agentes de inteligência artificial, dotado de recuperação contextual de informação a partir de bases documentais corporativas e integração operacional com a plataforma de gestão do SDLC) para a melhoria da completude, qualidade e governança dos artefatos de requisitos, em comparação com o processo conduzido exclusivamente por atores humanos, em um ambiente corporativo de grande porte do setor de telecomunicações.

---

## Material e Métodos

A pesquisa caracterizou-se como aplicada, de natureza qualitativa, com delineamento exploratório-descritivo, conduzida por meio de estudo de caso único em ambiente corporativo de grande porte do setor de telecomunicações. Em razão de restrições de confidencialidade, os dados utilizados foram anonimizados, preservando-se as propriedades estruturais e operacionais do ambiente analisado. O estudo enquadrou-se nas hipóteses de dispensa de submissão a Comitê de Ética em Pesquisa, por se basear em análise documental de artefatos organizacionais sem identificação de participantes.

O objeto do estudo foi a persona de um Product Owner (PO) sênior consultivo, responsável pela estruturação inicial de iniciativas de negócio em itens de trabalho hierarquicamente organizados, da especificação funcional aos critérios de teste. A persona foi operacionalizada por meio de seis dimensões analíticas previamente definidas (contexto e problema, objetivos, escopo e entregáveis, partes interessadas e impacto, resultados esperados, riscos, premissas e restrições), utilizadas como referencial tanto para a criação de novos itens quanto para a revisão de itens existentes. A responsabilidade decisória sobre os artefatos produzidos permaneceu, em todos os casos, sob supervisão e controle do PO humano.

O agente foi construído em plataforma corporativa de agentes de inteligência artificial, com base em um modelo de linguagem de larga escala (Large Language Model, LLM) configurado por meio de instruções textuais explícitas que codificaram a persona, suas crenças profissionais, padrões de comunicação e restrições operacionais. As restrições incluíram a proibição de produção de dados sem confirmação humana, a vedação à assunção de compromissos de prazo em nome de terceiros e a obrigação de registrar lacunas de informação como pendências verificáveis. O modelo, sua versão e os parâmetros gerais de inferência foram fixados ao longo do estudo, de modo a reduzir a variabilidade entre execuções.

A fundamentação contextual do agente foi obtida por meio de Geração Aumentada por Recuperação (Retrieval-Augmented Generation, RAG), com base em duas fontes de conhecimento corporativas conectadas por meio de mecanismos de busca indexada. A primeira fonte correspondeu ao conjunto histórico de itens de trabalho da plataforma de gestão do SDLC, incluindo iniciativas, épicos, features, histórias de usuário, tarefas, casos de teste e defeitos. A segunda fonte correspondeu à base documental técnica corporativa (wiki), contendo decisões arquiteturais, padrões de processo e documentação de projetos anteriores. Trechos relevantes foram recuperados de forma dinâmica e incorporados ao contexto de geração das respostas, ancorando as interações em decisões previamente acordadas, no racional técnico registrado e na terminologia utilizada no ambiente analisado.

A camada de execução do agente foi composta por cinco ações operacionais sobre a plataforma de gestão do SDLC, disponibilizadas por meio de conectores padronizados: leitura de detalhes de itens de trabalho, criação de itens de trabalho, atualização de itens de trabalho, leitura de comentários e criação de comentários. As ações foram acionadas pelo próprio agente em função do contexto da interação e das instruções recebidas, e seus parâmetros de entrada e saída foram tratados como parte integrante do método para fins de rastreabilidade. A execução ocorreu sob identidade de serviço nominalmente atribuída ao agente, com permissões restritas ao escopo do projeto e registro automático de autoria em cada operação. Operações de criação e atualização foram registradas como evidências verificáveis no próprio repositório operacional, preservando trilha de auditoria.

O agente operou em dois modos complementares. No modo conversacional, o agente conduziu diálogos com solicitantes de negócio e com o PO humano, formulando uma única pergunta por interação, priorizando completude, clareza e verificabilidade dos requisitos, e submetendo cada proposta à confirmação humana antes do registro. No modo orientado a eventos, o agente foi acionado por três gatilhos automatizados emitidos pela plataforma de gestão do SDLC: criação de item de trabalho, atualização de item de trabalho e atribuição de item de trabalho. Em ambos os modos, o agente registrou comentários nos próprios itens, com observações específicas e referenciadas às dimensões analíticas, de forma a manter o racional acessível para revisão posterior.

A constituição do conjunto de dados pré-intervenção foi obtida por meio de análise documental de uma iniciativa real concluída na organização, selecionada por critérios previamente definidos: cobertura completa do ciclo (da concepção em épico até a entrega em produção), volume e diversidade de itens de trabalho suficientes para caracterizar o fluxo, e disponibilidade integral de revisões, atualizações e mensagens correlatas para reconstituição factual. A iniciativa selecionada foi exportada da plataforma de gestão do SDLC e composta por vinte e seis itens de trabalho hierarquicamente organizados (iniciativa, épico, features, histórias de usuário, tarefas, casos de teste, defeitos e entregas), além de anexos e mensagens de aprovação correspondentes. Cada item foi caracterizado individualmente quanto a tipo, estado, número de revisões, número de atualizações, número de atores envolvidos e transições de estado. O resultado dessa caracterização constituiu a linha de base do estudo, representando o cenário em que a engenharia de requisitos foi conduzida exclusivamente por atores humanos.

A constituição do conjunto de dados pós-intervenção foi obtida pela operação do agente sobre uma necessidade de negócio equivalente à da linha de base, resultando em itens de trabalho gerados de acordo com os modos conversacional e orientado a eventos descritos. A análise dos dois conjuntos seguiu abordagem qualitativa comparativa, confrontando-se artefatos elaborados sem e com o apoio do agente segundo critérios de padronização estrutural das histórias de usuário, completude e explicitação dos critérios de aceitação, rastreabilidade entre objetivos de negócio e itens de trabalho, e completude inicial dos artefatos produzidos. As observações e os artefatos resultantes foram registrados de forma a permitir a reprodução do procedimento por outros profissionais em ambientes equivalentes.

---

## Referências

ACHARYA, D. B.; KUPPAN, K.; DIVYA, B. Agentic AI: Autonomous Intelligence for Complex Goals—A Comprehensive Survey. **IEEE Access**, v. 13, p. 18912-18936, 2025. DOI: 10.1109/ACCESS.2025.3532853.

AKBAR, M. A.; KHAN, A. A.; HAMZA, M.; GHAFFAR, A.; HAJIKHANI, A. Agentic AI in Software Engineering: Practitioner Perspectives Across the Software Development Life Cycle. 2025. Disponível em: https://ssrn.com/abstract=5520159. Acesso em: 22 abr. 2026.

ALAZZAWI, A.; YAS, Q.; RAHMATULLAH, B. A Comprehensive Review of Software Development Life Cycle methodologies: Pros, Cons, and Future Directions. **Iraqi Journal for Computer Science and Mathematics**, v. 4, n. 4, p. 173-190, 2023.

BORGHOFF, U. M.; BOTTONI, P.; PARESCHI, R. Human-Artificial Interaction in the Age of Agentic AI: A System-Theoretical Approach. 2025. Disponível em: https://arxiv.org/pdf/2502.14000. Acesso em: 24 out. 2025.

CHENG, H.; HUSEN, J. H.; PERALTA, S. R.; JIANG, B.; YOSHIOKA, N.; UBAYASHI, N.; WASHIZAKI, H. Generative AI for Requirements Engineering: A Systematic Literature Review. 2024. Disponível em: https://arxiv.org/html/2409.06741v1. Acesso em: 24 out. 2025.

DORA. **State of AI-assisted Software Development 2025**. Google Cloud, 2025. Disponível em: https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf. Acesso em: 22 abr. 2026.

STANDISH GROUP. **CHAOS Report: Beyond Infinity**. The Standish Group, 2020. Disponível em: https://www.standishgroup.com/. Acesso em: 22 abr. 2026.
