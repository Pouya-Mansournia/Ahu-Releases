# Ahu

Ahu is a Mac app for finding your way around your databases. It reads their structure (catalogs, schemas, tables, columns and comments) and lets you browse it, search it, run read-only queries, and get help from an AI assistant when you're not sure where to start.

It works with **Trino, PostgreSQL, MySQL / MariaDB, StarRocks and ClickHouse**.

This repository only holds the installers. You don't need to clone anything.

## Download

**Current release: Ahu 1.7.0 for Apple Silicon.** [Download the DMG](https://github.com/Pouya-Mansournia/Ahu-Releases/releases/download/v1.7.0/Ahu-1.7.0-arm64.dmg) or [view the release notes and checksum](https://github.com/Pouya-Mansournia/Ahu-Releases/releases/tag/v1.7.0).

1. Open the DMG and drag **Ahu** into **Applications**.
2. Open Ahu. The first launch takes about 10 seconds while it sets itself up.
3. If macOS says it can't verify the app, go to **System Settings › Privacy & Security** and click **Open Anyway**. You only need to do this once.

Ahu needs a Mac with Apple Silicon (M1 or newer). There is nothing else to install: Python and everything else it needs is included, and Ahu sets itself up.

## First steps

1. Open **Connect**, enter your server details and press **Connect**. Passwords are stored in the macOS Keychain.
2. Press **Discover** and select the connections to scan. Discovery reads database structure and metadata.
3. Explore, search and query.

## What you can do with it

- **Overview** of every connected source: tables per catalog, discovery health and how your catalog grows over time.
- **Explore and search** every catalog, schema, table and column, with charts of each catalog's tables and column types.
- **Ready-made queries for every table**, one click away in **Quick start**: latest rows, row count, rows per day, latest load time, column count, NULL count per column, daily sums, sums of the latest day and hourly sums.
- **Write and run queries** in a read-only editor with line numbers, syntax highlighting, SQL file import, text search, and full-screen editing. The pencil opens Quick query from any page. Results support chart view and CSV export. Saved queries are kept as `.sql` files in a folder you choose.
- **SQL autocomplete** suggests keywords, functions, and discovered tables and schemas as you type in any editable SQL field, including templates, schedules, and full-screen editors.
- **Federated SQL**: paste one read-only statement, detect its tables, choose a connection for each table, and preview the lookup steps. On supported queries, Ahu runs the source computation first and checks only the returned keys on the destination. The execution log reports each source separately.
- **Query plan analysis** shows the estimated database plan, operator counts, and a Mermaid diagram.
- **Cross-source queries**: run individual queries on separate connections and combine their results on your Mac.
- **AI assistant** (Claude, OpenAI, Gemini or Cloudflare Workers AI, with your own key). It only sends your question and relevant table and column names, never row data.
- **Learn SQL** with short lessons and a dictionary.
- **Documentation** of your catalog, generated on your Mac and exportable as HTML.

Ahu runs locally and connects to the databases you configure. A staged lookup can send join keys from one selected connection to another. If you enable AI, Ahu also connects to the provider you choose. The interface is in English, with Persian available for help text in **Settings**.

## Updates

You only install Ahu by hand once. After that it checks for new versions on its own, and you can also use **Ahu › Check for Updates…**. Click **Update Now** and it downloads the new version, checks that the file is intact, and restarts.

## Something went wrong?

Open **Help › Show Logs** in Ahu (or `~/Library/Logs/Ahu.log`). Logs never contain passwords.

---
Engineered by **P. Mansournia**
