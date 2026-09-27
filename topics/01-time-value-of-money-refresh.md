---
title: "01. TVM refresh"
layout: default
nav_order: 2
---

# Time value of money refresh
{: .no_toc }

*~8 min read*

**🎯 Interview frequent**

## Why it matters

Every valuation model in corporate finance—from a multi-stage Discounted Cash Flow (DCF) to bond pricing, synergy modeling, and capital budgeting—rests on the time value of money (TVM). A dollar today is worth more than a dollar tomorrow due to opportunity cost, inflation, and risk. In investment banking and corporate finance interviews, interviewers test TVM to see whether you truly understand discounting mechanics, compounding conventions, and cash flow timing, or whether you merely plug numbers into memorized templates.

## Core concepts

- **Present Value (\(PV\)) and Future Value (\(FV\)):** Cash flows occurring at different points in time cannot be compared directly. For a single cash flow \(C_t\) received at period \(t\) discounted at rate \(r\):
  \[
  PV = \frac{C_t}{(1 + r)^t} = C_t (1 + r)^{-t}, \quad FV_t = PV \cdot (1 + r)^t
  \]
- **Compounding Frequency & Effective Annual Rate (\(EAR\)):** If a nominal annual interest rate \(r_{\text{nom}}\) compounds \(m\) times per year, the effective annual yield is higher:
  \[
  EAR = \left(1 + \frac{r_{\text{nom}}}{m}\right)^m - 1
  \]
  As \(m \to \infty\), continuous compounding yields \(EAR = e^{r_{\text{nom}}} - 1\), and \(PV = C_t e^{-r t}\). Corporate finance models traditionally operate on discrete periodic discounting (annual or quarterly).
- **Annuities:** A stream of equal cash flows \(C\) paid across \(n\) periods:
  \[
  PV_{\text{annuity}} = C \sum_{t=1}^n \frac{1}{(1+r)^t} = \frac{C}{r} \left[1 - \frac{1}{(1 + r)^n}\right]
  \]
  If payments occur at the beginning of each period (annuity due), multiply the result by \((1 + r)\).
- **Perpetuities:** An infinite stream of identical cash flows:
  \[
  PV_{\text{perpetuity}} = \lim_{n \to \infty} \sum_{t=1}^n \frac{C}{(1+r)^t} = \frac{C}{r}
  \]
- **Growing Perpetuity (Gordon Growth Formula):** A constant cash flow growing at rate \(g\) where the first payment \(C_1 = C_0(1+g)\) arrives at \(t=1\), with \(r > g\):
  \[
  PV_{\text{growing perpetuity}} = \sum_{t=1}^\infty \frac{C_0(1+g)^t}{(1+r)^t} = \frac{C_1}{r - g}
  \]
  This formula forms the mathematical foundation of Terminal Value in corporate valuation (see [Free cash flow](../08-free-cash-flow/) and [Enterprise vs. equity value](../09-enterprise-vs-equity-value/)).
- **Matching Cash Flow to Discount Rate:** Never discount equity-level cash flows (e.g., FCFE, dividends) at WACC, and never discount unlevered cash flows (FCFF) at the cost of equity. Always match the risk and claimholder profile of the numerator and denominator (see [WACC](../04-wacc/)).

## Mental model

```
  t = 0               t = 1               t = 2               t = n
    |                   |                   |                   |
    |                   v                   v                   v
    |                 [ C1 ]              [ C2 ]              [ Cn ]
    |                   |                   |                   |
    +<-- discount ------+                   |                   |
    |     / (1+r)^1                         |                   |
    +<--------- discount -------------------+                   |
    |            / (1+r)^2                                      |
    +<------------------- discount -----------------------------+
                           / (1+r)^n

    PV = sum_{t=1}^n [ C_t / (1+r)^t ]
```

Discounting functions as an exchange rate across time: it translates uncertain, future claims into equivalent present certainty units based on the opportunity cost of capital.

## Interview questions

1. **How do you mathematically derive the growing perpetuity formula \(PV = C_1 / (r - g)\)? What economic assumption breaks if \(g \ge r\)?**  
   Answer: Write \(PV = \sum_{t=1}^\infty \frac{C_0(1+g)^t}{(1+r)^t} = \frac{C_0(1+g)}{1+r} \sum_{k=0}^\infty \left(\frac{1+g}{1+r}\right)^k\). Since \(r > g\), the common ratio \(x = \frac{1+g}{1+r} < 1\). The infinite geometric series sum is \(\frac{1}{1-x} = \frac{1}{1 - \frac{1+g}{1+r}} = \frac{1+r}{r-g}\). Multiplying by \(\frac{C_1}{1+r}\) yields \(PV = \frac{C_1}{r-g}\). If \(g \ge r\), the series diverges to infinity, implying the company grows faster than the overall economy indefinitely and would eventually consume all global wealth, violating economic equilibrium.

2. **Why do investment bankers use the "mid-year convention" in a DCF model, and how does it change the discount factors?**  
   Answer: In standard year-end discounting, cash flows are assumed to arrive in a single lump sum on the 365th day of each year (\(t = 1, 2, 3, \dots\)). In reality, businesses generate cash continuously throughout all twelve months. The mid-year convention assumes cash arrives evenly across the period, discounting at \(t = 0.5, 1.5, 2.5, \dots\):
   \[
   PV = \frac{C_t}{(1 + r)^{t - 0.5}}
   \]
   This increases the present value by approximately \((1 + r)^{0.5}\) (roughly half a year of compounding interest), better reflecting real-world cash generation.

3. **A company generates $100M of unlevered free cash flow next year, with an estimated cost of capital \(r = 9\%\) and long-term sustainable growth \(g = 2\%\). Calculate its terminal value today. What happens if expected inflation pushes \(r\) to 10% and \(g\) to 3%?**  
   Answer: Base case: \(PV = \frac{100}{0.09 - 0.02} = \frac{100}{0.07} \approx \$1,428.57\text{M}\). If both \(r\) and \(g\) increase by 100 bps in lockstep (spread \(r - g = 7\%\) remains constant), the denominator is unchanged, but nominal cash flows may adjust. If \(C_1\) remains $100M, \(PV = \frac{100}{0.10 - 0.03} = \$1,428.57\text{M}\). However, if higher inflation forces higher reinvestment (lower cash conversion) or widens the risk premium, the spread \(r - g\) expands, compressing valuation.

4. **A commercial bank advertises a loan with 12% stated interest compounded monthly. Another quotes 12.2% compounded annually. Which offers a lower effective borrowing cost?**  
   Answer: Calculate the EAR for the first loan: \(EAR = \left(1 + \frac{0.12}{12}\right)^{12} - 1 = (1.01)^{12} - 1 \approx 12.68\%\). The second loan has an EAR of \(12.20\%\). The second bank offers the cheaper financing despite a higher stated nominal APR because annual compounding avoids monthly interest compounding on unpaid interest.

## Watch

- [Time value of money](https://www.youtube.com/watch?v=733mgqrzNKs) — Khan Academy. Core intuition behind interest, purchasing power, and future claims.
- [Introduction to present value](https://www.youtube.com/watch?v=ks33lMoxst0) — Khan Academy. The mechanics of single-sum discounting.
- [Present Value 4 (and discounted cash flow)](https://www.youtube.com/watch?v=6WCfVjUTTEY) — Khan Academy. Summing discrete future cash flows to determine intrinsic value today.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 2: "How to Calculate Present Values".
- Damodaran, Aswath, *Investment Valuation*, Chapter 2: "Introduction to Valuation".
