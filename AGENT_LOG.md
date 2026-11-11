# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```

## 2026-11-11: Compare median home sale prices by city

- **Asked:** "Read AGENTS.md and docs/data_description_sheet.md first. Replace the placeholder index.html with a page comparing median home sale prices by city, computed from data/college_town_home_sales.csv. Use city and state together if needed to distinguish cities. Exclude sale prices below $10,000 and explain that filter on the page. Format median prices as whole dollars and include the number of eligible sales for each city. Keep all five original files in data/ unchanged and record this session in AGENT_LOG.md. Verify the calculations against the source CSV and report what you checked. Make the changes on a working branch and show them for review before opening a pull request or merging."
- **Agent produced:** Created branch `compare-city-median-prices` and replaced the placeholder with a plain HTML/CSS/JavaScript page that reads the source CSV, groups by city and state, excludes prices below `$10,000`, calculates medians in the browser, and shows whole-dollar medians with eligible-sale counts.
- **Checked or changed:** The first log update used the file's existing outline but did not satisfy its required dated entry format, so it was replaced with this entry. Independently checked the CSV with Python's standard-library CSV reader: 35,442 total rows, 40 excluded sales, 35,402 eligible sales, 18 city/state groups, and the same medians and counts used by the page. Confirmed the five original files in `data/` were not modified.
