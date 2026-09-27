---
title: "11. Working capital management"
layout: default
nav_order: 12
---

# Working capital management
{: .no_toc }

*~8 min read*

**Interview occasional**

## Why it matters

Working capital management governs a company’s operational liquidity—the day-to-day rhythm of purchasing raw materials, manufacturing inventory, extending customer trade credit, and paying vendor bills. In corporate finance modeling, working capital is the primary engine bridging the Income Statement and the Cash Flow Statement. In M&A and private equity transactions, the negotiation of the "working capital peg" is often a multi-million-dollar battleground that directly alters the net purchase price at closing.

## Core concepts

- **Operating Net Working Capital (NWC):**
  In corporate valuation and [Free cash flow](../08-free-cash-flow/) modeling, working capital is defined strictly on an **operating basis**:
  \[
  \text{Operating NWC} = \text{Operating Current Assets} - \text{Operating Current Liabilities}
  \]
  - **Operating Current Assets:** Accounts Receivable (AR), Inventory, Prepaid Expenses. *(Excludes Cash and Marketable Securities, which are non-operating assets in [Enterprise Value](../09-enterprise-vs-equity-value/)).*
  - **Operating Current Liabilities:** Accounts Payable (AP), Accrued Expenses, Deferred / Unearned Revenue. *(Excludes Short-Term Debt and the Current Portion of Long-Term Debt, which are financing liabilities).*
- **The Cash Conversion Cycle (CCC):**
  The duration (in days) between when a company pays cash for raw materials and when it collects cash from final customer sales:
  \[
  \text{CCC} = \text{DIO} + \text{DSO} - \text{DPO}
  \]
  - **Days Sales Outstanding (DSO):** Average days required to collect customer credit receivables:
    \[
    \text{DSO} = \frac{\text{Accounts Receivable}}{\text{Total Revenue}} \times 365
    \]
  - **Days Inventory Outstanding (DIO):** Average days inventory sits in warehouses before being sold:
    \[
    \text{DIO} = \frac{\text{Inventory}}{\text{Cost of Goods Sold (COGS)}} \times 365
    \]
  - **Days Payable Outstanding (DPO):** Average days the company takes to pay its trade vendors:
    \[
    \text{DPO} = \frac{\text{Accounts Payable}}{\text{COGS}} \times 365
    \]
- **Negative Working Capital and the Cash Float:**
  - Companies with superior supply-chain power (e.g., Amazon, Walmart) or enterprise software subscription models (e.g., Salesforce, Microsoft) operate with **negative working capital** or a negative CCC.
  - Customers pay immediately via credit card or prepay annual software subscriptions upfront (Deferred Revenue), while the firm negotiates 60- to 90-day vendor payment terms (high DPO).
  - Consequently, customers and suppliers provide interest-free financing that grows automatically as the business expands.
- **The M&A Working Capital Peg:**
  In a corporate acquisition, the headline enterprise purchase price assumes the target is delivered with a "normalized" level of working capital necessary to run operations without immediate post-closing equity injections.
  - At closing: If \(\text{Delivered NWC} > \text{Peg}\), the buyer pays the seller the surplus dollar-for-dollar.
  - If \(\text{Delivered NWC} < \text{Peg}\), the seller must reimburse the buyer or reduce the purchase price.

## Mental model

```
  Day 0                 Day 40 (DPO)             Day 60 (DIO)              Day 90 (DIO + DSO)
    |                         |                        |                         |
    v                         v                        v                         v
  Receive Raw Materials     Pay Cash to Supplier     Ship Finished Goods       Collect Cash
  [ Inventory created ]     [ Cash OUTFLOW ]         [ Accounts Receivable ]   [ Cash INFLOW ]
    |                         |                        |                         |
    +---- Inventory (60d) ----+                        +---- Receivables (30d) --+
                              |                                                  |
                              +<---------- Cash Conversion Cycle (50 days) ----->+
```

The Cash Conversion Cycle measures the financing gap: the number of days your cash is held hostage inside operational inventory and unpaid invoices.

## Interview questions

1. **Why do we exclude cash and short-term debt when calculating Working Capital for a DCF model?**  
   Answer: Working capital in a DCF measures the operational assets and liabilities required to support revenue generation. Cash is an uncommitted non-operating asset already accounted for as an addition when bridging Enterprise Value to Equity Value; including it in NWC would double-count it. Short-term debt and notes payable are financing choices paid to lenders; they belong to the firm’s capital structure and are serviced through interest and financing cash flows, not operational trade cycles.

2. **Is negative working capital always a sign of financial strength? When is it a warning sign of distress?**  
   Answer: For high-margin, scalable companies like Amazon or enterprise SaaS businesses, negative working capital is a powerful strength: it indicates high bargaining power over suppliers (high DPO) and upfront customer collections, generating a permanent interest-free operational cash float. However, for a struggling brick-and-mortar retailer, negative working capital is often a sign of impending insolvency: the firm has exhausted its cash reserves, stretched accounts payable past due dates because it cannot pay vendors, and vendors are on the verge of cutting off shipments.

3. **How does Deferred (Unearned) Revenue impact Free Cash Flow when an enterprise software vendor transitions from perpetual licenses to upfront annual SaaS subscriptions?**  
   Answer: When customers pay for an annual subscription on Day 1, the company collects 100% of the cash upfront, booking an increase in Cash and a corresponding Operating Current Liability called Deferred Revenue. On the income statement, revenue is recognized ratably over 12 months. Because \(\text{NWC} = \text{Operating Assets} - \text{Operating Liabilities}\), an increase in Deferred Revenue *decreases* NWC (\(\Delta\text{NWC} < 0\)). Since \(\Delta\text{NWC}\) is subtracted in the Free Cash Flow equation (\(-\Delta\text{NWC}\)), this creates an immediate **cash inflow boost** to FCF upfront.

4. **In an M&A deal, how is the 'target working capital peg' set, and why do buyers scrutinize seasonality?**  
   Answer: The working capital peg is typically calculated as the average trailing 12-month (LTM) operating NWC. However, for seasonal businesses (e.g., retailers who build massive inventory in October for holiday sales), an unadjusted 12-month average will distort closing adjustments. If closing occurs in November during peak inventory, actual NWC will vastly exceed an annual average peg, forcing the buyer to pay an unintended cash true-up. Bankers adjust the peg to reflect the historical seasonal average for that specific calendar month.

## Watch

- [Session 13: From Earnings to Time-weighted Incremental Cashflow Returns](https://www.youtube.com/watch?v=t-X2quPDxsM) — Prof. Aswath Damodaran (NYU Stern). Working capital dynamics, accruals vs. cash, and operational cash loops.
- [Session 7: Estimating Cash Flows](https://www.youtube.com/watch?v=8gYT3Xgs6NE) — Prof. Aswath Damodaran (NYU Stern). Non-cash working capital investments as a mandatory drag on reinvestment.

## Further reading

- Brealey, Myers, & Allen, *Principles of Corporate Finance*, Chapter 29: "Working Capital Management".
- Damodaran, Aswath, *Investment Valuation*, Chapter 10: "Estimating Cash Flows (Non-Cash Working Capital)".
