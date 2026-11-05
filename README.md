# Grove

Grove is a Mac app for finding your way around your databases. It reads their structure (catalogs, schemas, tables, columns and comments) and lets you browse it, search it, run read-only queries, and get help from an AI assistant when you're not sure where to start.

It works with **Trino, PostgreSQL, MySQL / MariaDB, StarRocks and ClickHouse**.

This repository only holds the installers. You don't need to clone anything.

## Download

Get the latest `.dmg` from the [Releases page](https://github.com/Pouya-Mansournia/grove-releases/releases/latest).

1. Open the DMG and drag **Grove** into **Applications**.
2. Open Grove. The first launch takes about 10 seconds while it sets itself up.
3. If macOS says it can't verify the app, go to **System Settings › Privacy & Security** and click **Open Anyway**. You only need to do this once.

Grove needs a Mac with Apple Silicon (M1 or newer). There is nothing else to install: Python and everything else it needs is included, and setup works offline.

## First steps

1. Open **Connect**, enter your server details and press **Connect**. Passwords are stored in the macOS Keychain.
2. Press **Discover** to read the structure of your databases. Only metadata is read, never table rows.
3. Explore, search and query.

## What you can do with it

- **Overview** of every connected source: tables per catalog, discovery health and how your catalog grows over time.
- **Explore and search** every catalog, schema, table and column, with charts of each catalog's tables and column types.
- **Write and run queries** in a read-only editor, with a chart view for results and CSV export. Saved queries are kept as `.sql` files in a folder you choose.
- **Cross-source queries**: run a query on each of two or more connections (each with its own login) and join the results on your Mac.
- **AI assistant** (Claude, OpenAI, Gemini or Cloudflare Workers AI, with your own key). It only sends your question and relevant table and column names, never row data.
- **Learn SQL** with short lessons and a dictionary.
- **Documentation** of your catalog, generated on your Mac and exportable as HTML.

Everything stays on your Mac: Grove talks only to your own databases and, if you enable it, the AI provider you choose. The interface is in English, with Persian available for help text in **Settings**.

## Updates

You only install Grove by hand once. After that it checks for new versions on its own, and you can also use **Grove › Check for Updates…**. Click **Update Now** and it downloads the new version, checks that the file is intact, and restarts.

## Something went wrong?

Open **Help › Show Logs** in Grove (or `~/Library/Logs/Grove.log`). Logs never contain passwords.
