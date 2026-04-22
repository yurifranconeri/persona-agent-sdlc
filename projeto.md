# Agentes de Inteligência Artificial Assumindo Personas no Ciclo de Vida de Desenvolvimento de Software

| | |
|---|---|
| **Aluno(a):** | Yuri Franconeri |
| **Orientador(a):** | Jorge Carlos Valverde Rebaza |
| **Curso:** | Engenharia de Software |

---

## Introdução

O Ciclo de Vida de Desenvolvimento de Software, ou *Software Development Life Cycle* (SDLC), é uma estrutura metodológica central da Engenharia de Software. Sua finalidade é impor uma disciplina estruturada e previsível a um processo intrinsecamente complexo e criativo, a construção de software ou soluções tecnológicas. O SDLC é um modelo de governança que decompõe o projeto em fases interdependentes, por exemplo, análise e descoberta do produto, seus requisitos, a arquitetura, a codificação e implementação técnica, os diversos testes funcionais e não funcionais, as estratégias de implementação, seguida da manutenção e operação da solução, com o objetivo de otimizar a alocação de recursos, garantir a qualidade do produto e, crucialmente, mitigar riscos.

Apesar da existência desses frameworks, a engenharia de software enfrenta uma problemática crônica, a dificuldade central reside na gestão da complexidade e na alta taxa de incerteza inerentes ao desenvolvimento da solução. Os problemas fundamentais não são somente técnicos, mas sistêmicos e processuais como na volatilidade de requisitos e falha de comunicação com requisitos incompletos, ambíguos ou em constante mudança, aliados à uma comunicação deficiente entre as partes interessadas e as equipes técnicas. Dívida técnica é causada pela pressão por velocidade (cronogramas irrealistas) frequentemente levando a atalhos e resultando em código ou solução de baixa qualidade que é difícil de manter, evoluir ou entender, e em ciclos de "retrabalho", onde os defeitos (bugs) são descobertos tardiamente, especialmente devido a testes inadequados, aumentando exponencialmente o custo da correção.

O impacto dessa problemática é medido há décadas. Estudos empíricos na área demonstram historicamente que uma baixa porcentagem dos projetos de software é concluída com sucesso dentro do prazo e do orçamento estipulados, evidenciando uma necessidade crítica de otimização dos processos de desenvolvimento. Relatórios recentes e análises de mercado indicam que mais da metade dos projetos enfrenta estouros orçamentários significativos (com alguns custando quase o dobro do estimado) e que uma porcentagem relevante (próxima de 19-31%) é cancelada antes mesmo da conclusão.

A introdução da Inteligência Artificial tem sido vista como a principal alavanca para superar essas ineficiências históricas. No entanto, a simples aplicação de ferramentas de IA em processos falhos não apenas falha em resolvê-los, como pode potencializá-los. Esta tensão é capturada por pesquisas sobre o estado de desenvolvimento de software assistido por IA. Embora a adoção da IA tenha se tornado quase universal (90% dos profissionais a utilizam), seu impacto é complexo, a IA atua como um "amplificador", ela potencializa as forças das organizações de alto desempenho e as disfunções daquelas com dificuldades. Embora a adoção da IA esteja agora associada a um aumento no *throughput* (vazão) da entrega de software, ela continua a aumentar a instabilidade da entrega.

É neste ponto que a integração humano-máquina no SDLC com IA assistiva e agêntica emerge como um paradigma distinto, as ferramentas de IA assistiva focam em tarefas discretas em conjunto com o humano e os sistemas agênticos são projetados para atuar no processo de forma autônoma podendo ser supervisionada pelas pessoas envolvidas. Esses agentes prometem a capacidade de raciocinar, planejar e orquestrar fluxos de trabalho complexos, abordando os desafios sistêmicos de colaboração e automação cognitiva. Diferente dos modelos tradicionais, os sistemas agênticos são definidos por sua autonomia, eles operam através de um ciclo contínuo de percepção, planejamento, ação e reflexão, permitindo-lhes decompor objetivos de alto nível em tarefas executáveis, tomar decisões de forma independente e adaptar-se a novos cenários. Essas soluções deixam de ser ferramentas somente baseadas em conversas munidos com *Large Language Model* (LLMs) e tornam-se colaboradores ativos com capacidade de utilização de Geração Aumentada por Recuperação (*Retrieval-Augmented Generation*, RAG) e ferramentas para extensão de suas capacidades utilizando *Model Context Protocol* (MCP), protocolos e frameworks para comunicação entre agentes, criando todo um sistema de agentes autônomos.

Nessa reimaginação do SDLC orquestrado pela sinergia de humano-máquina e prevendo cada vez maior aderência nas organizações de um organograma composto por agentes, haverá tarefas e responsabilidades, divididas e em colaboração mútua, entre eles para cada um dos envolvidos no SDLC. Recordando que esses papéis poderão ser realizados parcialmente ou em totalidade por agentes de IA, e adicionando a problemática da baixa eficiência em projetos complexos e IA atuando como um "amplificador" podendo aumentar a instabilidade da entrega surge a importância e motivação desta pesquisa. Analisar o impacto e a aplicação de agentes de Inteligência Artificial nas diversas fases do ciclo de desenvolvimento de software, dividindo papéis, responsabilidades e tarefas complexas com humanos, nessa colaboração mútua, justificando-se pela necessidade de modernizar a engenharia de software e mitigar seus desafios tradicionais.

---

## Objetivo

O objetivo principal deste projeto é responder à seguinte pergunta:

> *"De que forma e com qual impacto mensurável os agentes de inteligência artificial (IA), especificamente IA agêntica e generativa, assumindo personas, papéis e responsabilidades, em conjunto com pessoas podem ser aplicados para melhorar o ciclo de desenvolvimento de software (SDLC)?"*

Para alcançar tal objetivo, esse trabalho irá:

- Mapear, por meio de uma revisão sistemática da literatura, as principais personas do ciclo de desenvolvimento de software, suas tarefas, distingui-las e dividi-las entre agentes assistivos, agênticos e pessoas;
- Apresentar a distinção conceitual e prática entre IA assistiva (focada em tarefas discretas) e IA agêntica (focada na orquestração de workflows complexos) e suas aplicações atuais no SDLC;
- Estabelecer um framework conceitual que posicione a IA como uma solução para a automação cognitiva de processos, abordando os desafios sistêmicos que a simples aceleração de tarefas não resolve;
- Validar o impacto da IA agêntica e da IA assistiva trabalhando em conjunto com pessoas por meio de uma Prova de Conceito (PoC) de uma esteira de desenvolvimento de software;
- Analisar os resultados da PoC para quantificar a diferença de impacto entre um modelo de trabalho tradicional, sem IA assistiva e agêntica, e outra com colaboração humano-máquina (assistivo) junto com um modelo de orquestração agêntica (autônomo), propondo diretrizes para a integração eficaz de agentes no SDLC.

---

## Material e Métodos

Este projeto de pesquisa caracteriza-se como um estudo de natureza aplicada, empregando uma abordagem metodológica mista (qualitativa-quantitativa) para responder à pergunta de pesquisa. A metodologia será estruturada em fases sequenciais, alinhadas aos objetivos específicos do trabalho, combinando uma pesquisa exploratória e bibliográfica com uma prova de conceito.

O estudo será conduzido em **cinco fases principais**:

### Fase 1: Revisão Sistemática da Literatura (RSL)

Em linha com o primeiro objetivo específico, esta etapa qualitativa e exploratória mapeará exaustivamente as personas, papéis e tarefas críticas que compõem o Ciclo de Vida de Desenvolvimento de Software (SDLC), analisando a literatura existente para estabelecer uma distinção conceitual e prática clara entre a IA assistiva (focada na automação de tarefas discretas) e a IA agêntica (focada na orquestração autônoma de processos).

### Fase 2: Desenvolvimento do Framework Conceitual

Será utilizado os dados sintetizados da RSL como base para os requisitos do desenvolvimento que posicionará a IA não como uma ferramenta, mas como um sistema de "automação cognitiva de processos", capaz de assumir responsabilidades e interagir com diferentes estágios do SDLC.

### Fase 3: Desenvolvimento da Prova de Conceito

A partir dos resultados será desenvolvido o núcleo experimental e quantitativo da pesquisa, visando validar o impacto das diferentes abordagens de IA. Terá início pela definição do cenário simulado, suas premissas e requisitos, por exemplo, uma equipe multidisciplinar, com o propósito de entrega de software com metodologias ágeis para a entrega de uma de software com excelência percorrendo todo o SDLC.

Serão estabelecidos de um a três cenários de teste para a execução de tarefas pré-definidas do SDLC (ex: análise de requisitos, desenvolvimento e testes) com as respectivas ferramentas tradicionais de desenvolvimento de software, porém com o apoio de IA assistiva e IA agêntica em um sistema de multiagentes.

Antes do início do desenvolvimento ou configuração dos agentes, será criado um ambiente simulado que mimetiza um ecossistema de desenvolvimento profissional para servir como base para o SDLC, contando com:

- Ferramentas padrão de gestão de requisitos
- Repositório de código-fonte
- Ambiente de desenvolvimento integrado
- Plataforma para revisão e fusão de código
- Esteira de integração e entrega contínua
- Entre outros

Para agilizar o desenvolvimento dos agentes será utilizado modelos de IA generativas prontos e treinados, bem como plataformas de Inteligência Artificial, computação e serviços integradores com arquitetura sem servidor, tanto para o desenvolvimento dos agentes como para uma aplicação de exemplo.

Devido à abrangência do tema e da complexidade do desenvolvimento, serão selecionadas de duas a três personas centrais, por exemplo:

- **Dono do produto**
- **Desenvolvedor**
- **Engenheiro de testes**

Para serem emuladas ou personificadas pelos agentes com um pequeno conjunto de tarefas específicas, como criar histórias de usuário, codificar, documentar, escrever testes unitários e executar plano de testes. Com essas definições será possível implementar uma parte do SDLC orquestrado e apoiado por agentes.

### Fase 4: Coleta e Análise de Métricas

Com o objetivo de quantificar a diferença entre modelos de trabalho, esta fase focará na coleta e análise de métricas de desempenho. As métricas a serem avaliadas serão definidas após a pesquisa e elas podem ser, por exemplo:

| Categoria | Métricas |
|-----------|----------|
| **Produtividade** | Tempo de ciclo, número de tarefas concluídas |
| **Qualidade** | Taxas de defeitos, cobertura de testes, assertividade, quantidade de retrabalho |
| **Eficiência** | Custo computacional, intervenção humana necessária |

### Fase 5: Análise e Diretrizes

Os dados serão analisados estatisticamente para identificar diferenças significativas e mensurar o impacto da IA no SDLC. Com os resultados consolidados da RSL (qualitativos) e do protótipo (quantitativos) serão utilizados para propor um conjunto de diretrizes e boas práticas para a integração eficaz de agentes de IA no SDLC, respondendo à pergunta de pesquisa.

---

## Resultados Esperados

Este piloto demonstrará a capacidade prática de um sistema de inteligência artificial na personificação de papéis, responsabilidades e tarefas para a automação e trabalho em conjunto com humanos no ciclo de desenvolvimento para a engenharia de software.

Adicionalmente, a análise dos dados do protótipo e da revisão sistemática produzirá os seguintes resultados analíticos:

- Uma confirmação (baseada em evidências) da eficácia da IA Generativa em algumas fases do SDLC
- A quantificação do impacto da aplicação de agentes autônomos
- Um conjunto validado de métricas (quantitativas e qualitativas) para a aferição do impacto da IA no SDLC
- Uma análise do papel estratégico da IA agêntica como ferramenta de colaboração híbrida, distinguindo sua atuação da automação simples de tarefas e destacando seu papel no planejamento iterativo de problemas complexos

---

## Cronograma de Atividades

| Atividades Planejadas | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|-----------------------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:--:|
| Planejamento da pesquisa | ✓ | | | | | | | | | |
| Pesquisa e revisão da literatura | ✓ | ✓ | | | | | | | | |
| Desenvolvimento do framework | | ✓ | | | | | | | | |
| Desenvolvimento do protótipo | | ✓ | ✓ | ✓ | | | | | | |
| Resultados preliminares | | | | ✓ | ✓ | | | | | |
| Coleta de dados | | | | | ✓ | ✓ | | | | |
| Análise dos dados | | | | | | ✓ | ✓ | | | |
| Redação do trabalho | | | | | | ✓ | ✓ | | | |
| Revisão do orientador | | | | | | | ✓ | ✓ | | |
| Correções e entrega | | | | | | | | ✓ | ✓ | |
| Apresentação e defesa | | | | | | | | | ✓ | ✓ |

---

## Referências

1. AKBAR, M. A.; KHAN, A. A.; HAMZA, M.; GHAFFAR, A.; HAJIKHANI, A. **Agentic AI in Software Engineering: Practitioner Perspectives Across the Software Development Life Cycle**. September 16, 2025. Disponível em: https://ssrn.com/abstract=5520159 ou http://dx.doi.org/10.2139/ssrn.5520159

2. ACHARYA, D. B.; KUPPAN, K.; DIVYA, B. Agentic AI: Autonomous Intelligence for Complex Goals—A Comprehensive Survey. **IEEE Access**, v. 13, p. 18912-18936, 2025. DOI: 10.1109/ACCESS.2025.3532853

3. ALAZZAWI, A.; YAS, Q.; RAHMATULLAH, B. A Comprehensive Review of Software Development Life Cycle methodologies: Pros, Cons, and Future Directions. **Iraqi Journal for Computer Science and Mathematics**, v. 4, n. 4, p. 173-190, 2023.

4. CHENG, H.; HUSEN, J. H.; PERALTA, S. R.; JIANG, B.; YOSHIOKA, N.; UBAYASHI, N.; WASHIZAKI, H. **Generative AI for Requirements Engineering: A Systematic Literature Review**. 2024. Disponível em: https://arxiv.org/html/2409.06741v1. Acesso em: 24 out. 2025.

5. LENGYEL, F. **AI Agents in Software Testing and Test Automation**. 2025. Disponível em: https://www.researchgate.net/publication/389859723_AI_Agents_in_Software_Testing_and_Test_Automation. Acesso em: 24 out. 2025.

6. BORGHOFF, U. M.; BOTTONI, P.; PARESCHI, R. **Human-Artificial Interaction in the Age of Agentic AI: A System-Theoretical Approach**. 2025. Disponível em: https://arxiv.org/pdf/2502.14000. Acesso em: 24 out. 2025.

7. DORA. **State of AI-assisted Software Development 2025**. Google Cloud, 2025. Disponível em: https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf

8. STANDISH GROUP. **CHAOS Report: Beyond Infinity**. The Standish Group, 2020. Disponível em: https://www.standishgroup.com/