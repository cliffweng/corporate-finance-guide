# Contributing

Thanks for helping improve the guide. A few ground rules:

- **Scope**: one topic per file under `topics/`. Keep each topic readable in ~10 minutes.
- **Template**: follow the structure already used in existing topic files (Why it matters, Core concepts, Mental model, Interview questions, Watch, Further reading).
- **Links must be real**: only link to YouTube videos and articles you have personally verified exist (open the URL, confirm the title/content). Never guess a video ID or URL. Prefer Khan Academy, Aswath Damodaran (NYU Stern), and reputable corporate finance faculty lectures. If you are unsure of an exact URL, omit the video rather than invent one.
- **No invented product direction**: this guide covers corporate finance fundamentals for Penn builders, Wharton QF students, and IB/corp fin interview prep (WACC, FCF, EV, capital structure, valuation, and M&A). It is not full CFA L2 depth, not exotic derivatives, and not a quiz/auth site. If you want to propose a new topic or reorganize the curriculum, open an issue first.
- **Keep topics tight**: prefer accurate intuition, interview-ready answer keys, and clean mathematical rigor over encyclopedic coverage. Don't invent extra scope (no live market data feeds, no interactive spreadsheet tools, no login).
- **Local preview**:
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
  Then open `http://localhost:4000`.
- **MathJax delimiters**: MathJax delimiters in markdown must be double-escaped for kramdown: write `\\(` `\\)` `\\[` `\\]` in source so HTML keeps `\(` `\)` `\[` `\]` for MathJax.
- **Pull requests**: keep them focused (one topic or fix per PR) and describe what changed and why.
