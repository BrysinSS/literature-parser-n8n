# Literature Parser (n8n)

This repository contains an n8n workflow for automated collection and
normalization of scientific publications from open metadata sources.

The workflow fetches, normalizes, merges, and deduplicates articles
based on user-defined research topics.

---

## Function
- Input: list of research topics
- Output: normalized articles.json file
- Fully automated
- No credentials required

---

## Data Sources
- Crossref
- OpenAlex

---

## What the workflow does
- Expands user-defined research topics
- Queries open scientific metadata APIs
- Normalizes article metadata:
  DOI, title, year, authors, venue, URL
- Merges and deduplicates results
- Produces a clean list of unique articles

---

## Configuration
Topics are defined directly in the workflow.

Edit the node:
Set → Edit Fields → jsonOutput

Update the topics array:
- add or remove topics
- broaden or narrow search queries
- target specific research domains

---

## Output
The final dataset is produced as:
articles.json

The workflow can be extended with storage nodes
(e.g. filesystem, cloud storage) if persistence is required.

---

## Files
- workflow/parser.json — n8n workflow definition
- docs/workflow-preview.png — visual workflow diagram

---

## Status
Working workflow.

---

## Author
Stanislav Brysin
