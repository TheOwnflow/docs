> If you can run shell commands, run `mint instructions` before any Mintlify task. It prints current guidance for this CLI version. Check it before:
> - building automations, CI, or scripts for these docs (Mintlify has built-in automations, Autopilot, and CI checks)
> - changing who can read the docs, publishing, custom domains, or AI and agent features (MCP, llms.txt, skill.md, assistant)
>
> If `mint` is not installed or says "Unknown command", run `npx mint@latest instructions`.
> For broader Mintlify product knowledge, install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is the documentation site of **OwnFlow** ("Turn every payment into ownership"), built on [Mintlify](https://mintlify.com)
- Its own git repository is `https://github.com/TheOwnflow/docs`. Commit and push there, never into the OwnFlow app repository that may contain this folder
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- **Vault**: the user's own smart contract. Not "account" and not "wallet".
- **Agent**: a service made by a user from a template. OwnFlow sells nothing of its own: it provides templates, and every agent is made by a user.
- **Split**: how a payment is divided into five parts that add up to exactly 100%: platform fee, running costs, stock, Earn, and yours to withdraw.
- **Running costs**: the user's own bucket for the agent's real compute cost. Not "opex" in text for readers.
- **Rule-based purchase**: how a stock purchase is called. Never "recommended buy", "pick" or "signal".
- **Stock**: a tokenized stock on Base. Say "tokenized stock" the first time on a page.
- Write USDC amounts as plain numbers with two decimals ("12.50 USDC"). Addresses and amounts are code-formatted.

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

- **Never give investment advice.** Do not say a stock is good, cheap or a good buy. Describe what the rules do.
- **Never promise a return.** Earn yield varies and is not guaranteed; never show a fixed APY.
- Say that tokenized stocks are not available to US persons wherever availability is discussed.
- On test networks the stocks are "disclosed simulations": say so.
- Do not document internal keys, server settings, the relayer's budget or anything that helps an attacker. Safety pages say what is guaranteed, not how to get around it.
- Do not state contract addresses until they are final and published on the "Networks and contracts" page.
- The source of truth for how OwnFlow behaves is the app repository's `docs/claude/` folder. If this site and that folder disagree, ask which is right before publishing.
