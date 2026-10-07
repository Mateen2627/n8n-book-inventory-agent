# n8n Book Inventory AI Agent

An n8n chat workflow where an AI agent manages a book inventory stored in Airtable.

## What it does
- **Chat trigger**: you chat with the agent in n8n.
- **AI Agent** (OpenAI `gpt-5.4-mini`, low reasoning effort) with **Simple Memory** (last 3 messages).
- **Airtable tools** on the `Book Inventory Tracker` base / `Books` table:
  - `search_books`: find books by title keyword (or list all)
  - `update_book`: change Quantity on Hand / Min Quantity
  - `create_book`: add a new book

## Import into n8n
1. In n8n, create a new workflow, open the **...** menu, choose **Import from File**, and select `workflows/book-inventory-agent.json`.
2. Re-select your credentials on the nodes: an **OpenAI** credential on *OpenAI Chat Model* and an **Airtable Personal Access Token** on the three Airtable tools.
3. If you use a different Airtable base, update the base and table on the three Airtable tool nodes.

No secrets are stored in this repository; credentials are referenced only by name.
