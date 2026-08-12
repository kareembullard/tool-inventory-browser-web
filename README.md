# tool-inventory-browser-web

Live: [https://kareembullard.github.io/tool-inventory-browser-web/](https://kareembullard.github.io/tool-inventory-browser-web/)

Browse my real software tool inventory — filter, sort, and see how each tool links to my personal systems.

## What it is

A static, single-file web app version of [tool-inventory-browser](https://github.com/kareembullard/tool-inventory-browser) (the original Flask + SQLite desktop app). This public version:

- Shows my **actual tool inventory** — 91 tools exported from my Airtable workspace, published deliberately
- Filterable/sortable table (Area, Function, Platform, Main Use, search) plus a detail page per tool (`#/tool/<id>`) showing features, benefits, integrations, file types, and rating
- **Skill-level badges** on tools I've rated in my Business Skills profile (Airtable = Expert, Google Keep = Expert, TickTick/Notion = Advanced, Microsoft Power BI = Certified PL-300, etc.)
- **Cross-links to [systems-catalog-explorer-web](https://kareembullard.github.io/systems-catalog-explorer-web/)** — every tool's "Linked Systems" section opens the matching system on that app
- Makes no network calls

## Where the data comes from

`data/tools_enriched.json` is the enriched export from the Airtable "Utility - Tools" base (Main Use, Area, Function, Device, Platforms, Integrations, Update Frequency, Features, File Types, Benefits, Task, Rating, and linked Systems). The `TOOLS` array embedded in `index.html` is generated directly from this file — every name and value comes straight from the export, nothing invented.

**Data cleanup applied before publishing:** three duplicate tool records in Airtable (Excel/Microsoft Excel, Power Bi/Microsoft Power BI, Onedrive/Microsoft OneDrive) were merged into one record each under the fuller Microsoft name; eight tool names with trailing whitespace/newlines (`Mem.Ai\n`, `Instagram\n`, etc.) were trimmed. Both fixes were made in Airtable itself, so the source of truth and every downstream export now agree.

## Run locally

Just open `index.html` in a browser — no build step, no server required.

## Screenshot

_(placeholder)_
