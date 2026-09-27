---
title: "06. Leverage trade-offs"
layout: default
nav_order: 7
---

# Leverage trade-offs and financial distress
{: .no_toc }

*~9 min read*

**Interview occasional**

## Why it matters

While the interest tax shield creates a clear incentive to borrow, real corporations rarely finance themselves entirely with debt. The **Static Trade-off Theory** and **Pecking Order Theory** explain how corporate treasurers and private equity sponsors balance the tax shield against the escalating probability and costs of financial distress. In restructuring, leveraged finance, and M&A interviews, understanding leverage trade-offs explains why utility companies can sustain 70% debt loads while technology companies often maintain pristine, net-cash balance sheets.

## Core concepts

- **The Trade-off Model of Firm Value:**
  \[
  V_L = V_U + PV(\text{Interest Tax Shields}) - PV(\text{Financial Distress Costs})
  \]
  - As leverage (\(D/V\)) increases from zero, the tax shield (\(t_c D\)) dominates, increasing firm value and lowering [WACC](../04-wacc/).
  - Beyond an optimal leverage threshold (\(D^*\)), the marginal probability of default multiplied by the severity of financial distress outpaces the marginal tax benefit, destroying firm value.
- **Direct vs. Indirect Costs of Financial Distress:**
  - **Direct Costs:** Court fees, restructuring attorneys, turnaround advisors, restructuring investment bankers. Typically account for 2%–5% of pre-bankruptcy enterprise value.
  - **Indirect Costs:** The economic damage caused by the mere *threat* of insolvency long before formal Chapter 11 filing. Customers refuse to purchase goods requiring long-term warranties (e.g., cars, enterprise software); suppliers tighten credit terms to Cash on Delivery (COD); top executive talent departs; management is consumed by liquidity triage rather than strategic growth. Indirect costs frequently erode 10%–25% of firm value.
- **Agency Conflicts Between Equity and Debt Holders:**
  - **Debt Overhang (Underinvestment):** When a firm is in distress, equity holders may reject positive-NPV projects if the project's gains accrue primarily to existing senior lenders rather than equity.
  - **Asset Substitution (Risk Shifting):** Distressed equity acts like an out-of-the-money call option on firm assets. Equity holders have an incentive to invest in speculative, negative-NPV gambles: if the bet succeeds, equity captures the upside; if it fails, bondholders absorb the downside ("heads I win, tails lenders lose").
  - **Free Cash Flow Discipline (Jensen Hypothesis):** Contractual debt service prevents entrenched managers from squandering excess cash flow on empire-building acquisitions or corporate perks.
- **Pecking Order Theory (Myers & Majluf, 1984):**
  Due to asymmetric information between managers and outside investors, firms do not have a rigid target leverage ratio. Instead, they finance projects following a strict hierarchy:
  1. **Internal cash / retained earnings:** Zero information asymmetry, zero flotation costs.
  2. **Debt:** Lenders have senior priority, minimizing adverse selection discount.
  3. **Equity:** Used as a last resort. Investors infer that managers only issue equity when shares are overvalued, triggering an immediate stock price drop upon announcement.

## Mental model

```
  Firm Value (V)
       ^
       |                    Optimal Debt Ratio (D*)
       |                            |
  V*   |---------------------------*  (Max Firm Value, Min WACC)
       |                         /   \
       |                        /     \--- PV of Financial Distress Costs
       |                       /       \   (Direct + Indirect + Agency)
       |   + PV(Tax Shield)   /
  V_U  |---------------------/
       |                    /  MM with taxes line
       |                   /
       |                  /
       +-----------------+------------------------------------------> Leverage (D/V)
       0%               D*                                         100%
```

Think of leverage like structural load on a bridge: steel cables allow for longer spans and tax efficiency, but loading beyond structural tolerances causes catastrophic resonance and collapse.

## Interview questions

1. **Why does a public company's stock price typically fall upon the announcement of a secondary equity offering, but often remains unchanged or rises upon a debt offering?**  
   Answer: Under the Pecking Order and asymmetric information theory, corporate managers possess superior information regarding the firm's true asset value and earnings trajectory. If managers believe their stock is undervalued, they will borrow debt rather than sell cheap equity. Announcing a primary or secondary equity offering signals to the market that management believes the stock is currently overvalued or that internal cash generation is severely constrained. Conversely, a debt issuance signals management's confidence in future cash flows to service contractual interest.

2. **Contrast the capital structure of a regulated electric utility with that of an enterprise SaaS company. Why are their debt capacities completely different?**  
   Answer: A regulated utility possesses stable, recession-resistant demand, monopolistic market positioning, predictable rate-base cash flows, and tangible collateral (power plants, transmission lines). Its probability of distress is exceptionally low, allowing it to carry heavy leverage (e.g., 60%–70% debt) to exploit tax shields. Conversely, a SaaS company has highly volatile recurring growth, few tangible liquidatable assets (intellectual property is difficult to liquidate in liquidation), and high indirect distress costs (customers will not adopt mission-critical software from a vendor that might go bust). Thus, tech firms maintain low debt or net-cash positions.

3. **What is the 'debt overhang' problem, and how do senior lenders protect themselves against it?**  
   Answer: Debt overhang occurs when a financially distressed firm identifies a project with a positive NPV, but because debt is trading at a steep discount, the project's cash inflows will merely pay down underwater debt without leaving any residual return for equity. Because equity holders control capital allocation, they will rationally refuse to inject capital, leaving value on the table. Senior lenders protect against this via negative covenants (covenants restricting debt incurrence, requiring minimum liquidity, or mandating maintenance capex) and by restructuring debt obligations out of court to align incentives.

4. **What are the key determinants of a company's debt capacity in an LBO or recapitalization?**  
   Answer:  
   - Free cash flow predictability and margin stability across economic cycles.  
   - Capital expenditure requirements (low CapEx leaves more FCF for debt amortization).  
   - Asset tangibility (collateral base for senior secured credit facilities).  
   - Cyclicality and operational leverage (fixed vs. variable cost structure).  
   - Existing debt covenant headroom and current credit rating thresholds.

## Watch

- [Session 20: Optimizing Debt Mix - APV and Peer Group Pressure](https://www.youtube.com/watch?v=-3nN_LeX2W0) — Prof. Aswath Damodaran (NYU Stern). Comparing cost of capital vs. APV approaches to sizing debt capacity.
- [Session 21: Debt Design](https://www.youtube.com/watch?v=4glb7Ze5ZuI) — Prof. Aswath Damodaran (NYU Stern). Matching debt duration, currency, and cash flow profile to firm assets.
- [Session 24: Distressed Equity as an option](https://www.youtube.com/watch?v=L2luFJSpQo8) — Prof. Aswath Damodaran (NYU Stern). Treating levered equity as an out-of-the-money call option on firm value.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 18: "How Much Should a Corporation Borrow?".
- Myers, Stewart C., & Majluf, Nicholas S. (1984), "Corporate Financing and Investment Decisions when Firms Have Information that Investors Do Not Have", *Journal of Financial Economics*.
