# Growth Models: Mathematical Background

**Linear, exponential, logarithmic and logistic growth**, explained mathematically and in words, with derivations, key properties, estimation from data and a worked example for each model. Written to accompany the five Python notebooks (`01_linear_growth.ipynb` to `05_model_comparison.ipynb`), where every model is simulated and fitted.

> **Status.** Working draft for a thesis on teaching these models in Grade 11. The mathematics and every worked number were checked numerically. The links to the literature rely on abstracts and catalogue pages, not on full texts (see the reference list at the end). The "things to watch" lists mix points reported in the literature with my own suggestions, and each list says which is which.

## Contents

1. [Linear growth](#1-linear-growth)
2. [Exponential growth and decay](#2-exponential-growth-and-decay)
3. [Logarithmic growth](#3-logarithmic-growth)
4. [Logistic growth](#4-logistic-growth)
5. [Comparing the four models](#5-comparing-the-four-models)
6. [References](#6-references)

## Notation

| Symbol | Meaning |
|---|---|
| $t$ | time (or the independent variable) |
| $y,\ N,\ P$ | the growing quantity (generic, exponential and logistic notation) |
| $a,\ b$ | intercept and slope (linear), or offset and scale (logarithmic) |
| $N_0,\ P_0$ | initial value, $N(0)$ or $P(0)$ |
| $r$ | continuous growth rate (exponential and logistic) |
| $b$ in $N_0 b^{t}$ | growth factor per unit of time, $b = e^{r}$ |
| $K$ | carrying capacity (logistic) |
| $t_0$ | time of the logistic inflection point |
| $T_d,\ T_{1/2}$ | doubling time, half-life |
| $\ln$ | natural logarithm (base $e \approx 2.71828$) |

Math is written in LaTeX between `$...$` (inline) and `$$...$$` (display). GitHub, VS Code and Jupyter all render it.

---

## 1. Linear growth

### 1. Definition

A quantity $y$ grows **linearly** in time $t$ if

$$
y(t) = a + b\,t, \qquad a, b \in \mathbb{R}.
$$

- $a = y(0)$ is the **intercept**: the starting value.
- $b$ is the **slope**: the change in $y$ per unit of time. It has the units of $y$ divided by the units of $t$ (euros per week, centimetres per hour).
- If $b>0$ the quantity increases, if $b<0$ it decreases (linear *decay*), and if $b=0$ it is constant.

### 2. Where it comes from: a constant rate of change

Linear growth is what we get when the **rate of change is constant**:

$$
\frac{dy}{dt} = b.
$$

Integrating from $0$ to $t$ gives $y(t) = y(0) + \int_0^t b\,ds = a + bt$.

In **discrete time**, with steps of length $\Delta t$, the same assumption reads

$$
y_{n+1} = y_n + b\,\Delta t = y_n + d, \qquad d = b\,\Delta t,
$$

which is an **arithmetic progression** with common difference $d$, and whose general term is $y_n = y_0 + n\,d$. This is the link between linear functions and arithmetic progressions in the Grade 11 programme.

### 3. The characteristic property: equal steps, equal additions

For any $t$ and any step $h$,

$$
y(t+h) - y(t) = \big(a + b(t+h)\big) - \big(a + bt\big) = b\,h .
$$

The change over an interval depends **only on the length $h$ of the interval**, never on where it starts. Consequently:

- the **average rate of change** over *any* interval equals $b$;
- the first differences $\Delta y$ of equally spaced data are all equal (the test used in the notebook);
- the second differences are zero, because $y''(t) = 0$: the graph has no curvature.

The **relative** (percentage) rate of change is *not* constant:

$$
\frac{y'(t)}{y(t)} = \frac{b}{a + bt},
$$

which shrinks as $y$ grows (when $a, b > 0$). A constant additive gain is a smaller and smaller percentage of an ever larger quantity.

### 4. Graph and shape

- The graph is a **straight line** with slope $b$ and vertical intercept $a$.
- The **root** (where $y=0$) is at $t = -a/b$, if $b\neq 0$.
- It is monotone (increasing for $b>0$, decreasing for $b<0$) and has no horizontal asymptote.

### 5. Inverse and "time to target"

Solving $y = a + bt$ for $t$ gives the inverse function, which is also linear:

$$
t = \frac{y - a}{b}.
$$

The time needed to reach a target value $y^{*}$ is therefore

$$
t^{*} = \frac{y^{*} - a}{b}.
$$

### 6. Estimating $a$ and $b$ from data (least squares)

Given measurements $(t_i, y_i)$, $i = 1,\dots,n$, the least-squares line minimises $\sum_i (y_i - a - b t_i)^2$. Setting the partial derivatives with respect to $a$ and $b$ to zero gives

$$
\hat b = \frac{\sum_i (t_i - \bar t)(y_i - \bar y)}{\sum_i (t_i - \bar t)^2}, \qquad
\hat a = \bar y - \hat b\,\bar t ,
$$

where $\bar t$ and $\bar y$ are the sample means. The coefficient of determination is

$$
R^2 = 1 - \frac{\sum_i (y_i - \hat a - \hat b t_i)^2}{\sum_i (y_i - \bar y)^2}.
$$

A residual plot with no pattern supports the linear model; a curved pattern in the residuals is a warning that another model fits better.

### 7. Assumptions and limits

- The rate of change is **constant**: nothing speeds it up or slows it down.
- The quantity is **unbounded**: it keeps growing (or falling) forever. Real quantities usually are not, so a linear model is typically valid only over a limited range. Extrapolating far beyond the data is risky.

### 8. Worked example

A student has €20 and saves €7.50 per week, so $y(t) = 20 + 7.5\,t$.

- After 20 weeks: $y(20) = 20 + 7.5 \times 20 = 170$ euros.
- Savings reach €250 when $t^{*} = \dfrac{250 - 20}{7.5} = 30.67$ weeks.
- Each week adds €7.50, but the *percentage* growth falls from $7.5/20 = 37.5\%$ in the first week to $7.5/170 \approx 4.4\%$ around week 20.

### 9. Things to watch (suggestions for teaching, not drawn from the literature)

- Do not confuse "increases by the same **amount**" (linear) with "increases by the same **percentage**" (exponential). The signature of linearity is constant *differences*.
- Check units of the slope when interpreting it.
- A straight-looking graph over a short window does not prove the model is linear (see the model-comparison notebook).

---

## 2. Exponential growth and decay

### 1. Definition

A quantity $N$ grows (or decays) **exponentially** in time $t$ if

$$
N(t) = N_0\,e^{rt} = N_0\,b^{\,t}, \qquad N_0 > 0,\quad b = e^{r} > 0,\ b \neq 1 .
$$

- $N_0 = N(0)$ is the starting value.
- $r$ is the **continuous growth rate** (per unit of time). $r>0$ gives growth, $r<0$ gives decay.
- $b = e^{r}$ is the **growth factor** per unit of time: the quantity is multiplied by $b$ every time $t$ increases by 1. If the quantity grows by a percentage $i$ per time unit, then $b = 1 + i$, so $i = e^{r} - 1$ and $r = \ln(1+i)$. For small $r$, $i \approx r$ (for example $r = 0.02$ gives $i = 2.02\%$).

### 2. Where it comes from: growth proportional to size

Suppose the rate of growth is **proportional to the amount already present**:

$$
\frac{dN}{dt} = r\,N .
$$

(Each individual contributes the same expected number of offspring, or each euro earns the same interest.) Separate variables and integrate:

$$
\int \frac{dN}{N} = \int r\,dt \;\Longrightarrow\; \ln N = rt + C \;\Longrightarrow\; N(t) = e^{C} e^{rt} = N_0 e^{rt},
$$

where $N_0 = e^{C} = N(0)$.

In **discrete time** the same assumption is $N_{n+1} = b\,N_n$, a **geometric progression** with ratio $b$, whose general term is $N_n = N_0\,b^{\,n}$. This links exponential functions to geometric progressions.

**Continuous compounding.** If money earns annual rate $r$ compounded $m$ times a year, the balance after $t$ years is $P(1 + r/m)^{mt}$. As $m \to \infty$,

$$
\left(1 + \frac{r}{m}\right)^{mt} \longrightarrow e^{rt},
$$

which is why $e$ appears. For $r = 5\%$ and $t = 1$: $m=1$ gives $1.050000$, $m=12$ gives $1.051162$, $m=365$ gives $1.051267$, and the limit is $e^{0.05} = 1.051271$.

### 3. The characteristic property: equal steps, equal ratios

For any $t$ and step $h$,

$$
\frac{N(t+h)}{N(t)} = \frac{N_0 e^{r(t+h)}}{N_0 e^{rt}} = e^{rh},
$$

which does **not depend on $t$**. Therefore:

- the **relative rate of change** is constant: $\dfrac{N'(t)}{N(t)} = r$;
- the ratios of consecutive values of equally spaced data are all equal, while the differences keep growing;
- the exponential function satisfies the **functional equation** $f(s+t) = f(s)\,f(t)$ (adding times multiplies amounts), and the nonzero continuous functions with this property are exactly the exponentials $e^{cx}$.

### 4. Doubling time and half-life

The **doubling time** $T_d$ is the time to multiply $N$ by 2:

$$
N_0 e^{rT_d} = 2N_0 \;\Longrightarrow\; T_d = \frac{\ln 2}{r} .
$$

It does not depend on the starting value or on when we start counting. Hence $N(t) = N_0\,2^{\,t/T_d}$. For percentage growth $i$ per period, $T_d = \dfrac{\ln 2}{\ln(1+i)}$. The well-known "rule of 70" ($T_d \approx 70 / (100\,i)$ periods) comes from $\ln 2 \approx 0.693$: at 3% per year, $T_d = 23.45$ years exactly versus $70/3 = 23.3$ by the rule.

For decay ($r<0$) the corresponding quantity is the **half-life**: $T_{1/2} = \dfrac{\ln 2}{|r|}$, and $N(t) = N_0\,(1/2)^{t/T_{1/2}}$.

### 5. Graph and shape

- It passes through $(0, N_0)$ and is always positive.
- For $r>0$: $N'(t) = rN > 0$ (increasing) and $N''(t) = r^2 N > 0$ (**convex**: the curve bends upward). For $r<0$ the function decreases, but is still convex.
- The **horizontal asymptote** is $N = 0$: as $t \to -\infty$ for $r>0$, as $t\to+\infty$ for $r<0$.
- Exponential growth eventually beats any power of $t$: $\displaystyle \lim_{t\to\infty} \frac{t^{k}}{e^{rt}} = 0$ for every $k$ when $r>0$. This is the mathematical content of "exponential growth is faster than polynomial growth".

### 6. Linearisation with logarithms

Taking the natural logarithm of $N = N_0 e^{rt}$:

$$
\ln N = \ln N_0 + r\,t .
$$

So $\ln N$ is a **linear function of $t$** with slope $r$ and intercept $\ln N_0$. On a graph with a **logarithmic vertical axis** (semi-log graph) an exponential appears as a straight line. On a base-10 axis the slope is $r\,\log_{10} e = r/\ln 10 \approx 0.434\,r$.

### 7. Inverse function

Solving for $t$:

$$
t = \frac{1}{r}\,\ln\!\frac{N}{N_0} .
$$

The inverse of an exponential function is a logarithmic function. This is the bridge to the next model.

### 8. Estimating $N_0$ and $r$ from data

- **Log-linear regression:** regress $\ln N_i$ on $t_i$ (the least-squares formulas of the linear model). Then $\hat r$ is the slope and $\hat N_0 = e^{\text{intercept}}$. This is appropriate when the errors are **multiplicative** (a percentage of each value), which is typical for counts.
- **Nonlinear least squares:** minimise $\sum (N_i - N_0 e^{r t_i})^2$ directly. This treats errors as **additive** and gives more weight to the largest values.
- The doubling time then follows as $\hat T_d = \ln 2 / \hat r$.

### 9. Assumptions and limits

- The relative growth rate is **constant**: no crowding, no resource limits.
- The quantity is **unbounded**. Exponential growth cannot continue indefinitely in a finite system, which is why exponential models usually describe only the *early* phase of a process. After that, a limiting model such as the logistic is needed.

### 10. Worked example

A bacterial culture starts with $N_0 = 500$ cells and doubles every 40 minutes.

- Growth rate: $r = \dfrac{\ln 2}{40} = 0.01733$ per minute, equivalent to a growth factor $e^{r} = 1.01748$, that is **1.75% per minute**.
- After 3 hours: $N(180) = 500 \cdot 2^{180/40} = 500 \cdot 2^{4.5} \approx 11\,314$ cells.
- Time to reach one million cells: $t = 40\,\log_2\!\dfrac{10^6}{500} = 40 \times 10.97 \approx 438.6$ minutes (about 7.3 hours).

### 11. Framing the same fact in two ways

"Grows by 1.75% per minute" and "doubles every 40 minutes" describe the same process. The literature on exponential growth bias (Schonger & Sele, 2021) reports that the bias is much smaller when problems use doubling times. This is a useful thing to test with students.

### 12. Things to watch (suggestions for teaching, partly drawn from the sources)

- Moving the minus sign of an exponent onto the base, and composing growth factors incorrectly when given two coordinates, were reported as common errors (Bergsma, 2019). A good exercise: given two points $(t_1, N_1)$ and $(t_2, N_2)$ find $b = (N_2/N_1)^{1/(t_2 - t_1)}$.
- A growth *rate* $r$ and a growth *percentage* $i$ are different numbers ($r = \ln(1+i)$).
- The notation $b^{t}$ and $e^{rt}$ describe the same function; students should move freely between them.

---

## 3. Logarithmic growth

### 1. Definition

A quantity $y$ follows a **logarithmic** growth model in time $t$ if

$$
y(t) = a + b\,\ln t, \qquad t > 0,\quad b \neq 0 .
$$

- $a$ is the value of $y$ at $t = 1$ (because $\ln 1 = 0$).
- $b$ controls how fast $y$ rises. For $b > 0$ the quantity increases **ever more slowly**: this is the pattern of *diminishing returns*.
- Other bases are possible: since $\log_c t = \dfrac{\ln t}{\ln c}$, we can write $y = a + b'\,\log_c t$ with $b' = b\,\ln c$. In base 10, $b' = b\ln 10 \approx 2.303\,b$.

### 2. Reminder: the logarithm

$\ln$ is the inverse of the exponential function: $\ln t = s \iff t = e^{s}$. Its main properties are

$$
\ln(xy) = \ln x + \ln y, \qquad \ln\frac{x}{y} = \ln x - \ln y, \qquad \ln(x^{p}) = p\,\ln x,
$$

with $\ln 1 = 0$, $\ln e = 1$, domain $(0,\infty)$ and range $\mathbb{R}$. Its derivative is $\dfrac{d}{dt}\ln t = \dfrac{1}{t}$. The first property, **products become sums**, is the source of everything below.

### 3. Where it comes from

There are several ways to arrive at the same model.

**(a) A rate that falls in proportion to elapsed time.** If $\dfrac{dy}{dt} = \dfrac{b}{t}$, then $y(t) = a + b\ln t$. The longer the process has run, the smaller each further increment.

**(b) The inverse of an exponential.** If the *time* needed to reach level $y$ grows exponentially with $y$, say $t = e^{(y-a)/b}$, then solving for $y$ gives $y = a + b\ln t$. Equivalently: the rate falls **exponentially with the level already achieved**, $\dfrac{dy}{dt} = b\,e^{-(y-a)/b}$. Each further unit of improvement is harder to win than the last.

**(c) Multiplicative input, additive response.** In many perception and measurement scales equal *ratios* of the input produce equal *differences* in the output. Examples are the decibel scale for sound ($L = 10\log_{10}(I/I_0)$), the pH scale and earthquake magnitude scales. This is the idea behind the Weber–Fechner law in psychology.

### 4. The characteristic property: equal ratios in $t$, equal increments in $y$

For any $k > 0$,

$$
y(kt) - y(t) = b\,\ln(kt) - b\,\ln t = b\,\ln k ,
$$

independent of $t$. In particular **each doubling of $t$ adds $b\ln 2 \approx 0.693\,b$ to $y$**, and each tenfold increase adds $b\ln 10 \approx 2.303\,b$. This is the mirror image of the exponential model:

| | Step in the input | Effect on the output |
|---|---|---|
| Exponential, $N = N_0 e^{rt}$ | add $h$ to $t$ | **multiply** $N$ by $e^{rh}$ |
| Logarithmic, $y = a + b\ln t$ | **multiply** $t$ by $k$ | add $b\ln k$ to $y$ |

### 5. Graph and shape

- **Domain** $t > 0$. As $t \to 0^{+}$, $y \to -\infty$ (for $b>0$): the graph has a **vertical asymptote** at $t = 0$.
- **Root:** $y = 0$ at $t = e^{-a/b}$.
- **Increasing** for $b>0$, since $y'(t) = \dfrac{b}{t} > 0$.
- **Concave** (curving downward): $y''(t) = -\dfrac{b}{t^{2}} < 0$. The slope decreases towards 0 but never reaches it.
- **Unbounded, but very slow:** $y \to \infty$ as $t \to \infty$, yet $\ln t$ grows more slowly than any positive power of $t$, that is $\displaystyle\lim_{t\to\infty}\frac{\ln t}{t^{p}} = 0$ for every $p>0$.

### 6. A straight line on a logarithmic axis

$y = a + b\,x$ with $x = \ln t$. So $y$ plotted against $\ln t$, or against $t$ on a **logarithmic horizontal axis**, is a straight line with slope $b$.

### 7. The time to reach a target grows exponentially

Solving for $t$ gives the inverse (an exponential function):

$$
t^{*} = e^{(y^{*} - a)/b}.
$$

So *raising the target by a fixed number of points multiplies the required time by a fixed factor*. This is the quantitative meaning of diminishing returns.

### 8. Estimating $a$ and $b$ from data

Set $x_i = \ln t_i$ and use the least-squares formulas of the **linear model** on $(x_i, y_i)$:

$$
\hat b = \frac{\sum_i (x_i - \bar x)(y_i - \bar y)}{\sum_i (x_i - \bar x)^2}, \qquad \hat a = \bar y - \hat b\,\bar x .
$$

### 9. The logarithm as a tool in the other models

Beyond being a model of its own, the logarithm is the **transformation that linearises** the others:

- exponential: $\ln N$ against $t$ is a straight line (slope $r$);
- power laws $y = c\,t^{p}$: $\ln y$ against $\ln t$ is a straight line (slope $p$);
- logistic: $\ln\dfrac{P}{K-P}$ against $t$ is a straight line (slope $r$);
- solving equations such as $b^{t} = c$ gives $t = \ln c / \ln b$.

### 10. Assumptions and limits

- The model is usually an **empirical description** of diminishing returns, not a mechanism derived from first principles (although (a) and (b) above give simple mechanisms).
- It is **singular at $t=0$** ($y \to -\infty$), so it should only be used for $t$ above some starting point.
- It is **unbounded**: a real learning curve eventually reaches a ceiling, and then a bounded model such as the logistic describes it better.
- Over a limited range a logarithmic curve can look similar to a power function with a small exponent, so a good fit alone does not prove the model.

### 11. Worked example

A learning curve: score $= 30 + 12\ln(\text{hours})$.

- After 1 hour the score is 30. After 2 hours it is $30 + 12 \ln 2 = 38.3$, after 4 hours $46.6$, after 8 hours $55.0$ (exact values $30$, $38.32$, $46.64$, $54.95$): **each doubling of practice time adds the same 8.3 points** ($12\ln 2$).
- To reach a score of 85: $t^{*} = e^{(85-30)/12} = e^{4.583} \approx 97.8$ hours.
- To reach 95: $t^{*} = e^{65/12} \approx 225.1$ hours. **Ten more points more than double the practice time.**
- In base 10 the same model reads $y = 30 + 27.6\,\log_{10} t$ (because $12 \times 2.303 = 27.6$).

### 12. Things to watch (suggestions for teaching, partly drawn from the sources)

- The literature notes that the logarithm is much less studied than the exponential and that covariation of **arithmetic and geometric progressions** has been proposed as a route to understanding it (Ferrari; Trejo, Ferrari & Martínez, 2021). For example, when $t$ runs through $1, 2, 4, 8, 16$ (a geometric progression), $y$ runs through an arithmetic progression.
- Students often read a logarithmic axis as if it were linear. A study on exponential growth bias in graphs reports that log scales can lead to errors in describing graphs, while linear scales mislead when predicting (Melnik-Leroy et al., 2023).
- Distinguish clearly between $\ln t$ (a *function of time* here) and $\ln N$ (a transformation of the *data* in the exponential model).

---

## 4. Logistic growth

### 1. Definition

A quantity $P$ grows **logistically** if

$$
P(t) = \frac{K}{1 + A\,e^{-rt}}, \qquad A = \frac{K - P_0}{P_0}, \qquad 0 < P_0 < K,\ r > 0,
$$

or, equivalently, writing $t_0 = \dfrac{\ln A}{r}$,

$$
P(t) = \frac{K}{1 + e^{-r(t - t_0)}} .
$$

- $K$ is the **carrying capacity**: the upper limit that $P$ approaches.
- $r$ is the **intrinsic growth rate**: the exponential rate seen early on, when $P \ll K$.
- $P_0 = P(0)$ is the initial value.
- $t_0$ is the time of the **inflection point**, where $P = K/2$ and growth is fastest.

The graph is the S-shaped (*sigmoid*) curve. A third equivalent form is $P(t) = \dfrac{P_0 e^{rt}}{1 + \frac{P_0}{K}\left(e^{rt} - 1\right)}$.

### 2. Where it comes from: growth that slows as the limit approaches

In the exponential model the **per-capita** growth rate $\dfrac{1}{P}\dfrac{dP}{dt}$ is a constant $r$. In a finite environment this cannot last. The simplest correction is to let the per-capita rate **decrease linearly** as $P$ approaches $K$:

$$
\frac{1}{P}\frac{dP}{dt} = r\left(1 - \frac{P}{K}\right)
\quad\Longleftrightarrow\quad
\boxed{\frac{dP}{dt} = r\,P\left(1 - \frac{P}{K}\right)} .
$$

This is the **logistic equation** (Verhulst, 1838). Two readings of the same equation:

- The factor $\left(1 - \dfrac{P}{K}\right)$ is the **fraction of the capacity still available**. It is close to 1 when $P$ is small (almost exponential growth) and close to 0 when $P$ is near $K$ (growth stops).
- Expanding, $\dfrac{dP}{dt} = rP - \dfrac{r}{K}P^{2}$: a growth term proportional to $P$ minus a **crowding** term proportional to $P^{2}$ (the number of pairs of individuals competing).

### 3. Solving the equation

Separate variables:

$$
\frac{dP}{P\,(1 - P/K)} = r\,dt .
$$

Use partial fractions: $\dfrac{1}{P(1 - P/K)} = \dfrac{1}{P} + \dfrac{1}{K - P}$ (check: $\dfrac{1}{P} + \dfrac{1}{K-P} = \dfrac{K}{P(K-P)}$). Integrating both sides,

$$
\ln P - \ln(K - P) = rt + C \;\Longrightarrow\; \frac{P}{K - P} = C'\,e^{rt}, \qquad C' = \frac{P_0}{K - P_0}.
$$

Solving for $P$:

$$
P = \frac{K\,C' e^{rt}}{1 + C' e^{rt}} = \frac{K}{1 + \dfrac{1}{C'}\,e^{-rt}} = \frac{K}{1 + A\,e^{-rt}}, \qquad A = \frac{K - P_0}{P_0}.
$$

### 4. Key properties

**(a) Limits.** As $t \to \infty$, $P \to K$. As $t \to -\infty$, $P \to 0$. The values $P = 0$ and $P = K$ are the two **equilibria** of the equation; $P=0$ is unstable and $P = K$ is stable.

**(b) Growth rate as a function of $P$.** $\dfrac{dP}{dt} = rP(1 - P/K)$ is a **parabola** in $P$ with roots $0$ and $K$. It is largest at $P = K/2$, where

$$
\left.\frac{dP}{dt}\right|_{\max} = r\,\frac{K}{2}\left(1 - \frac12\right) = \frac{rK}{4}.
$$

**(c) Inflection point.** Differentiating $P' = rP - \dfrac{r}{K}P^{2}$ again,

$$
P'' = rP' - \frac{2r}{K}\,P\,P' = r\,P'\left(1 - \frac{2P}{K}\right).
$$

Since $P' > 0$ for $0<P<K$, the curve is **convex** (accelerating) while $P < K/2$, **concave** (decelerating) while $P > K/2$, with the inflection at $P = K/2$, i.e. at $t = t_0 = \dfrac{\ln A}{r}$.

**(d) Symmetry.** The curve is symmetric about its inflection point:

$$
P(t_0 + s) + P(t_0 - s) = K \quad\text{for all } s,
$$

because $\dfrac{K}{1 + e^{-rs}} + \dfrac{K}{1 + e^{rs}} = K$.

**(e) Early phase is exponential.** When $P \ll K$, $1 - P/K \approx 1$ and $\dfrac{dP}{dt} \approx rP$, so $P(t) \approx P_0 e^{rt}$. Formally, using the third form in section 1, $P(t) \to P_0 e^{rt}$ as $K \to \infty$. So **the exponential is the logistic with no limit**.

**(f) Late phase is also exponential.** The distance to the limit shrinks exponentially:

$$
K - P(t) = \frac{K\,e^{-r(t - t_0)}}{1 + e^{-r(t - t_0)}} \;\approx\; K\,e^{-r(t - t_0)} \quad (t \gg t_0).
$$

**(g) Rise time.** The time to go from $10\%$ to $90\%$ of $K$ is $\dfrac{2\ln 9}{r} \approx \dfrac{4.39}{r}$, since $P = qK$ occurs at $t = t_0 + \dfrac{1}{r}\ln\dfrac{q}{1-q}$.

### 5. Linearisation

**Logit.** From $\dfrac{P}{K-P} = e^{r(t - t_0)}$,

$$
\ln\frac{P}{K - P} = r\,(t - t_0),
$$

a **straight line in $t$** with slope $r$ and intercept $-r t_0$. If $K$ is known, regressing $\ln\dfrac{P}{K-P}$ on $t$ estimates $r$ and $t_0$.

**Per-capita growth.** The equation also says $\dfrac{P'}{P} = r - \dfrac{r}{K}P$: the per-capita growth rate is a **decreasing straight line in $P$**, with intercept $r$ and slope $-r/K$, crossing zero at $P = K$. With data, plot $\dfrac{\Delta P/\Delta t}{P}$ against $P$ and read $r$ and $K$ from the line. This needs no calculus.

### 6. The discrete version, and a warning

Stepping forward in time steps $\Delta t$ (as in spreadsheets and Vensim):

$$
P_{n+1} = P_n + r\,P_n\left(1 - \frac{P_n}{K}\right)\Delta t .
$$

For small $\Delta t$ this approximates the logistic curve closely. But the recurrence is **not** the same object as the continuous model. Put $h = r\,\Delta t$ and $y_n = \dfrac{h}{1+h}\dfrac{P_n}{K}$. Then

$$
y_{n+1} = (1 + h)\,y_n\,(1 - y_n),
$$

which is the **logistic map** $y \mapsto \mu y(1-y)$ with $\mu = 1 + h$. Its behaviour depends on $\mu$:

| $\mu = 1 + r\,\Delta t$ | Long-run behaviour |
|---|---|
| $1 < \mu \le 2$ | converges monotonically to $K$ (like the continuous curve) |
| $2 < \mu < 3$ | converges to $K$ with damped oscillations |
| $3 < \mu < 3.57$ (approximately) | sustained cycles (period 2, 4, ...) |
| larger $\mu$ | irregular (chaotic) behaviour |

(In the checks run for this document, $\mu = 1.5$ and $2.5$ converged; $\mu = 3.2$ settled into a 2-cycle; $\mu = 3.5$ into a 4-cycle; $\mu = 3.9$ was irregular.) So a time step that is too large creates behaviour that the continuous model does not have. In the logistic notebook, $r = 0.5$ and $\Delta t = 4$ or $5$ give $\mu = 3$ and $3.5$.

### 7. Estimating $K$, $r$, $t_0$ from data

- **Nonlinear least squares** on $\sum_i (P_i - K/(1 + e^{-r(t_i - t_0)}))^2$, with starting values such as $K \approx 1.2 \max P_i$, $r \approx 0.3$, $t_0 \approx$ median of $t_i$.
- **Linearisation** (logit or per-capita growth) when a rough estimate of $K$ is available.
- **Identifiability warning:** $K$ is only well determined once the data **reach or pass the inflection point**. Data from the early, exponential-looking phase cannot reveal the limit (see the simulation in the logistic notebook).

### 8. Assumptions and limits

- $K$ and $r$ are **constant** in time and the same for all individuals.
- The population is "well mixed" and responds **instantly** (no delays).
- Real data are rarely exactly logistic. In the rumour simulation in the notebook, the rate fitted to the whole curve (about 1.35) is larger than the rate measured in the early phase (about 1.09). Extensions such as the Gompertz or Richards curves allow other shapes.

### 9. Worked example

A yeast culture: $K = 1000$, $r = 0.5$ per hour, $P_0 = 10$.

- $A = \dfrac{K - P_0}{P_0} = 99$ and $t_0 = \dfrac{\ln 99}{0.5} = 9.19$ hours.
- $P(10) = \dfrac{1000}{1 + 99\,e^{-5}} = 599.9$.
- Maximum growth rate $\dfrac{rK}{4} = 125$ per hour, reached at $P = 500$ (at $t = t_0 = 9.19$ h).
- The culture goes from $10\%$ to $90\%$ of $K$ in $\dfrac{2\ln 9}{0.5} = 8.79$ hours (from $t = 4.80$ h to $t = 13.59$ h).
- Early on, $P(8) \approx 10\,e^{0.5\cdot 8} = 545.98$ would be the exponential prediction, but the logistic value is $P(8) = 355.5$: the limit is already pulling growth down.

### 10. Things to watch (suggestions for teaching, partly drawn from the sources)

- A review of the logistic equation in mathematics education reports that the main difficulties involve **multiple representations** (the equation, the curve, the rate) and communicating across disciplines. Showing the three representations side by side, and the recurrence, helps (see the notebook).
- A teaching experiment with high-school students (Castillo-Garsow, 2013) moved from exponential growth to the logistic model and warns that several ways of thinking about exponential growth are often used without being distinguished for students.
- Students need the idea that growth can **look exponential at first** and still be limited. Asking "what could stop this growth?" is the natural step from the exponential to the logistic model.

---

## 5. Comparing the four models

### 1. One question, four models: what is the growth rate proportional to?

The four models can be read as four answers to the question *"what determines how fast the quantity changes?"*

| Model | Growth rate $dy/dt$ | Relative rate $\dfrac{1}{y}\dfrac{dy}{dt}$ | Closed form | Discrete version |
|---|---|---|---|---|
| **Linear** | constant: $b$ | $\dfrac{b}{y}$ (falls as $y$ grows) | $y = a + bt$ | $y_{n+1} = y_n + d$ (arithmetic progression) |
| **Exponential** | proportional to $y$: $rN$ | constant: $r$ | $N = N_0 e^{rt}$ | $N_{n+1} = b\,N_n$ (geometric progression) |
| **Logarithmic** | inversely proportional to time: $b/t$ | $\dfrac{b}{t\,y}$ | $y = a + b\ln t$ | increments $b\ln\dfrac{t_{n+1}}{t_n}$ |
| **Logistic** | $rP\left(1 - \dfrac{P}{K}\right)$ | $r\left(1 - \dfrac{P}{K}\right)$ (falls linearly in $P$) | $P = \dfrac{K}{1 + Ae^{-rt}}$ | $P_{n+1} = P_n + rP_n(1 - P_n/K)\Delta t$ |

### 2. Properties side by side

| | Linear | Exponential | Logarithmic | Logistic |
|---|---|---|---|---|
| **What is constant over equal steps of $t$** | differences $\Delta y$ | ratios $y_{t+1}/y_t$ | differences per **doubling** of $t$ | none (differences rise, then fall) |
| **Shape** | straight line | convex (accelerating) | concave (decelerating) | S-shaped: convex then concave |
| **Second derivative** | $0$ | $r^{2}N > 0$ | $-b/t^{2} < 0$ | changes sign at $P = K/2$ |
| **Long-run behaviour** | unbounded, steady | unbounded, ever faster (or decays to 0) | unbounded, ever slower | **bounded** by $K$ |
| **Inverse function** | $t = (y-a)/b$, linear | $t = \frac{1}{r}\ln\frac{N}{N_0}$, logarithmic | $t = e^{(y-a)/b}$, exponential | $t = t_0 + \frac{1}{r}\ln\frac{P}{K-P}$ |
| **Straight line when plotting...** | $y$ against $t$ | $\ln y$ against $t$ | $y$ against $\ln t$ | $\ln\frac{P}{K-P}$ against $t$ |
| **Parameters to estimate** | $a,\ b$ | $N_0,\ r$ | $a,\ b$ | $K,\ r,\ t_0$ |
| **Typical context** | constant-speed travel, fixed weekly saving | early epidemic, compound interest, radioactive decay | learning curves, decibels, pH | limited populations, rumours, saturation |

### 3. How the models are related

- **Exponential and logistic.** The logistic equation reduces to the exponential when $K \to \infty$ (or when $P \ll K$). The exponential is the *early phase* of the logistic.
- **Exponential and logarithmic.** They are **inverse functions**: $y = \ln t$ undoes $t = e^{y}$. Swapping the roles of input and output turns one into the other. In the exponential model adding to $t$ multiplies $N$; in the logarithmic model multiplying $t$ adds to $y$.
- **Each model is a straight line after a transformation.** Linear: $(t, y)$. Exponential: $(t, \ln y)$. Logarithmic: $(\ln t, y)$. Logistic: $\left(t, \ln\frac{P}{K-P}\right)$. Choosing the transformation under which the data look straight is a practical way of choosing the model.
- **Linear as a local approximation.** Every differentiable model is approximately linear over a short window: $y(t+h) \approx y(t) + y'(t)\,h$. This is why a short window of data can look linear whatever the true model is, and why extrapolating a line beyond the data is dangerous.

### 4. A decision guide

1. **Do equal time steps add the same amount?** Then think *linear*.
2. **Do equal time steps multiply by the same factor (the same percentage)?** Then think *exponential*.
3. **Does each doubling of the effort or time add the same amount, with ever slower gains?** Then think *logarithmic*.
4. **Does growth speed up, peak and then slow towards a ceiling?** Then think *logistic*.
5. **Always check against the context.** Ask what physically drives the rate, whether there is a limit, and over what range the model is meant to apply.

### 5. Choosing between models with data

- **Residual plots:** curved or systematically patterned residuals mean the model is missing something.
- **Transformed plots:** straight line on semi-log (exponential), on log-$t$ axis (logarithmic), or in the logit plot (logistic).
- **Information criteria:** AIC $= n\ln(\mathrm{RSS}/n) + 2k$ trades off fit (RSS) against the number of parameters $k$ (the logistic has 3, the others 2). The comparison notebook shows by simulation that with little noise and the whole curve the right model is usually picked, and that with only the early part of the curve the models become hard to tell apart.

### 6. How these ideas connect with the literature reviewed

These links are based on abstracts, not on the full texts.

- **Covariation and splitting.** Confrey and Smith (1995) propose building the exponential function from a multiplicative "splitting" operation together with a covariation approach (two quantities changing together). The constant-ratio property in the exponential file ("equal steps, equal ratios") is the mathematical counterpart.
- **Several ways of thinking at once.** Castillo-Garsow (2013) warns that mathematicians use several, sometimes contradictory, ways of thinking about exponential growth (for example repeated multiplication versus continuous proportional growth) and that these may not be made distinct for students. This document shows both: $N_{n+1} = bN_n$ and $dN/dt = rN$.
- **Framing.** Schonger and Sele (2021) report that exponential growth bias is much smaller with doubling times. The exponential file gives the doubling time explicitly ("Doubling time and half-life").
- **Representations of the logistic equation.** A review of the logistic equation in mathematics education reports multiple representations as a main difficulty. The logistic section above shows four: the rate equation, the closed form, the S-curve and the parabola of rate against $P$.
- **Logarithm through progressions.** Ferrari proposes covarying arithmetic and geometric progressions to build the logarithm; the doubling property of the logarithmic model is exactly that covariation.

---

## 6. References

Sources cited in this document. All links were returned by searches; the descriptions come from abstracts.

- Bergsma, Y. (2019). *Students' understanding of exponents and exponential functions at a secondary school in the northern Netherlands* (Bachelor's thesis, University of Groningen). https://fse.studenttheses.ub.rug.nl/20116
- Castillo-Garsow, C. (2013). The role of multiple modeling perspectives in students' learning of exponential growth. *Mathematical Biosciences and Engineering*, 10(5&6), 1437–1453. https://www.aimspress.com/article/id/2461
- Confrey, J., & Smith, E. (1995). Splitting, covariation, and their role in the development of exponential functions. *Journal for Research in Mathematics Education*, 26(1), 66–86. https://doi.org/10.2307/749228
- Ferrari, M. *La covariación como elemento de resignificación de la función logaritmo*. (Year unconfirmed.) https://funes.uniandes.edu.co/wp-content/uploads/tainacan-items/32454/1216675/FerrariLacovariacionAlme2005.pdf
- Melnik-Leroy, G. A., et al. (2023). Is my visualization better than yours? Analyzing factors modulating exponential growth bias in graphs. *Frontiers in Psychology*. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2023.1125810/pdf
- Qualitative analysis of the logistic equation in Mathematics Education. *Educare* (UNA, Costa Rica). https://www.revistas.una.ac.cr/index.php/EDUCARE/article/view/18642
- Schonger, M., & Sele, D. (2021). Intuition and exponential growth: bias and the roles of parameterization and complexity. *Mathematics and Financial Economics*. https://link.springer.com/article/10.1007/s00591-021-00306-7
- Trejo, M., Ferrari, M., & Martínez, G. (2021). Covariación logarítmico-exponencial en futuros profesores de matemáticas: un estudio de caso. *Educación Matemática*, 33(1), 41–70. https://www.redalyc.org/journal/405/40576157003/40576157003.pdf
- Verhulst, P.-F. (1838). Notice sur la loi que la population poursuit dans son accroissement. *Correspondance mathématique et physique*, 10, 113–121. (Cited from memory; no link was retrieved, please verify.)
