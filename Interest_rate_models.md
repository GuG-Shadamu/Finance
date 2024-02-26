# Comparison of Common Interest Rate Models with Parameters









| Model                                                       | Characteristics                                                                   | Use Cases                                                       | Key Parameters                                                                 |
| ----------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| **Black-Scholes Model**                                     | Assumes constant volatility and lognormal distribution of rates.                  | European options on bonds, interest rate caps, and floors.      | Volatility (σ)                                                                 |
| **Black Model (Black 76)**                                  | Adapted for futures, assumes lognormal distribution of future rates.              | Options on interest rate futures.                               | Volatility (σ)                                                                 |
| **Vasicek Model**                                           | First short-rate model, assumes mean reversion and normally distributed rates.    | Bond pricing, bond options.                                     | Mean reversion rate (a), long-term mean level (b), volatility (σ)              |
| **Cox-Ingersoll-Ross (CIR)**                                | Ensures positive interest rates with mean reversion and chi-squared distribution. | Zero-coupon bonds, certain interest rate derivatives.           | Mean reversion rate (a), long-term mean level (b), volatility (σ)              |
| **Heath-Jarrow-Morton (HJM) Framework**                     | Models the entire forward rate curve, accounts for drift and volatility.          | Complex interest rate derivatives, entire yield curve products. | Drift (μ(t)), volatility (σ(t, T)) functions of time and maturity              |
| **Hull-White Model**                                        | Allows for time-varying parameters, an extension of Vasicek and CIR.              | European and American bond options, caps, and floors.           | Mean reversion rate (a), time-dependent volatility (σ(t))                      |
| **Libor Market Model (BGM)**                                | Models forward LIBOR rates, accounts for lognormal distribution.                  | Swaptions, caplets, and other LIBOR-based derivatives.          | Volatilities (σ), correlations between different LIBOR rates                   |
| **Multi-Factor Models (e.g., G2++, Two-Factor Hull-White)** | Models several sources of risk simultaneously.                                    | Products sensitive to various parts of the yield curve.         | Multiple mean reversion rates (a1, a2), volatilities (σ1, σ2), correlation (ρ) |


# Comparison of Common Volatility Models for Interest Rate Derivatives with Parameters

| Model                                        | Characteristics                                                               | Use Cases                                                                       | Key Parameters                                                                           |
| -------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| **SABR Model**                               | Stochastic volatility model with specific parameters for volatility dynamics. | Interest rate caps, floors, swaptions; captures volatility smile.               | α (vol of vol), β (volatility elasticity), ρ (correlation), ν (volatility of volatility) |
| **Local Volatility Models (Dupire)**         | Volatility as a function of asset price and time.                             | Equity and FX derivatives; fits observed volatility surface precisely.          | Local volatility function σ(S, t) dependent on asset price (S) and time (t)              |
| **Jump-Diffusion Models (Merton, Kou)**      | Incorporates jumps in asset prices along with continuous Brownian motion.     | Markets with sudden price moves or asymmetric risk of jumps.                    | Volatility (σ), jump intensity (λ), jump size distribution parameters                    |
| **Stochastic Local Volatility (SLV) Models** | Combines stochastic and local volatility features for a better fit.           | Exotic options where both market and smile dynamics are important.              | Local volatility surface σ(S, t), stochastic volatility parameters (as in SABR)          |
| **Levy Process Models**                      | Uses Lévy processes for asset price evolution, capturing jumps and fat tails. | Derivatives in markets with significant jump risks or fat-tailed distributions. | Parameters defining the Lévy process (e.g., scale, location, jump intensity)             |
| **Bergomi Model**                            | Focuses on the dynamics of forward volatilities and correlations.             | Pricing volatility derivatives, managing volatility risk in complex markets.    | Forward variance curve, vol of vol, correlation structures                               |
