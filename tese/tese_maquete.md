# [TÍTULO PROVISÓRIO: Modelos de crescimento e modelos de grafos no 11.º ano — uma sequência de tarefas de modelação em MACS]

> **Maquete de dissertação / relatório.** Mestrado em Ensino de Matemática (3.º ciclo do ensino básico e ensino secundário).
> Escrita em português de Portugal, na ortografia anterior ao Acordo Ortográfico de 1990.
>
> **Como usar este ficheiro.** Cada secção tem: (i) o que escrever, (ii) uma extensão-alvo, (iii) o material já recolhido que a alimenta e (iv) um marcador `[[POPULAR]]`. Procura `[[` para ver o que falta. Apaga os blocos `> **Guia**` à medida que escreves.
>
> **Aviso.** O tema exacto da tese, a instituição e o regulamento não foram indicados. Adapta a estrutura ao regulamento da tua instituição (dissertação, projecto ou relatório de estágio têm exigências diferentes). Nada neste ficheiro é resultado empírico: todas as secções de resultados estão vazias de propósito.

---

## 0. Quadro de decisões em aberto

Resolve estes pontos **primeiro**: condicionam o resto.

| # | Decisão | Opções | Escolha |
|---|---|---|---|
| D1 | Tipo de trabalho | Dissertação · Projecto · Relatório de estágio (PES) | [[POPULAR]] |
| D2 | Foco | Crescimento · Grafos · Ambos (ponte factorial/exponencial) | [[POPULAR]] |
| D3 | Desenho | (A) Estudo de caso qualitativo com 1 turma · (B) Quase-experimental pré/pós com 2 turmas · (C) *Design-based research* (ciclos de intervenção) · (D) Estudo de tarefas + análise documental (sem alunos) | [[POPULAR]] |
| D4 | Dimensão da intervenção | 4–6 aulas · 8–12 aulas · um período | [[POPULAR]] |
| D5 | Variável de interesse | Compreensão conceptual · Erros e dificuldades · Uso da tecnologia · Atitudes/motivação · Capacidade de análise crítica de modelos | [[POPULAR]] |
| D6 | Língua do texto | Português · Inglês (resumo em ambas) | [[POPULAR]] |
| D7 | Estilo de citação | APA 7 · Outro exigido pela instituição | [[POPULAR]] |

---

## Páginas preliminares

### Folha de rosto
[[POPULAR: título, autor, grau, instituição, orientador(es), data. Seguir o modelo da instituição.]]

### Dedicatória (opcional)
[[POPULAR]]

### Agradecimentos
[[POPULAR]]

### Resumo
> **Guia.** 200 a 300 palavras. Escrever **no fim**. Estrutura: contexto (1 frase), problema/objectivo (1), método (2), resultados principais (2–3), conclusão/implicação (1).

[[POPULAR]]

**Palavras-chave:** [[POPULAR: 4 a 6, por exemplo, modelação matemática; crescimento exponencial; crescimento logístico; teoria de grafos; ensino secundário]]

### Abstract
[[POPULAR: tradução do resumo]]

**Keywords:** [[POPULAR]]

### Índices
- Índice geral · Índice de figuras · Índice de tabelas · Lista de abreviaturas e siglas (MACS, AE, DGE, PES, QI, RGPD, ...)

[[POPULAR: gerados no fim]]

---

## Capítulo 1. Introdução

> **Guia.** 8 a 12 páginas. Convém ser concreta: quem, onde, o quê, porquê. Material de apoio: `README.md` (visão geral do projecto).

### 1.1 Contexto e motivação
[[POPULAR: porquê este tema? Experiência da PES, dificuldades conhecidas dos alunos com funções exponenciais e logísticas, relevância social (epidemias, crescimento populacional, logística urbana).]]

### 1.2 Problema de investigação
[[POPULAR: 1 parágrafo a enunciar o problema.]]

### 1.3 Questões de investigação e objectivos

> **Guia.** 2 a 4 questões. Cada questão deve ter, mais à frente, um instrumento e uma forma de análise (ver o Quadro de coerência, secção 4.8). Seguem-se **sugestões** a adaptar ao desenho escolhido em D3.

| Código | Sugestão de questão | Desenho que a suporta |
|---|---|---|
| QI1 | Que dificuldades e erros evidenciam os alunos do 11.º ano ao distinguir e interpretar modelos de crescimento linear, exponencial, logarítmico e logístico? | A, B, C |
| QI2 | Em que medida uma sequência de tarefas de modelação com dados (simulados/oficiais) e tecnologia promove a capacidade de escolher e criticar um modelo? | B, C |
| QI3 | Que estratégias usam os alunos para resolver problemas de grafos (Euler, Hamilton) e como lidam com a explosão combinatória? | A, C |
| QI4 | Como percepcionam os alunos o papel da tecnologia (calculadora gráfica, folha de cálculo) na modelação? | A, B, C |

[[POPULAR: questões finais]]

**Objectivos.** [[POPULAR: geral + específicos, em verbos mensuráveis]]

### 1.4 Relevância e contributo
[[POPULAR]]

### 1.5 Estrutura da dissertação
[[POPULAR: parágrafo a descrever os capítulos]]

---

## Capítulo 2. Enquadramento curricular

> **Guia.** 8 a 12 páginas. Descrever o que o currículo pede, com citações. Material de apoio: secção 0 e secção 1 de `desafios_11ano_crescimento_e_grafos.md` (mapa de alinhamento). **As citações das Aprendizagens Essenciais foram obtidas por leitura automática de excertos: verifica-as no documento original.**

### 2.1 A Matemática Aplicada às Ciências Sociais (MACS) no ensino secundário
[[POPULAR: finalidade da disciplina, organização por domínios, carga horária.]]

### 2.2 O domínio "Modelação matemática" no 11.º ano
- Subtema 1: modelos de crescimento populacional
- Subtema 2: modelos de grafos

[[POPULAR: aprendizagens essenciais, conhecimentos, capacidades e atitudes, com citações. Fontes: DGE, *Aprendizagens Essenciais de MACS (11.º)*; DGE, *Programa de MACS*.]]

### 2.3 Orientações para a tecnologia, os dados e a avaliação
[[POPULAR: calculadora gráfica, folha de cálculo, sensores, dados oficiais; avaliação das aprendizagens.]]

### 2.4 O que o currículo não nomeia
[[POPULAR: por exemplo, árvore geradora mínima e a condição "entradas = saídas" nos grafos orientados são extensões neste trabalho. Confirmar no programa oficial.]]

---

## Capítulo 3. Enquadramento teórico

> **Guia.** 25 a 35 páginas. Divide-se em quatro blocos: matemática (3.1), didáctica da modelação (3.2), investigação sobre crescimento (3.3) e sobre grafos (3.4). Material de apoio: `literature_review.md`, `literature_review_growth_models.md`, `explanations/*.md`.

### 3.1 Os modelos matemáticos em estudo

> **Guia.** Resumir, **sem copiar**, as ideias centrais. Material: `explanations/01…05` (definição, derivação, propriedades, exemplos verificados numericamente).

#### 3.1.1 Crescimento linear
[[POPULAR: $y = a + bt$; diferenças constantes; progressão aritmética.]]

#### 3.1.2 Crescimento exponencial
[[POPULAR: $N = N_0 e^{rt}$; razões constantes; tempo de duplicação; progressão geométrica; ligação discreto/contínuo.]]

#### 3.1.3 Crescimento logarítmico
[[POPULAR: $y = a + b\ln t$; cada duplicação de $t$ acrescenta a mesma quantidade; rendimentos decrescentes; função inversa da exponencial.]]

#### 3.1.4 Crescimento logístico
[[POPULAR: $P = K/(1 + Ae^{-rt})$; $dP/dt = rP(1 - P/K)$; ponto de inflexão em $K/2$; taxa máxima $rK/4$; modelo discreto e seus limites.]]

#### 3.1.5 Comparação, linearização e escolha de modelos
[[POPULAR: regressão, resíduos, AIC; extrapolação e identificabilidade de $K$.]]

#### 3.1.6 Modelos de grafos
[[POPULAR: grafo, grau, caminho, circuito; Euler (condição de existência, repetição mínima); Hamilton e caixeiro-viajante; árvores como esquema combinatório; heurísticas (vizinho mais próximo); crescimento factorial $(n-1)!/2$; grafos orientados.]]

### 3.2 Modelação matemática e tecnologia no ensino

> **Guia.** Aqui entra a parte "ensino". As referências abaixo são **sementes**: lê os textos completos antes de citar.

#### 3.2.1 Modelação e aplicações
[[POPULAR: ciclo de modelação, competências, trabalho com dados reais. Pesquisar: Blum & Borromeo Ferri; Kaiser; Niss; orientações curriculares portuguesas e do NCTM.]]

#### 3.2.2 Tecnologia no ensino da Matemática
[[POPULAR: calculadora gráfica, folha de cálculo, programação; sensores.]]

#### 3.2.3 Erros, concepções alternativas e raciocínio covariacional
[[POPULAR]]

### 3.3 Investigação sobre a aprendizagem do crescimento exponencial, logarítmico e logístico

| Tema | Fonte-semente | Nota (verificar o texto completo) |
|---|---|---|
| Divisão e covariação na génese da função exponencial | Confrey & Smith (1995) | Baseada no resumo |
| Várias perspectivas de modelação do crescimento exponencial | Castillo-Garsow (2013) | Baseada no resumo |
| Viés do crescimento exponencial e tempos de duplicação | Schonger & Sele (2021) | Baseada no resumo |
| Erros em gráficos de crescimento exponencial | Melnik-Leroy et al. (2023) | Baseada no resumo |
| Compreensão de expoentes e funções exponenciais no secundário | Bergsma (2019) | Tese de licenciatura |
| Covariação logarítmico-exponencial | Trejo, Ferrari & Martínez (2021); Ferrari (s.d.) | Baseada no resumo |
| Análise qualitativa da equação logística | *Educare* (UNA, Costa Rica) | Baseada no resumo |

[[POPULAR: síntese crítica por tema, com lacunas identificadas. Procurar também investigação portuguesa (APM, SPM, repositórios de teses).]]

### 3.4 Investigação sobre a aprendizagem de grafos e de optimização discreta
[[POPULAR: fontes-semente: actividade *Epidemics on Networks* (NRICH); Harrington et al., módulos de redes para adolescentes (arXiv:1302.6567). Procurar mais literatura sobre o ensino de grafos no secundário e sobre o caixeiro-viajante em contexto escolar.]]

### 3.5 Síntese e lacuna de investigação
> **Guia.** 1 página. Resumir o que se sabe e o que falta: é aqui que a tua pergunta ganha sentido.

[[POPULAR]]

---

## Capítulo 4. Metodologia

> **Guia.** 15 a 20 páginas. Tudo o que um leitor precisa para **repetir** o estudo. Material: secção "Recolha de dados e ética" de `desafios_11ano_crescimento_e_grafos.md`.

### 4.1 Paradigma e opções metodológicas
[[POPULAR: justificar o desenho escolhido em D3 (qualitativo/interpretativo, quase-experimental, DBR).]]

### 4.2 Contexto e participantes
| Elemento | Descrição |
|---|---|
| Escola / contexto | [[POPULAR: descrever sem identificar]] |
| Turma(s), n.º de alunos | [[POPULAR]] |
| Idades, perfil | [[POPULAR]] |
| Selecção da amostra | [[POPULAR: conveniência, turma da PES, etc.]] |
| Papel do investigador | [[POPULAR: professor/investigador; implicações para a objectividade]] |

> **Guia.** Usar códigos (A1, A2, …) em vez de nomes.

### 4.3 A intervenção: sequência de tarefas
[[POPULAR: descrever a sequência escolhida, aula a aula, ligando-a às Aprendizagens Essenciais.]]

> **Banco de tarefas já elaborado.** `desafios_11ano_crescimento_e_grafos.md` contém: A1–A8 (crescimento), A9–A16 (variedade), A17–A20 (avançados), B1–B7 (grafos), B8–B14 (variedade), B15–B19 (avançados), BIO1–BIO8 e FIS1–FIS7 (interdisciplinares).

| Aula | Tarefa(s) | Objectivo | Tecnologia | Tempo |
|---|---|---|---|---|
| 1 | [[POPULAR: ex. A1, A2]] | [[POPULAR]] | [[POPULAR]] | 90 min |
| 2 | [[POPULAR]] | | | |
| ... | | | | |

### 4.4 Instrumentos de recolha de dados
| Instrumento | Finalidade | QI | Momento | Estado |
|---|---|---|---|---|
| Teste diagnóstico (pré) | Concepções iniciais | QI1 | Antes | [[POPULAR]] |
| Produções escritas dos alunos (fichas) | Estratégias e erros | QI1, QI3 | Durante | [[POPULAR]] |
| Notas de campo / diário do investigador | Contexto e interacção | todas | Durante | [[POPULAR]] |
| Gravações áudio das discussões em grupo (opcional) | Raciocínio oral | QI1, QI3 | Durante | [[POPULAR]] |
| Ficheiros da calculadora/folha de cálculo | Uso da tecnologia | QI4 | Durante | [[POPULAR]] |
| Teste final (pós) | Evolução | QI1, QI2 | Depois | [[POPULAR]] |
| Questionário de percepção | Atitudes e tecnologia | QI4 | Depois | [[POPULAR]] |
| Entrevista semiestruturada (subamostra) | Aprofundar | todas | Depois | [[POPULAR]] |

[[POPULAR: descrever e validar cada instrumento (revisão por especialistas, piloto).]]

### 4.5 Procedimentos de recolha
[[POPULAR: calendário, quem recolhe, onde se guardam os dados.]]

### 4.6 Análise de dados
- **Qualitativa:** análise de conteúdo com categorias. Sugestões de categorias iniciais para os erros (a refinar com os dados): tratar crescimento exponencial como linear; confundir taxa de variação com valor; extrapolar fora do intervalo dos dados; ignorar o limite $K$ da logística; confundir circuito de Euler com circuito de Hamilton; usar a heurística sem verificar a optimalidade.
- **Quantitativa (se aplicável):** estatística descritiva; testes de comparação pré/pós adequados ao tamanho da amostra.

[[POPULAR: descrever o procedimento de codificação, a fiabilidade entre codificadores e o software.]]

### 4.7 Questões éticas e protecção de dados
- Pedido de autorização à direcção do agrupamento/escola.
- Consentimento informado dos alunos e dos encarregados de educação (se menores).
- Anonimização, armazenamento seguro, RGPD.
- Se forem aplicados **inquéritos em meio escolar**, verificar o procedimento nacional de autorização aplicável (por exemplo, a plataforma de monitorização de inquéritos em meio escolar da DGE) [[POPULAR: confirmar a regra em vigor]].
- Parecer da comissão de ética da instituição, se exigido.

[[POPULAR: texto final e número dos pareceres]]

### 4.8 Quadro de coerência

| Questão | Instrumentos | Análise | Capítulo de resultados |
|---|---|---|---|
| QI1 | [[POPULAR]] | [[POPULAR]] | 6.1 |
| QI2 | [[POPULAR]] | [[POPULAR]] | 6.2 |
| QI3 | [[POPULAR]] | [[POPULAR]] | 6.3 |
| QI4 | [[POPULAR]] | [[POPULAR]] | 6.4 |

### 4.9 Rigor, validade e limitações do desenho
[[POPULAR: credibilidade, transferibilidade, triangulação; ameaças à validade; viés do professor-investigador.]]

---

## Capítulo 5. Concepção das tarefas

> **Guia.** 12 a 18 páginas. Justificar as escolhas didácticas. Material: `desafios_11ano_crescimento_e_grafos.md`, `notebooks/` e `explanations/`.

### 5.1 Princípios de desenho
[[POPULAR: por exemplo, partir de situações concretas; prever antes de calcular (A2); confronto entre modelos (A6); análise crítica obrigatória; ponte entre crescimento e grafos (B4); tecnologia como ferramenta e não como substituto.]]

### 5.2 Descrição das tarefas escolhidas
[[POPULAR: para cada tarefa usada: enunciado resumido, objectivo, conhecimentos mobilizados, dificuldades antecipadas, solução esperada.]]

### 5.3 Uso de dados simulados e de dados oficiais
[[POPULAR: justificar; limites. Os dados de exemplo do banco de tarefas são **simulados**.]]

### 5.4 Materiais complementares
- Cadernos Python (`notebooks/01…05`): simulação e ajuste de modelos, para uso do professor.
- Explicações matemáticas (`explanations/01…05`).

[[POPULAR]]

### 5.5 Antecipação de dificuldades
[[POPULAR: quadro "dificuldade esperada → como a tarefa a aborda".]]

---

## Capítulo 6. Resultados

> **Guia.** 25 a 35 páginas. **Só descrever** (a interpretação vai para o Capítulo 7). Citar produções dos alunos com códigos. Organizar por questão. **Esta secção é preenchida só com dados reais.**

### 6.1 Resultados da QI1 (dificuldades e erros)
[[POPULAR]]

### 6.2 Resultados da QI2 (sequência de tarefas e escolha/crítica de modelos)
[[POPULAR]]

### 6.3 Resultados da QI3 (grafos)
[[POPULAR]]

### 6.4 Resultados da QI4 (tecnologia)
[[POPULAR]]

### 6.5 Síntese dos resultados
[[POPULAR: tabela-resumo]]

---

## Capítulo 7. Discussão

> **Guia.** 10 a 15 páginas. Interpretar à luz do Capítulo 3. Evitar generalizar para além do desenho.

### 7.1 Discussão por questão
[[POPULAR]]

### 7.2 Articulação com a literatura
[[POPULAR: onde confirma, onde contradiz, onde acrescenta.]]

### 7.3 Implicações para o ensino de MACS
[[POPULAR]]

### 7.4 Limitações
[[POPULAR: amostra, tempo, efeito do investigador, dados simulados vs reais, possível efeito de novidade.]]

---

## Capítulo 8. Conclusões

> **Guia.** 4 a 6 páginas.

### 8.1 Respostas às questões
[[POPULAR]]

### 8.2 Recomendações para a prática
[[POPULAR]]

### 8.3 Sugestões para investigação futura
[[POPULAR: por exemplo, repetir com várias turmas; comparar dados simulados e reais; incluir grafos orientados e árvores geradoras; medir retenção a longo prazo.]]

### 8.4 Reflexão final
[[POPULAR: reflexão pessoal enquanto professor/investigador.]]

---

## Referências

> **Guia.** Formato conforme D7. **Não incluir nada que não tenhas lido.** As entradas abaixo são sementes; confirma ano, título e dados em cada fonte.

**Documentos oficiais**
- DGE. *Aprendizagens Essenciais: Matemática Aplicada às Ciências Sociais, 11.º ano.* https://www.dge.mec.pt/sites/default/files/Curriculo/Aprendizagens_Essenciais/11_macs.pdf
- DGE. *Programa de Matemática Aplicada às Ciências Sociais.* https://dge.mec.pt/sites/default/files/Secundario/Documentos/Programas/mat_aplicada_cien_soc.pdf

**Investigação**
- Bergsma, Y. (2019). *Students' understanding of exponents and exponential functions at a secondary school in the northern Netherlands.* Bachelor's thesis, University of Groningen. https://fse.studenttheses.ub.rug.nl/20116
- Castillo-Garsow, C. (2013). The role of multiple modeling perspectives in students' learning of exponential growth. *Mathematical Biosciences and Engineering, 10*(5&6), 1437–1453. https://www.aimspress.com/article/id/2461
- Confrey, J., & Smith, E. (1995). Splitting, covariation, and their role in the development of exponential functions. *Journal for Research in Mathematics Education, 26*(1), 66–86. https://doi.org/10.2307/749228
- Harrington, H. A., Beguerisse Díaz, M., Rombach, M. P., Keating, L. M., & Porter, M. A. (s.d.). Teach network science to teenagers. https://arxiv.org/pdf/1302.6567
- Melnik-Leroy, G. A., et al. (2023). Is my visualization better than yours? Analyzing factors modulating exponential growth bias in graphs. *Frontiers in Psychology.* https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2023.1125810/pdf
- Schonger, M., & Sele, D. (2021). Intuition and exponential growth: bias and the roles of parameterization and complexity. *Mathematics and Financial Economics.* https://link.springer.com/article/10.1007/s00591-021-00306-7
- Trejo, M., Ferrari, M., & Martínez, G. (2021). Covariación logarítmico-exponencial en futuros profesores de matemáticas: un estudio de caso. *Educación Matemática, 33*(1), 41–70. https://www.redalyc.org/journal/405/40576157003/40576157003.pdf
- Verhulst, P.-F. (1838). Notice sur la loi que la population poursuit dans son accroissement. *Correspondance mathématique et physique, 10*, 113–121. (Citada de memória: verificar.)

**Recursos**
- NRICH. *Epidemics on Networks.* https://nrich.maths.org/12123

[[POPULAR: acrescentar tudo o que for efectivamente lido, incluindo literatura portuguesa.]]

---

## Apêndices

| Apêndice | Conteúdo | Ficheiro de origem | Estado |
|---|---|---|---|
| A | Sequência completa de tarefas (fichas de aluno) | `desafios_11ano_crescimento_e_grafos.md` (sem as chaves) | [[POPULAR]] |
| B | Chaves de correcção e justificações | idem | [[POPULAR]] |
| C | Teste diagnóstico e teste final | [[POPULAR: a criar]] | [[POPULAR]] |
| D | Questionário e guião de entrevista | [[POPULAR: a criar]] | [[POPULAR]] |
| E | Pedidos de autorização e modelos de consentimento | [[POPULAR: a criar]] | [[POPULAR]] |
| F | Cadernos Python e requisitos | `notebooks/` | pronto |
| G | Explicações matemáticas | `explanations/` | pronto |
| H | Tabelas de codificação e exemplos de produções | [[POPULAR]] | [[POPULAR]] |
| I | Dados anonimizados (se permitido) | [[POPULAR]] | [[POPULAR]] |

---

## Anexo de trabalho 1. Mapa do material já existente para a tese

| Material | Alimenta | Estado |
|---|---|---|
| `README.md` | Cap. 1 (visão geral) | Pronto (rever) |
| `literature_review.md` | Cap. 3.2–3.4 | Fontes-semente; ler textos completos |
| `literature_review_growth_models.md` | Cap. 3.3 | Fontes-semente; ler textos completos |
| `explanations/01…05` e `growth_models_theory.md` | Cap. 3.1 | Pronto (números verificados por código) |
| `notebooks/01…05` | Cap. 5.4, Apêndice F | Executam como código; nunca abertos em Jupyter |
| `desafios_11ano_crescimento_e_grafos.md` | Cap. 2.4, 4.3, 5, Apêndices A–B | Pronto; dados simulados; citações do currículo a confirmar |

## Anexo de trabalho 2. Calendário (preencher)

| Fase | Início | Fim | Marco |
|---|---|---|---|
| Pedido de autorizações | [[POPULAR]] | [[POPULAR]] | Autorizações recebidas |
| Teste piloto dos instrumentos | | | |
| Intervenção | | | |
| Recolha de dados | | | |
| Análise | | | |
| Redacção dos capítulos 6 a 8 | | | |
| Revisão e entrega | | | |

## Anexo de trabalho 3. Lista de verificação final

- [ ] Todas as questões de investigação têm resposta no Cap. 8
- [ ] Cada questão tem instrumento e análise (secção 4.8)
- [ ] Todas as citações no texto estão nas Referências e vice-versa
- [ ] Todas as citações de currículo foram confirmadas no original
- [ ] Todos os dados são anonimizados
- [ ] Os resultados não incluem interpretações (ficam no Cap. 7)
- [ ] Todos os marcadores `[[POPULAR]]` foram resolvidos
- [ ] Resumo e *abstract* concordam
- [ ] Índices, figuras e tabelas numerados
- [ ] Verificação ortográfica na norma escolhida
