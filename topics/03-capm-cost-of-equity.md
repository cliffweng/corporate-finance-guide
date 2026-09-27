---
title: "03. CAPM & cost of equity"
layout: default
nav_order: 4
---

# Capital Asset Pricing Model and cost of equity
{: .no_toc }

*~9 min read*

**🎯 Interview frequent**

## Why it matters

The Capital Asset Pricing Model (CAPM) is the corporate finance standard for pricing equity capital. Unlike debt—which carries an observable contractual coupon—equity has no guaranteed cash payout. Equity investors demand a rate of return commensurate with the systematic risk they bear. In investment banking valuation, the cost of equity (\\(r_e\\)) is the primary component of the Weighted Average Cost of Capital ([WACC](../04-wacc/)) and the sole discount rate for Free Cash Flow to Equity ([FCFE](../08-free-cash-flow/)). Interviewers frequently probe how beta is estimated, unlevered, and relevered across capital structures.

## Core concepts

- **The CAPM Formula:**

\\[
r_e = r_f + \beta_e \cdot \left(E[R_m] - r_f\right) = r_f + \beta_e \cdot ERP
\\]

  - **Risk-Free Rate (\\(r_f\\)):** The yield on a default-free government security matching the currency and horizon of the cash flows (typically the 10-Year or 30-Year US Treasury bond).
  - **Equity Risk Premium (\\(ERP = E[R_m] - r_f\\)):** The incremental return investors demand over risk-free bonds to hold the aggregate market portfolio. Typically ranges between 4.5% and 6.0% in mature markets.
  - **Equity Beta (\\(\beta_e\\)):** The sensitivity of the stock's excess returns to market excess returns:

\\[
\beta_e = \frac{\text{Cov}(R_i, R_m)}{\text{Var}(R_m)} = \rho_{im} \frac{\sigma_i}{\sigma_m}
\\]

- **Asset Beta vs. Equity Beta (Business Risk vs. Financial Risk):**
  - **Unlevered Beta (\\(\beta_U\\) or \\(\beta_{\text{asset}}\\)):** Measures the fundamental business risk of the operating assets, completely independent of how the company is financed.
  - **Levered Beta (\\(\beta_L\\) or \\(\beta_{\text{equity}}\\)):** Amplifies business risk by the financial leverage of debt. Debt holders have senior priority on cash flows; equity holders absorb the residual variance.
- **The Hamada Equation:** Assuming risk-free debt (\\(\beta_D \approx 0\\)) and a constant dollar debt shield:

\\[
\beta_L = \beta_U \left[1 + (1 - t) \frac{D}{E}\right] \iff \beta_U = \frac{\beta_L}{1 + (1 - t) \frac{D}{E}}
\\]

  *(Where \\(D/E\\) is the market debt-to-equity ratio and \\(t\\) is the marginal corporate tax rate.)*
- **Bottom-Up Beta (The Banking Standard):**
  Regression betas on a single stock are notoriously unreliable (standard errors often exceed 0.25). Instead, analysts use bottom-up estimation:
  1. Identify a peer group of publicly traded pure-play companies in the same industry.
  2. Gather each peer's levered regression beta (\\(\beta_L\\)), market capitalization (\\(E\\)), and net debt (\\(D\\)).
  3. Unlever each peer's beta to extract its asset beta (\\(\beta_U\\)) using its own tax rate and \\(D/E\\).
  4. Calculate the peer group median or trimmed average \\(\beta_U\\).
  5. Relever this industry asset beta to the target company's current or target capital structure.

## Mental model

```
  Expected Return E[R]
      ^                                  Security Market Line (SML)
      |                                  /
      |                                 /  Slope = Equity Risk Premium (ERP)
      |                                /
  r_e |-------------------------------* [ Firm Equity: r_e = r_f + beta * ERP ]
      |                              /|
      |                             / |
  E[Rm]---------------------------*  |
      |                          /|  |
      |                         / |  |
  r_f |------------------------/  |  |
      +-----------------------+---+--+----------------------------------> Beta (beta)
      0                      beta=1  beta_e
```

The Security Market Line (SML) represents equilibrium pricing. Any asset plotted above the SML generates positive abnormal return (\\(\alpha > 0\\)); assets below are overpriced given their risk.

## Interview questions

1. **Walk me through how you estimate the cost of equity for a private enterprise or a non-public division.**  
   Answer:  
   1. Find 4–6 public comparable companies operating in the same sector with similar business models.  
   2. Retrieve the equity beta (\\(\beta_L\\)) of each peer and unlever using its respective tax rate and market \\(D/E\\) ratio: \\(\beta_{U, i} = \frac{\beta_{L, i}}{1 + (1 - t_i)(D_i/E_i)}\\).  
   3. Take the median of the peer unlevered betas to establish the pure business asset risk (\\(\beta_U\\)).  
   4. Relever this benchmark \\(\beta_U\\) to the private firm's target capital structure: \\(\beta_{L, \text{target}} = \beta_U \left[1 + (1 - t_{\text{target}})\frac{D_{\text{target}}}{E_{\text{target}}}\right]\\).  
   5. Plug \\(\beta_{L, \text{target}}\\) into CAPM with the current 10-year Treasury yield (\\(r_f\\)) and market ERP: \\(r_e = r_f + \beta_{L, \text{target}} \cdot ERP\\).

2. **What does a negative beta imply? What would its expected return be relative to the risk-free rate, and why would any rational investor hold it?**  
   Answer: A negative beta (\\(\beta < 0\\)) means the asset's returns are negatively correlated with the overall market. By the CAPM formula, \\(r_e = r_f + \beta(ERP) < r_f\\). Its expected return is strictly *lower* than the risk-free rate. Rational investors willingly accept this discount because the asset acts as portfolio insurance—it surges during catastrophic market downturns, dramatically lowering total portfolio variance when marginal utility of wealth is highest (e.g., gold or out-of-the-money puts).

3. **If a company executes a debt-financed share repurchase, what happens to its asset beta (\\(\beta_U\\)) and its equity beta (\\(\beta_L\\))?**  
   Answer: The asset beta (\\(\beta_U\\)) remains unchanged because the underlying operational business assets, product markets, and operating cash flows have not altered. However, the equity beta (\\(\beta_L\\)) increases because financial leverage (\\(D/E\\)) rises. With a fixed interest burden, the residual cash flows to equity become significantly more volatile relative to swings in operating profit.

4. **Why is the 10-year Treasury yield preferred as the risk-free rate rather than the 3-month Treasury bill or 30-year bond?**  
   Answer: The 3-month T-bill contains significant reinvestment risk and is heavily influenced by short-term Federal Reserve monetary actions, whereas corporate equity is a long-duration asset. The 30-year bond carries higher duration risk and liquidity/term premiums. The 10-year US Treasury provides an optimal benchmark that approximates the average duration of corporate cash flows in typical 5- to 10-year DCF projections without undue term-structure distortions.

## Watch

- [Session 6: Risk - From Models to Inputs](https://www.youtube.com/watch?v=ooQkd7OUXtc) — Prof. Aswath Damodaran (NYU Stern). Setting up the CAPM equation, risk-free rate choices, and ERP.
- [Session 8: Betas and Beyond!](https://www.youtube.com/watch?v=niH52NaFbAs) — Prof. Aswath Damodaran (NYU Stern). Understanding regression betas, fundamentals of beta, and peer-group estimation.
- [Session 5: Betas (Relative Risk Measures)](https://www.youtube.com/watch?v=qKy5UGcvWaw) — Prof. Aswath Damodaran (NYU Stern). Sector betas, business risk, operating leverage, and financial leverage.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 8: "Portfolio Theory and the Capital Asset Pricing Model".
- Damodaran, Aswath, *Investment Valuation*, Chapter 4: "The Basics of Risk".
