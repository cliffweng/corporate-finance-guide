---
title: "13. M&A intro"
layout: default
nav_order: 14
---

# Mergers and acquisitions fundamentals
{: .no_toc }

*~10 min read*

**Interview occasional**

## Why it matters

Mergers and acquisitions (M&A) represent the most consequential, high-stakes capital allocation decisions a corporate board can make. A major transaction can double a company's market footprint overnight or destroy billions in shareholder value through overpayment and flawed integration. In investment banking M&A and corporate development interviews, analysts are expected to evaluate deal economics fluently: strategic rationale, consideration mix (cash vs. debt vs. stock), Goodwill creation, and mental-math accretion/dilution analysis.

## Core concepts

- **Strategic Motives and Synergies:**
  - **Cost Synergies ("Hard Synergies"):** Tangible operational overlap eliminated upon closing: consolidating corporate headquarters, laying off redundant administrative staff, merging sales forces, closing duplicate warehouses, and extracting volume vendor discounts. Investment bankers model cost synergies aggressively (e.g., 50%–80% realization).
  - **Revenue Synergies ("Soft Synergies"):** Cross-selling the target's products through the acquirer's global sales channels, entering new geographic markets, or bundling products. Viewed with skepticism by institutional investors and discounted heavily in transaction models.
- **Financing Structure (Cash vs. Debt vs. Stock):**
  - **Cash:** Cheapest consideration; the acquirer only forfeits after-tax interest income earned on cash balances: \\(r\_{\text{cash}}(1 - t)\\). Maximizes EPS accretion but consumes liquidity.
  - **Debt:** Moderate cost; the acquirer borrows at its after-tax marginal borrowing cost: \\(r\_d(1 - t)\\). Very accretive when interest rates are low, but raises financial leverage and distress risk.
  - **Stock:** Most expensive consideration; cost of stock is the reciprocal of the acquirer's P/E ratio (its earnings yield: \\(E/P\\)). Protects balance sheet cash and shares downside risk with the seller, but dilutes ownership.
- **Accretion / Dilution Mechanics:**
  - **Accretive Deal:** Combined Pro Forma EPS is strictly *greater* than the Acquirer’s Standalone EPS.
  - **Dilutive Deal:** Combined Pro Forma EPS is *lower* than the Acquirer’s Standalone EPS.
  - **The 100% Stock Rule of Thumb:**  
    In an all-stock transaction with no synergies, the deal is **accretive if and only if the Acquirer's P/E multiple is higher than the Target's effective purchase P/E multiple**:

\\[
(P/E)\_{\text{Acquirer}} > (P/E)\_{\text{Target}} \iff \text{Accretive}
\\]

  *Proof:* To purchase $1 of target net income, an acquirer trading at 20x P/E must issue $20 of stock, representing only $1 of its own earnings. If the target is bought at 10x P/E, that same $20 of issued stock buys $2 of target earnings. Net earnings grow faster than share count.
- **Pro Forma Net Income Formula:**

\\[
\begin{aligned}
\text{Pro Forma Net Income} &= \text{Acquirer Net Income} + \text{Target Net Income} \\
&\quad + \text{After-Tax Synergies} \\
&\quad - \text{After-Tax Incremental Interest Expense} \\
&\quad - \text{After-Tax Foregone Interest on Cash} \\
&\quad - \text{New After-Tax D\&A from Asset Write-Ups}
\end{aligned}
\\]

- **Purchase Price Allocation (PPA) and Goodwill:**
  When an acquirer purchases a target for an equity purchase price exceeding the book value of the target’s net assets, it writes up identifiable assets (tangible PP&E and intangible patents/brands) to fair market value. The unallocated residual premium is capitalized as **Goodwill**:

\\[
\text{Goodwill} = \text{Equity Purchase Price} - \text{Fair Market Value of Net Identifiable Assets}
\\]

  Under US GAAP, Goodwill is **not amortized**. Instead, it sits permanently on the balance sheet and is tested annually for impairment.

## Mental model

```
  Acquirer Net Income               Target Net Income
          \                                /
           +------------------------------+
                          |
                          v
               Pre-Deal Combined Earnings
               + After-Tax Synergies
               - After-Tax Financing Costs (Interest / Cash Foregone)
               - After-Tax Asset Write-Up D&A
               ======================================================
               = Pro Forma Combined Net Income
                               |
                               v  Divide by:
    [ Acquirer Existing Shares + New Shares Issued for Target ]
                               |
                               v
                     PRO FORMA COMBINED EPS
```

Think of an acquisition like blending two juices: if you pour in a sweeter juice (higher earnings yield / lower P/E), the combined glass becomes sweeter (accretive). If you pour in watery juice (expensive P/E), the overall concentration drops (dilutive).

## Interview questions

1. **In an all-stock transaction with zero synergies, Acquirer A trades at a P/E of 25x and acquires Target T at a purchase P/E of 15x. Is the transaction accretive or dilutive? What if it were an all-cash deal financed at 5% after-tax interest?**  
   Answer:  
   - **All-Stock Deal:** The transaction is **accretive**. Because Acquirer A has a higher P/E multiple than the purchase P/E of Target T (\\(25x > 15x\\)), the acquirer is paying with highly valued currency. The target provides an earnings yield of \\(1/15 = 6.67\%\\), while the acquirer's cost of stock is only \\(1/25 = 4.0\%\\). Earnings increase by more than the shares issued.  
   - **All-Cash Deal:** Compare the Target's earnings yield (\\(6.67\%\\)) to the after-tax cost of cash (\\(5.0\%\\)). Because \\(6.67\% > 5.0\%\\), the all-cash deal is also **accretive**.

2. **A buyer with a P/E of 10x acquires a target with a P/E of 20x in an all-stock deal. Can this transaction ever be accretive? How?**  
   Answer: Yes, if **synergies** are sufficiently large. While the baseline financial math without synergies is dilutive, if the acquirer can capture enough post-tax cost synergies or revenue cross-sell synergies, the incremental net income will outweigh the dilution from the newly issued shares.

3. **Walk me through the creation of Goodwill in an M&A transaction. Does Goodwill get amortized?**  
   Answer: Goodwill is created when the purchase price of an acquired company exceeds the fair market value of its net identifiable assets (assets minus liabilities). The acquirer revalues the target’s balance sheet to fair value (writing up tangible PP&E, software, customer contracts, and patents). The residual difference between the purchase price paid and these net fair assets is recorded as Goodwill on the asset side of the consolidated balance sheet. Under US GAAP, public companies do not amortize Goodwill; instead, it is tested at least annually for impairment. If the asset’s fair value falls below carrying value, an impairment charge is recorded on the income statement.

4. **Why do corporate buyers overwhelmingly prefer to pay with cash rather than stock if their balance sheet permits?**  
   Answer:  
   - **Cost of Capital:** Cash is almost always the cheapest form of acquisition currency (earning near risk-free post-tax returns), resulting in maximum EPS accretion.  
   - **Ownership Retention:** Cash avoids issuing new equity, preventing dilution of the existing shareholders' ownership and voting control.  
   - **Speed and Simplicity:** Cash deals require less SEC registration documentation and do not require acquirer shareholder approval votes in most jurisdictions, speeding up execution and regulatory certainty.

## Watch

- [Session 12: Acquisition Ornaments: Synergy, control & complexity](https://www.youtube.com/watch?v=QneDmX_WUyA) — Prof. Aswath Damodaran (NYU Stern). Real vs. illusory synergies, the control premium, and why most M&A fails.
- [Session 14: Equity analysis, acquisitions as projects and NPV vs IRR](https://www.youtube.com/watch?v=nGN9YNTNjuQ) — Prof. Aswath Damodaran (NYU Stern). Evaluating an acquisition as an incremental capital project.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 31: "Mergers".
- Damodaran, Aswath, *Investment Valuation*, Chapter 25: "Valuing Acquisitions and Takeovers".
