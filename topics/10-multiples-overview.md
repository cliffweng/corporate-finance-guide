---
title: "10. Multiples overview"
layout: default
nav_order: 11
---

# Valuation multiples overview
{: .no_toc }

*~9 min read*

**🎯 Interview frequent**

## Why it matters

While a Discounted Cash Flow (DCF) model assesses the intrinsic value of a company based on projected cash flows, relative valuation (comparable company analysis and precedent transactions) reflects the price the market is actually paying today. Valuation multiples synthesize operational performance, growth expectations, and risk into a single standardized ratio. In investment banking pitch books, fairness opinions, and private equity buyout analyses, multiples provide the market reality check against intrinsic models. Interviewers test your ability to match the correct multiple to the correct industry and diagnose how leverage and accounting policies distort them.

## Core concepts

- **Enterprise-Level Multiples (Capital Structure Neutral):**
  - **EV / Revenue:** Used for early-stage, fast-growing software or biotech companies that have not yet achieved positive profitability. Revenue is difficult to manipulate via accounting discretion, but ignores cost structure and unit economics entirely.
  - **EV / EBITDA:** The primary workhorse multiple in investment banking and leveraged buyouts. Because EBITDA is calculated before interest expense, tax rates, and non-cash depreciation policies, EV / EBITDA allows comparison of companies with divergent capital structures and differing asset ages.
  - **EV / EBIT:** Superior to EV / EBITDA for **capital-intensive industries** (e.g., manufacturing, airlines, heavy equipment). In these sectors, equipment wears out rapidly, and Capital Expenditures (CapEx) represent a mandatory ongoing cash drain. Depreciation reflects that economic cost; EV / EBIT penalizes firms with heavy capital replacement requirements, whereas EV / EBITDA ignores them.
- **Equity-Level Multiples (Post-Debt / Levered):**
  - **P / E (Price-to-Earnings Ratio):**

\\[
\frac{P}{E} = \frac{\text{Equity Value}}{\text{Net Income}} = \frac{\text{Share Price}}{\text{Earnings Per Share (EPS)}}
\\]

  The most widely cited multiple among equity research analysts. Unlike EV multiples, P / E is heavily influenced by financial leverage: taking on debt introduces interest expense, shrinking net income and altering the denominator.
  - **P / B (Price-to-Book Value):**

\\[
\frac{P}{B} = \frac{\text{Equity Value}}{\text{Book Value of Equity}}
\\]

  Essential for commercial banks, insurance companies, and balance-sheet-heavy financial institutions whose assets consist primarily of liquid loans and securities marked near fair value.
- **The First-Principles Drivers of Multiples:**
  Every multiple can be derived mathematically from the Gordon Growth model. For the P/E ratio, with dividend payout ratio \\((1 - b)\\), cost of equity \\(r\_e\\), and growth rate \\(g\\):

\\[
\frac{P\_0}{E\_1} = \frac{1 - b}{r\_e - g}
\\]

  Similarly, EV / EBITDA is fundamentally driven by:

\\[
\frac{\text{EV}}{\text{EBITDA}} \propto \frac{(1 - t) \cdot (1 - \text{Reinvestment Rate})}{\text{WACC} - g}
\\]

  A multiple is never "cheap" or "expensive" in isolation: high multiples reflect superior expected growth (\\(g\\)), higher returns on invested capital (lower required reinvestment), or lower risk ([WACC](../04-wacc/)).
- **Public Comps vs. Precedent Transactions:**
  - **Public Trading Comps:** Reflect current liquid, minority-stake market valuations without any change of control.
  - **Precedent Transactions:** Reflect historical acquisitions of entire businesses. They typically trade at a **20%–30% premium** (the "control premium") over undisturbed trading prices because the acquirer pays for the right to control capital allocation, replace management, and realize operational synergies.

## Mental model

```
  INCOME STATEMENT LEVEL                  CORRESPONDING MULTIPLES
  ======================================================================
  Revenue                                 EV / Revenue
     - Operating Expenses
  ----------------------------------------------------------------------
  EBITDA                                  EV / EBITDA
     - Depreciation & Amortization
  ----------------------------------------------------------------------
  Operating Income (EBIT)                 EV / EBIT
     - Interest Expense (Financing)
     - Taxes
  ----------------------------------------------------------------------
  Net Income (Equity Holders Only)        P / E, Equity Value / Net Income
```

Think of a multiple as an inverted capitalization rate: an 8.0x EV / EBITDA multiple implies the market is pricing the operating stream at a \\(\frac{1}{8.0} = 12.5\%\\) gross cash yield before taxes and reinvestment.

## Interview questions

1. **Why is EV / EBIT preferred over EV / EBITDA when valuing a steel manufacturer or commercial airline?**  
   Answer: Both steel manufacturing and commercial airlines are heavily capital-intensive businesses requiring billions in ongoing CapEx to maintain and replace aging blast furnaces, rolling mills, and aircraft. Depreciation is a real proxy for the economic depletion of these productive physical assets. EV / EBITDA ignores depreciation entirely, making companies that run old, nearly depreciated equipment look artificially identical to firms that have invested heavily in modern, efficient assets. EV / EBIT incorporates this depreciation burden, providing a truer comparison of operational cash profitability.

2. **Company A and Company B have identical operating revenues, cost structures, and EBITDA. Company A has zero debt, while Company B is 70% debt-financed. How will their EV / EBITDA and P / E multiples compare?**  
   Answer:  
   - **EV / EBITDA:** The multiples should be identical (or very close), because Enterprise Value and EBITDA are both capital-structure neutral. EV captures the total operating value regardless of debt, and EBITDA is measured before interest expense.  
   - **P / E:** Company B’s P / E ratio will likely be different. Company B incurs substantial interest expense, resulting in significantly lower Net Income. Depending on whether the interest tax shield benefit outweighs the increased cost of equity due to financial risk, Company B's P / E will reflect this leverage distortion.

3. **Why do Precedent Transactions almost always produce higher valuation multiples than Public Trading Comparables for the same target?**  
   Answer: In a precedent transaction, the strategic or financial acquirer is purchasing 100% control of the company rather than a minority public share. The buyer pays a **control premium** (historically 20%–30% above the undisturbed share price) for the legal right to control the board, redirect free cash flows, optimize capital structure, shut down redundant headquarters, and capture revenue and cost synergies. Public trading comps reflect frictionless, liquid minority purchases with zero control.

4. **If two companies have the exact same expected earnings growth and risk profile, why might Company X trade at 20x P/E while Company Y trades at 12x P/E?**  
   Answer: Look at their **Return on Equity (ROE)** and capital reinvestment efficiency. By the formula \\(\frac{P}{E} = \frac{1 - g/\text{ROE}}{r\_e - g}\\), if Company X has an ROE of 30% while Company Y has an ROE of 12%, Company X only needs to reinvest a small fraction of its earnings to generate the same growth rate \\(g\\), allowing it to pay out the rest in dividends or buybacks. Company Y must retain almost all its net earnings just to keep up. Investors pay a premium multiple for capital-light, high-return businesses.

5. **When is Price-to-Book (P/B) the primary valuation multiple, and when is it completely useless?**  
   Answer: P/B is the gold standard for valuing commercial banks, insurance carriers, and investment trusts. For these institutions, the balance sheet consists of liquid financial assets, government bonds, and loans marked close to fair market value, and regulatory capital requirements are tied directly to book equity. Conversely, P/B is useless for asset-light software, consulting, and consumer brand companies (e.g., Apple, Microsoft, Nike), where the true productive assets—proprietary software, brand equity, intellectual property—are never capitalized on the balance sheet under GAAP.

## Watch

- [Session 14: Relative Valuation - First Principles](https://www.youtube.com/watch?v=WDZwqSierZ4) — Prof. Aswath Damodaran (NYU Stern). The foundation of relative multiples, four basic steps in multiple analysis.
- [Session 15: PE Ratios](https://www.youtube.com/watch?v=42iyR6Geqiw) — Prof. Aswath Damodaran (NYU Stern). Mathematical derivation of P/E, growth vs. risk tradeoffs, PEG ratios.
- [Session 16: Other Earnings Multiples](https://www.youtube.com/watch?v=xI-KTlxfNDU) — Prof. Aswath Damodaran (NYU Stern). EV/EBITDA, EV/EBIT, and enterprise value fundamentals.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 4: "Valuing Common Stocks".
- Damodaran, Aswath, *Investment Valuation*, Chapter 17: "Fundamental Principles of Relative Valuation".
