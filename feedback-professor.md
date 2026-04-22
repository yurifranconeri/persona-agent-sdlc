Revisei teu trabalho na plataforma mas te compartilho por aqui, também, meus comentários.

O aluno propõe e descreve um agente de IA atuando como Product Owner na engenharia de requisitos, apoiado por RAG e integrações via APIs e MCP, e reporta resultados preliminares de melhora na estruturação de histórias de usuário e rastreabilidade, com um diagnóstico inicial do fluxo. Há, porém, pontos de atenção a considerar para reduzir erros no TCC final: o desenho experimental ainda não isola o efeito do agente de mudanças de processo, as métricas estão parcialmente definidas e não padronizadas, há risco de inferência causal prematura, e a implementação descrita carece de detalhamento suficiente para replicabilidade e auditoria técnica (configuração do RAG, avaliação de qualidade, governança e controle de variabilidade).


Dessa maneira, listo os potenciais conflitos técnicos com sugestões de melhora visando evitar problemas na versão final do TCC:

1. Precisa melhorar a introdução, levantamento da bibliografia com casos similares mesmo que em outros contextos, a necessidade de enfrentar o problema (lacuna) e dizer exatamente o que será feito.

2. Métricas operacionais pouco definidas, “5 bugs por cada dia de desenvolvimento estimado” não especifica denominador, tipo de bug (produção, QA, regressão), severidade, janela temporal, nem como “dia estimado” é calculado. O aluno deve normalizar indicadores (ex.: bugs por story point, por KLOC, por release) e explicitar regras de contagem e fonte.

3. Benchmark implícito sem referência, o texto afirma “maturidade baixa a intermediária” e “referências amplamente adotadas” sem citar o framework/benchmark (DORA, Flow Metrics, etc.) e sem thresholds. O aluno deve citar a(s) referência(s) e declarar os critérios de classificação.

4. Pré-pós intervenção sem controle, os achados pós-agente são majoritariamente qualitativos (“maior recorrência”, “menor necessidade”) e sem mensuração comparável ao baseline. O aluno deve definir um protocolo de avaliação pré-registrado, com mesma janela temporal, mesma unidade de análise, e, se possível, grupo controle (time/produto sem agente) ou desenho quasi-experimental (diferença-em-diferenças).

5. Risco de causalidade indevida, há narrativa de que gargalos de requisitos “explicam” bugs e retrabalho, mas sem análise de ligação causal (ex.: rastreio requisito-defeito, classificação de causa raiz), o aluno deve incluir método de atribuição (RCA, taxonomia de defeitos, linkage por IDs) e reportar proporções verificáveis.

6. Confidencialidade e dados simulados, o uso de dados anonimizados e “quando necessário, dados simulados” pode introduzir viés e comprometer validade externa. O aluno deve separar claramente o que é real versus simulado, justificar o método de simulação, e mostrar que propriedades estatísticas relevantes foram preservadas (distribuições, variância, correlações). Isto é vital para dar validade técnica e reproducibilidade ao projeto.

7. Replicabilidade insuficiente do RAG, descreve-se “fontes heterogêneas” e recuperação dinâmica, mas faltam detalhes de chunking, embeddings, índice, top-k, reranking, critérios de atualização, e tratamento de versões de documentos. O aluno deve documentar arquitetura e parâmetros mínimos para reprodução e auditoria.

8. Avaliação de qualidade do agente incompleta, não há métrica objetiva para “redução de ambiguidades” e “melhor padronização”, o aluno deve criar rubrica de qualidade de requisitos (completude, testabilidade, univocidade, rastreabilidade), aplicar avaliação cega por avaliadores independentes e reportar concordância (ex.: kappa).

9. Controle de variabilidade do LLM ausente. Não se descreve modelo, temperatura, prompts, políticas de memória, nem reprodutibilidade (semente/versões). Então, o aluno deve fixar parâmetros, registrar versões e executar repetição experimental para estimar variância e robustez.

10. Efeito de “amplificador” citado mas não operacionalizado, o texto afirma que IA amplifica práticas existentes, porém não mede governança/processo. O aluno deve operacionalizar variáveis de processo (ex.: padronização de briefing, Definition of Ready, qualidade do backlog) e testar interação “qualidade do processo versus ganho do agente”.

11. Integrações via MCP e APIs sem especificação de segurança e governança. Isto pode ser opcional, mas há criação/atualização de itens de trabalho automatizada sem definir controles (permissões, logs, aprovação humana, rollback). Então, o aluno deve descrever salvaguardas e trilha de auditoria.

12. Definição de unidade experimental e amostragem ausente, não está claro quantas demandas/histórias foram analisadas, como foram selecionadas, e se há sazonalidade. O aluno deve declarar N, critérios de inclusão, e garantir comparabilidade (complexidade, domínio, prioridade).

13. Erros de redação que afetam precisão técnica. Há typo como “ferramenta de gstão” e inconsistências de termos. O aluno deve revisar tecnicamente para evitar ambiguidade e ruído na metodologia.





Listo a seguir, as melhorias necessárias para garantir sucesso no desenvolvimento do projeto de TCC:

1. Fechar um desenho experimental mensurável, com hipóteses testáveis, grupo controle ou estratégia quasi-experimental, janela temporal fixa e critérios de inclusão.

2. Definir um “painel” de métricas por etapa da engenharia de requisitos (tempo de refinamento, nro. de iterações de esclarecimento, completude de critérios de aceitação, retrabalho downstream, defeitos atribuídos a requisitos), com regras de cálculo e fontes.

3. Documentar a implementação do agente para replicabilidade, arquitetura RAG, parâmetros, versionamento, governança, logs, e protocolos de aprovação humana.

4. Transformar “melhora percebida” em evidência, rubrica de qualidade aplicada de forma cega, estatística básica (efeito, IC, significância quando aplicável) e análise de sensibilidade/ablação (sem RAG, sem MCP, apenas assistivo vs agêntico).

5. Explicitar limites e riscos, onde o agente falha, como evita alucinação, como lida com conflitos de fontes e como garante rastreabilidade confiável.