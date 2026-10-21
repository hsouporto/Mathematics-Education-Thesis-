# Objectivos e questões orientadoras de aprendizagem — conjunto Bebras 2025 adaptado a MACS 11.º

**Estado:** rascunho de trabalho para a tese. Português de Portugal, na ortografia anterior ao Acordo Ortográfico de 1990.

> **Base.** Este documento assenta nas 12 adaptações de `bebras_2025_adaptado_macs11.md` (P1 a P12). Os objectivos e as questões **não foram testados com alunos**; confirma-os num piloto. Alguns problemas (código de Gray, soma módulo 2, mínimo múltiplo comum) vão além do programa e são enriquecimento. Se partilhares os materiais, indica a fonte (Bebras PT 2025) e a licença CC BY-NC-SA 4.0.

---

## 1. Objectivos de aprendizagem (para o professor)

**Finalidade geral.** Com este conjunto, o aluno deve reconhecer que problemas de aspecto computacional (ordenar, codificar, contar, planear percursos) se podem descrever com os modelos de MACS 11.º: crescimento populacional e grafos. O professor deve usá-lo para que o aluno passe de «resolver um quebra-cabeças» a **identificar o modelo**, justificar essa escolha e dizer onde o modelo deixa de servir. É o mesmo fio condutor do banco de desafios, mas com um estilo de problema mais próximo de uma prova de pensamento computacional.

**Crescimento.** O aluno deve distinguir, perante uma situação ou uma tabela, crescimento linear, quadrático, exponencial e logarítmico, usando diferenças e razões entre termos consecutivos (P1, P9 e P11). Deve perceber que a função logarítmica é a inversa da exponencial: duplicar um número acrescenta um bit (P2), e o erro causado pela alteração de um bit dobra de posição em posição (P6). Deve ainda justificar porque é que a soma $1+2+\dots+n$ cresce de forma quadrática e a razão entre termos consecutivos tende para 1, ao contrário de $2^n$. O professor pode avaliar isto pedindo sempre a classificação do crescimento, com a razão ou a diferença que a sustenta.

**Grafos.** O aluno deve modelar uma situação por um grafo, orientado ou não, e identificar vértices, arestas e pesos (P3, P7, P10 e P12). Deve calcular graus, aplicar a condição de existência de circuitos de Euler e distinguir Euler de Hamilton, incluindo em grafos de estados e de trocas como o $K_{3,3}$. Deve reconhecer que o grafo das trocas é bipartido e que a soma módulo 2 de dois grafos com graus pares tem graus pares. Deve também compreender que o significado do peso (tempo ou número de mudanças, em P12) muda a solução óptima, o que cumpre a aprendizagem de discutir o significado dos pesos. O professor deve exigir o desenho do grafo antes de qualquer cálculo.

**Contagem, árvores e algoritmos.** O aluno deve usar árvores como esquema combinatório para contar possibilidades, com e sem restrições (P5 e P8), e comparar crescimentos como $n!$, $2^n$ e $n^2$. Deve descrever estratégias passo a passo, como aplicar uma rede de comparadores (P1), codificar e decodificar por divisão ao meio (P8) e planear um percurso com horários (P12). Deve ainda verificar se uma estratégia chega ao resultado certo, por exemplo ao perceber que retirar um comparador faz a rede falhar. O professor pode avaliar não só o resultado mas a clareza do procedimento e a verificação.

**Competências transversais e cuidados.** Em todos os problemas, o aluno deve justificar por escrito, usar a linguagem matemática com rigor e fazer uma análise crítica do modelo, indicando os seus limites. Isto liga ao que o programa pede sobre análise crítica e sobre a tecnologia (calculadora, folha de cálculo) como apoio e não como substituto do raciocínio. Convém lembrar que alguns problemas vão além do programa: o código de Gray, a soma módulo 2 e o mínimo múltiplo comum são enriquecimento, e a avaliação deve respeitar essa distinção. Convém ainda indicar a fonte e a licença (CC BY-NC-SA 4.0) quando os materiais forem partilhados.

---

## 2. Questões orientadoras (para conduzir as aulas)

O professor pode colocá-las antes, durante e depois de cada problema.

### Questões gerais (todo o conjunto)
- Que situação real, ou que problema, está por trás deste enunciado?
- Que modelo de MACS o descreve: crescimento (linear, quadrático, exponencial, logarítmico) ou grafo?
- Como sei que o modelo está certo? O que verifico antes de aceitar a resposta?

### Crescimento (P1, P2, P6, P9, P11)
- O que se mantém constante quando o valor aumenta: a diferença ou a razão entre termos consecutivos?
- Se o valor duplicar, o que acontece ao resultado? Acrescenta uma quantidade fixa ou multiplica por um factor fixo?
- Quando é que um crescimento quadrático deixa de ser «lento» em comparação com um exponencial? Em que ponto a diferença se torna enorme?
- Porque é que a função logarítmica aparece quando perguntamos «quantos bits» ou «quantos dígitos» são precisos?

### Grafos (P3, P4, P7, P10, P12)
- Quais são os vértices e as arestas? Têm sentido? Têm peso, e o que significa esse peso?
- Todos os graus são pares? O que isso me diz sobre um circuito que passa em todas as arestas?
- Preciso de passar por todas as arestas ou por todos os vértices? Isso muda o tipo de circuito?
- Se mudar o critério (tempo, número de mudanças, custo), a melhor solução muda? Porquê?

### Contagem, árvores e algoritmos (P1, P5, P8)
- Posso representar as possibilidades numa árvore? Que ramos posso eliminar logo, sem os explorar?
- Quantas possibilidades há sem restrições e quantas com as restrições do problema? Como cresce esse número?
- Consigo escrever os passos de uma estratégia de forma que outra pessoa a siga sem me perguntar nada? Como mostro que ela funciona sempre?

### Análise crítica e tecnologia (transversais)
- Onde é que este modelo deixa de descrever bem a situação?
- O que mudaria se os dados fossem outros ou o número de elementos crescesse muito?
- A calculadora ou a folha de cálculo ajudou-me a decidir, ou apenas a calcular? O que teria de fazer à mão para ter a certeza?

---

## 3. Questões orientadoras de aprendizagem (o que o aluno deve saber responder no fim)

| Objectivo | Questão orientadora de aprendizagem | Problemas | Evidência de aprendizagem |
|---|---|---|---|
| Modelos de crescimento | Como sei se uma sequência cresce de forma linear, quadrática, exponencial ou logarítmica? | P1, P2, P6, P9, P11 | Classifica e justifica com a diferença ou a razão entre termos consecutivos |
| Logaritmo e exponencial | Porque é que duplicar um número acrescenta sempre a mesma quantidade (1 bit)? | P2, P6 | Explica a relação entre a função logarítmica e a exponencial, com exemplo |
| Grafos como modelo | Que vértices, arestas e pesos descrevem esta situação, e o que significa cada peso? | P3, P7, P10, P12 | Desenha o grafo antes de calcular, com legenda dos pesos |
| Euler e Hamilton | Quando existe um percurso que passa em todas as arestas? E em todos os vértices? | P3, P7, P10 | Calcula graus e conclui, distinguindo os dois tipos de circuito |
| Critério e solução | Se mudar o critério (tempo, mudanças, custo), a melhor solução muda? | P12 | Compara soluções para dois critérios e explica a diferença |
| Contagem e árvores | De quantas formas posso fazer isto, e que ramos posso eliminar logo? | P1, P5, P8 | Constrói a árvore, poda e conta; compara $n!$, $2^n$ e $n^2$ |
| Estratégias e verificação | Os passos que escrevi funcionam sempre? Como o mostro? | P1, P8, P12 | Descreve o procedimento passo a passo e testa com um caso extremo |
| Análise crítica | Até onde vale este modelo e o que o faria falhar? | todos | Identifica pelo menos um limite do modelo, por escrito |

**Como usar a tabela.** Em cada aula, o professor escolhe **uma ou duas** questões e escreve-as no quadro, em vez de usar a tabela inteira. O aluno responde-lhes no início, a partir do que já sabe, e volta a respondê-las no fim. Isto dá uma comparação simples entre «antes» e «depois», útil para a tese.

---

## 4. Ligação à dissertação

| Onde na maquete | Uso |
|---|---|
| Cap. 1.3 (objectivos) | Adaptar a secção 1 como objectivos específicos |
| Cap. 4.3 (intervenção) | Escolher as questões orientadoras de cada aula |
| Cap. 4.4 (instrumentos) | Usar a tabela da secção 3 como guião de teste «antes/depois» (a criar) |
| Cap. 6 (resultados) | Descrever as respostas dos alunos por questão orientadora |
