# Logistic growth

$P(t) = K / (1 + A e^{-rt})$: growth that is exponential at first and **levels off** at a limit $K$.

**Companion notebook:** `04_logistic_growth.ipynb` (simulated data, fitting and exercises). This file is the mathematical explanation; the notebook is left unchanged.

> **Note on sources.** The mathematics and every worked number in this file were checked numerically. The statements about the literature rely on abstracts and catalogue pages, not on full texts, so check each source before citing it.

---

## 1. Definition

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

## 2. Where it comes from: growth that slows as the limit approaches

In the exponential model the **per-capita** growth rate $\dfrac{1}{P}\dfrac{dP}{dt}$ is a constant $r$. In a finite environment this cannot last. The simplest correction is to let the per-capita rate **decrease linearly** as $P$ approaches $K$:

$$
\frac{1}{P}\frac{dP}{dt} = r\left(1 - \frac{P}{K}\right)
\quad\Longleftrightarrow\quad
\boxed{\frac{dP}{dt} = r\,P\left(1 - \frac{P}{K}\right)} .
$$

This is the **logistic equation** (Verhulst, 1838). Two readings of the same equation:

- The factor $\left(1 - \dfrac{P}{K}\right)$ is the **fraction of the capacity still available**. It is close to 1 when $P$ is small (almost exponential growth) and close to 0 when $P$ is near $K$ (growth stops).
- Expanding, $\dfrac{dP}{dt} = rP - \dfrac{r}{K}P^{2}$: a growth term proportional to $P$ minus a **crowding** term proportional to $P^{2}$ (the number of pairs of individuals competing).

## 3. Solving the equation

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

## 4. Key properties

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

## 5. Linearisation

**Logit.** From $\dfrac{P}{K-P} = e^{r(t - t_0)}$,

$$
\ln\frac{P}{K - P} = r\,(t - t_0),
$$

a **straight line in $t$** with slope $r$ and intercept $-r t_0$. If $K$ is known, regressing $\ln\dfrac{P}{K-P}$ on $t$ estimates $r$ and $t_0$.

**Per-capita growth.** The equation also says $\dfrac{P'}{P} = r - \dfrac{r}{K}P$: the per-capita growth rate is a **decreasing straight line in $P$**, with intercept $r$ and slope $-r/K$, crossing zero at $P = K$. With data, plot $\dfrac{\Delta P/\Delta t}{P}$ against $P$ and read $r$ and $K$ from the line. This needs no calculus.

## 6. The discrete version, and a warning

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

## 7. Estimating $K$, $r$, $t_0$ from data

- **Nonlinear least squares** on $\sum_i (P_i - K/(1 + e^{-r(t_i - t_0)}))^2$, with starting values such as $K \approx 1.2 \max P_i$, $r \approx 0.3$, $t_0 \approx$ median of $t_i$.
- **Linearisation** (logit or per-capita growth) when a rough estimate of $K$ is available.
- **Identifiability warning:** $K$ is only well determined once the data **reach or pass the inflection point**. Data from the early, exponential-looking phase cannot reveal the limit (see the simulation in the logistic notebook).

## 8. Assumptions and limits

- $K$ and $r$ are **constant** in time and the same for all individuals.
- The population is "well mixed" and responds **instantly** (no delays).
- Real data are rarely exactly logistic. In the rumour simulation in the notebook, the rate fitted to the whole curve (about 1.35) is larger than the rate measured in the early phase (about 1.09). Extensions such as the Gompertz or Richards curves allow other shapes.

## 9. Worked example

A yeast culture: $K = 1000$, $r = 0.5$ per hour, $P_0 = 10$.

- $A = \dfrac{K - P_0}{P_0} = 99$ and $t_0 = \dfrac{\ln 99}{0.5} = 9.19$ hours.
- $P(10) = \dfrac{1000}{1 + 99\,e^{-5}} = 599.9$.
- Maximum growth rate $\dfrac{rK}{4} = 125$ per hour, reached at $P = 500$ (at $t = t_0 = 9.19$ h).
- The culture goes from $10\%$ to $90\%$ of $K$ in $\dfrac{2\ln 9}{0.5} = 8.79$ hours (from $t = 4.80$ h to $t = 13.59$ h).
- Early on, $P(8) \approx 10\,e^{0.5\cdot 8} = 545.98$ would be the exponential prediction, but the logistic value is $P(8) = 355.5$: the limit is already pulling growth down.

## 10. Things to watch (suggestions for teaching, partly drawn from the sources)

- A review of the logistic equation in mathematics education reports that the main difficulties involve **multiple representations** (the equation, the curve, the rate) and communicating across disciplines. Showing the three representations side by side, and the recurrence, helps (see the notebook).
- A teaching experiment with high-school students (Castillo-Garsow, 2013) moved from exponential growth to the logistic model and warns that several ways of thinking about exponential growth are often used without being distinguished for students.
- Students need the idea that growth can **look exponential at first** and still be limited. Asking "what could stop this growth?" is the natural step from the exponential to the logistic model.

---

## References

- Castillo-Garsow, C. (2013). The role of multiple modeling perspectives in students' learning of exponential growth. *Mathematical Biosciences and Engineering*, 10(5&6), 1437–1453. https://www.aimspress.com/article/id/2461
- Qualitative analysis of the logistic equation in Mathematics Education. *Educare* (UNA, Costa Rica). https://www.revistas.una.ac.cr/index.php/EDUCARE/article/view/18642
- Verhulst, P.-F. (1838). Notice sur la loi que la population poursuit dans son accroissement. *Correspondance mathématique et physique*, 10, 113–121. (Cited from memory; no link was retrieved, please verify.)
