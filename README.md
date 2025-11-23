This repository contains an n8n workflow for automated collection and normalization of scientific articles from open sources such as Crossref and OpenAlex.

The workflow allows you to define any number of research topics and automatically fetches relevant publications for each topic.

🔍 What the parser does

Expands a list of user-defined topics

Sends API requests to Crossref and OpenAlex

Normalizes returned metadata (DOI, title, year, authors, venue, URL)

Merges and deduplicates publications from both sources

Produces a clean articles.json file with unique articles

The workflow is fully modular and does not require any credentials.

⚙️ How to change the topics

Modify the n8n node:

Set → Edit Fields → jsonOutput

Inside JSON, update the array:

{
  "topics": [
    {
      "topic_id": "T01",
      "topic_query": "your search keywords"
    },
    ...
  ]
}


You can:

add more topics,

remove topics,

broaden the search queries,

or narrow them down to a specific domain.

📤 Exporting results

The final data is produced by the node:

Convert to File → articles.json


You may optionally attach any storage node (Google Drive, AWS S3, filesystem) to save it automatically.

🖼 Workflow Preview

A visual representation of the workflow is included in docs/workflow-preview.png.

📦 Files in the repository
workflow/
  parser.json             → n8n workflow file
docs/
  workflow-preview.png    → visual representation of the workflow
