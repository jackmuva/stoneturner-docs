> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

{/* Add product-specific terms and preferred usage */}
{/* Example: Use "workspace" not "project", "member" not "user" */}

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

{/* Define what should and shouldn't be documented */}
{/* Example: Don't document internal admin features */}

## Cursor Cloud specific instructions

- This repo is a Mintlify docs site (no `package.json`); the only "service" is the Mintlify preview server.
- The `mint` CLI is installed globally via npm into `$HOME/.npm-global` (the update script keeps it installed). `$HOME/.bashrc` adds `$HOME/.npm-global/bin` to `PATH`, so login shells (including new tmux sessions) can run `mint` directly.
- Run the dev server from the repo root (where `docs.json` lives): `mint dev` serves at `http://localhost:3000`. The site root `/` 307-redirects to `/overview`.
- Validate content with `mint broken-links` (the closest thing to a lint/test for this repo). If the CLI misbehaves, `mint update` refreshes it.
- Ignore the `nvm ... incompatible with nvm` warning printed on shell startup; it is caused by the npm global `prefix` config and does not affect `mint`.
- Browser note: Chrome in this VM intermittently crashes with "Aw, Snap! Error code 4" (renderer OOM) when loading pages; the docs site itself is fine. Reload to recover, and prefer `curl` (e.g. `curl -sI localhost:3000/overview`) for quick verification.
