# Desafios e trabalhos para o 11.º ano (MACS): modelos de crescimento e modelos de grafos

**Estado:** rascunho de trabalho para a tese. Escrito em português de Portugal, na ortografia anterior ao Acordo Ortográfico de 1990. Tempos em blocos de 90 minutos ("aula"); são estimativas minhas, não vêm do programa.

> **Antes de usar.** Os números de todos os exemplos foram calculados por código e, quando há dados, são **simulados** (estão assinalados). As referências ao programa e às Aprendizagens Essenciais vêm de uma leitura automática de excertos dos documentos oficiais da DGE; **confirma as citações no original** antes de as usar na tese. Não recebi o programa que mencionaste no início da conversa, por isso baseei-me nos documentos públicos.

---

## 0. Contexto

**Em que programa encaixa.** Em Matemática Aplicada às Ciências Sociais (MACS) do 11.º ano, o domínio **"Modelação matemática"** tem dois subtemas, que correspondem às duas categorias pedidas:

1. **Modelos de crescimento populacional**
2. **Modelos de grafos**

Interpretei "grafos" como este segundo subtema (teoria de grafos aplicada a sistemas de distribuição e recolha), e não como gráficos de funções.

**O que as Aprendizagens Essenciais pedem** (citações; confirmar no original):

| Subtema | Aprendizagem essencial |
|---|---|
| Grafos | "Procurar modelos que descrevam situações realistas de sistemas de distribuições ou de recolhas." |
| Grafos | "Encontrar estratégias passo a passo para encontrar possíveis soluções." |
| Grafos | "Para cada modelo procurar esquemas combinatórios (árvores) que permitam calcular pesos totais de caminhos possíveis." |
| Grafos | "Discutir sobre a utilidade e a viabilidade económica da procura de soluções óptimas." |
| Crescimento | "Compreender modelos discretos e contínuos de crescimento populacional." |
| Crescimento | "Comparar o crescimento linear com o crescimento exponencial através do estudo de progressões aritméticas e geométricas." |
| Crescimento | "Comparar os crescimentos linear, exponencial, logarítmico e logístico." |

**O que o programa acrescenta** (resumo, não citação):

- *Grafos:* sistemas de distribuição (correio, limpeza de ruas, recolha de lixo, patrulhamento); vértices, arestas, caminhos e circuitos; circuitos de Euler e algoritmos para o mínimo de repetições; circuitos hamiltonianos e problema do caixeiro-viajante; árvores para somar pesos e comparar soluções; grafos orientados (sentidos nas ruas). Discutir o significado dos pesos (quilómetros, consumo, poluição, custo). Actividades sugeridas: problemas sobre mapas e apresentar propostas a responsáveis locais.
- *Crescimento:* modelos discretos (progressões aritméticas e geométricas) e contínuos (funções exponencial, logarítmica e logística, introduzidas em situações concretas). Simulações, de preferência com **dados oficiais portugueses e mundiais**, obtenção de modelos por **regressão**, **análise crítica** dos modelos escolhidos e discussão de vantagens e desvantagens dos modelos discretos e contínuos. Exemplo histórico: Malthus.
- *Ferramentas:* calculadora gráfica (uso obrigatório), computador e folha de cálculo, sensores de recolha de dados.

**Limites desta leitura.**

- O excerto do programa que li **não nomeia** "árvore geradora mínima" nem "caminho mais curto". O desafio B6 usa a primeira e está marcado como **extensão opcional**.
- O programa indica 30 aulas de 90 minutos para o conjunto dos dois subtemas, mas a tabela estava mal formatada na leitura. Confirma no original.
- Nada aqui foi testado com alunos.

---

## 1. Mapa de alinhamento

| Desafio | Aprendizagem essencial / elemento do programa | Tecnologia |
|---|---|---|
| A1 Duas contas, dois destinos | Linear vs exponencial por progressões | Folha de cálculo |
| A2 Prevê antes de calcular | Compreender o crescimento exponencial; análise crítica | Calculadora |
| A3 De Malthus aos dados oficiais | Discreto e contínuo; dados oficiais; regressão; análise crítica | Calculadora gráfica |
| A4 O arrefecimento | Modelo contínuo; recolha com sensores; regressão | Sensor + calculadora |
| A5 A minha curva de aprendizagem | Modelo logarítmico; comparar modelos | Calculadora gráfica |
| A6 Detectives de dados | Comparar linear, exponencial, logarítmico e logístico | Calculadora gráfica |
| A7 O boato | Modelo logístico; discreto vs contínuo; simulação | Folha de cálculo |
| A8 Projecto de crescimento | Dados oficiais; regressão; análise crítica | Livre |
| A9 A regra dos 72 | Progressões geométricas; tempo de duplicação | Folha de cálculo |
| A10 Xadrez e papel dobrado | Linear vs exponencial por progressões | Calculadora |
| A11 Escalas logarítmicas | Modelo logarítmico | Calculadora |
| A12 Linearizar para descobrir a taxa | Regressão; modelo exponencial | Calculadora gráfica |
| A13 Jogo dos dados | Modelo discreto de decaimento; simulação | Dados + folha de cálculo |
| A14 Quando o modelo discreto enlouquece | Discreto vs contínuo (enriquecimento) | Folha de cálculo |
| A15 Pescar sem esgotar | Modelo logístico; análise crítica | Folha de cálculo |
| A16 Associa a história ao modelo | Comparar os quatro crescimentos | Papel |
| B1 Do mapa ao grafo | Situações realistas; significado dos pesos | Papel / GeoGebra |
| B2 O camião do lixo | Euler; estratégia passo a passo; mínimo de repetições | Papel |
| B3 Visitar todos os locais | Hamilton; caixeiro-viajante; árvores e pesos totais | Folha de cálculo |
| B4 Quantas rotas? | Viabilidade económica de soluções óptimas | Folha de cálculo |
| B5 Ruas de sentido único | Grafos orientados | Papel |
| B6 Ligar edifícios (opcional) | Árvores (extensão) | Papel |
| B7 Projecto de grafos | Propostas a responsáveis locais | Livre |
| B8 Königsberg e a casinha | Euler (condição de existência) | Papel |
| B9 O carteiro com dois ímpares | Euler; mínimo de repetições | Papel |
| B10 Seis entregas | Hamilton; árvores; heurística | Folha de cálculo |
| B11 Torneios e grafos completos | Grafos completos; contagem | Papel |
| B12 Mesmo mapa, outro peso | Significado dos pesos | Folha de cálculo |
| B13 Árvores de contagem | Esquemas combinatórios (árvores) | Papel |
| B14 Concurso de algoritmos | Estratégias passo a passo | Papel / folha de cálculo |
| A17 Estimar K por linearização (avançado) | Modelo logístico; regressão | Folha de cálculo |
| A18 O número e (avançado) | Discreto vs contínuo | Calculadora |
| A19 Escolha com AIC (avançado) | Comparar modelos; análise crítica | Folha de cálculo |
| A20 Demonstrar a logística (avançado) | Modelo logístico; rigor | Papel |
| B15 Demonstrar Euler (avançado) | Euler; justificação | Papel |
| B16 O cubo (avançado) | Euler vs Hamilton | Papel |
| B17 Limite inferior com árvore (avançado) | Árvores; viabilidade de soluções óptimas | Papel |
| B18 Troca 2-opt (avançado) | Estratégias passo a passo | Papel |
| B19 Programar e medir (avançado) | Viabilidade económica; crescimento factorial | Python / folha de cálculo |
| BIO1 Bactérias | Crescimento exponencial | Calculadora |
| BIO2 Curva de crescimento de uma cultura | Modelo logístico | Calculadora gráfica |
| BIO3 Um medicamento no organismo | Progressões; recorrência | Folha de cálculo |
| BIO4 Carbono-14 | Decaimento exponencial; logaritmos | Calculadora |
| BIO5 Contágio por gerações | Progressão geométrica | Calculadora |
| BIO6 Redes alimentares | Grafos orientados; progressão geométrica | Papel |
| BIO7 Cruzamentos de Mendel | Árvores de probabilidade | Papel |
| BIO8 A abelha e as flores | Hamilton; vizinho mais próximo | Papel / folha de cálculo |
| FIS1 Arrefecer uma bebida | Modelo exponencial | Calculadora |
| FIS2 Condensador | Exponencial; linearização | Sensor / simulação |
| FIS3 Radioisótopos | Decaimento exponencial | Calculadora |
| FIS4 Queda com resistência do ar | Modelo com tecto | Calculadora |
| FIS5 A luz debaixo de água | Exponencial; escala logarítmica | Calculadora |
| FIS6 Cabos eléctricos | Árvores (extensão) | Papel |
| FIS7 Drone e linhas de alta tensão | Euler | Papel |

**Pontes entre as duas partes.** B4 (número de rotas) usa o crescimento factorial, que ultrapassa qualquer exponencial. B6 compara o número de arestas de uma árvore (linear) com o de um grafo completo (quadrático).

**Legenda de nível:** ⭐ base · ⭐⭐ intermédio · ⭐⭐⭐ exigente. Os blocos **🔑 Chave do professor** podem ser retirados antes de distribuir as fichas.

---

## 2. Parte A: modelos de crescimento populacional

### A1. Duas contas, dois destinos ⭐ (1 aula)

**Objectivo.** Comparar crescimento linear e exponencial através de progressões aritméticas e geométricas.

**Tarefa.** A Ana põe 100 € numa conta que acrescenta 10 € por semana: $u_n = 100 + 10n$. O Bruno põe 100 € numa conta que rende 5% por semana: $v_n = 100\cdot 1{,}05^{\,n}$.

1. Calcula os termos até $n = 52$ e traça os dois gráficos.
2. Em que semana o Bruno passa a ter mais do que a Ana?
3. Repete com 2% e com 8% por semana. Que relação há entre a taxa e a semana da ultrapassagem?
4. Calcula as diferenças $u_{n+1} - u_n$ e as razões $v_{n+1}/v_n$. Qual das duas é constante em cada sequência?
5. **Análise crítica.** Uma conta pode render 5% por semana durante um ano? Que limites tem este modelo?

**Entregável.** Tabela, gráfico e um parágrafo a explicar a diferença entre "somar sempre o mesmo" e "multiplicar sempre pelo mesmo".

**🔑 Chave do professor.** Com 5%, o Bruno ultrapassa a Ana na **semana 27** (373,35 € contra 370 €). Com 2% ultrapassa na semana 136 e com 8% na semana 7. Na semana 52: Ana 620 €, Bruno 1 264,28 €. As diferenças da Ana são constantes (10); as razões do Bruno são constantes (1,05).

### A2. Prevê antes de calcular ⭐⭐ (1 aula)

**Objectivo.** Perceber que a intuição subestima o crescimento exponencial e que o enunciado conta.

**Tarefa.** Divide a turma ao meio, sem dizer o motivo. Cada aluno escreve a previsão **antes** de usar a calculadora.

- **Versão X:** "O número de casos de uma doença aumenta 12,25% por dia. Hoje há 100 casos. Quantos haverá daqui a 30 dias?"
- **Versão Y:** "O número de casos duplica de 6 em 6 dias. Hoje há 100 casos. Quantos haverá daqui a 30 dias?"

Depois: (1) calcular o valor exacto; (2) comparar as medianas das previsões das duas versões; (3) comparar com a previsão "linear" ($100\,(1 + 0{,}1225\times 30)$); (4) discutir porque é que se subestima e que versão é mais transparente.

**🔑 Chave do professor.** As duas versões descrevem o mesmo processo: valor exacto **≈ 3 200 casos** (3 203 com 12,25%; 3 200 com a duplicação de 6 em 6 dias, pois $2^{1/6} - 1 = 12{,}246\%$). A previsão linear dá ≈ 468 casos. Ao fim de 12 dias há 400 casos nas duas versões.

*Base na literatura.* Descreve-se um "viés do crescimento exponencial": as pessoas tendem a subestimar o crescimento exponencial, e esse viés é muito menor quando se usam tempos de duplicação (Schonger & Sele, 2021). Com uma turma pequena a diferença pode não aparecer, por isso trata isto como pergunta exploratória, não como prova. Registos anónimos (ver secção 7).

### A3. De Malthus aos dados oficiais ⭐⭐ (1 a 2 aulas)

**Objectivo.** Ligar o modelo discreto ao contínuo e analisar criticamente um modelo ajustado a dados oficiais.

**Tarefa.**

1. Malthus (1798) defendeu que a população cresce em progressão geométrica e os alimentos em progressão aritmética. Representa-o com $P_n = P_0\, r^n$ e $A_n = A_0 + d\,n$. O que acontece a longo prazo?
2. Recolhe dados oficiais de população (Portugal: INE ou PORDATA; mundo: Nações Unidas) para um período à tua escolha (por exemplo, várias décadas).
3. Na calculadora gráfica faz a regressão exponencial ($y = a\cdot b^x$) e a linear. Compara os gráficos e os resíduos.
4. Relaciona os dois modelos: $P_{n+1} = r\,P_n$ (discreto) e $P(t) = P_0\,e^{kt}$ (contínuo), com $r = e^{k}$.
5. **Análise crítica.** O modelo exponencial serve para o mundo? E para Portugal? Onde falha e que factores faltam?

**Entregável.** Relatório de duas páginas com gráfico, parâmetros e crítica ao modelo.

**🔑 Chave do professor.** Não incluí números reais: o programa pede que os alunos trabalhem dados oficiais, e a recolha faz parte do trabalho. Procura que os alunos concluam que um ajuste pode ser bom num intervalo e enganador fora dele, e que o resultado depende do período escolhido.

### A4. Medir para modelar: o arrefecimento ⭐⭐ (1 aula + recolha)

**Objectivo.** Recolher dados com sensor, ajustar um modelo exponencial e perceber porque é que só funciona depois de subtrair a temperatura ambiente.

**Segurança.** Água muito quente: o professor manuseia a água; usar recipiente estável e longe das mãos.

**Tarefa.** Regista a temperatura $T$ de uma chávena de água quente de 2 em 2 minutos durante 30 minutos (sensor ligado à calculadora, ou termómetro) e a temperatura ambiente $T_a$.

1. Faz a regressão exponencial a $T$.
2. Faz a regressão exponencial a $T - T_a$.
3. Faz a regressão linear a $T$.
4. Compara os resíduos dos três ajustes e explica o resultado.
5. Interpreta o parâmetro $b$ (factor por minuto) e calcula a "meia-vida" da diferença $T - T_a$.

**🔑 Chave do professor.** Exemplo **simulado** (não são medições reais), com $T_a = 20\,°C$:

| t (min) | 0 | 2 | 4 | 6 | 8 | 10 | 12 | 14 |
|---|---|---|---|---|---|---|---|---|
| T (°C) | 89,8 | 84,0 | 77,9 | 73,9 | 69,0 | 64,5 | 60,7 | 57,4 |

| t (min) | 16 | 18 | 20 | 22 | 24 | 26 | 28 | 30 |
|---|---|---|---|---|---|---|---|---|
| T (°C) | 54,0 | 51,1 | 48,7 | 46,2 | 43,8 | 41,7 | 39,9 | 38,0 |

- Regressão exponencial a $T - 20$: $a \approx 70{,}0$, $b \approx 0{,}956$ por minuto ($k \approx 0{,}045$), meia-vida ≈ **15,4 min**.
- Soma dos quadrados dos resíduos: **0,75** (modelo $20 + a\,b^t$), 17,5 (exponencial em $T$) e 124,7 (linear em $T$).
- Conclusão esperada: a temperatura tende para a ambiente, não para zero. É a **diferença** que decai exponencialmente.

### A5. A minha curva de aprendizagem ⭐⭐ (recolha numa semana + 1 aula)

**Objectivo.** Modelar o progresso de uma aprendizagem com o modelo logarítmico e discutir os seus limites. Liga directamente ao tema da tese.

**Tarefa.** Cada aluno escolhe uma tarefa treinável e mensurável (teste de digitação em palavras por minuto, jogo de memória, contas de cabeça em 1 minuto) e regista a pontuação em **10 tentativas** feitas em dias diferentes.

1. Faz o gráfico das pontuações.
2. Ajusta o modelo linear e o logarítmico $y = a + b\ln x$ (e o logístico, se os dados o permitirem).
3. Interpreta $b$: cada vez que duplicas o número de tentativas, a pontuação sobe cerca de $b\ln 2$.
4. Prevê quantas tentativas precisas para atingir um objectivo e discute a fiabilidade da previsão.
5. O que acontece a longo prazo? Existe um tecto?

**Ética.** Participação voluntária, dados anónimos, pontuações pessoais **não** entram na avaliação.

**🔑 Chave do professor.** Exemplo **simulado** (palavras por minuto, tentativas 1 a 10): 19,6; 24,7; 26,5; 26,9; 29,2; 31,4; 31,4; 32,3; 33,8; 35,6.

- Regressão logarítmica: $y \approx 19{,}41 + 6{,}44\ln x$ (a simulação usou $20 + 6\ln x$). Cada duplicação das tentativas acrescenta cerca de 4,5 palavras por minuto.
- Soma dos quadrados dos resíduos: 5,78 (logarítmico) contra 13,32 (linear).
- **Extrapolação:** para 30 palavras por minuto o ajuste dá 5,2 tentativas (o modelo verdadeiro, 5,3). Para 40 dá 24,5 (o verdadeiro, 28). Quanto mais longe dos dados, mais a previsão se afasta. Discute isto com os alunos.

### A6. Qual é o modelo? Detectives de dados ⭐⭐⭐ (1 aula)

**Objectivo.** Escolher e justificar o modelo (linear, exponencial, logarítmico ou logístico) para quatro conjuntos de dados.

**Ficha do aluno.** Dados **simulados**; $t = 1, \dots, 10$.

| t | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| **D1** | 16,1 | 25,7 | 26,0 | 34,3 | 37,2 | 47,7 | 52,2 | 58,3 | 59,7 | 68,4 |
| **D2** | 10,4 | 13,8 | 18,9 | 25,4 | 32,7 | 41,9 | 54,9 | 79,6 | 101,8 | 135,4 |
| **D3** | 12,6 | 18,7 | 28,5 | 33,2 | 34,5 | 36,1 | 36,4 | 40,3 | 40,2 | 42,2 |
| **D4** | 2,2 | 5,4 | 13,3 | 27,7 | 55,6 | 96,1 | 136,8 | 162,1 | 180,7 | 205,0 |

1. **Diagnóstico sem regressão:** calcula as diferenças $y_{t+1} - y_t$ e as razões $y_{t+1}/y_t$. O que observas em cada conjunto?
2. **Regressões:** faz as quatro na calculadora e compara gráficos e resíduos.
3. **Decisão:** escolhe um modelo para cada conjunto e justifica por escrito.
4. **Armadilha:** com D4, usa apenas os **4 primeiros pontos**, ajusta o modelo exponencial e prevê o valor em $t = 10$. Compara com o valor observado e explica.

**🔑 Chave do professor.**

| Conjunto | Modelo usado na simulação | Ajuste obtido (Python) |
|---|---|---|
| D1 | linear: $12 + 5{,}5\,t$, ruído de desvio-padrão 2 | $y \approx 11{,}41 + 5{,}66\,t$ |
| D2 | exponencial: $8\,e^{0{,}28\,t}$, ruído multiplicativo de 4% | $y \approx 7{,}78\,e^{0{,}286\,t}$ |
| D3 | logarítmico: $10 + 14\ln t$, ruído de desvio-padrão 1,2 | $y \approx 12{,}53 + 13{,}07\ln t$ |
| D4 | logístico: $K=200$, $r=0{,}9$, $t_0=6$, ruído multiplicativo de 4% | $K \approx 208{,}9$; $r \approx 0{,}789$; $t_0 \approx 6{,}27$ |

- As calculadoras fazem a regressão exponencial sobre $\ln y$, por isso os valores podem diferir ligeiramente dos acima.
- **Sinais a procurar:** D1 tem diferenças quase constantes; D2 tem razões quase constantes (cerca de 1,33); D3 tem diferenças a diminuir (e cada duplicação de $t$ acrescenta quase o mesmo); D4 tem razões que descem de ≈ 2,5 para ≈ 1,1 e diferenças que sobem e depois descem.
- **Discussão útil:** em D2 o ajuste logístico dá $K \approx 22\,000$, sem sentido. Um logístico sem curvatura visível é indistinguível de um exponencial. Em D3 o logístico quase empata com o logarítmico.
- **Armadilha:** os 4 primeiros pontos de D4 (2,2; 5,4; 13,3; 27,7) têm razões 2,45; 2,46; 2,08, quase constantes. A regressão exponencial prevê **≈ 4 800** em $t = 10$; o valor observado é **205,0**. O ajuste logístico com 4 pontos dá $K \approx 75$ (errado) e com 3 pontos dá um $K$ da ordem de $10^6$ (sem sentido). Com 5 pontos já dá $K \approx 207$, porque os dados chegam à zona do ponto de inflexão ($t_0 \approx 6$). **O limite só se estima bem quando a curva já começou a curvar.**

### A7. O boato ⭐⭐ (1 aula)

**Objectivo.** Ver uma simulação passar de crescimento exponencial a logístico e comparar a recorrência discreta com a curva contínua.

**Tarefa.** Numa turma de $N = 30$ alunos (adapta ao número real). Ronda 0: um aluno sabe o boato. Em cada ronda, **cada aluno que já sabe** escolhe **um colega ao acaso** (outro aluno, por cartas numeradas, dado ou gerador aleatório) e conta-lhe o boato. As actualizações são simultâneas.

1. Regista o número de alunos informados no fim de cada ronda. Repetir em 3 grupos e tirar a média.
2. Faz o gráfico. Em que rondas parece exponencial? Quando abranda e porquê?
3. Na calculadora gráfica faz a regressão logística. Interpreta $K$ e o ponto de inflexão.
4. Numa folha de cálculo, constrói a recorrência $P_{n+1} = P_n + P_n\left(1 - \dfrac{P_n}{N}\right)$ com $P_0 = 1$ e compara com os teus dados.
5. E se cada aluno contasse a **dois** colegas por ronda? Prevê antes de simular.

**🔑 Chave do professor.** Simulação do mesmo processo, com $N = 30$ e 4 000 repetições:

| Ronda | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Média de informados | 1,0 | 2,0 | 3,9 | 7,2 | 12,3 | 18,4 | 23,8 | 27,2 | 28,9 | 29,6 | 29,8 | 29,9 | 30,0 |
| Recorrência logística | 1,0 | 2,0 | 3,8 | 7,1 | 12,6 | 19,9 | 26,6 | 29,6 | 30,0 | 30,0 | 30,0 | 30,0 | 30,0 |

- Ajuste logístico à média: $K \approx 30{,}2$, $r \approx 0{,}82$, $t_0 \approx 4{,}4$ rondas.
- A recorrência é uma **aproximação**: acerta nas primeiras rondas (3,8; 7,1; 12,6) e satura mais depressa do que o processo real, porque na realidade vários alunos podem escolher o mesmo colega. Aproveita para falar das vantagens e desvantagens dos modelos discretos e contínuos.
- Cada simulação individual varia: nas 10 verificadas, todos ficaram informados entre a ronda 7 e a 12.

### A8. Projecto: modelar um fenómeno real e defender o modelo ⭐⭐⭐ (2 a 3 aulas + trabalho autónomo)

**Objectivo.** Aplicar o ciclo completo: dados oficiais, regressões, escolha do modelo e análise crítica.

**Tarefa (grupos de 2 a 3).**

1. Escolhe uma série de dados **oficiais** (população de uma cidade, utilizadores de internet, casos de uma doença, produção de energia solar, vendas de um produto).
2. Faz o gráfico e ajusta os quatro modelos com a calculadora ou o computador.
3. Compara os ajustes (resíduos, forma da curva) e escolhe um modelo, justificando.
4. Mostra o risco de extrapolar: o que prevê o teu modelo para daqui a 10 anos? É plausível?
5. Discute modelo discreto vs contínuo para o teu caso.
6. Apresenta em 5 minutos, com uma secção obrigatória: **"onde é que o meu modelo falha?"**

**Avaliação.** Grelha da secção 5.

### Desafios adicionais de crescimento (A9–A16)

Os desafios A9 a A16 acrescentam variedade: jogos, escalas, ciência, ambiente e simulação. Podem ser usados isoladamente.

### A9. A regra dos 72 ⭐⭐ (1 aula)

**Objectivo.** Relacionar a taxa de juro com o tempo de duplicação e avaliar um atalho de cálculo mental.

**Tarefa.** Um capital cresce a uma taxa fixa $i$ por ano: $C_n = C_0\,(1+i)^n$.

1. Para $i = 1\%, 2\%, 3\%, 5\%, 6\%, 8\%, 9\%, 12\%, 18\%$, determina o número de anos em que o capital duplica (por tentativa na folha de cálculo, ou resolvendo $(1+i)^n = 2$ com logaritmos).
2. Compara com $72/i$ (com $i$ em percentagem). Para que taxas a regra funciona melhor?
3. O tempo de duplicação depende do capital inicial? Justifica.
4. **Análise crítica.** Porque é que a regra é tão útil para decidir "de cabeça" e quando deixa de ser fiável?

**🔑 Chave do professor.** Tempo de duplicação exacto $\dfrac{\ln 2}{\ln(1+i)}$ contra $72/i$:

| $i$ (%) | 1 | 2 | 3 | 5 | 6 | 8 | 9 | 12 | 18 |
|---|---|---|---|---|---|---|---|---|---|
| Exacto (anos) | 69,66 | 35,00 | 23,45 | 14,21 | 11,90 | 9,01 | 8,04 | 6,12 | 4,19 |
| $72/i$ | 72,0 | 36,0 | 24,0 | 14,4 | 12,0 | 9,0 | 8,0 | 6,0 | 4,0 |

A regra é muito boa entre 6% e 10%, e o erro cresce para taxas muito baixas ou muito altas. O tempo de duplicação **não depende** do capital inicial: $C_0$ simplifica-se na equação. (O valor 72 é escolhido por ter muitos divisores; a regra "69,3" seria mais exacta para taxas pequenas.)

### A10. O tabuleiro de xadrez e o papel dobrado ⭐ (1 aula)

**Objectivo.** Sentir a diferença entre somar e multiplicar sempre o mesmo, com duas histórias clássicas.

**Tarefa.**

1. **Os grãos.** Numa casa do tabuleiro põe-se 1 grão, na seguinte 2, depois 4, e assim sucessivamente (cada casa tem o dobro da anterior). Quantos grãos tem a casa 64? E quantos há no tabuleiro todo? Compara com uma versão linear em que cada casa tem mais 1 grão do que a anterior.
2. **O papel.** Uma folha tem 0,1 mm de espessura. Cada dobra duplica o número de camadas. Calcula a espessura depois de 10, 20, 30 e 42 dobras. Compara com distâncias conhecidas (altura de um prédio, Terra–Lua).
3. Escreve a fórmula de cada sequência e classifica-a (aritmética ou geométrica).
4. **Análise crítica.** Porque é que, na prática, não conseguimos dobrar uma folha mais de 7 ou 8 vezes? O que falha no modelo?

**🔑 Chave do professor.**

- Casa 64: $2^{63} = 9\,223\,372\,036\,854\,775\,808$ grãos. No tabuleiro todo: $2^{64} - 1 = 18\,446\,744\,073\,709\,551\,615$. A versão linear dá 64 grãos na casa 64.
- Espessura $= 0{,}1\ \text{mm} \times 2^n$: 10 dobras ≈ 102,4 mm; 20 dobras ≈ 105 m; 30 dobras ≈ 107 km; 42 dobras ≈ 440 000 km, mais do que a distância Terra–Lua (cerca de 384 000 km, valor aproximado).
- O modelo ignora o comprimento de papel consumido em cada dobra, que também duplica; é um bom exemplo de limite físico de um modelo.

### A11. Escalas logarítmicas: decibéis, pH e sismos ⭐⭐ (1 aula)

**Objectivo.** Ver o modelo logarítmico como escala e perceber por que razão se usa quando os valores abrangem muitas ordens de grandeza.

**Tarefa.**

1. A intensidade sonora em decibéis é $L = 10\log_{10}\!\left(\dfrac{I}{I_0}\right)$. Calcula $L$ quando $I/I_0 = 1,\ 2,\ 10,\ 100,\ 1\,000$. O que acontece a $L$ quando a intensidade **duplica**? E quando **multiplica por 10**?
2. O pH é $-\log_{10}[\mathrm{H}^+]$. Quantas vezes é maior a concentração de $\mathrm{H}^+$ numa solução de pH 3 do que numa de pH 6?
3. Num sismo, cada aumento de 1 na escala de Richter corresponde a cerca de 32 vezes mais energia libertada ($10^{1,5}$). Quantas vezes mais energia liberta um sismo de magnitude 7 do que um de magnitude 5?
4. Liga ao modelo $y = a + b\ln t$: em todas estas escalas, o que significa "multiplicar a grandeza por um factor fixo"?
5. Porque é que se usam estas escalas em vez de números "normais"?

**🔑 Chave do professor.**

- Decibéis: razão 1 → 0 dB; 2 → 3,01 dB; 10 → 10 dB; 100 → 20 dB; 1 000 → 30 dB. Duplicar a intensidade acrescenta cerca de 3 dB; multiplicar por 10 acrescenta 10 dB.
- pH 3 contra pH 6: $10^{3} = 1\,000$ vezes mais $\mathrm{H}^+$.
- Magnitude 7 contra 5: $(10^{1,5})^{2} = 10^{3} = 1\,000$ vezes mais energia.
- Multiplicar a grandeza por um factor fixo **soma** um valor fixo na escala: é a propriedade do modelo logarítmico.

### A12. Linearizar para descobrir a taxa (papel semilogarítmico) ⭐⭐⭐ (1 aula)

**Objectivo.** Usar a transformação logarítmica para testar e ajustar um modelo exponencial.

**Tarefa.** Usa o conjunto **D2** de A6.

1. Calcula $\ln y$ para cada valor e representa $(t, \ln y)$. O que observas?
2. Faz a regressão linear de $\ln y$ sobre $t$. A recta tem declive $m$ e ordenada na origem $c$. Mostra que $y = e^{c}\,(e^{m})^{t}$.
3. Compara com a regressão exponencial da calculadora.
4. Calcula o tempo de duplicação $\ln 2 / m$.
5. Repete com D1 (linear). A transformação $(t, \ln y)$ também dá uma recta? Que diferença vês?

**🔑 Chave do professor.** Com D2: declive $m \approx 0{,}2839$, $e^{c} \approx 7{,}90$, factor por unidade de tempo $e^{m} \approx 1{,}328$ e tempo de duplicação ≈ **2,44** unidades. (O gerador usou $8e^{0{,}28t}$.) A regressão exponencial da calculadora faz exactamente este cálculo. Com D1, a representação $(t, \ln y)$ é curva: só os dados exponenciais ficam em linha recta depois da transformação.

### A13. Jogo dos dados: decaimento exponencial ⭐ (1 aula, prática)

**Objectivo.** Construir um modelo de decaimento com material simples e ligá-lo à "meia-vida".

**Tarefa.** Cada grupo tem 30 dados (ou moedas). Em cada ronda, lançam-se todos os dados que restam e **retiram-se os que saírem 6**. Registar quantos restam.

1. Faz o gráfico do número de dados que restam em cada ronda.
2. Quantos dados prevês que restem após cada ronda? Escreve o modelo $N_n = N_0\,b^{\,n}$ e estima $b$.
3. Junta os resultados de todos os grupos e compara a média com o modelo.
4. Estima a "meia-vida" (rondas para metade dos dados).
5. **Variante.** Retiram-se os dados que saírem 5 ou 6. Prevê o novo $b$ e a meia-vida **antes** de jogar.
6. Compara com o arrefecimento de A4: o que decai exponencialmente em cada caso?

**🔑 Chave do professor.** Cada dado sai com probabilidade $1/6$, logo $b = 5/6 \approx 0{,}833$. Com 100 dados, o valor esperado por ronda é: 100; 83,3; 69,4; 57,9; 48,2; 40,2; 33,5; 27,9; 23,3; 19,4; 16,2; 13,5; 11,2. Meia-vida $\ln 2 / \ln(6/5) \approx$ **3,8 rondas**. Na variante $b = 2/3$ e meia-vida $\ln 2/\ln 1{,}5 \approx 1{,}7$ rondas. Com 30 dados a aleatoriedade é grande: usa isto para mostrar que um modelo descreve a **tendência** e que juntar grupos reduz a variação.

### A14. Quando o modelo discreto "enlouquece" ⭐⭐⭐ (1 aula, folha de cálculo)

**Objectivo.** Comparar o modelo discreto logístico com o contínuo e descobrir os limites do discreto.

**Tarefa.** Constrói na folha de cálculo $P_{n+1} = P_n + r\,P_n\left(1 - \dfrac{P_n}{K}\right)$ com $K = 100$ e $P_0 = 5$.

1. Para $r = 0{,}5$ e $r = 1{,}8$, representa $P_n$ para 40 períodos. O que acontece?
2. Repete para $r = 2{,}2$, $r = 2{,}6$ e $r = 3{,}2$. Descreve o comportamento.
3. O modelo contínuo logístico (curva em S) alguma vez ultrapassa $K$ ou oscila? E o discreto?
4. Discute: o que representa um período muito longo (taxa $r$ grande por período)?

**🔑 Chave do professor.**

| $r$ | Comportamento | Exemplo |
|---|---|---|
| 0,5 | aproxima-se de 100 sem ultrapassar | $P_{10} = 86{,}0$ |
| 1,8 | ultrapassa 100 e estabiliza em 100 | $P_{10} = 102{,}2$ |
| 2,2 | oscila indefinidamente entre ≈ 74,6 e ≈ 116,3 | ciclo de período 2 |
| 2,6 | valores irregulares, sem padrão claro | ex.: $P_{10} = 45{,}1$ |
| 3,2 | os valores saem de controlo e tornam-se negativos | sem sentido |

O modelo discreto converge para $K$ se $r < 2$. O contínuo nunca oscila, o que mostra uma **desvantagem do discreto** (os passos grandes distorcem a dinâmica) e uma vantagem (fácil de simular). É conteúdo de enriquecimento.

### A15. Pescar sem esgotar ⭐⭐⭐ (1 aula, folha de cálculo)

**Objectivo.** Usar o modelo logístico para discutir sustentabilidade e decidir uma quota.

**Tarefa.** Um lago tem capacidade $K = 1\,000$ peixes e taxa de crescimento $r = 0{,}4$ por ano. Cada ano pescam-se $h$ peixes: $P_{n+1} = P_n + 0{,}4\,P_n\left(1 - \dfrac{P_n}{1000}\right) - h$, com $P_0 = 500$.

1. Simula 30 anos para $h = 80$, $h = 100$ e $h = 110$. Descreve cada caso.
2. Qual é o maior valor de $h$ que a população consegue sustentar? Em que população é atingido?
3. Porque é que a pesca máxima é arriscada?
4. Que quota recomendarias a um responsável local? Justifica.

**🔑 Chave do professor.**

- $h = 80$: a população sobe e estabiliza em ≈ **723,6** (equilíbrio estável).
- $h = 100$: fica em 500 (o máximo sustentável é $rK/4 = 100$, atingido em $P = K/2$).
- $h = 110$: a população desce todos os anos e, no ano 22, o modelo dá valor negativo: **colapso**.
- Com $h = 100$ o equilíbrio é frágil: o crescimento natural menos a pesca é $-0{,}4\,(P-500)^2/1000 \le 0$, por isso qualquer queda abaixo de 500 não recupera. Uma quota abaixo do máximo (por exemplo, 80) dá margem de segurança.

### A16. Associa a história ao modelo ⭐ (30 a 45 min, sem calculadora)

**Objectivo.** Treinar a escolha qualitativa do modelo antes de ajustar fórmulas.

**Tarefa.** Para cada situação, escolhe o modelo (linear, exponencial, logarítmico ou logístico), justifica numa frase e indica um **limite** do modelo.

1. Um bidão enche com uma torneira de caudal constante.
2. O número de células de uma cultura no início, com muito alimento.
3. Um jogador melhora muito nas primeiras horas de treino e depois cada vez menos.
4. Uma aplicação nova: poucos utilizadores, depois uma subida rápida, e por fim quase toda a população interessada já a usa.
5. O saldo de uma conta com juros compostos.
6. A temperatura de uma bebida quente a aproximar-se da temperatura da sala.
7. Uma bola a rolar a velocidade constante: distância percorrida.

**🔑 Chave do professor.** 1 linear · 2 exponencial · 3 logarítmico (ou logístico, se houver tecto; discutir) · 4 logístico · 5 exponencial · 6 exponencial **para a diferença** de temperaturas (A4) · 7 linear. Aceita justificações bem argumentadas em 3 e 6.

---

## 3. Parte B: modelos de grafos

### B1. Do mapa ao grafo ⭐ (1 aula)

**Objectivo.** Representar uma situação real por um grafo e discutir o significado dos pesos.

**Tarefa.**

1. Escolhe uma situação de distribuição ou recolha (recolha de lixo num bairro, entrega de correio, patrulhamento do recreio, distribuição do jornal da escola).
2. Desenha o mapa e transforma-o num grafo: vértices (cruzamentos ou locais), arestas (ruas ou ligações) e **pesos**.
3. Preenche uma tabela com o grau de cada vértice e verifica que a soma dos graus é o dobro do número de arestas.
4. O grafo é conexo? Justifica.
5. **Pesos.** Que significado podem ter (quilómetros, tempo, consumo, poluição, custo)? Mostra, com um exemplo, como a solução óptima pode mudar consoante o peso escolhido.

**Entregável.** Grafo, tabela de graus e um parágrafo sobre o significado dos pesos.

**🔑 Chave do professor.** A verificação "soma dos graus = 2 × arestas" apanha erros de desenho. No grafo de B2: graus 2, 3, 3, 2, 3, 3, soma 16 = 2 × 8 arestas.

### B2. O camião do lixo: circuitos de Euler ⭐⭐ (1 a 2 aulas)

**Objectivo.** Descobrir quando existe um percurso que passa em todas as ruas uma só vez e como minimizar repetições quando não existe.

**Ficha do aluno.** Um bairro com 6 cruzamentos, A a F. As ruas e os comprimentos (em centenas de metros) são:

| Rua | AB | AF | BC | BE | CD | DE | EF | CF |
|---|---|---|---|---|---|---|---|---|
| Comprimento | 4 | 6 | 3 | 7 | 5 | 4 | 3 | 8 |

1. Desenha o grafo e calcula o grau de cada vértice.
2. O camião consegue passar por todas as ruas **uma única vez** e voltar ao ponto de partida? Que condição sobre os graus observas?
3. Se não consegue, que ruas deve repetir para gastar o mínimo? Descreve a estratégia **passo a passo** e justifica.
4. Qual é o comprimento do melhor percurso?
5. Remove a rua CF. Passa a existir um percurso (sem ter de regressar)? Onde começa e onde acaba?
6. Quantas ruas novas, no mínimo, teriam de ser construídas para existir um circuito sem repetições? Onde?

**🔑 Chave do professor.**

- Graus: A 2, B 3, C 3, D 2, E 3, F 3. Há **4 vértices de grau ímpar** (B, C, E, F), logo **não existe** circuito de Euler. Comprimento total das ruas: 40 (4,0 km).
- Estratégia: emparelhar os vértices ímpares de modo que o total dos caminhos mais curtos entre pares seja mínimo.
- Distâncias mais curtas entre ímpares: BC = 3, BE = 7, BF = 10 (via E), CE = 9 (via D), CF = 8, EF = 3.
- Emparelhamentos: {BC, EF} = 6; {BE, CF} = 15; {BF, CE} = 19. **O melhor repete as ruas BC e EF.**
- Melhor percurso: 40 + 6 = **46** (4,6 km).
- Sem a rua CF restam 2 vértices ímpares (B e E): existe um **percurso de Euler de B até E**, com 32 (3,2 km), sem repetições.
- Para um circuito sem repetições bastam **2 ruas novas** (por exemplo, uma ligando B a F e outra ligando C a E, que ainda não existem), que deixam todos os graus pares.

### B3. Visitar todos os locais: Hamilton e caixeiro-viajante ⭐⭐ (1 a 2 aulas)

**Objectivo.** Usar uma árvore de possibilidades para calcular os pesos totais de todos os circuitos e comparar com uma estratégia passo a passo.

**Ficha do aluno.** Uma escola **fictícia** com 5 locais: Portaria (P), Biblioteca (B), Cantina (C), Ginásio (G) e Laboratórios (L). Distâncias em metros:

| | P | B | C | G | L |
|---|---|---|---|---|---|
| **P** | 0 | 180 | 160 | 110 | 300 |
| **B** | 180 | 0 | 250 | 190 | 270 |
| **C** | 160 | 250 | 0 | 230 | 220 |
| **G** | 110 | 190 | 230 | 0 | 260 |
| **L** | 300 | 270 | 220 | 260 | 0 |

Um visitante começa e acaba na Portaria e quer passar **uma só vez** em cada um dos outros locais.

1. Constrói a **árvore de possibilidades** (com P no início). Quantas sequências há? Porque é que cada circuito aparece duas vezes?
2. Calcula o peso total de cada circuito e identifica o de menor peso.
3. **Vizinho mais próximo:** parte da Portaria e vai sempre para o local mais próximo ainda não visitado; no fim, volta. Quanto dá? Compara com o óptimo.
4. Repete o vizinho mais próximo partindo de outro local. O resultado muda?
5. Vale a pena procurar o óptimo? (Ver B4.)

**🔑 Chave do professor.** Há $4! = 24$ sequências, e cada circuito conta-se duas vezes (sentido contrário), logo **12 circuitos**:

| Circuito | Peso (m) | Circuito | Peso (m) |
|---|---|---|---|
| P–C–L–B–G–P | **950** | P–B–L–G–C–P | 1 100 |
| P–B–G–L–C–P | 1 010 | P–B–G–C–L–P | 1 120 |
| P–B–L–C–G–P | 1 010 | P–C–G–B–L–P | 1 150 |
| P–B–C–L–G–P | 1 020 | P–C–B–G–L–P | 1 160 |
| P–C–B–L–G–P | 1 050 | P–G–C–B–L–P | 1 160 |
| P–G–B–C–L–P | 1 070 | P–B–C–G–L–P | 1 220 |

- **Óptimo: 950 m**, circuito P–C–L–B–G–P (único).
- **Vizinho mais próximo a partir de P:** P–G–B–C–L–P = 1 070 m, **12,6% acima** do óptimo.
- A partir de B: 1 010 m. A partir de C, G ou L: **950 m** (o óptimo). O ponto de partida muda o resultado.
- As distâncias são todas diferentes, para não haver empates na estratégia.

### B4. Quantas rotas? A explosão combinatória ⭐⭐ (1 aula)

**Objectivo.** Ligar os dois subtemas: perceber porque é que procurar a solução óptima pode ser inviável e comparar tipos de crescimento.

**Tarefa.**

1. Num grafo completo com $n$ locais, o número de circuitos de Hamilton é $\dfrac{(n-1)!}{2}$. Verifica com $n = 5$ (B3: 12 circuitos) e completa uma tabela na folha de cálculo para $n = 4, \dots, 10$.
2. Representa na mesma folha $(n-1)!/2$, $2^n$ e $n^3$. Compara os gráficos. Calcula as razões entre termos consecutivos de cada sequência.
3. Se um computador testar $10^9$ rotas por segundo (hipótese), quanto tempo demora para $n = 15$, $20$ e $25$?
4. **Discussão (aprendizagem essencial).** Qual é a utilidade e a viabilidade económica de procurar a solução óptima, comparada com a do vizinho mais próximo? Quando compensa?

**🔑 Chave do professor.**

| $n$ | Circuitos $(n-1)!/2$ | $2^n$ | $n^3$ | Tempo a $10^9$ rotas/s |
|---|---|---|---|---|
| 5 | 12 | 32 | 125 | desprezável |
| 6 | 60 | 64 | 216 | desprezável |
| 7 | 360 | 128 | 343 | desprezável |
| 8 | 2 520 | 256 | 512 | desprezável |
| 10 | 181 440 | 1 024 | 1 000 | 0,18 ms |
| 12 | 19 958 400 | 4 096 | 1 728 | 20 ms |
| 15 | 43 589 145 600 | 32 768 | 3 375 | ≈ 44 s |
| 18 | 177 843 714 048 000 | 262 144 | 5 832 | ≈ 49 h |
| 20 | ≈ $6{,}08\times 10^{16}$ | 1 048 576 | 8 000 | ≈ 1,9 anos |
| 25 | ≈ $3{,}10\times 10^{23}$ | 33 554 432 | 15 625 | ≈ 9,8 milhões de anos |

- A razão entre termos consecutivos de $(n-1)!/2$ é $n$: **cresce sem limite**. Em $2^n$ é constante (2). O factorial ultrapassa qualquer exponencial.
- A velocidade de $10^9$ rotas por segundo é uma hipótese; os tempos são ordens de grandeza.
- Para $n = 5$ (B3) o vizinho mais próximo ficou 12,6% acima do óptimo no pior caso. Discute se essa diferença justifica o custo de procurar mais.

### B5. Ruas de sentido único: grafos orientados ⭐⭐ (1 aula)

**Objectivo.** Descobrir a condição para um circuito que percorre cada rua uma vez no sentido permitido.

**Ficha do aluno.** Um bairro com 5 cruzamentos (1 a 5) e 6 ruas: 1–2, 2–3, 3–1, 3–4, 4–5, 5–3 (dois triângulos que partilham o cruzamento 3).

1. Sem sentidos únicos, existe circuito de Euler? Encontra um.
2. A câmara quer sentido único em todas as ruas. Escolhe sentidos para que o camião ainda consiga percorrer cada rua uma só vez e voltar ao início.
3. Mostra uma escolha **errada** (por exemplo, 1→2, 2→3, 1→3, com o outro triângulo orientado como quiseres) e explica porque falha.
4. Que regra observas sobre as ruas que entram e as que saem de cada cruzamento?
5. Quantas formas há de dar sentido às 6 ruas? Em quantas o camião consegue fazer o circuito?

**🔑 Chave do professor.** Graus: 1, 2, 4, 2, 2 para os cruzamentos 1, 2, 3, 4, 5 (todos pares), logo existe circuito de Euler.

- Regra: em cada cruzamento, o número de ruas que **entram** tem de ser igual ao número de ruas que **saem** (e o grafo tem de ser conexo).
- Orientação válida: cada triângulo orientado **ciclicamente** (por exemplo, 1→2→3→1 e 3→4→5→3).
- Há $2^6 = 64$ formas de orientar as 6 ruas, e só **4** têm entradas iguais a saídas em todos os cruzamentos (2 sentidos por triângulo).
- Ligação ao crescimento: com $m$ ruas há $2^m$ orientações possíveis. Com 30 ruas são $2^{30} = 1\,073\,741\,824$.
- A condição "entradas = saídas" não é nomeada no excerto do programa que li; trata como extensão natural dos grafos orientados.

### B6. Ligar os edifícios com o mínimo de cabo ⭐⭐ (opcional, 1 aula)

> **Extensão opcional.** O excerto do programa que li não nomeia a árvore geradora mínima. Usa-a só se o programa da tua escola a incluir ou como enriquecimento.

**Tarefa.** Com as distâncias de B3, a escola quer ligar os 5 locais com cabo de fibra, ao menor comprimento total, sem fazer circuitos fechados.

1. Ordena as 10 ligações possíveis por comprimento.
2. Escolhe-as por ordem crescente, recusando as que formam um circuito fechado, até ligares todos os locais (algoritmo de Kruskal).
3. Quantas ligações tem a rede obtida? Compara com o número de ligações de um grafo completo com $n$ locais, $n(n-1)/2$.
4. Compara o comprimento do cabo com o do melhor circuito de B3.

**🔑 Chave do professor.** Ordem: PG 110, PC 160, PB 180, BG 190 (recusada: fecha o circuito P–B–G), CL 220. **Rede mínima: PG, PC, PB, CL = 670 m**, com 4 ligações ($n - 1$). O melhor circuito de B3 tem 950 m.

Crescimento das ligações: árvore $n-1$ (linear) contra grafo completo $n(n-1)/2$ (quadrático).

| $n$ | 5 | 10 | 20 | 50 | 100 |
|---|---|---|---|---|---|
| Árvore: $n-1$ | 4 | 9 | 19 | 49 | 99 |
| Grafo completo | 10 | 45 | 190 | 1 225 | 4 950 |

### B7. Projecto: propor uma solução a quem decide ⭐⭐⭐ (2 a 3 aulas + trabalho autónomo)

**Objectivo.** Modelar um problema local de distribuição ou recolha, propor soluções e discutir a sua viabilidade.

**Tarefa (grupos de 2 a 3).**

1. Escolhe um problema real e local (recolha de resíduos num bairro, limpeza de ruas, entrega de correio, patrulhamento do recreio).
2. Recolhe o mapa e as medidas (distâncias, tempos). Não uses moradas de pessoas.
3. Modela com um grafo e **define o que significa o peso** (quilómetros, tempo, combustível, emissões).
4. Procura soluções com o que aprendeste (Euler, Hamilton, vizinho mais próximo) e **compara pelo menos duas alternativas**.
5. Discute a **viabilidade económica** de procurar a solução óptima (liga a B4).
6. Apresenta uma proposta de uma página e 3 minutos orais a um destinatário real ou simulado (junta de freguesia, direcção da escola).

**Avaliação.** Grelha da secção 5.

### Desafios adicionais de grafos (B8–B14)

### B8. Pontes de Königsberg e desenhar sem levantar o lápis ⭐ (1 aula)

**Objectivo.** Descobrir, a partir de puzzles, a condição de existência de percursos de Euler.

**Tarefa.**

1. **Königsberg.** Quatro zonas de terra (A, B, C, D) estão ligadas por 7 pontes: A tem 5 pontes, B, C e D têm 3 cada. É possível passar por todas as pontes uma só vez? Representa por um grafo (zonas = vértices, pontes = arestas) e justifica.
2. **A casinha.** Desenha um quadrado com as duas diagonais e um telhado triangular. Os vértices são A e B (base), C e D (topo do quadrado) e E (ponta do telhado). As arestas são AB, AC, BD, CD, AD, BC, CE e DE. É possível desenhá-la sem levantar o lápis e sem repetir linhas? Onde tens de começar?
3. Inventa um desenho que **não** se consiga fazer e outro que se consiga com recomeço no ponto inicial.

**🔑 Chave do professor.**

- Königsberg: graus 5, 3, 3, 3, ou seja, 4 vértices ímpares, logo **impossível** (nem circuito nem percurso).
- Casinha: graus A 3, B 3, C 4, D 4, E 2; soma 16 = 2 × 8 arestas. Há **2 vértices ímpares** (A e B): existe um percurso de Euler que começa num e acaba no outro.
- Resumo: 0 vértices ímpares → circuito de Euler; 2 → percurso de Euler entre eles; mais de 2 → impossível.

### B9. O carteiro com dois cruzamentos ímpares ⭐⭐ (1 aula)

**Objectivo.** Aplicar a estratégia de repetição mínima numa situação mais simples do que B2.

**Ficha do aluno.** Sete cruzamentos (A a G) e dez ruas (comprimentos em centenas de metros): AB 5, AC 3, BC 4, BD 6, CD 8, CE 5, DE 2, DF 7, EG 6, FG 3.

1. Desenha o grafo e determina o grau de cada vértice.
2. O carteiro pode percorrer todas as ruas uma só vez e voltar ao ponto de partida? Se não, quais as ruas a repetir, no mínimo?
3. Se o carteiro puder terminar noutro cruzamento, qual é o percurso mais curto e onde começa e acaba?
4. Compara os dois cenários (circuito com repetição e percurso aberto).

**🔑 Chave do professor.**

- Graus: A 2, B 3, C 4, D 4, E 3, F 2, G 2 (soma 20 = 2 × 10). Os ímpares são **B e E**. Comprimento total das ruas: 49.
- Caminho mais curto de B a E: B–D–E = 6 + 2 = 8 (B–C–E dá 9). Repetem-se BD e DE.
- Circuito com repetição: 49 + 8 = **57** (5,7 km).
- Percurso aberto de B até E (ou de E até B), sem repetições: **49** (4,9 km).

### B10. Seis entregas: o mapa de uma turma inteira ⭐⭐ (1 a 2 aulas, trabalho colaborativo)

**Objectivo.** Perceber que com 6 locais já há 60 circuitos e organizar o trabalho por grupos.

**Ficha do aluno.** Um estafeta parte do armazém A e visita B, C, D, E e F uma só vez cada, voltando a A. Distâncias em unidades de 100 m (mapa fictício):

| | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| **A** | 0 | 60 | 40 | 100 | 55 | 175 |
| **B** | 60 | 0 | 140 | 90 | 95 | 120 |
| **C** | 40 | 140 | 0 | 80 | 145 | 50 |
| **D** | 100 | 90 | 80 | 0 | 35 | 160 |
| **E** | 55 | 95 | 145 | 35 | 0 | 20 |
| **F** | 175 | 120 | 50 | 160 | 20 | 0 |

1. Quantos circuitos distintos existem? (Usa uma árvore e a fórmula $(n-1)!/2$.)
2. Divide os circuitos pelos grupos da turma (por exemplo, por segundo local visitado) e determina o de menor peso.
3. Aplica o vizinho mais próximo partindo de cada um dos 6 locais. Qual a diferença para o óptimo?
4. Qual o interesse prático de uma boa heurística?

**🔑 Chave do professor.** $(6-1)!/2 = 60$ circuitos. O óptimo, **295**, é o circuito A–B–D–E–F–C–A (único; o seguinte tem 355). Vizinho mais próximo: a partir de A, B, D ou E dá 295 (o óptimo, às vezes percorrido ao contrário); a partir de F dá 355; a partir de C dá **405** (37% acima do óptimo). Mais uma vez, o ponto de partida muda o resultado.

### B11. Torneios, apertos de mão e grafos completos ⭐ (1 aula)

**Objectivo.** Usar o grafo completo $K_n$ para ligar contagens combinatórias, Euler e Hamilton.

**Tarefa.**

1. Numa turma, cada aluno cumprimenta cada outro uma vez. Quantos apertos de mão há para $n = 5, 8, 16, 20$? Modela por um grafo.
2. Um torneio todos contra todos de $n$ equipas: quantos jogos há? E se for com jogos em casa e fora?
3. Para que valores de $n$ existe circuito de Euler em $K_n$? (Calcula o grau de cada vértice.) Verifica com $K_4$ e $K_5$.
4. Existe sempre circuito de Hamilton em $K_n$ ($n \ge 3$)? Justifica.
5. Classifica o crescimento do número de arestas de $K_n$ (linear, quadrático, exponencial?).

**🔑 Chave do professor.** Arestas de $K_n$: $n(n-1)/2$. Valores: 10 (n = 5), 28 (n = 8), 120 (n = 16), 190 (n = 20). Com jogos em casa e fora há $n(n-1)$. Cada vértice tem grau $n-1$, logo há circuito de Euler quando $n$ é **ímpar** ($K_5$ sim, $K_4$ não). Há sempre circuito de Hamilton em $K_n$ (todos os vértices estão ligados entre si). O crescimento é **quadrático**, não exponencial.

### B12. Mesmo mapa, outro peso, outra solução ⭐⭐ (1 aula)

**Objectivo.** Mostrar que a "melhor" solução depende do que o peso representa.

**Tarefa.** Usa a escola fictícia de B3. A câmara informa que a ligação **Cantina–Laboratórios** (220 m) vai ter obras e demora o equivalente a 520 m.

1. Recalcula o peso dos 12 circuitos com o novo valor para C–L.
2. Qual é agora o circuito óptimo? Muda?
3. Qual o peso do circuito que era óptimo em B3 com as obras?
4. Dá exemplos de três "pesos" diferentes que poderiam definir o mesmo mapa (tempo, custo, poluição) e discute se o óptimo seria o mesmo.

**🔑 Chave do professor.** O circuito P–C–L–B–G–P, que era óptimo (950 m), usa C–L e passa a pesar $950 - 220 + 520 = 1\,250$. O novo óptimo é **P–C–B–L–G–P = 1 050** (160 + 250 + 270 + 260 + 110), único; o seguinte é P–B–L–G–C–P com 1 100. As soluções óptimas dependem do critério, o que liga ao objectivo "discutir o significado dos pesos".

### B13. Árvores de contagem ⭐ (1 aula)

**Objectivo.** Usar árvores como esquema combinatório para contar possibilidades e restringir percursos.

**Tarefa.**

1. Um menu tem 3 entradas, 4 pratos e 2 sobremesas. Constrói a árvore e conta os menus possíveis.
2. Um código tem 3 algarismos distintos (0 a 9). Quantos códigos há?
3. Em B3, quantos circuitos começam por P–G (Portaria–Ginásio)? Constrói apenas esse ramo da árvore e calcula o peso de cada um.
4. Explica como uma árvore pode "podar" caminhos que já são piores do que o melhor conhecido e porque isso poupa trabalho.

**🔑 Chave do professor.** 1) $3\times4\times2 = 24$. 2) $10\times9\times8 = 720$. 3) Depois de P–G sobram 3 locais por ordenar: $3! = 6$ sequências; todas contam como circuitos diferentes desde que se fixe o sentido. Os pesos obtêm-se da tabela de B3 (P–G–B–C–L–P = 1 070, por exemplo). 4) Se um ramo já ultrapassa o melhor total, não vale a pena continuá-lo.

### B14. Concurso de algoritmos ⭐⭐⭐ (1 a 2 aulas)

**Objectivo.** Desenvolver estratégias passo a passo e compará-las.

**Ficha do aluno.** Sete locais A a G, distâncias em unidades de 100 m (mapa fictício, sem relação com um mapa real):

| | A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|---|
| **A** | 0 | 100 | 130 | 185 | 25 | 165 | 140 |
| **B** | 100 | 0 | 55 | 120 | 180 | 45 | 35 |
| **C** | 130 | 55 | 0 | 75 | 95 | 175 | 80 |
| **D** | 185 | 120 | 75 | 0 | 105 | 145 | 110 |
| **E** | 25 | 180 | 95 | 105 | 0 | 190 | 20 |
| **F** | 165 | 45 | 175 | 145 | 190 | 0 | 50 |
| **G** | 140 | 35 | 80 | 110 | 20 | 50 | 0 |

**Tarefa.** Cada grupo desenha um **algoritmo** (instruções claras, passo a passo) para construir um circuito que parte de A e visita todos os locais. Pode ser o vizinho mais próximo, "escolher sempre a ligação mais curta que não feche o circuito antes do fim", ou outra ideia. Cada grupo aplica-o, regista o peso e apresenta o procedimento. Depois a turma compara.

1. Quantos circuitos existem? (Fórmula $(n-1)!/2$.)
2. Qual é o melhor resultado obtido pela turma? Qual a sua distância relativa ao óptimo (que só o professor conhece)?
3. Que dificuldades surgiram? Um algoritmo pode dar um resultado diferente consoante o ponto de partida?

**🔑 Chave do professor.** $(7-1)!/2 = 360$ circuitos. Óptimo: **455**, circuito A–D–C–B–F–G–E–A (185 + 75 + 55 + 45 + 50 + 20 + 25); o seguinte tem 465. Vizinho mais próximo: 475 a partir de A, B, E ou F (+4,4%); 490 a partir de G (+7,7%); 520 a partir de C ou D (+14,3%).

### Desafios avançados (para os melhores alunos) ⭐⭐⭐⭐

Estes desafios vão além do que o programa pede (demonstrações, optimização, programação). São **enriquecimento**: não devem ser avaliados como obrigatórios. Podem ser dados a pares de alunos fortes, em trabalho autónomo, com apresentação curta à turma.

### A17. Estimar o limite $K$ da logística por linearização ⭐⭐⭐⭐ (trabalho autónomo)

**Objectivo.** Perceber como se estima $K$ e porque é tão sensível aos dados.

**Tarefa.** Usa o conjunto **D4** de A6 (que ultrapassa 200 no último ponto).

1. Mostra que, se $P = \dfrac{K}{1+Ae^{-rt}}$, então $\ln\dfrac{P}{K-P} = r\,(t - t_0)$ com $t_0 = \dfrac{\ln A}{r}$ (uma recta em $t$).
2. Porque é que $K$ tem de ser maior do que o maior valor observado? Qual é o valor mínimo possível para $K$ com D4?
3. Para vários valores de $K$ (por exemplo, de 206 a 260), calcula $\ln\dfrac{P}{K-P}$ para os 10 pontos e a regressão linear contra $t$. Representa o coeficiente de determinação $R^2$ em função de $K$.
4. Escolhe o $K$ que maximiza $R^2$ e compara com a regressão logística da calculadora.
5. Discute: quanto muda $r$ quando $K$ muda de 210 para 220? O que isso diz sobre a fiabilidade de prever o limite?

**🔑 Chave do professor.**

- Como $P_{10} = 205{,}0$, tem de ser $K > 205{,}0$.
- Com $K = 210$: $r \approx 0{,}851$, $t_0 \approx 6{,}27$ ($R^2 \approx 0{,}990$). Com $K = 220$: $r \approx 0{,}778$, $t_0 \approx 6{,}61$ ($R^2 \approx 0{,}994$).
- A varredura de $K$ entre 206 e 260 dá $R^2$ máximo perto de $K \approx 216$ ($R^2 \approx 0{,}995$), enquanto o ajuste logístico directo (mínimos quadrados em $P$) dá $K \approx 208{,}9$ (o valor verdadeiro da simulação é 200). Linearizar e ajustar directamente **minimizam erros diferentes**; por isso as estimativas diferem. É uma boa oportunidade para discutir.
- O último ponto está perto de $K$, e aí $\ln\frac{P}{K-P}$ muda muito com $K$: pequenos erros nos dados deslocam $K$.

### A18. De onde vem o número $e$? Juros contínuos ⭐⭐⭐⭐ (1 aula)

**Objectivo.** Ligar o modelo discreto (capitalização) ao contínuo ($e^{rt}$).

**Tarefa.** Um capital $C_0 = 1$ cresce à taxa anual $100\%$ (para simplificar), capitalizado $n$ vezes por ano: $C(1) = \left(1 + \frac1n\right)^n$.

1. Calcula $\left(1 + \frac1n\right)^n$ para $n = 1, 10, 100, 1\,000, 10^6$. O que observas?
2. Com taxa anual $r$ e capitalização $n$ vezes por ano, o capital após $t$ anos é $C_0\left(1 + \frac rn\right)^{nt}$. Mostra, com a mesma ideia, que o limite quando $n\to\infty$ é $C_0\,e^{rt}$.
3. Um banco paga 5% ao ano. Compara o capital após 10 anos, a partir de 1 000 €, com capitalização anual, mensal e contínua.
4. Relaciona a razão discreta $b = 1+i$ com a taxa contínua $k$: $b = e^{k}$. Calcula $k$ para $i = 5\%$.
5. Qual a taxa anual equivalente (efectiva) a uma taxa contínua de 5%?

**🔑 Chave do professor.**

- $\left(1+\frac1n\right)^n$: $n=1 \to 2$; $n=10 \to 2{,}5937$; $n=100 \to 2{,}7048$; $n=1\,000 \to 2{,}7169$; $n=10^6 \to 2{,}71828$ (tende para $e \approx 2{,}71828$).
- Para 1 000 € a 5% durante 10 anos: anual $1\,000\cdot 1{,}05^{10} \approx 1\,628{,}89$ €; mensal $1\,000\left(1+\frac{0{,}05}{12}\right)^{120} \approx 1\,647{,}01$ €; contínua $1\,000\,e^{0{,}5} \approx 1\,648{,}72$ €.
- $k = \ln 1{,}05 \approx 0{,}04879$. Taxa efectiva de $5\%$ contínua: $e^{0{,}05}-1 \approx 5{,}127\%$.

### A19. Qual o melhor modelo? Comparação com AIC ⭐⭐⭐⭐ (1 aula)

**Objectivo.** Usar um critério quantitativo que equilibra o ajuste e o número de parâmetros.

**Tarefa.** Para cada conjunto D1–D4 de A6, ajusta os quatro modelos (linear, exponencial, logarítmico, logístico) e calcula a soma dos quadrados dos resíduos (RSS). Depois calcula $\text{AIC} = n\ln\dfrac{\text{RSS}}{n} + 2k$, com $n = 10$ e $k$ o número de parâmetros (2 nos três primeiros modelos, 3 no logístico).

1. Preenche a tabela de AIC. O valor menor indica o modelo preferido.
2. O critério escolhe o modelo que gerou os dados em todos os casos? Se não, porquê?
3. Em D2 e D3 o logístico quase empata com o melhor. Como se explica? A penalização $2k$ ajuda?
4. **Limites.** Com 10 pontos, quão fiável é a escolha? O que mudaria com 30 pontos ou com mais ruído?

**🔑 Chave do professor.** AIC (RSS entre parênteses), ajustes por mínimos quadrados não lineares:

| | Linear | Exponencial | Logarítmico | Logístico |
|---|---|---|---|---|
| **D1** | **17,5** (38,4) | 28,7 (117,6) | 37,2 (276,6) | 19,3 (37,7) |
| **D2** | 55,7 (1 764,4) | **10,6** (19,3) | 66,8 (5 343,8) | 12,6 (19,3) |
| **D3** | 29,6 (129,8) | 33,5 (191,8) | **12,1** (22,4) | 14,2 (22,7) |
| **D4** | 57,6 (2 123,5) | 65,0 (4 471,5) | 74,9 (12 011,5) | **31,7** (130,8) |

Em cada conjunto o AIC mais baixo coincide com o modelo que gerou os dados. Em D2 o logístico tem o mesmo RSS que o exponencial (o ajuste degenera para $K$ enorme) e perde por causa do parâmetro extra. Em D1 o logístico tem RSS ligeiramente inferior ao linear, mas não compensa o terceiro parâmetro. Estes resultados são de **um** conjunto simulado e não provam que o critério acerta sempre; o caderno 05 do projecto estuda isto por simulação.

### A20. Demonstrar a logística e o ponto de máximo crescimento ⭐⭐⭐⭐ (trabalho autónomo)

**Objectivo.** Verificar algebricamente que a curva em S resolve a equação da taxa e determinar onde o crescimento é máximo.

**Tarefa.**

1. Seja $u = Ae^{-rt}$ e $P = \dfrac{K}{1+u}$. Mostra que $\dfrac{dP}{dt} = rP\left(1-\dfrac PK\right)$. (Sugestão: $u' = -ru$.)
2. A taxa $\dfrac{dP}{dt}$ vista como função de $P$ é uma parábola. Determina o seu máximo e o valor de $P$ onde ocorre.
3. Mostra que o máximo da taxa ocorre quando $u = 1$, ou seja, $t_0 = \dfrac{\ln A}{r}$, e que nesse instante $P = K/2$.
4. Aplica a D4 com $K = 200$ e $r = 0{,}9$: qual é a taxa máxima e para que população? Confirma numa tabela de variações médias.
5. Qual a interpretação para quem gere uma população (por exemplo, a pesca de A15)?

**🔑 Chave do professor.**

1. $P' = \dfrac{-K u'}{(1+u)^2} = \dfrac{Kru}{(1+u)^2}$ e $rP\left(1-\dfrac PK\right) = r\cdot\dfrac{K}{1+u}\cdot\dfrac{u}{1+u}$, que é igual.
2. A parábola $rP - rP^2/K$ tem máximo em $P = K/2$, com valor $rK/4$.
3. $P = K/2 \iff 1+u = 2 \iff u = 1 \iff t = \ln A / r$.
4. Taxa máxima $0{,}9\times200/4 = 45$ unidades por unidade de tempo, quando $P = 100$.
5. O ponto de crescimento máximo é onde a população se recupera mais depressa, e o rendimento máximo sustentável é $rK/4$ (ver A15).

### B15. Demonstrar a condição de Euler ⭐⭐⭐⭐ (1 aula)

**Objectivo.** Passar da observação à demonstração.

**Tarefa.**

1. **Lema dos apertos de mão.** Mostra que a soma dos graus é $2a$ (com $a$ o número de arestas). Conclui que o número de vértices de grau ímpar é par.
2. Mostra que, num circuito de Euler, cada vez que o percurso **entra** num vértice também **sai**; deduz que todos os vértices têm grau par.
3. Mostra que um percurso de Euler que não é circuito tem exactamente dois vértices de grau ímpar (o primeiro e o último).
4. (Desafio extra) Explica por que razão, num grafo conexo com todos os graus pares, existe sempre circuito de Euler. Basta descrever a ideia da demonstração.
5. Usa estes resultados para mostrar que não existe um grafo com 5 vértices de grau ímpar.

**🔑 Chave do professor.**

1. Cada aresta contribui com 1 ao grau de cada uma das suas duas extremidades, logo a soma dos graus é $2a$, um número par. Se houvesse um número ímpar de vértices ímpares, a soma seria ímpar.
2. Em cada passagem por um vértice usam-se duas arestas (uma que entra, outra que sai), e no início/fim a primeira e a última aresta emparelham-se no vértice inicial. Logo o grau é par.
3. O vértice inicial usa uma aresta de saída sem entrada correspondente, e o final uma entrada sem saída: ambos têm grau ímpar; os restantes são pares.
4. Ideia: partindo de um vértice, avança-se sem repetir arestas; com graus pares, só se fica "preso" no ponto de partida. Se sobrarem arestas, juntam-se os circuitos que passam por vértices comuns (conexidade).
5. Impossível, pelo lema (o número de vértices ímpares é par).

### B16. O cubo: Hamilton sim, Euler não ⭐⭐⭐⭐ (1 aula)

**Objectivo.** Mostrar que os dois tipos de circuito são independentes.

**Tarefa.** O grafo do cubo tem 8 vértices (os cantos do cubo) e 12 arestas (as arestas do cubo).

1. Calcula o grau de cada vértice. Existe circuito de Euler?
2. Encontra um circuito de Hamilton.
3. Quantos circuitos de Hamilton distintos tem (considera iguais os que diferem só no ponto de partida e no sentido)?
4. Dá um exemplo de grafo com circuito de Euler mas sem circuito de Hamilton, ou explica por que é difícil encontrar um.
5. Resume numa frase a diferença entre "passar por todas as **arestas**" e "passar por todos os **vértices**".

**🔑 Chave do professor.**

1. Cada vértice tem grau 3 (ímpar); não existe circuito de Euler.
2. Por exemplo, numerando os cantos em binário (000, 001, 011, 010, 110, 111, 101, 100) e voltando a 000 (cada passo muda um bit).
3. Há **6** circuitos de Hamilton distintos (12 percursos dirigidos a partir de um vértice dado, contando os dois sentidos).
4. Por exemplo, dois triângulos que partilham um vértice (B5): todos os graus são pares, mas o vértice partilhado seria visitado duas vezes num circuito que passa por todos os vértices, por isso **não** há circuito de Hamilton.
5. Euler: cobrir todas as arestas (condição simples sobre os graus). Hamilton: visitar todos os vértices (não há condição simples e geral; é o problema difícil).

### B17. Quão bom pode ser o óptimo? Um limite inferior ⭐⭐⭐⭐ (1 aula)

**Objectivo.** Provar que o peso de qualquer circuito de Hamilton é, pelo menos, o peso da árvore geradora mínima.

**Tarefa.** Usa o mapa de B14.

1. Constrói a árvore geradora mínima (Kruskal) e calcula o seu peso $T$.
2. Mostra que, se retirares uma aresta a um circuito de Hamilton, obténs uma árvore que liga todos os locais. Conclui que $\text{óptimo} \ge T$.
3. Compara $T$ com o óptimo (455) e com o resultado do vizinho mais próximo.
4. Qual a utilidade de ter um limite inferior? O que garante se uma heurística obtiver um valor perto do limite?
5. O limite é "apertado" neste exemplo? Como poderia melhorar?

**🔑 Chave do professor.** Kruskal em B14: EG 20, AE 25, BG 35, BF 45, BC 55, CD 75. **$T = 255$.** Um circuito de Hamilton com $n$ vértices tem $n$ arestas; retirando uma, ficam $n-1$ arestas que ligam todos os vértices sem circuito fechado, ou seja, uma árvore geradora, de peso pelo menos $T$. Logo, o óptimo é $\ge 255$. Como 455 é o óptimo, o limite está a 56% do óptimo (255/455 ≈ 56%); é um limite **fraco**. Serve para garantir qualidade: se uma heurística der 475, sabe-se que o óptimo está entre 255 e 475. Para o apertar, pode-se somar à árvore a menor aresta que fecha o circuito (desafio extra).

### B18. Melhorar uma solução: a troca 2-opt ⭐⭐⭐⭐ (1 a 2 aulas)

**Objectivo.** Perceber que uma solução razoável pode ser melhorada por trocas locais.

**Tarefa.** A troca **2-opt** escolhe dois pontos do circuito e **inverte** o troço entre eles; mantém a troca se o peso diminuir. Parte do circuito do vizinho mais próximo a partir de C em B14.

1. Calcula o circuito do vizinho mais próximo a partir de C e o seu peso.
2. Aplica trocas 2-opt, uma de cada vez, enquanto o peso diminuir. Regista cada passo.
3. Chegaste ao óptimo (455)? Repete a partir de G.
4. Porque é que o método pode parar num circuito que não é o óptimo?

**🔑 Chave do professor.**

- Vizinho mais próximo a partir de C: C–B–G–E–A–F–D–C = **520**.
- Uma sequência possível de trocas: 520 → C–A–E–G–B–F–D–C = 475 → C–A–E–G–F–B–D–C = 465 → C–B–F–G–E–A–D–C = **455**, o óptimo. (A ordem em que se escolhem as trocas pode variar o caminho.)
- A partir de G: G–E–A–B–F–D–C–G = 490 → G–F–B–A–E–D–C–G = 480. Já **não** há troca que melhore, mas 480 > 455: o método ficou num óptimo **local**.

### B19. Programar e medir a explosão combinatória ⭐⭐⭐⭐ (1 a 2 aulas, projecto)

**Objectivo.** Medir, num computador, o custo de procurar o óptimo e ligá-lo ao crescimento factorial.

**Tarefa.** O programa seguinte testa todos os circuitos (inclui os dois sentidos).

```python
from itertools import permutations

def melhor_circuito(d):
    n = len(d)
    melhor = None
    for perm in permutations(range(1, n)):
        circ = (0,) + perm + (0,)
        peso = sum(d[circ[i]][circ[i + 1]] for i in range(n))
        if melhor is None or peso < melhor[0]:
            melhor = (peso, circ)
    return melhor
```

1. Testa com a matriz de B14 (7 locais): deves obter 455.
2. Gera matrizes aleatórias com $n = 6, 7, 8, 9, 10$ e mede o tempo de execução para cada $n$.
3. Quantas sequências testa o programa para cada $n$? Compara a razão entre tempos de $n$ consecutivos com a razão entre os números de sequências.
4. Extrapola o tempo para $n = 15$ e $n = 20$. Quanto durariam?
5. Propõe uma melhoria (por exemplo, não contar as sequências em sentido inverso, ou parar um ramo quando já passou o melhor peso).

**🔑 Chave do professor.** O programa percorre $(n-1)!$ sequências: $n=6 \to 120$; $n=7 \to 720$; $n=8 \to 5\,040$; $n=9 \to 40\,320$; $n=10 \to 362\,880$. Passar de $n$ para $n+1$ locais multiplica o trabalho por $n$ (por exemplo, de 7 para 8 locais, por 7). Os tempos dependem do computador: pede aos alunos que meçam e comparem as razões. Para a matriz de B14, o resultado correcto é `(455, (0, 3, 2, 1, 5, 6, 4, 0))`, ou seja, A–D–C–B–F–G–E–A. Se não souberem Python, a tarefa pode ser feita numa folha de cálculo para $n \le 7$ ou o professor pode fornecer o programa.

### Problemas de Biologia e de Física (ligação interdisciplinar)

Problemas curtos para trabalhar com colegas de Biologia e de Física (ou nas aulas de MACS). Todos os dados são **simulados** ou resultam de modelos simples; nenhum substitui dados reais de laboratório. Os problemas de grafos reutilizam mapas anteriores, o que poupa tempo ao professor.

### BIO1. Bactérias: dobrar de 20 em 20 minutos ⭐ (30 a 45 min)

**Contexto.** Uma bactéria divide-se em duas a cada 20 minutos, com alimento ilimitado.

1. Escreve o número de bactérias após $n$ divisões e após $t$ horas.
2. Quantas haverá ao fim de 10 horas, partindo de 1 bactéria?
3. Quanto tempo é preciso para chegar a mil milhões ($10^9$)?
4. **Análise crítica.** Porque é que, num frasco real, isto não se mantém?

**🔑 Chave do professor.** $N = 2^{3t}$ (3 divisões por hora). Em 10 h: $2^{30} = 1\,073\,741\,824$. Para $10^9$: $\log_2 10^9 \approx 29{,}9$ divisões, ou seja, cerca de **9,97 h** (≈ 9 h 58 min). A resposta à análise crítica é a falta de nutrientes e o acumular de resíduos: ligação à logística (BIO2).

### BIO2. A curva de crescimento de uma cultura ⭐⭐ (1 aula)

**Contexto.** A turbidez (densidade óptica, OD) de uma cultura mede-se de 2 em 2 horas. Dados **simulados** (modelo logístico sem ruído):

| $t$ (h) | 0 | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 | 18 | 20 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| OD | 0,002 | 0,009 | 0,035 | 0,131 | 0,398 | 0,802 | 1,069 | 1,165 | 1,191 | 1,198 | 1,199 |

1. Faz o gráfico. Identifica as fases: arranque lento, crescimento rápido, estabilização.
2. Calcula as razões entre valores consecutivos. Em que fase são aproximadamente constantes?
3. Faz a regressão logística na calculadora. Interpreta $K$, $r$ e o ponto de inflexão.
4. Em que instante é o crescimento mais rápido? Qual é a taxa máxima?
5. Acrescenta ruído aos dados (arredonda a 2 casas decimais) e repete. O que mudou?

**🔑 Chave do professor.** Parâmetros usados: $K = 1{,}2$, $r = 0{,}7\ \text{h}^{-1}$, $t_0 = 9\ \text{h}$ (a regressão recupera $K \approx 1{,}200$; $r \approx 0{,}700$; $t_0 \approx 9{,}00$). As razões nas primeiras fases são ≈ 3,7 a 3,9, perto de $e^{1{,}4} \approx 4{,}06$ (arredondamentos a 3 casas distorcem os valores pequenos). A taxa máxima é $rK/4 = 0{,}21$ OD por hora, em $t = 9$ h (onde OD $= K/2 = 0{,}6$). A fase de latência (*lag*) real, que o modelo logístico simples não tem, pode ser discutida.

### BIO3. Um medicamento no organismo ⭐⭐⭐ (1 aula, folha de cálculo)

**Contexto.** Um fármaco tem **meia-vida de 6 h** no sangue (a quantidade presente reduz-se a metade de 6 em 6 horas).

1. Toma-se uma dose de 200 mg. Que quantidade resta ao fim de 6, 12 e 24 horas?
2. Quanto tempo demora a ficar abaixo de 10 mg?
3. Agora toma-se uma dose de 200 mg **de 8 em 8 horas**. Constrói a recorrência: $C_{n+1} = b\,C_n + 200$ (quantidade imediatamente após cada toma). Determina $b$.
4. O que acontece a longo prazo? Determina o valor para o qual a quantidade se aproxima e interpreta.
5. Se a dose segura máxima no sangue fosse 300 mg, esta posologia seria adequada?

**🔑 Chave do professor.**

- Após 6, 12 e 24 h: 100, 50 e 12,5 mg. Abaixo de 10 mg: $6\log_2 20 \approx 25{,}9$ h.
- $b = 0{,}5^{8/6} \approx 0{,}397$. Quantidades logo após cada toma: 200; 279,4; 310,9; 323,4; 328,3; 330,3; 331,1; 331,4; …
- Tende para $\dfrac{200}{1-b} \approx 331{,}6$ mg (pico, logo após a toma) e $\approx 131{,}6$ mg (mínimo, imediatamente antes da toma seguinte).
- O pico estabiliza **acima** de 300 mg; a posologia não seria adequada. Aproveita para falar de acumulação: a soma de uma progressão geométrica.

### BIO4. Datação por carbono-14 ⭐⭐ (1 aula)

**Contexto.** Num organismo vivo a proporção de carbono-14 é constante; depois da morte decai com meia-vida de 5 730 anos (valor usual).

1. Escreve a fracção que resta após $t$ anos: $f(t) = 0{,}5^{\,t/5730}$.
2. Um osso tem 25% do carbono-14 de um osso vivo. Qual a idade?
3. E se tiver 10%? E 60%?
4. Porque é que a técnica não serve para amostras muito antigas (por exemplo, milhões de anos)?

**🔑 Chave do professor.** 25% → 2 meias-vidas = **11 460 anos**. 10% → $5730\log_2 10 \approx 19\,035$ anos. 60% → $5730\log_2(1/0{,}6) \approx 4\,223$ anos (e 30% → 9 953 anos). Para amostras muito antigas resta uma fracção demasiado pequena para medir; é um limite do método, que se liga à propriedade "dobrar em cada período" da função exponencial.

### BIO5. Contágio por gerações ⭐⭐ (1 aula)

**Contexto (modelo simplificado).** Cada pessoa infectada contagia em média $R_0 = 2{,}5$ pessoas na geração seguinte (sem imunidade nem medidas de controlo). Começa-se com 1 caso.

1. Quantos casos há na geração 1, 2, 5 e 10?
2. Compara com um crescimento linear de 2,5 casos novos por geração.
3. Se uma fracção $p$ da população estiver imune, quantos novos casos produz cada infectado? Para que valor de $p$ deixa de haver crescimento?
4. **Análise crítica.** Que simplificações tornam este modelo irrealista?

**🔑 Chave do professor.** Casos: 2,5 (geração 1); 6,2 (2); 97,7 (5); 9 536,7 (10) — sequência geométrica de razão 2,5. A linear dá 25 na geração 10. Com imunidade $p$, o número médio de novos casos é $R_0(1-p)$; o crescimento para quando $R_0(1-p) \le 1$, ou seja $p \ge 1 - 1/R_0 = 60\%$ (limiar de imunidade de grupo neste modelo simplificado). Limitações: população finita (logística), gerações sobrepostas, comportamentos que mudam, etc. Liga com A7.

### BIO6. Redes alimentares e a regra dos 10% ⭐⭐ (1 aula)

**Contexto.** Numa rede alimentar, os vértices são espécies e há uma aresta **orientada** de $X$ para $Y$ se $Y$ se alimenta de $X$. Considera: erva → coelho, erva → insecto, insecto → ave, coelho → raposa, ave → raposa.

1. Desenha o grafo orientado. Quantas arestas entram e saem de cada vértice?
2. Quantos caminhos orientados diferentes levam da erva à raposa? Que cadeias alimentares são?
3. Em cada nível trófico passa, em média, 10% da energia para o nível seguinte. Se a erva contém 10 000 kJ, quanta energia chega a cada nível ao longo de uma cadeia (erva, 1.º consumidor, 2.º consumidor, …)?
4. Que tipo de sequência é esta? Quantos níveis podem existir, na prática?

**🔑 Chave do professor.** Há **2 caminhos** da erva à raposa: erva–coelho–raposa e erva–insecto–ave–raposa. A energia segue uma progressão geométrica de razão 0,1: 10 000; 1 000; 100; 10; 1 kJ. O decaimento rápido explica que as cadeias tenham poucos níveis (na prática, 4 ou 5). (A regra dos 10% é uma média aproximada.)

### BIO7. Cruzamentos de Mendel e árvores de probabilidade ⭐⭐ (1 aula)

**Contexto.** Dois progenitores heterozigóticos ($Aa \times Aa$) têm, em cada filho, probabilidade $3/4$ de manifestar o carácter dominante e $1/4$ de manifestar o recessivo.

1. Constrói a árvore de possibilidades para 3 filhos (dominante D ou recessivo R). Quantos ramos tem?
2. Qual a probabilidade de exactamente 2 dos 3 filhos terem o carácter dominante?
3. E a de pelo menos um filho recessivo?
4. Como cresce o número de ramos da árvore com o número de filhos? De que tipo é o crescimento?

**🔑 Chave do professor.** A árvore tem $2^3 = 8$ ramos (com pesos diferentes). Exactamente 2 dominantes: $3\times\left(\tfrac34\right)^2\times\tfrac14 = \tfrac{27}{64} \approx 42{,}2\%$. Pelo menos um recessivo: $1 - \left(\tfrac34\right)^3 = \tfrac{37}{64} \approx 57{,}8\%$. O número de ramos cresce como $2^n$ (exponencial), ao contrário do número de circuitos de Hamilton (B4), que é factorial.

### BIO8. A abelha e as flores ⭐⭐ (1 aula)

**Contexto.** Uma abelha parte da colmeia, visita cinco flores e regressa à colmeia. Usa o mapa de **B10**, com A = colmeia e B a F = flores, e distâncias em **metros** (em vez de centenas de metros).

1. Quantas rotas diferentes existem?
2. Qual a rota mais curta? Qual o seu comprimento?
3. Estudos de comportamento animal mostram que as abelhas tendem a repetir trajectos curtos entre as mesmas flores. Que estratégia simples poderia explicar isto (liga ao vizinho mais próximo)?
4. A abelha "calcula" as 60 rotas? Que vantagem tem uma regra simples?

**🔑 Chave do professor.** $(6-1)!/2 = 60$ rotas. A melhor é A–B–D–E–F–C–A, com **295 m**. O vizinho mais próximo dá 295 m partindo de A (ou de B, D e E). A discussão do ponto 4 é aberta; não afirmes que as abelhas usam um método específico sem apoiar numa fonte.

### FIS1. Arrefecer uma bebida (lei do arrefecimento) ⭐⭐ (1 aula)

**Contexto.** Uma chávena de chá está a 90 °C numa sala a 20 °C. Admite $T(t) = 20 + 70\,e^{-0{,}045\,t}$ (com $t$ em minutos).

1. Em quanto tempo chega a 60 °C? E a 37 °C?
2. Quanto tempo demora a perder metade da diferença para a temperatura ambiente?
3. Porque é que o chá nunca chega a 10 °C?
4. Compara com A4: onde estão os dados e onde está o modelo?

**🔑 Chave do professor.** 60 °C: $t = \ln(70/40)/0{,}045 \approx 12{,}4$ min. 37 °C: $\ln(70/17)/0{,}045 \approx 31{,}5$ min. Meia-vida da diferença: $\ln 2/0{,}045 \approx 15{,}4$ min. A temperatura tende para a ambiente (20 °C), não para menos.

### FIS2. Descarga de um condensador ⭐⭐⭐ (1 aula, laboratório ou simulação)

**Contexto.** Um condensador carregado a $V_0 = 9\ \text{V}$ descarrega-se através de uma resistência. A tensão é $V(t) = V_0\,e^{-t/\tau}$, com $\tau = RC$. Com $R = 10\ \text{k}\Omega$ e $C = 100\ \mu\text{F}$ tem-se $\tau = 1\ \text{s}$.

1. Calcula $V$ para $t = 1, 2, 3$ e $5$ s.
2. Em quanto tempo a tensão cai para metade? E para 1 V?
3. Mostra que $\ln V$ em função de $t$ é uma recta e que o declive é $-1/\tau$. Como usarias isto para determinar $\tau$ com dados medidos?
4. Se $C$ duplicasse, o que aconteceria à curva?

**🔑 Chave do professor.** $V(1) = 3{,}31$ V; $V(2) = 1{,}22$ V; $V(3) = 0{,}45$ V; $V(5) = 0{,}06$ V. Metade: $\tau\ln2 \approx 0{,}69$ s. Até 1 V: $\tau\ln 9 \approx 2{,}20$ s. Com $C$ duplicado, $\tau = 2$ s e a descarga é mais lenta; a meia-vida duplica. Liga com A12 (linearização).

### FIS3. Radioisótopos em medicina ⭐⭐ (1 aula)

**Contexto.** Um radioisótopo usado em diagnóstico tem meia-vida de **6 h**.

1. Que percentagem da actividade inicial resta após 24 h?
2. Quanto tempo é preciso para a actividade descer a 1% do valor inicial? E a 0,1%?
3. Porque é que a meia-vida curta é uma vantagem para o doente, mas obriga a planear o transporte?
4. Relaciona com o jogo dos dados (A13).

**🔑 Chave do professor.** Após 24 h (4 meias-vidas): $0{,}5^4 = 6{,}25\%$. Para 1%: $6\log_2 100 \approx 39{,}9$ h. Para 0,1%: $6\log_2 1000 \approx 59{,}8$ h. O tempo de espera é proporcional ao número de meias-vidas, mas a actividade cai exponencialmente. No jogo dos dados a razão era $5/6$ por ronda; aqui é $0{,}5^{1/6} \approx 0{,}891$ por hora.

### FIS4. Queda com resistência do ar: um modelo com tecto ⭐⭐⭐ (1 aula)

**Contexto.** Um paraquedista em queda tem velocidade $v(t) = v_T\left(1 - e^{-t/\tau}\right)$, com $v_T = 55\ \text{m/s}$ e $\tau = 5{,}6\ \text{s}$. Sem resistência do ar, $v = 9{,}8\,t$.

1. Calcula $v$ para $t = 0, 5, 10, 15, 20, 30$ s e compara com $9{,}8\,t$.
2. Para onde tende $v$? Que tipo de modelo é (compara com o logístico e o logarítmico)?
3. Mostra que o declive em $t = 0$ é $v_T/\tau \approx 9{,}8\ \text{m/s}^2$. O que significa?
4. Em que se parece e em que difere este modelo do logístico?

**🔑 Chave do professor.** Valores: 0; 32,5; 45,8; 51,2; 53,5; 54,7 m/s (sem resistência: 49 m/s aos 5 s e 98 m/s aos 10 s). Tende para a **velocidade terminal** $v_T = 55$ m/s. O declive inicial $55/5{,}6 \approx 9{,}82$ m/s² coincide praticamente com a aceleração da gravidade. Diferença para o logístico: aqui o crescimento é sempre desacelerado (não há fase de aceleração), pelo que a curva é côncava desde o início, sem ponto de inflexão.

### FIS5. A luz debaixo de água ⭐⭐ (1 aula)

**Contexto.** Cada metro de água absorve 30% da luz que o atinge: a intensidade a $d$ metros é $I(d) = I_0\cdot 0{,}7^{\,d}$.

1. Que fracção da luz inicial resta a 1, 2, 5 e 10 m?
2. A que profundidade fica 50% da luz? E 1% (limite aproximado para a fotossíntese)?
3. Compara com o decaimento em tempo (BIO4, FIS3). O que tem em comum?
4. Relaciona com a escala logarítmica de A11: como exprimirias a perda em decibéis?

**🔑 Chave do professor.** Fracções: 0,70; 0,49; 0,168; 0,0282. 50% a $\ln0{,}5/\ln0{,}7 \approx$ **1,94 m**; 1% a $\ln0{,}01/\ln0{,}7 \approx$ **12,9 m**. É o mesmo modelo exponencial, com a profundidade no lugar do tempo. Cada metro corresponde a $10\log_{10}0{,}7 \approx -1{,}55$ dB.

### FIS6. Cabos eléctricos com o mínimo de comprimento ⭐⭐ (1 aula)

> Requer o desafio opcional B6 (árvore geradora mínima).

**Contexto.** A escola de B3 quer instalar um cabo eléctrico que ligue os 5 locais. O cabo custa 2 € por metro.

1. Qual o comprimento mínimo de cabo para ligar os 5 locais sem circuitos fechados? Quanto custa?
2. Qual o custo se o cabo formar o circuito de menor peso de B3 (um anel que passa em todos os locais)?
3. Quando é que o anel pode compensar, apesar de custar mais?

**🔑 Chave do professor.** Árvore mínima: PG, PC, PB, CL = **670 m**, logo **1 340 €**. O melhor anel tem 950 m, logo 1 900 €. O anel custa mais 560 €, mas oferece um caminho alternativo se um troço falhar (redundância); isto liga com a discussão da viabilidade económica.

### FIS7. Um drone a inspeccionar linhas de alta tensão ⭐⭐ (1 aula)

**Contexto.** Usa o grafo de **B9**: os vértices são torres e as arestas as linhas, com comprimentos em centenas de metros. Um drone tem **autonomia de 5,0 km** e tem de sobrevoar cada linha pelo menos uma vez.

1. Qual o comprimento total das linhas? O drone pode passar em todas sem repetir e regressar ao ponto de partida?
2. Se tiver de regressar ao ponto de partida, qual o percurso mínimo e a sua distância? Consegue com uma só bateria?
3. Se puder aterrar numa torre diferente (por exemplo, com carregamento), qual o percurso mínimo e onde começa?
4. Que decisão recomendarias?

**🔑 Chave do professor.** Total das linhas: 49 (4,9 km). Vértices ímpares: B e E. Circuito com repetição: 49 + 8 = 57 (**5,7 km**), que excede os 5,0 km. Percurso aberto de B a E (ou de E a B): **4,9 km**, dentro da autonomia, mas obriga a aterrar na torre oposta. Se não houver essa possibilidade, são necessárias duas baterias (ou uma recarga) para o circuito. O problema liga Euler e restrições físicas reais (autonomia).

---

## 4. Extensões opcionais (fora do excerto do programa que consultei)

- **Epidemia numa rede.** A actividade "Epidemics on Networks" (NRICH) usa uma rede social impressa e um dado: cada contacto de um infectado fica infectado se sair 1 ou 2. Os alunos contam casos e passos, repetem a partir de outros pontos e analisam a "curva epidémica". Liga-se a A7. Fonte: https://nrich.maths.org/12123
- **Redes e pequenos mundos.** Harrington et al. descrevem módulos para alunos de 13 a 16 anos (pequenos mundos, doença, teoria de grafos com as pontes de Königsberg). Não tem avaliação quantitativa dos resultados. Fonte: https://arxiv.org/pdf/1302.6567

---

## 5. Grelha de avaliação (partilhada pelos projectos A8 e B7)

| Critério | Consolidado | Em desenvolvimento | Inicial |
|---|---|---|---|
| **Modelação** | Traduz a situação para modelo (função ou grafo) e explica as escolhas | Modelo correcto, com pouca justificação | Modelo incompleto ou inadequado |
| **Procedimentos e tecnologia** | Usa calculadora, folha de cálculo ou algoritmo com correcção e sentido crítico | Erros pontuais ou uso mecânico | Erros frequentes |
| **Raciocínio e justificação** | Justifica cada passo com linguagem matemática | Justifica parte dos passos | Apresenta resultados sem justificar |
| **Análise crítica** | Identifica limites do modelo, riscos de extrapolar e viabilidade | Refere limites sem os explorar | Não discute limites |
| **Comunicação** | Clara, organizada, ajustada ao destinatário | Compreensível, com falhas de organização | Confusa |

---

## 6. Sugestão de sequência

Estimativas minhas; ajusta ao calendário real. Há mais desafios do que aulas: escolhe os que servem a turma. Os desafios A9 a A16 e B8 a B14 foram acrescentados depois dos originais e podem substituir ou complementar os primeiros.

| Fase | Actividades | Tempo estimado |
|---|---|---|
| 1. Crescimento discreto | A1, A2, A9, A10 (escolher 2 ou 3) | 2 a 3 aulas |
| 2. Crescimento contínuo | A3, A4, A5, A11, A12, A13 (escolher 3 ou 4) | 3 a 4 aulas |
| 3. Comparar modelos | A6, A7, A16 (A14 e A15 como enriquecimento) | 2 a 3 aulas |
| 4. Grafos | B1, B2, B3, B5 e, para variar, B8, B9, B10, B11, B13 | 4 a 6 aulas |
| 5. Ponte entre as duas partes | B4, B12, B14 | 1 a 2 aulas |
| 6. Projectos | A8 e B7 (um ou ambos) | 2 a 3 aulas cada |

---

## 7. Recolha de dados e ética

- Nos desafios A2 e A5 os alunos geram dados sobre si. Mantém-nos **anónimos** e a participação **voluntária**.
- Se usares estes dados na tese, precisas de **consentimento informado** dos alunos e dos encarregados de educação, e da escola, antes de recolher qualquer dado.
- Nunca avalies o desempenho individual nas tarefas de A5 e nunca recolhas moradas de pessoas em B7.
- Não coloques dados pessoais no repositório da tese.

---

## 8. Fontes

**Documentos oficiais (leitura automática de excertos; confirmar no original)**

- DGE, *Aprendizagens Essenciais, Matemática Aplicada às Ciências Sociais, 11.º ano*: https://www.dge.mec.pt/sites/default/files/Curriculo/Aprendizagens_Essenciais/11_macs.pdf
- DGE, *Programa de Matemática Aplicada às Ciências Sociais*: https://dge.mec.pt/sites/default/files/Secundario/Documentos/Programas/mat_aplicada_cien_soc.pdf

**Actividades e literatura**

- NRICH, *Epidemics on Networks*: https://nrich.maths.org/12123
- Harrington, H. A., Beguerisse Díaz, M., Rombach, M. P., Keating, L. M., & Porter, M. A. *Teach network science to teenagers*: https://arxiv.org/pdf/1302.6567
- Schonger, M., & Sele, D. (2021). Intuition and exponential growth: bias and the roles of parameterization and complexity. *Mathematics and Financial Economics*: https://link.springer.com/article/10.1007/s00591-021-00306-7

**Dados oficiais para A3 e A8 (a recolher pelos alunos):** INE (ine.pt), PORDATA (pordata.pt), Nações Unidas, *World Population Prospects* (population.un.org/wpp).
