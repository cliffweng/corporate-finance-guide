---
title: "02. Risk and return"
layout: default
nav_order: 3
---

# Risk and return
{: .no_toc }

*~9 min read*

**🎯 Interview frequent**

## Why it matters

Corporate finance is fundamentally the study of capital allocation under uncertainty. Every dollar a corporation invests in a project, equipment, or an acquisition could have been returned to investors to deploy in the capital markets. Therefore, the required return on any corporate investment depends entirely on the risk of that investment. In technical finance interviews, understanding how risk is decomposed into systematic and unsystematic components explains why corporations do not receive valuation premiums simply for diversifying across unrelated businesses, and why standard deviation is not the proper discount metric for equity investors.

## Core concepts

- **Expected Return and Variance:** For an asset with payoff states \(i = 1, \dots, S\) occurring with probabilities \(p_i\):
  \[
  E[R] = \sum_{i=1}^S p_i R_i, \quad \sigma^2 = \sum_{i=1}^S p_i \left(R_i - E[R]\right)^2
  \]
  Standard deviation (\(\sigma\)) measures total volatility—both upside and downside dispersion around the mean.
- **Covariance and Correlation:** The joint dispersion of two assets \(A\) and \(B\):
  \[
  \text{Cov}(R_A, R_B) = \sigma_{AB} = E\left[(R_A - E[R_A])(R_B - E[R_B])\right]
  \]
  \[
  \rho_{AB} = \frac{\sigma_{AB}}{\sigma_A \sigma_B}, \quad \text{where } -1 \le \rho_{AB} \le 1
  \]
- **Portfolio Variance (Two Assets):**
  \[
  \sigma_p^2 = w_A^2 \sigma_A^2 + w_B^2 \sigma_B^2 + 2 w_A w_B \text{Cov}(R_A, R_B)
  \]
  Whenever \(\rho_{AB} < 1\), the portfolio standard deviation \(\sigma_p\) is strictly less than the weighted average of individual standard deviations: \(\sigma_p < w_A \sigma_A + w_B \sigma_B\). Diversification is a mathematical free lunch.
- **The Limits of Diversification (Large \(N\)):** In an equally weighted portfolio of \(N\) assets where \(w_i = 1/N\):
  \[
  \sigma_p^2 = \frac{1}{N} \overline{\sigma_i^2} + \left(1 - \frac{1}{N}\right) \overline{\text{Cov}}
  \]
  As \(N \to \infty\), the first term \(\frac{1}{N}\overline{\sigma_i^2} \to 0\). Individual variances vanish completely. The remaining risk is purely the average covariance between assets (\(\overline{\text{Cov}}\)).
- **Decomposition of Risk:**
  - **Unsystematic (Idiosyncratic / Firm-Specific) Risk:** Lawsuits, executive turnover, strike action, failed R&D. Can be eliminated at zero cost by holding a diversified portfolio.
  - **Systematic (Market / Macro) Risk:** GDP shocks, interest rate cycles, energy shocks, geopolitical turmoil. Affects all productive capital and cannot be diversified away.
- **The Core Axiom of Modern Finance:** Capital markets only compensate investors for bearing systematic risk. Because diversified investors set marginal prices, no asset earns an expected return premium for idiosyncratic volatility.

## Mental model

```
  Portfolio Volatility (sigma)
      ^
      |  \
      |   \   Total Risk = Idiosyncratic + Systematic
      |    \
      |     \--- Unsystematic Risk (diversified away)
      |          ====================================
      |--------------------------------------------- Systematic Risk Floor
      |                                              (undiversifiable macro risk)
      +---------------------------------------------> Number of Assets (N)
           1      5      10      20      30+
```

An investor holding 30+ uncorrelated stocks eliminates ~90% of idiosyncratic risk. Therefore, a corporate manager cannot create value simply by diversifying corporate operations—shareholders can replicate that diversification at negligible brokerage cost without the conglomerate discount.

## Interview questions

1. **A biotechnology stock has an annual standard deviation of 70%, but its beta against the S&P 500 is only 0.4. How can a stock be extremely volatile yet have a low beta? Which metric determines its cost of equity?**  
   Answer: Beta measures systematic risk (\(\beta_i = \text{Cov}(R_i, R_m)/\sigma_m^2 = \rho_{im}\sigma_i/\sigma_m\)). The biotech company's high volatility is driven almost entirely by firm-specific events—FDA drug trial results, clinical data readouts, and patent disputes—which have zero correlation with macroeconomic GDP growth or market indices. In a well-diversified portfolio, these clinical binary outcomes cancel out against uncorrelated events in other stocks. Under standard asset pricing (CAPM), only its systematic risk (\(\beta = 0.4\)) determines its required cost of equity (\(r_e = r_f + \beta \cdot ERP\)).

2. **Why do publicly traded conglomerates trade at a "conglomerate discount" instead of a diversification premium?**  
   Answer: Shareholders do not need a corporation to diversify for them; investors can diversify their own personal portfolios across sectors with minimal fees and greater liquidity. Operating multiple disparate divisions inside one corporate shell introduces bureaucratic inefficiencies, capital misallocation (cross-subsidizing failing divisions with cash cows), agency conflicts, and opacity that makes individual business lines difficult for public analysts to value.

3. **Can you combine two risky assets with positive standard deviations to form a risk-free portfolio (\(\sigma_p = 0\))? Under what condition?**  
   Answer: Yes, if the two assets are perfectly negatively correlated (\(\rho = -1\)). Setting \(\sigma_p^2 = (w_A\sigma_A - w_B\sigma_B)^2 = 0\) with \(w_B = 1 - w_A\) yields:
   \[
   w_A = \frac{\sigma_B}{\sigma_A + \sigma_B}, \quad w_B = \frac{\sigma_A}{\sigma_A + \sigma_B}
   \]
   At these weights, movements in asset A perfectly offset movements in asset B, eliminating portfolio variance entirely.

4. **When estimating the historical equity risk premium (ERP), should you use arithmetic or geometric average returns?**  
   Answer: The arithmetic average return is the unbiased estimator of the expected return over a single forward-looking period (e.g., the next 1 year). The geometric mean (CAGR) measures the compound multi-year growth rate of wealth, which accounts for volatility drag (\(R_{\text{geom}} \approx R_{\text{arith}} - \frac{1}{2}\sigma^2\)). For single-period annual discounting in corporate finance models, standard modern finance theory prefers the arithmetic mean, though many practitioners use geometric averages or forward-looking implied premiums (e.g., Damodaran approach) to avoid upward bias over long investment horizons.

## Watch

- [Session 5: End Game Closure and First Steps on Risk](https://www.youtube.com/watch?v=4KIw09ULq5g) — Prof. Aswath Damodaran (NYU Stern). The transition from corporate governance to risk definition, variance, and covariance.
- [Session 4: Equity Risk Premiums](https://www.youtube.com/watch?v=U3D9a_H_Vrs) — Prof. Aswath Damodaran (NYU Stern). Understanding the macro price of risk, historical vs. forward-looking implied premiums.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 7: "Introduction to Risk, Return, and the Opportunity Cost of Capital".
- Damodaran, Aswath, *Applied Corporate Finance*, Chapter 3: "Risk and Return: Foundations".
