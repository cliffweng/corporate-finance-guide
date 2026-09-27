---
title: "14. Interview patterns"
layout: default
nav_order: 15
---

# Corporate finance interview patterns
{: .no_toc }

*~10 min read*

**🎯 Interview frequent**

## Why it matters

Investment banking, corporate development, and private equity technical interviews recycle a small set of canonical case structures: walk me through a DCF, trace an accounting change across the three financial statements, evaluate a capital structure recapitalization, or perform mental accretion/dilution math. Mastering these patterns allows you to deliver structured, confident, and mathematically bulletproof responses under pressure. This page integrates the entire curriculum—from [TVM](../01-time-value-of-money-refresh/) and [WACC](../04-wacc/) to [FCF](../08-free-cash-flow/), [EV](../09-enterprise-vs-equity-value/), and [M&A](../13-ma-intro/)—into actionable interview frameworks.

## Core concepts

- **Pattern A: The End-to-End DCF Walkthrough (The 5-Step Architecture):**
  1. **Project Unlevered Free Cash Flows (FCFF):** Forecast operational performance over a 5- to 10-year explicit horizon: \\(\text{FCFF} = \text{EBIT}(1 - t) + \text{D\&A} - \text{CapEx} - \Delta\text{NWC}\\).
  2. **Calculate WACC:** Blend the cost of equity (via [CAPM](../03-capm-cost-of-equity/)) and after-tax cost of debt using market value weights.
  3. **Estimate Terminal Value (TV):** Capture all cash flows beyond the projection horizon using either the **Gordon Growth Method** (\\(\text{TV}\_n = \frac{\text{FCFF}\_{n+1}}{\text{WACC} - g}\\)) or the **Exit Multiple Method** (\\(\text{TV}\_n = \text{EBITDA}\_n \times \text{Multiple}\\)).
  4. **Discount to Enterprise Value:** Discount explicit FCFF and Terminal Value back to \\(t=0\\) using WACC (often applying the mid-year convention).
  5. **Bridge to Equity Value and Per-Share Price:** Add cash, subtract net debt, preferred equity, and minority interest. Divide diluted equity value by total diluted shares.
- **Pattern B: The Three-Statement Accounting Walkthrough:**
  Always structure your answer in three sequential phases:
  1. **Income Statement:** State change in operating profit, tax impact, and final change in Net Income.
  2. **Cash Flow Statement:** Start with Net Income at the top of Cash Flow from Operations, make non-cash add-backs, factor in working capital / CapEx, and state the net change in cash.
  3. **Balance Sheet:** Adjust Cash on the asset side, update PP&E / working capital, and balance against Retained Earnings (via Net Income) and debt liabilities.
- **Pattern C: Fast M&A Mental Math:**
  Compare the target's earnings yield against the acquirer's after-tax cost of consideration:
  - If \\(\frac{1}{(P/E)\_{\text{target}}} > \text{After-Tax Cost of Financing} \implies\\) **Accretive**.
  - Financing costs: Cash \\(= r\_{\text{cash}}(1 - t)\\); Debt \\(= r\_d(1 - t)\\); Stock \\(= \frac{1}{(P/E)\_{\text{acquirer}}}\\).
- **Pattern D: The Valuation Football Field Hierarchy:**
  Valuation methodologies typically yield values in the following order (from highest to lowest):
  1. **Precedent Transactions:** Highest (includes 20%–30% control premium and expected synergies).
  2. **DCF Analysis:** High to variable (management forecasts often carry optimistic growth assumptions).
  3. **Public Trading Comparables:** Baseline market valuation (liquid, minority interest without control premium).
  4. **LBO Floor Valuation:** Lowest (financial sponsors constrain their purchase price to satisfy a strict 20%+ target IRR hurdle).

## Mental model

```
  STEP 1: Explicit FCF (Years 1-5)         STEP 3: Terminal Value (Year 5+)
  [ FCFF_1 ] [ FCFF_2 ] ... [ FCFF_5 ]      TV_5 = FCFF_6 / (WACC - g)
       |          |              |                      |
       +----------+--------------+----------------------+
                                 |
                                 v  STEP 2 & 4: Discount at WACC
                      [ ENTERPRISE VALUE (EV) ]
                                 |
                                 v  STEP 5: Balance Sheet Bridge
                      + Cash & Non-Operating Assets
                      - Total Debt
                      - Preferred Stock
                      - Non-controlling Interest
                      ====================================
                      = EQUITY VALUE
                                 |
                                 v  Divide by Diluted Shares (TSM)
                      = INTRINSIC PRICE PER SHARE
```

Deliver your answers like a partner delivering an executive summary: headline conclusion first, structured roadmap second, clean math third.

## Interview questions

1. **Walk me through a DCF from revenue down to per-share intrinsic value in 90 seconds.**  
   Answer:  
   "A DCF values a business based on the present value of its future cash flows. First, I project Unlevered Free Cash Flow over a 5- to 10-year period: start with EBIT, multiply by \\((1 - \text{Tax Rate})\\) to get NOPAT, add back Depreciation & Amortization, subtract Capital Expenditures, and subtract the Change in Net Working Capital.  
   Second, I determine the discount rate by calculating WACC, blending the cost of equity from CAPM and after-tax cost of debt using market value weights.  
   Third, I calculate the Terminal Value at the end of the projection period using either the Gordon Growth method with a conservative long-term GDP growth rate or an Exit Multiple based on comparable companies.  
   Fourth, I discount both the interim projected cash flows and the Terminal Value back to the present day using WACC to determine Enterprise Value.  
   Finally, I bridge from Enterprise Value to Equity Value by adding cash and subtracting total debt, preferred equity, and minority interest. Dividing this equity value by diluted shares gives the intrinsic value per share."

2. **Walk me through the three statements if Depreciation increases by $10. Assume a 20% corporate tax rate.**  
   Answer:  
   - **Income Statement:** Operating Income (EBIT) decreases by $10. At a 20% tax rate, taxes decrease by $2, so Net Income declines by **$8**.  
   - **Cash Flow Statement:** Net Income at the top of Cash from Operations starts down $8. We add back the non-cash $10 depreciation expense. Net cash flow increases by **+$2** (the tax savings from the depreciation tax shield).  
   - **Balance Sheet:** On the Asset side, Cash increases by +$2, but Net PP&E decreases by -$10, so total assets decline by **-$8**. On the Liabilities and Equity side, no liabilities change, and Retained Earnings falls by **-$8** due to the drop in Net Income. Both sides balance at -$8.

3. **A company buys a $100 machine financed with $50 of cash and $50 of debt. In Year 1, the machine depreciates by $20, and interest expense on the debt is $5 (paid in cash). At a 20% tax rate, walk through Year 1 on the three statements.**  
   Answer:  
   - **Income Statement:** Operating income drops by $20 (depreciation). Pre-tax income drops by $25 ($20 D&A + $5 interest). Taxes decrease by \\(20\% \times \$25 = \$5\\). Net Income falls by **-$20**.  
   - **Cash Flow Statement:** Net Income starts at -$20. Add back $20 non-cash depreciation. Cash from operations is **$0**. No investing activities. Cash from financing is $0. Net change in cash is **$0**.  
   - **Balance Sheet:** Assets: Cash is unchanged ($0), PP&E declines by -$20 due to depreciation; total assets are **-$20**. Liabilities & Equity: Debt remains $50 ($0 change), Retained Earnings drops by **-$20** (via Net Income). Both sides balance at -$20.

4. **How do you cross-check Terminal Value between the Gordon Growth method and the Exit Multiple method?**  
   Answer: You back out the implied metric of each method. If you calculate Terminal Value using the Exit Multiple method (e.g., 10x EV / EBITDA), set that resulting dollar figure equal to the Gordon Growth equation \\(\frac{\text{FCFF}\_{n+1}}{\text{WACC} - g}\\) and solve for the implied perpetual growth rate \\(g\\). If the implied growth rate exceeds historical long-term GDP growth (e.g., >3%), the exit multiple is too aggressive. Conversely, if you use Gordon Growth with a 2% rate, divide the resulting Terminal Value by projected Year \\(n\\) EBITDA to ensure the implied exit multiple aligns with historical industry trading multiples.

5. **Why does an LBO valuation typically establish the floor of the valuation football field?**  
   Answer: Private equity sponsors are strictly financial buyers who typically target a 20%–25% hurdle IRR and carry no operational synergies with the target (unlike strategic acquirers who can justify paying control premiums for cost and revenue synergies). Because the financial sponsor’s purchase price is constrained by the debt capacity of the target and the strict required equity return, the maximum price a PE firm can pay while hitting its return hurdle is almost always lower than what a strategic acquirer or DCF model suggests.

## Watch

- [Session 1: Introduction to Valuation](https://www.youtube.com/watch?v=znmQ7oMiQrM) — Prof. Aswath Damodaran (NYU Stern). The philosophy of valuation, biases, and structural valuation methods.
- [Session 9: Terminal Value](https://www.youtube.com/watch?v=83yR6EFEl5Y) — Prof. Aswath Damodaran (NYU Stern). Mechanics of terminal value, perpetual growth constraints, and common pitfalls.
- [Session 25: Closing Thoughts](https://www.youtube.com/watch?v=Q_8rnowvoYw) — Prof. Aswath Damodaran (NYU Stern). Synthesis of corporate finance, investment decisions, and capital literacy.

## Further reading

- Rosenbaum, Joshua, & Pearl, Joshua, *Investment Banking: Valuation, LBOs, M&A, and IPOs*, Chapter 3: "Discounted Cash Flow Analysis".
- Damodaran, Aswath, *Investment Valuation*, Chapter 12: "Closure in Valuation: Estimating Terminal Value".
