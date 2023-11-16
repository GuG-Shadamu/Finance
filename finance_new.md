# Derivative Reviews

## Black-Scholes Model

### **Assumption**

  1. No dividends are paid out during the life of the option
  2. Market movements cannot be predicted (random)
  3. No transaction cost
  4. The risk-free rate and volatility of the underlying asset are known and **constant**
  5. The returns of the underlying asset are normally distributed
  6. The option is European and can only be exercised at expiration

### Model Black-Scholes Equation and its Logarithmic Form  

$$\frac{dS}{S} = \mu dt + \sigma dB$$

Where:

- $\mu$ is the expected return or drift.
- $\sigma$ is the stock's volatility.
- $dB$ is the increment of a Wiener process or Brownian motion.

Using new process:

$$X(t) = \ln(S(t))$$

By applying Ito's Lemma, the differential $dX(t)$ is:

$$dX(t) = \frac{dS}{S} - \frac{1}{2} \sigma^2 dt$$

Substituting the original SDE into this equation, we obtain:

$$dX(t) = (\mu - \frac{1}{2} \sigma^2) dt + \sigma dB$$

The term $\frac{1}{2} \sigma^2$ arises from Ito's Lemma due to the quadratic variation of the Brownian motion.


### Put - Call Parity

$$e^{(-rT)}K + Call = e^{-qT}S(0) + Put $$



## Levy's Theorem (Quatratic Variance)
  
A continues martingale is a Brownian motion **if and only if** its quadratic variation over each interval [0, T] equals T


## Martingale

A martingale is a type of stochastic process that models a fair game. In formal terms, a real-valued stochastic process $X_t$ is considered a martingale if it satisfies certain conditions.

A stochastic process $X_t$ is a martingale with respect to a filtration $\mathcal{F}_t$ if:

1. **Integrability**: $E[|X_t|] < \infty$ for all $t$.
   - The expected value of the absolute value of $X_t$ is finite for all $t$.

2. **Adaptedness**: $X_t$  is $\mathcal{F}_t$-measurable for each $t$. (the value of the process at time $t$ t doesn't depend on any future information; it's only based on what we know up to and including time $t$ .)
   - $X_t$ is adapted to the filtration $\mathcal{F}_t$.

3. **Martingale Property**: $E[X_{t+s} | \mathcal{F}_t] = X_t$ for all $s \geq 0$ and $t$.
   - The conditional expected value of $X_{t+s}$, given all the information up to time $t$, is $X_t$.
  

## Ito's

### Ito Processes

Let $X(t)$ and $Y(t)$ be defined as:

$$
\begin{aligned}
dX_t &= a_1(t, X_t) dt + b_1(t, X_t) dW_{1t} \\
dY_t &= a_2(t, Y_t) dt + b_2(t, Y_t) dW_{2t}
\end{aligned}
$$

### Ito's Lemma for 2 processes (multi Ito's processes)

For a twice-differentiable function $g(t, x, y)$ , the differential $dZ(t)$ is given by:

$$
\begin{aligned}
dZ(t) &= \frac{\partial g}{\partial t} dt + \frac{\partial g}{\partial x} dX_t + \frac{\partial g}{\partial y} dY_t \\
&\quad + \frac{1}{2} \frac{\partial^2 g}{\partial x^2} (b_1(t, X_t))^2 dt + \frac{1}{2} \frac{\partial^2 g}{\partial y^2} (b_2(t, Y_t))^2 dt \\
&\quad + \frac{\partial^2 g}{\partial x \partial y} b_1(t, X_t) b_2(t, Y_t) dt
\end{aligned}
$$

Here, $\frac{\partial g}{\partial t}$, $\frac{\partial g}{\partial x}$, $\frac{\partial g}{\partial y}$, $\frac{\partial^2 g}{\partial x^2}$, $\frac{\partial^2 g}{\partial y^2}$, and $\frac{\partial^2 g}{\partial x \partial y}$ are the partial derivatives of $g$ with respect to $t$, $x$, and $y$, and their second-order mixed derivatives.

### Ito Lemma for Brownian motion

Let $B(t)$ be a standard Brownian motion, and let $f(t, x)$ be a twice continuously differentiable function. If $X(t)$ is given by

$$X(t) = f(t, B(t))$$

then the differential $dX(t)$ is given by:

$$dX(t) = \frac{\partial f}{\partial t} dt + \frac{\partial f}{\partial x} dB(t) + \frac{1}{2} \frac{\partial^2 f}{\partial x^2} dt$$
