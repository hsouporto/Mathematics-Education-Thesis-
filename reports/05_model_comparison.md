# Comparing the four growth models

The four models side by side: what is constant, shape, limits, inverse, linearisation, how to choose.

**Companion notebook:** `05_model_comparison.ipynb` (simulated data, fitting and exercises). This file is the mathematical explanation; the notebook is left unchanged.

> **Note on sources.** The mathematics and every worked number in this file were checked numerically. The statements about the literature rely on abstracts and catalogue pages, not on full texts, so check each source before citing it.

---

## 1. One question, four models: what is the growth rate proportional to?

The four models can be read as four answers to the question *"what determines how fast the quantity changes?"*

| Model | Growth rate $dy/dt$ | Relative rate $\dfrac{1}{y}\dfrac{dy}{dt}$ | Closed form | Discrete version |
|---|---|---|---|---|
| **Linear** | constant: $b$ | $\dfrac{b}{y}$ (falls as $y$ grows) | $y = a + bt$ | $y_{n+1} = y_n + d$ (arithmetic progression) |
| **Exponential** | proportional to $y$: $rN$ | constant: $r$ | $N = N_0 e^{rt}$ | $N_{n+1} = b\,N_n$ (geometric progression) |
| **Logarithmic** | inversely proportional to time: $b/t$ | $\dfrac{b}{t\,y}$ | $y = a + b\ln t$ | increments $b\ln\dfrac{t_{n+1}}{t_n}$ |
| **Logistic** | $rP\left(1 - \dfrac{P}{K}\right)$ | $r\left(1 - \dfrac{P}{K}\right)$ (falls linearly in $P$) | $P = \dfrac{K}{1 + Ae^{-rt}}$ | $P_{n+1} = P_n + rP_n(1 - P_n/K)\Delta t$ |

## 2. Properties side by side

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

## 3. How the models are related

- **Exponential and logistic.** The logistic equation reduces to the exponential when $K \to \infty$ (or when $P \ll K$). The exponential is the *early phase* of the logistic.
- **Exponential and logarithmic.** They are **inverse functions**: $y = \ln t$ undoes $t = e^{y}$. Swapping the roles of input and output turns one into the other. In the exponential model adding to $t$ multiplies $N$; in the logarithmic model multiplying $t$ adds to $y$.
- **Each model is a straight line after a transformation.** Linear: $(t, y)$. Exponential: $(t, \ln y)$. Logarithmic: $(\ln t, y)$. Logistic: $\left(t, \ln\frac{P}{K-P}\right)$. Choosing the transformation under which the data look straight is a practical way of choosing the model.
- **Linear as a local approximation.** Every differentiable model is approximately linear over a short window: $y(t+h) \approx y(t) + y'(t)\,h$. This is why a short window of data can look linear whatever the true model is, and why extrapolating a line beyond the data is dangerous.

## 4. A decision guide

1. **Do equal time steps add the same amount?** Then think *linear*.
2. **Do equal time steps multiply by the same factor (the same percentage)?** Then think *exponential*.
3. **Does each doubling of the effort or time add the same amount, with ever slower gains?** Then think *logarithmic*.
4. **Does growth speed up, peak and then slow towards a ceiling?** Then think *logistic*.
5. **Always check against the context.** Ask what physically drives the rate, whether there is a limit, and over what range the model is meant to apply.

## 5. Choosing between models with data

- **Residual plots:** curved or systematically patterned residuals mean the model is missing something.
- **Transformed plots:** straight line on semi-log (exponential), on log-$t$ axis (logarithmic), or in the logit plot (logistic).
- **Information criteria:** AIC $= n\ln(\mathrm{RSS}/n) + 2k$ trades off fit (RSS) against the number of parameters $k$ (the logistic has 3, the others 2). The comparison notebook shows by simulation that with little noise and the whole curve the right model is usually picked, and that with only the early part of the curve the models become hard to tell apart.

## 6. How these ideas connect with the literature reviewed

These links are based on abstracts, not on the full texts.

- **Covariation and splitting.** Confrey and Smith (1995) propose building the exponential function from a multiplicative "splitting" operation together with a covariation approach (two quantities changing together). The constant-ratio property in the exponential file ("equal steps, equal ratios") is the mathematical counterpart.
- **Several ways of thinking at once.** Castillo-Garsow (2013) warns that mathematicians use several, sometimes contradictory, ways of thinking about exponential growth (for example repeated multiplication versus continuous proportional growth) and that these may not be made distinct for students. This document shows both: $N_{n+1} = bN_n$ and $dN/dt = rN$.
- **Framing.** Schonger and Sele (2021) report that exponential growth bias is much smaller with doubling times. The exponential file gives the doubling time explicitly ("Doubling time and half-life").
- **Representations of the logistic equation.** A review of the logistic equation in mathematics education reports multiple representations as a main difficulty. The logistic section above shows four: the rate equation, the closed form, the S-curve and the parabola of rate against $P$.
- **Logarithm through progressions.** Ferrari proposes covarying arithmetic and geometric progressions to build the logarithm; the doubling property of the logarithmic model is exactly that covariation.

---

## References

- Castillo-Garsow, C. (2013). The role of multiple modeling perspectives in students' learning of exponential growth. *Mathematical Biosciences and Engineering*, 10(5&6), 1437–1453. https://www.aimspress.com/article/id/2461
- Confrey, J., & Smith, E. (1995). Splitting, covariation, and their role in the development of exponential functions. *Journal for Research in Mathematics Education*, 26(1), 66–86. https://doi.org/10.2307/749228
- Qualitative analysis of the logistic equation in Mathematics Education. *Educare* (UNA, Costa Rica). https://www.revistas.una.ac.cr/index.php/EDUCARE/article/view/18642
- Ferrari, M. *La covariación como elemento de resignificación de la función logaritmo*. (Year unconfirmed.) https://funes.uniandes.edu.co/wp-content/uploads/tainacan-items/32454/1216675/FerrariLacovariacionAlme2005.pdf
- Schonger, M., & Sele, D. (2021). Intuition and exponential growth: bias and the roles of parameterization and complexity. *Mathematics and Financial Economics*. https://link.springer.com/article/10.1007/s00591-021-00306-7
