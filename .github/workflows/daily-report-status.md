---
name: Daily Report Status

on:
  schedule:
    - cron: "0 9 * * *"
  workflow_dispatch:

permissions:
  contents: read
  issues: read

engine: gemini
network: defaults

safe-outputs:
  create-issue:
    max: 1
---

# daily-report-status

Generate an activity report in a new issue.

## Instructions

1. Review recent repository activity and summarize the most important work completed since the last report.
2. Highlight key updates, blockers, open questions, and next steps in a concise markdown report.
3. Create a new issue with a clear title that reflects the reporting period, and include the report in the issue body.
4. Keep the report factual, brief, and actionable for maintainers.
