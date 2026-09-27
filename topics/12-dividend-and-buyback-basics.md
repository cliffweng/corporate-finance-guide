---
title: "12. Dividends & buybacks"
layout: default
nav_order: 13
---

# Dividend policy and share repurchases
{: .no_toc }

*~8 min read*

**Interview occasional**

## Why it matters

When a mature corporation generates free cash flow in excess of available positive-NPV reinvestment opportunities, the board of directors faces a fundamental capital allocation decision: should the cash be held on the balance sheet, distributed as recurring cash dividends, or deployed into share repurchases? Payout policy reflects management's long-term capital literacy, signaling posture, and governance discipline. In equity research and corporate finance interviews, understanding how buybacks impact EPS, share count, and intrinsic value without creating "accounting magic" is a critical skill.

## Core concepts

- **Modigliani-Miller Dividend Irrelevance (1961):**
  In frictionless capital markets (no taxes, no transaction costs, symmetric information), **dividend policy has zero effect on shareholder wealth or firm value**.
  - A firm's total value is determined solely by its investment policy and operating asset earnings.
  - If a firm pays no dividend, an investor desiring current income can create a "homemade dividend" by selling a fraction of their shares.
  - If a firm pays a dividend that an investor does not need, they can immediately reinvest the cash by purchasing additional shares.
- **Cash Dividends vs. Share Repurchases:**
  - **Cash Dividends:** A recurring, contractual-like cash distribution declared per share. Boards treat dividends as sticky commitments; cutting a dividend sends a severe negative distress signal to the market. On the **ex-dividend date**, the stock price drops by exactly the per-share dividend amount in a tax-neutral world.
  - **Share Repurchases (Buybacks):** Flexible, discretionary open-market repurchases or tender offers. Cash leaves the balance sheet, and shares outstanding are retired:

\\[
\text{New Shares} = \text{Old Shares} - \frac{\text{Cash Spent}}{\text{Repurchase Price}}
\\]

  Equity Value declines by the cash spent, but because share count shrinks proportionally, **per-share intrinsic value is unchanged** if shares are bought at fair value.
- **The EPS Accretion Trap:**
  Repurchasing shares reduces the share count, which mechanically increases Earnings Per Share (EPS) whenever the earnings yield of the stock exceeds the foregone interest on cash:

\\[
\text{Earnings Yield} = \frac{\text{EPS}}{P} = \frac{1}{\text{P/E}} > r_{\text{cash}}(1 - t)
\\]

  *Critical Interview Point:* **EPS accretion does NOT equal value creation.** If a board repurchases shares at $100 when their intrinsic value is only $70, management transfers wealth directly from remaining long-term shareholders to departing selling shareholders, destroying intrinsic value despite higher headline EPS.
- **Why Boards Prefer Buybacks over Dividends:**
  1. **Financial Flexibility:** Buybacks can be dialed up or paused across economic cycles without the catastrophic stock price penalty associated with a dividend cut.
  2. **Tax Efficiency:** Dividends force an immediate taxable event on all taxable shareholders. Buybacks allow investors to defer taxes until they voluntarily choose to sell, paying lower long-term capital gains rates.
  3. **Offsetting Option Dilution:** Repurchasing shares neutralizes dilution caused by executive stock-based compensation (RSUs and stock options).

## Mental model

```
  Operational Free Cash Flow
             |
             v
  [ Reinvestment in Positive-NPV Projects ] ---> If ROIC > WACC, reinvest 100%
             |
             v (Excess Cash Remaining)
  +---------------------------------------+
  | Capital Return Policy                 |
  +---------------------------------------+
        /                           \
       v                             v
  [ Cash Dividends ]            [ Share Repurchases ]
  - High commitment / sticky    - Maximum flexibility
  - Mandatory taxable event     - Tax-deferred capital gains
  - Lowers ex-dividend price    - Shrinks share count, boosts EPS
```

Paying a dividend is like taking cash out of your company’s corporate bank account and handing it to the owner: the owner now holds cash, but the company's valuation drops by that exact cash amount.

## Interview questions

1. **If a company with 10 million shares trading at $50 per share spends $50 million of cash to repurchase shares at market price, what is the stock price immediately following the buyback in an efficient market?**  
   Answer: Exactly $50 per share.  
   - Initial Market Cap: \\(10\text{M} \times \$50 = \$500\text{M}\\).  
   - Cash leaves the firm: New Market Cap \\(= \$500\text{M} - \$50\text{M} = \$450\text{M}\\).  
   - Shares repurchased: \\(\$50\text{M} / \$50 = 1\text{M shares}\\).  
   - Remaining shares: \\(10\text{M} - 1\text{M} = 9\text{M shares}\\).  
   - New Share Price: \\(\frac{\$450\text{M}}{9\text{M}} = \$50\\).  
   The remaining shareholders own a larger slice of a smaller pie, leaving per-share wealth identical.

2. **Can a company execute an EPS-accretive share repurchase that actually destroys shareholder value?**  
   Answer: Yes. Consider a company whose stock trades at a P/E of 10x (an earnings yield of \\(1/10 = 10\%\\)). It borrows debt at a 4% after-tax interest rate to repurchase shares. Because the 10% earnings yield exceeds the 4% after-tax cost of debt, EPS increases immediately. However, if the stock's intrinsic value is only $20 but management repurchases shares at $40, management is paying $2.00 of corporate cash for every $1.00 of intrinsic asset value. Furthermore, the added debt increases financial distress risk and raises WACC. The headline EPS rises, but true shareholder value is destroyed.

3. **What is the 'dividend clientele effect,' and why does it make sudden changes in dividend policy dangerous for a stock price?**  
   Answer: Different investor groups prefer different payout policies based on their tax status and liquidity needs. High-net-worth individual investors prefer low or zero dividends to defer capital gains taxes, whereas pension funds, endowments, and retirees seek steady cash yields for living expenses. Over time, an established dividend payer attracts a shareholder base optimized for regular income. If the company suddenly eliminates or slashes its dividend, the income-seeking clientele is forced to dump the stock, triggering sharp short-term selling pressure.

4. **What is a 'dividend yield trap,' and what financial ratios reveal it?**  
   Answer: A dividend yield trap occurs when an investor buys a stock with an unsustainably high dividend yield (e.g., 11%) without realizing that the high yield is driven by a collapsing stock price caused by deteriorating core fundamentals. Key ratios that reveal the trap include:  
   - **Dividend Payout Ratio:** \\(\text{Dividends Paid} / \text{Net Income} > 100\%\\) (paying out more than it earns).  
   - **FCF Dividend Coverage:** \\(\text{Dividends Paid} / \text{Free Cash Flow} > 1.0\\) (the company must borrow debt or issue equity just to sustain the dividend).  
   - **Net Debt / EBITDA:** High leverage indicates debt covenants may soon restrict dividend payments.

## Watch

- [Session 22: Dividends - First Steps](https://www.youtube.com/watch?v=sH2u90cP_Uo) — Prof. Aswath Damodaran (NYU Stern). The history of dividend policy, measuring cash returns to equity, and FCFE vs. dividends.
- [Session 23: Good & Bad Reasons for paying dividends](https://www.youtube.com/watch?v=ZKFRzS_vHx0) — Prof. Aswath Damodaran (NYU Stern). The signaling role of dividends, stock buybacks vs. dividends, and the dividend puzzle.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 16: "Payout Policy".
- Damodaran, Aswath, *Applied Corporate Finance*, Chapter 10: "The Dividend Decision".
