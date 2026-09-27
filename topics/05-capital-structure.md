---
title: "05. Capital structure"
layout: default
nav_order: 6
---

# Capital structure and Modigliani-Miller
{: .no_toc }

*~9 min read*

**🎯 Interview frequent**

## Why it matters

Capital structure refers to the specific mix of debt, equity, and hybrid instruments a corporation uses to fund its overall operations and growth. In 1958, Franco Modigliani and Merton Miller published their groundbreaking irrelevance proposition, establishing modern corporate finance theory. Understanding Modigliani-Miller (MM) is essential because it demonstrates that in frictionless markets, financial engineering cannot create economic value. Real-world corporate capital structure decisions matter *only* because of specific market frictions: corporate taxes, costs of financial distress, agency conflicts, and information asymmetry.

## Core concepts

- **Modigliani-Miller Proposition I (No Taxes, 1958):**  
  In a frictionless market (no taxes, no transaction costs, no bankruptcy penalties, equal borrowing rates for firms and individuals, symmetric information), the market value of any firm is completely independent of its capital structure:

\\[
V_L = V_U
\\]

  A firm's value is determined entirely by the earning power and systematic risk of its underlying real assets, not by how claims on those cash flows are sliced.
- **The Homemade Leverage Mechanism:**  
  If a levered firm were to trade at a premium over an identical unlevered firm, investors could sell shares in the levered firm, buy shares in the unlevered firm, and borrow on their personal margin accounts at the same rate \\(r_d\\) to replicate the exact same risk-return payoff at a lower cost. Arbitrage forces \\(V_L = V_U\\).
- **Modigliani-Miller Proposition II (No Taxes):**  
  As a company issues cheaper debt, the financial risk of common equity increases, raising the cost of equity linearly:

\\[
r_e = r_0 + \left(r_0 - r_d\right) \frac{D}{E}
\\]

  *(Where \\(r_0\\) is the unlevered cost of capital / return on assets.)*  
  The benefit of substituting cheap debt for expensive equity is exactly offset by the increase in the cost of equity. As a result, [WACC](../04-wacc/) remains completely flat.
- **MM Proposition I with Corporate Taxes (1963):**  
  Because governments allow corporations to deduct interest payments from taxable corporate income, debt creates an annual cash savings known as the **interest tax shield** (\\(t_c \cdot r_d \cdot D\\)). Discounting this perpetual tax shield at the cost of debt \\(r_d\\):

\\[
PV(\text{Tax Shield}) = \frac{t_c \cdot r_d \cdot D}{r_d} = t_c D
\\]

  Therefore, the levered firm value equals the unlevered value plus the capitalized tax shield:

\\[
V_L = V_U + t_c D
\\]

- **MM Proposition II with Corporate Taxes:**  
  With taxes, the increase in \\(r_e\\) is dampened by the tax deduction:

\\[
r_e = r_0 + \left(r_0 - r_d\right)(1 - t_c) \frac{D}{E}
\\]

  Consequently, with corporate taxes alone, WACC decreases monotonically with leverage, implying that firms should maximize debt (100% debt financing). This extreme theoretical conclusion highlights the necessity of incorporating bankruptcy costs (see [Leverage trade-offs](../06-leverage-tradeoffs/)).

## Mental model

```
  Frictionless World (MM 1958)              World With Taxes (MM 1963)
  +--------------------------------+        +--------------------------------+
  |                                |        |  Tax Shield: + t_c * D         |
  |     Operating Assets           |        +--------------------------------+
  |                                |        |                                |
  |  Total Firm Value = V_U        |        |     Operating Assets           |
  |  (Pie size is fixed)           |        |                                |
  |                                |        |  Total Firm Value = V_L > V_U  |
  +--------------------------------+        +--------------------------------+
        /                    \                    /                    \
   [ Equity ]             [ Debt ]           [ Equity ]             [ Debt ]
   Residual               Senior             Residual               Senior
```

Think of corporate earnings as a pizza. Cutting the pizza into more slices (debt vs. equity) doesn't create more food. But if the tax authority agrees to take a smaller bite whenever you cut the pizza into triangular debt slices, the remaining pizza for investors becomes bigger.

## Interview questions

1. **Explain the Modigliani-Miller theorem to a CEO in non-technical terms. Why is it often called the 'pie model'?**  
   Answer: The value of a business is determined by its ability to generate operational cash flows from its factories, software, and customers—the size of the pie. Slicing that pie into debt claims (contractual interest) and equity claims (residual dividends) does not make the pie any larger. An investor can recreate any capital mix on their own. Therefore, financing decisions do not create value unless they reduce taxes paid to the government or resolve real-world market frictions.

2. **If MM Proposition II proves that debt is cheaper than equity but raises the cost of equity, why doesn't WACC change in a zero-tax world?**  
   Answer: Although debt is cheaper than equity because lenders have senior claims on assets, adding debt introduces financial risk to common stockholders. To compensate for bearing this leverage risk, equity holders demand a higher expected return (\\(r_e\\)). The mathematical increase in \\(r_e\\) multiplied by equity weight \\((E/V)\\) exactly neutralizes the lower cost of debt \\(r_d\\) multiplied by debt weight \\((D/V)\\). The weighted average cost of capital remains invariant at \\(r_0\\).

3. **Under MM with corporate taxes, what is the theoretical optimal capital structure? Why don't real firms follow this advice?**  
   Answer: Under MM with corporate taxes alone, the optimal capital structure is 100% debt, because every incremental dollar of debt adds \\(t_c\\) dollars of present value via interest tax deductibility. Real-world corporations do not do this because MM with taxes ignores the offsetting costs of financial distress: default risk, lost customers, employee departures, legal fees, agency costs of debt, and debt covenants. The static trade-off theory balances the tax shield against these distress costs.

4. **What is 'homemade leverage,' and how would an investor exploit a mispriced levered company?**  
   Answer: Homemade leverage is the ability of individual investors to borrow margin debt on personal accounts to replicate corporate debt. If Levered Firm L trades at a market value greater than identical Unlevered Firm U (\\(V_L > V_U\\)), an investor holding shares in L can sell them, purchase proportional equity in U, and personally borrow an identical amount of debt. The investor generates the exact same net cash flow stream with lower total invested capital, pocketing an immediate arbitrage profit.

## Watch

- [Session 17: The Debt/Equity Trade off](https://www.youtube.com/watch?v=wk6yec9pGAs) — Prof. Aswath Damodaran (NYU Stern). The transition from MM irrelevance to tax benefits and real-world frictions.
- [Session 18: Optimizing the Debt Mix](https://www.youtube.com/watch?v=uF3JdUS57-s) — Prof. Aswath Damodaran (NYU Stern). Walking through the cost of capital approach to finding optimal leverage.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 17: "Does Debt Policy Matter?".
- Damodaran, Aswath, *Applied Corporate Finance*, Chapter 7: "Capital Structure: The Choices and the Trade-off".
