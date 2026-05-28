---
name: web-scraper-summarizer
description: Scrape any URL and return structured summary with key facts, sentiment, and main topics.
version: 1.0.0
---
# Web Scraper & Summarizer
## Goal
Scrape a URL and produce a structured JSON summary.
## Inputs
- url (string, required): The URL to scrape and summarize
- max_tokens (integer, optional, default 500): Max summary length
## Procedure
1. Use requests/httpx to fetch the URL content
2. Extract main text using BeautifulSoup or readability
3. Generate summary using LLM with key facts, sentiment (positive/neutral/negative), and 3-5 topic tags
4. Return JSON: { url, title, summary, sentiment, topics, word_count, scraped_at }
## Output
JSON summary object with title, summary, sentiment, topics.
