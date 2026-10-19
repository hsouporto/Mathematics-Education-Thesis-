# Linear growth

$y(t) = a + b\,t$: constant **additions** per unit of time.

**Companion notebook:** `01_linear_growth.ipynb` (simulated data, fitting and exercises). This file is the mathematical explanation; the notebook is left unchanged.

> **Note on sources.** The mathematics and every worked number in this file were checked numerically. The statements about the literature rely on abstracts and catalogue pages, not on full texts, so check each source before citing it.

---

## 1. Definition

A quantity $y$ grows **linearly** in time $t$ if

$$
y(t) = a + b\,t, \qquad a, b \in \mathbb{R}.
$$

- $a = y(0)$ is the **intercept**: the starting value.
- $b$ is the **slope**: the change in $y$ per unit of time. It has the units of $y$ divided by the units of $t$ (euros per week, centimetres per hour).
- If $b>0$ the quantity increases, if $b<0$ it decreases (linear *decay*), and if $b=0$ it is constant.

## 2. Where it comes from: a constant rate of change

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

## 3. The characteristic property: equal steps, equal additions

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

## 4. Graph and shape

- The graph is a **straight line** with slope $b$ and vertical intercept $a$.
- The **root** (where $y=0$) is at $t = -a/b$, if $b\neq 0$.
- It is monotone (increasing for $b>0$, decreasing for $b<0$) and has no horizontal asymptote.

## 5. Inverse and "time to target"

Solving $y = a + bt$ for $t$ gives the inverse function, which is also linear:

$$
t = \frac{y - a}{b}.
$$

The time needed to reach a target value $y^{*}$ is therefore

$$
t^{*} = \frac{y^{*} - a}{b}.
$$

## 6. Estimating $a$ and $b$ from data (least squares)

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

## 7. Assumptions and limits

- The rate of change is **constant**: nothing speeds it up or slows it down.
- The quantity is **unbounded**: it keeps growing (or falling) forever. Real quantities usually are not, so a linear model is typically valid only over a limited range. Extrapolating far beyond the data is risky.

## 8. Worked example

A student has €20 and saves €7.50 per week, so $y(t) = 20 + 7.5\,t$.

- After 20 weeks: $y(20) = 20 + 7.5 \times 20 = 170$ euros.
- Savings reach €250 when $t^{*} = \dfrac{250 - 20}{7.5} = 30.67$ weeks.
- Each week adds €7.50, but the *percentage* growth falls from $7.5/20 = 37.5\%$ in the first week to $7.5/170 \approx 4.4\%$ around week 20.

## 9. Things to watch (suggestions for teaching, not drawn from the literature)

- Do not confuse "increases by the same **amount**" (linear) with "increases by the same **percentage**" (exponential). The signature of linearity is constant *differences*.
- Check units of the slope when interpreting it.
- A straight-looking graph over a short window does not prove the model is linear (see the model-comparison notebook).
