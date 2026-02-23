# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-file shopping list web application (`shopping-list.html`) built with vanilla HTML/CSS/JavaScript. No build process, package manager, or dependencies — open directly in a browser.

## Running the App

```bash
# Open in default browser
xdg-open shopping-list.html

# Or serve locally (if needed)
python3 -m http.server 8000
```

## Architecture

All application logic lives in `shopping-list.html` as a self-contained file:

- **State**: `items` array (each item: `{ text, done }`) held in memory and synced to `localStorage` under the key `"shopping-items"`
- **Persistence**: `save()` serializes state → `render()` rebuilds the DOM from state on every change
- **UI**: Korean-language interface with flexbox layout; no external stylesheets or scripts

Key functions: `addItem`, `toggleItem(index)`, `deleteItem(index)`, `clearDone`, `save`, `render`

## MCP Servers Available

The workspace has Playwright, Notion, Context7, and Sequential Thinking MCP servers configured (see `.claude/settings.local.json`).
