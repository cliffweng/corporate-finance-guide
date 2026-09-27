---
title: "09. Enterprise vs. equity value"
layout: default
nav_order: 10
---

# Enterprise value vs. equity value
{: .no_toc }

*~10 min read*

**🎯 Interview frequent**

## Why it matters

The relationship between Enterprise Value (EV) and Equity Value is the bedrock of corporate finance, investment banking valuation, and M&A deal structuring. Enterprise Value represents the total economic value of a company’s core operating assets, independent of its capital structure. Equity Value (market capitalization) represents the market value of the residual claim belonging exclusively to common shareholders. In technical interviews, failing to correctly bridge between EV and Equity Value, or mixing enterprise metrics with equity metrics in multiples, is an immediate disqualifier.

## Core concepts

- **Enterprise Value (EV):** The total value of the firm's core operating business available to **all financial claimants** (debt lenders, preferred stockholders, common equity holders).
  - **The Classic Bridge Formula:**

\\[
\text{EV} = \text{Equity Value} + \text{Total Debt} + \text{Preferred Stock} + \text{Non-controlling Interest} - \text{Cash \& Equivalents}
\\]

  Or expressed via Net Debt:

\\[
\text{EV} = \text{Equity Value} + \text{Net Debt} + \text{Preferred Stock} + \text{Non-controlling Interest}
\\]

  Where \\(\text{Net Debt} = \text{Total Debt} - \text{Cash \& Equivalents}\\).
- **Equity Value (Market Cap):**

\\[
\text{Equity Value} = \text{Diluted Shares Outstanding} \times \text{Current Share Price}
\\]

  Diluted shares must account for in-the-money stock options, warrants, and restricted stock units (RSUs) using the **Treasury Stock Method (TSM)**.
- **Why Cash is Subtracted:**
  1. **Non-Operating Asset:** Enterprise Value measures the value of the firm’s core productive, operating business. Cash is an uninvested, non-operating asset sitting on the balance sheet.
  2. **Acquisition Mechanics:** If an acquirer buys a company, they inherit the target's cash balance, which can immediately be used to pay off existing debt or partially fund the purchase price, lowering the net cash cost of acquiring the operating assets.
- **Why Non-controlling (Minority) Interest is Added:**
  Under GAAP/IFRS, if a parent company owns more than 50% of a subsidiary, it must **consolidate 100%** of the subsidiary's financial statements onto its own income statement (100% of Revenue, Operating Expenses, and EBITDA). However, the parent company's stock price and market capitalization reflect only its proportional ownership stake. To ensure valuation ratios like \\(\text{EV} / \text{EBITDA}\\) compare apples to apples, the value of the portion of the subsidiary the parent does *not* own (the minority interest) must be added to Enterprise Value.
- **Why Preferred Stock is Added:**
  Preferred stock carries senior priority over common stock and pays contractual dividends. Like debt, it represents a senior claim on corporate assets that an acquirer must assume or refinance.
- **Other Bridge Line Items:**
  - **+ Capital Leases (and Operating Leases under IFRS 16 / ASC 842):** Financial obligations to make lease payments treated as debt equivalents.
  - **+ Unfunded Pension Obligations:** Long-term legal liabilities owed to retired employees.
  - **- Equity Investments in Unconsolidated Affiliates:** Non-operating minority holdings (20%–50% ownership) whose earnings are recorded below operating profit.
- **The Golden Rule of Multiples Matching:**
  - **Enterprise Metrics:** Compare Enterprise Value to income statement lines *before* interest expense has been deducted (\\(\text{EV} / \text{Revenue}\\), \\(\text{EV} / \text{EBITDA}\\), \\(\text{EV} / \text{EBIT}\\), \\(\text{EV} / \text{FCFF}\\)).
  - **Equity Metrics:** Compare Equity Value to income statement lines *after* interest expense and preferred dividends have been deducted (\\(\text{P} / \text{E}\\), \\(\text{Price} / \text{Book}\\), \\(\text{Equity Value} / \text{FCFE}\\)).

## Mental model

```
             ASSET SIDE                               CLAIMS SIDE
  +--------------------------------+        +--------------------------------+
  |                                |        | Common Equity Value            |
  |                                |        | (Share Price x Diluted Shares) |
  |   Operating Assets             |        +--------------------------------+
  |   (Enterprise Value)           |        | Total Debt (Short + Long-term) |
  |                                |        +--------------------------------+
  |                                |        | Preferred Stock                |
  +--------------------------------+        +--------------------------------+
  | Cash & Non-Operating Assets    |        | Non-controlling Interest       |
  +--------------------------------+        +--------------------------------+
```

Think of buying a house: the purchase price of the physical property and structure is the **Enterprise Value**. If you take on a mortgage for $400k and put down $100k of your own money, your personal equity is $100k (**Equity Value**). If the seller leaves $20k in cash on the kitchen counter, your net cost to acquire the property is reduced by $20k.

## Interview questions

1. **Walk me through the bridge from Equity Value to Enterprise Value. Why is each item added or subtracted?**  
   Answer: Start with Equity Value (diluted share count \\(\times\\) share price). Add Total Debt (both short-term and long-term), because debt holders have senior claims on firm cash flows that an acquirer must assume. Add Preferred Stock, which is senior to common equity and carries a fixed dividend claim. Add Non-controlling Interest, because 100% of the subsidiary's operational metrics are consolidated on the income statement, requiring the matching non-owned equity value to be included in EV. Finally, subtract Cash and Cash Equivalents, because cash is a non-operating asset that an acquirer can use to immediately pay down debt or offset the purchase price.

2. **Can Enterprise Value be negative? What does that indicate about a company?**  
   Answer: Yes. A company has a negative Enterprise Value when its cash and cash equivalents exceed its total market capitalization plus outstanding debt (\\(\text{Cash} > \text{Equity Value} + \text{Debt}\\)). This typically happens to distressed biotechnology firms whose clinical trials have failed, or declining technology companies burning cash. It implies that the market values the company's core operating business at less than zero—the market expects management to incinerate the remaining cash pile on loss-making operations.

3. **A company has 1,000 common shares trading at $20 each. It also has 200 employee stock options with a strike price of $10. Using the Treasury Stock Method (TSM), calculate diluted equity value.**  
   Answer:  
   - All 200 options are in-the-money (\\(\$10 < \$20\\)), so they will be exercised.  
   - Exercising the options brings cash proceeds of \\(200 \times \$10 = \$2,000\\) to the company.  
   - Under TSM, the company uses this $2,000 of cash to repurchase shares at the current market price of $20: \\(\$2,000 / \$20 = 100\text{ shares repurchased}\\).  
   - Net new diluted shares issued: \\(200 - 100 = 100\text{ shares}\\).  
   - Total diluted share count: \\(1,000 + 100 = 1,100\text{ shares}\\).  
   - Diluted Equity Value: \\(1,100 \times \$20 = \$22,000\\).

4. **If a company issues $100M of new debt and leaves the proceeds in its checking account as cash, what happens to Equity Value and Enterprise Value?**  
   Answer:  
   - **Equity Value:** Unchanged ($0 change) because the new cash asset is exactly offset by the new debt liability; shareholder equity is unaffected.  
   - **Enterprise Value:** Unchanged ($0 change) because Enterprise Value formula adds Debt (+$100M) and subtracts Cash (-$100M), leaving Net Debt and EV identical. EV measures core operating assets, and holding uninvested cash does not change the earning power of the core operations.

5. **Why is EV / Net Income an invalid valuation multiple?**  
   Answer: It violates the fundamental matching principle. The numerator (Enterprise Value) reflects the total value of operating assets available to *all* capital providers (debt and equity). The denominator (Net Income) is an equity-only metric: interest expense has already been deducted, meaning debt holders have already been paid. Comparing all-capital value to equity-only profit creates an apples-to-oranges distortion across different capital structures. The correct metrics are \\(\text{EV} / \text{EBITDA}\\) or \\(\text{Price} / \text{Earnings}\\).

## Watch

- [Session 2: Intrinsic Value - Foundation](https://www.youtube.com/watch?v=8vYQpWXQ5hE) — Prof. Aswath Damodaran (NYU Stern). The firm vs. equity valuation divide and Enterprise Value definitions.
- [Session 11: Loose Ends in Valuation](https://www.youtube.com/watch?v=C5ZDAEqQkvA) — Prof. Aswath Damodaran (NYU Stern). Cash adjustments, cross holdings, minority interest, and employee stock options.
- [Session 25: Valuation - The Last Frontier!](https://www.youtube.com/watch?v=XxdjBiF0bVc) — Prof. Aswath Damodaran (NYU Stern). Reconciling operating asset value with equity value per share.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 4: "Valuing Common Stocks".
- Damodaran, Aswath, *Investment Valuation*, Chapter 16: "Firm Valuation: Cost of Capital and APV Approaches".
