---
title: "04. WACC"
layout: default
nav_order: 5
---

# Weighted Average Cost of Capital (WACC)
{: .no_toc }

*~10 min read*

**🎯 Interview frequent**

## Why it matters

The Weighted Average Cost of Capital (WACC) is the universal hurdle rate in corporate finance. It measures the minimum average return a company must generate across all its productive assets to satisfy its capital providers—senior lenders, subordinated bondholders, preferred shareholders, and common equity investors. In investment banking, WACC is the discount rate used to discount Unlevered Free Cash Flows ([FCFF](../08-free-cash-flow/)) to determine Enterprise Value ([EV](../09-enterprise-vs-equity-value/)). A 100-basis-point swing in WACC can swing a multi-billion-dollar valuation by 15–20%, making WACC mechanics one of the most heavily tested areas in financial interviews.

## Core concepts

- **The Standard Formula:**

\\[
\text{WACC} = \left(\frac{E}{V}\right) r_e + \left(\frac{D}{V}\right) r_d (1 - t) + \left(\frac{P}{V}\right) r_p
\\]

  - \\(E\\): Market value of common equity (market capitalization: \\(\text{share price} \times \text{diluted shares}\\)).
  - \\(D\\): Market value of debt.
  - \\(P\\): Market value of preferred stock (if applicable).
  - \\(V = E + D + P\\): Total market enterprise capitalization.
  - \\(r_e\\): Cost of equity derived via [CAPM](../03-capm-cost-of-equity/).
  - \\(r_d\\): Pre-tax marginal cost of debt.
  - \\(t\\): Marginal corporate tax rate.
  - \\(r_p\\): Cost of preferred stock (\\(D_p / P_0\\)).
- **Weights MUST Reflect Market Values, Not Book Values:**
  Book values represent sunk, historical accounting entries. Investors in capital markets do not commit capital based on historical costs; they require a return on the *current market value* of their investments. If a company has a book equity of $100M and a market cap of $1B, using book weights drastically overweights debt and underestimates the true economic cost of capital.
- **Cost of Debt (\\(r_d\\)) is Forward-Looking:**
  - **Never use the historical coupon rate.** The coupon on an existing bond reflects financing conditions at issuance.
  - Use the current **Yield to Maturity (YTM)** on the company’s long-term liquid public bonds.
  - If public debt is illiquid or unrated, estimate a **synthetic credit rating** based on the interest coverage ratio (\\(\text{EBIT} / \text{Interest Expense}\\)) and add the corresponding corporate default spread to the risk-free rate:

\\[
r_d = r_f + \text{Default Spread}_{\text{rating}}
\\]

- **The Interest Tax Shield (\\(1 - t\\)):**
  Because interest payments are tax-deductible expenses on the income statement, the government effectively subsidizes debt financing. Each dollar of interest saves \\(t\\) dollars in taxes, yielding an effective after-tax borrowing cost of \\(r_d(1-t)\\). Note that preferred dividends are paid from *net income* (after tax) and therefore provide no tax deduction.
- **WACC vs. APV (Adjusted Present Value):**
  - Standard WACC assumes the firm manages toward a **constant target debt-to-equity ratio** over time, automatically adjusting debt levels as firm value changes.
  - If a deal has a fixed, changing nominal debt repayment schedule (such as an LBO or project finance loan), WACC breaks down. In those cases, **Adjusted Present Value (APV)** is mathematically superior: value the unlevered firm at \\(r_u\\) and add the PV of specific interest tax shields separately.

## Mental model

```
  Total Enterprise Capital (V = E + D)
  +-------------------------------------------------------------+
  | Common Equity (E / V)                                       |  Required Return: r_e
  | - Residual claim                                            |  (Determined by CAPM)
  | - Highest risk, highest required return                     |
  +-------------------------------------------------------------+
  | Senior Debt (D / V)                                         |  Required Return: r_d * (1 - t)
  | - Contractual cash flows, senior collateral                 |  (Subsidized by tax shield)
  | - Lower risk, cheaper cost                                  |
  +-------------------------------------------------------------+
                                 |
                                 v
        WACC = (E/V) * r_e  +  (D/V) * r_d * (1 - t)
```

Think of WACC as the blended hourly billing rate of a multidisciplinary firm: you weight each professional's billing rate by their proportional share of total hours worked.

## Interview questions

1. **If debt is cheaper than equity due to seniority and the tax shield, why doesn't a corporation finance itself with 100% debt to minimize WACC?**  
   Answer: As leverage increases, the probability of financial distress and bankruptcy escalates non-linearly. Higher debt increases financial risk for equity holders, causing equity beta (\\(\beta_L\\)) and cost of equity (\\(r_e\\)) to rise steeply. Beyond an optimal threshold, bondholders also demand higher credit spreads, causing \\(r_d\\) to surge. Eventually, the soaring costs of equity and debt—along with direct and indirect bankruptcy costs—outweigh the incremental tax shield, causing overall WACC to increase (see [Capital structure](../05-capital-structure/) and [Leverage trade-offs](../06-leverage-tradeoffs/)).

2. **A company has a market cap of $600M and debt of $400M. Cost of equity is 10%, pre-tax cost of debt is 5%, and the tax rate is 20%. Calculate WACC. What happens if the corporate tax rate increases to 30%?**  
   Answer:  
   Total Capital \\(V = 600 + 400 = \$1,000\text{M}\\).  
   Equity weight \\(w_e = 0.60\\), Debt weight \\(w_d = 0.40\\).  
   After-tax cost of debt \\(= 5\% \times (1 - 0.20) = 4.0\%\\).  

\\[
\text{WACC} = (0.60 \times 10\%) + (0.40 \times 4.0\%) = 6.0\% + 1.6\% = 7.6\%
\\]

   If the tax rate increases to 30%, the interest tax shield expands: after-tax cost of debt drops to \\(5\% \times (1 - 0.30) = 3.5\%\\).  

\\[
\text{New WACC} = (0.60 \times 10\%) + (0.40 \times 3.5\%) = 6.0\% + 1.4\% = 7.4\%
\\]

   Higher corporate tax rates make debt tax deductibility more valuable, lowering WACC (assuming pretax rates and leverage stay fixed).

3. **An analyst uses the historical bond coupon rate (8%) instead of current yield-to-maturity (4%) in WACC because 'that is what the company actually pays each quarter.' Why is this an error?**  
   Answer: The coupon rate is a sunk historical contractual obligation set when the bond was issued years ago. WACC is a forward-looking opportunity cost of capital for discounting future cash flows. If the company were to raise marginal capital today or refinance, it would borrow at the prevailing market YTM (4%). Using the 8% coupon falsely inflates WACC, artificially depressing the company’s DCF valuation.

4. **Should a corporate conglomerate use its company-wide WACC (8%) to evaluate a speculative AI robotics project?**  
   Answer: No. A company-wide WACC reflects the average risk of existing operational assets. The discount rate must reflect the *risk of the project*, not the risk of the sponsoring firm. Evaluating a high-risk venture at an artificially low corporate WACC leads to over-investing in value-destroying risky projects (accepting negative NPV projects), while evaluating low-risk projects at corporate WACC rejects value-creating safe investments. The project should be discounted at an industry-pure-play hurdle rate.

## Watch

- [Session 11: Costs of Debt and Capital](https://www.youtube.com/watch?v=-7aLvhVuPH0) — Prof. Aswath Damodaran (NYU Stern). Detailed walk through debt ratings, synthetic spreads, equity weights, and WACC calculations.
- [Session 6: Cost of Debt and Capital](https://www.youtube.com/watch?v=N_FH89DCdGs) — Prof. Aswath Damodaran (NYU Stern). Blending financing sources into a single cost of capital framework.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 9: "Risk and the Cost of Capital".
- Damodaran, Aswath, *Applied Corporate Finance*, Chapter 7: "Financing Details: Determining the Capital Structure".
