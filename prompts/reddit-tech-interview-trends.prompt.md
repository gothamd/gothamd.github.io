# Reddit Tech Interview Trends Prompt

## Purpose
Automate the retrieval and summarization of the latest Reddit trends for tech interviews, focusing on:
- Senior interview experiences at Anthropic, OpenAI
- FAANG Engineering Manager, Principal, or Staff Engineer interview experiences
- Latest LLM/AI interview questions

## Workflow Steps

### 1. Search Reddit
Search for the following queries (sort by new, time filter: week):
- "interview experience Anthropic OR OpenAI senior OR experienced"
- "interview experience FAANG Engineering Manager OR Principal Engineer OR Staff Engineer"
- "latest interview questions LLM OR AI OR artificial intelligence"

### 2. Summarize
Summarize the most relevant posts for each category.

### 3. Create the daily report
Save the summary as `reports/reddit-tech-interview-trends-summary-YYYY-MM-DD.md` (using today's date).

The file must begin with this Jekyll front matter:
```
---
layout: default
title: "Reddit Tech Interview Trends – Month DD, YYYY"
date: YYYY-MM-DD
---
```

### 4. Update the reports index
Open `reports/index.md` and prepend a new entry to the **Reports** list (below the `## Reports` heading), keeping newest-first order:
```
- [Month DD, YYYY – Reddit Tech Interview Trends](./reddit-tech-interview-trends-summary-YYYY-MM-DD)
```

### 5. Commit and push to GitHub Pages
Stage the `reports/` and `prompts/` folders, then commit and push:
```
git add reports/ prompts/
git commit -m "Add Reddit tech interview trends summary YYYY-MM-DD"
git push origin main
```

The new report will be live at `https://gothamd.github.io/reports/reddit-tech-interview-trends-summary-YYYY-MM-DD` after GitHub Pages rebuilds.

---

**Note:**
- Adjust search queries or time filters for broader/narrower results.
- Prompt files live in `prompts/` and are tracked by git.
