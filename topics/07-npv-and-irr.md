---
title: "07. NPV and IRR"
layout: default
nav_order: 8
---

# Net Present Value and Internal Rate of Return
{: .no_toc }

*~9 min read*

**🎯 Interview frequent**

## Why it matters

Capital budgeting is the process of deciding which long-term projects, expansions, or acquisitions a company should fund. Net Present Value (NPV) and Internal Rate of Return (IRR) are the two primary metrics used to evaluate capital investments. While corporate executives and private equity sponsors frequently quote IRR because percentage returns are intuitive and easy to benchmark, modern corporate finance proves that NPV is the gold standard for shareholder wealth maximization. Interviewers routinely test whether you understand the mathematical and economic traps inherent in IRR.

## Core concepts

- **Net Present Value (NPV):** The total present value of all future expected cash inflows minus the initial cash outlay:
  \[
  \text{NPV} = -C_0 + \sum_{t=1}^n \frac{C_t}{(1 + r)^t}
  \]
  - **Decision Rule:** Accept any project where \(\text{NPV} > 0\). For mutually exclusive projects, select the project that maximizes total absolute dollar NPV.
  - **Value Additivity:** \(\text{NPV}(A + B) = \text{NPV}(A) + \text{NPV}(B)\). NPV directly measures the incremental wealth added to common equity.
- **Internal Rate of Return (IRR):** The discount rate \(r^*\) at which the net present value of a project exactly equals zero:
  \[
  0 = -C_0 + \sum_{t=1}^n \frac{C_t}{(1 + \text{IRR})^t}
  \]
  - **Decision Rule:** Accept if \(\text{IRR} > r\) (where \(r\) is the hurdle rate or [WACC](../04-wacc/)).
- **The Four Fatal Traps of IRR:**
  1. **The Reinvestment Rate Fallacy:** Mathematically, IRR implicitly assumes all intermediate cash flows (\(C_1, C_2, \dots\)) are reinvested for the remainder of the project life at the **IRR itself**. If a project delivers a 50% IRR, it assumes all interim cash distributions can be redeployed at 50% returns, which is virtually impossible. NPV realistically assumes interim cash flows are reinvested at the firm's opportunity cost of capital (\(r\)).
  2. **Scale Insensitivity:** Investing $10 today to receive $30 in one year generates an extraordinary **200% IRR**, but only **$17 of net dollar profit** (at \(r = 10\%\)). Investing $10,000,000 to receive $15,000,000 generates a modest **50% IRR**, but delivers **$3,636,364 of net dollar wealth**. Equity holders spend dollars, not percentages.
  3. **Multiple or No IRRs:** By Descartes' Rule of Signs, an equation has as many real roots as there are sign changes in the cash flow sequence. If cash flows alternate (e.g., negative outlay, positive operating cash, followed by negative environmental decommissioning or nuclear cleanup costs), there can be multiple IRRs or no real IRR.
  4. **Timing and Crossover Conflicts:** For mutually exclusive projects, the project with the higher IRR may have a lower NPV at the firm's actual cost of capital due to differences in cash flow duration.
- **The Crossover Rate (Fisher's Rate):** The discount rate at which two competing projects produce identical NPVs:
  \[
  \text{NPV}_A(r_{\text{cross}}) = \text{NPV}_B(r_{\text{cross}}) \iff \text{NPV}_{A - B}(r_{\text{cross}}) = 0
  \]
  It is found by calculating the IRR of the incremental cash flows \((C_{t, A} - C_{t, B})\).

## Mental model

```
  NPV ($)
     ^
     |    Project A (Long-term, high NPV at low rates)
     | \  Project B (Front-loaded, high IRR)
     |  \
     |   \      /
     |    \    /
     |     \  /
  NPV|------*  <-- Crossover Rate (r_cross)
     |     / \
     |    /   \
     |   /     \
   0 +--+-------+--------+-----------------------------------> Discount Rate (r)
        |       |        |
        0    r_cross   IRR_A   IRR_B
```

- When \(r < r_{\text{cross}}\): Project A has a higher NPV. Always choose A, even though \(\text{IRR}_B > \text{IRR}_A\).
- When \(r > r_{\text{cross}}\): Project B has both higher NPV and higher IRR.

## Interview questions

1. **You have two mutually exclusive projects. Project A has an IRR of 40% and an NPV of $5M. Project B has an IRR of 22% and an NPV of $25M. The company's WACC is 10%. Which project do you accept, and why?**  
   Answer: Choose Project B. Shareholder wealth maximization requires selecting the project that generates the highest absolute dollar value addition. Project B creates $25M of present-value net wealth for equity holders, compared to only $5M from Project A. The higher IRR of Project A is misleading due to scale or cash flow timing; you cannot pay shareholder dividends with a percentage rate of return.

2. **How do you calculate the crossover rate between two projects, and what is its strategic significance?**  
   Answer: Subtract the cash flow stream of Project B from Project A at each period to construct an incremental cash flow profile: \(\Delta C_t = C_{t, A} - C_{t, B}\). The crossover rate is the IRR of this incremental cash flow series (\(\text{NPV}_{\Delta C} = 0\)). If the company’s actual cost of capital is lower than the crossover rate, the project with the longer cash flow duration (Project A) is superior. If the cost of capital is above the crossover rate, the faster-payback project (Project B) is superior.

3. **Can a project have multiple IRRs? Provide an example of when this occurs.**  
   Answer: Yes. A project has multiple IRRs whenever the sequence of cash flows changes sign more than once. For example, a strip-mining project requires an initial investment of -$100M at \(t=0\), generates positive cash flows of +$250M at \(t=1\), and incurs a massive environmental cleanup and site remediation cost of -$160M at \(t=2\). Because the signs change from negative to positive to negative, the quadratic polynomial has two distinct real roots (two separate discount rates where NPV = 0). In such cases, IRR is economically meaningless, and decision-makers must rely on NPV or Modified IRR (MIRR).

4. **In private equity, sponsors frequently prioritize IRR over Multiple on Invested Capital (MoIC), yet LPs care deeply about both. How does timing distort this relationship?**  
   Answer: IRR is sensitive to the holding period: \(\text{IRR} = \text{MoIC}^{1/t} - 1\). A PE firm that buys an asset for $100M and flips it 6 months later for $130M achieves an annualized IRR of ~69%, but only a 1.3x MoIC. While the fund’s headline IRR looks spectacular, the fund returned very few absolute dollars to Limited Partners (LPs), who must now find new investments for that capital. Conversely, a 2.5x MoIC over 7 years yields a 14% IRR. LPs demand a balance: high MoIC generates substantial total carry dollars, while high IRR prevents capital from being tied up in low-yielding assets.

## Watch

- [Session 12: Show me the money: First steps in Return Measurement](https://www.youtube.com/watch?v=y8wqXTbzZFA) — Prof. Aswath Damodaran (NYU Stern). Accounting returns vs. time-weighted cash flow returns.
- [Session 14: Equity analysis, acquisitions as projects and NPV vs IRR](https://www.youtube.com/watch?v=nGN9YNTNjuQ) — Prof. Aswath Damodaran (NYU Stern). Project evaluation rules, side-by-side comparison of NPV vs. IRR, and capital rationing.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 5: "Net Present Value and Other Investment Criteria".
- Damodaran, Aswath, *Applied Corporate Finance*, Chapter 5: "Measuring Return on Capital: NPV vs. IRR".
