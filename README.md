# Corporate Finance Study Guide

A practical corporate finance study guide for Penn builders, Wharton QF students, and investment banking / corporate finance interview prep — covering WACC, FCF, capital structure, valuation, and M&A with clean math and capital literacy.

**Live site:** https://cliffweng.github.io/corporate-finance-guide/  
*(Also accessible via custom domain path: [cliffweng.com/corporate-finance-guide/](https://cliffweng.com/corporate-finance-guide/))*

## Roadmap

14 topics, one file each under [`topics/`](topics/), ordered foundational → applied:

1. Time value of money refresh
2. Risk and return
3. CAPM & cost of equity
4. WACC (Weighted Average Cost of Capital)
5. Capital structure & Modigliani-Miller
6. Leverage trade-offs & distress
7. NPV and IRR
8. Free cash flow (FCFF & FCFE)
9. Enterprise value vs. equity value
10. Multiples overview
11. Working capital management
12. Dividend and buyback basics
13. M&A intro & accretion/dilution
14. Corporate finance interview patterns

## Interview hotspots

Every topic page carries a badge (🎯 Frequent / Occasional / Background) so you know where to spend prep time. If you're short on time, prioritize these:

- **WACC** — the anchor of DCF valuation; interviewers probe market-value weights, post-tax cost of debt, asset beta unlevering/relevering, and how capital structure shifts WACC.
- **Free cash flow (FCFF & FCFE)** — the core metric of corporate valuation; expect a flawless walk from EBIT or Net Income to Unlevered FCF (\(\text{EBIT}(1-t) + \text{D\&A} - \text{CapEx} - \Delta\text{NWC}\)) and why each line item is adjusted.
- **Enterprise value vs. equity value** — the bedrock bridge of corporate finance; interviewers test the EV formula (\(\text{EV} = \text{Equity Value} + \text{Total Debt} + \text{Preferred Stock} + \text{Non-controlling Interest} - \text{Cash}\)), why cash is subtracted, and matching enterprise vs. equity cash flows and multiples.
- **NPV and IRR** — capital budgeting fundamentals; expect the reinvestment rate trap of IRR, mutually exclusive project conflict under scale or timing differences, and why NPV is the golden rule.
- **Multiples overview** — relative valuation intuition; interviewers test matching enterprise metrics (EV/EBITDA, EV/EBIT) vs. equity metrics (P/E), capital structure neutrality, and accounting distortion traps.
- **Interview patterns** — end-to-end DCF walkthroughs, 3-statement linking, quick accretion/dilution mental math, and structured valuation cases in 8–10 minutes.
- **Foundational & frequent**: Risk and return, CAPM & cost of equity, capital structure (MM I & II), and TVM refresh.

**Occasional** (still essential for well-rounded prep, less likely to anchor an entire technical round): leverage trade-offs & distress, working capital management, dividend and buyback basics, M&A intro.

This split reflects the rigorous technical demands of top investment banking (M&A / Restructuring) and corporate finance interviews.

## How to use this guide

Each topic page is designed to be read in **~10 minutes** and follows the same structure: why it matters, core concepts, a mental model (ASCII diagram or crisp intuition), 3–5 interview questions with brief answer keys, and a short list of verified YouTube videos. Read them in order, or jump straight to what you need. No backend, no market data feed, no auth, no sign-up — just read the pages.

## How to contribute

See [CONTRIBUTING.md](CONTRIBUTING.md). In short: one topic per file, keep it under ~10 minutes to read, and only link to sources (especially YouTube videos) you've personally verified exist. Open an issue before proposing new topics or restructuring the curriculum.

## Decisions

These are the product locks this guide was built against — echoed here so future contributors don't accidentally relitigate them:

- **Audience**: Penn CS+stats+econ builders + Wharton QF students + IB/corp fin interview prep. Bias toward IB interview rigor (WACC/FCF/EV) with clean math.
- **Time-boxed**: every topic is readable in 10 minutes or less. Depth is balanced with interview scannability; further reading links point to advanced treatises (Brealey/Myers, Damodaran).
- **Learning + interview prep in one page**: each topic pairs core corporate finance mechanics with interview questions, rather than splitting them into separate tracks.
- **Real links only**: every YouTube link is verified to exist before being added. No invented URLs, ever.
- **Static site, GitHub Pages, Just the Docs**: no backend, no auth, no paid data, no quizzes. Cheap to host, cheap to maintain, easy to contribute to via plain Markdown + front matter.

## Enabling GitHub Pages

Just the Docs is configured via `_config.yml` (remote theme). After this lands on `main`:

1. Repo **Settings → Pages**.
2. **Build and deployment → Source**: **Deploy from a branch**.
3. Branch: `main` / folder: `/ (root)`.
4. Save. Site publishes to https://cliffweng.github.io/corporate-finance-guide/

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## License

[MIT](LICENSE)
