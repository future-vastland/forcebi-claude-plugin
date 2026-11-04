# ForceBI plugin for Claude

The `forcebi` plugin (version 1.0.0) for Claude: claude.ai Chat, Cowork and Claude Code. It pairs the ForceBI connector with a skill (`forcebi-answer`) that gives Claude the ForceBI data rules and answer style. The data is read-only and limited to your own ForceBI login, company and permissions.

> **Server URL (Q6):** `.mcp.json` uses `https://mcp.forcetechai.com/mcp`, the production MCP host that Ali chose on 4 Nov 2026. It works only after the host is deployed (DNS and TLS). It must be one fixed URL: Chat ignores a URL with `${user_config.*}`.

## What it does

- **Connector** (`.mcp.json`): the ForceBI MCP server. It answers questions about sales, collections, debtors and aging, pending purchase orders, slow-moving stock, inactive customers, product sales, salesperson targets and WhatsApp performance, for the reports your role may read.
- **Skill** (`skills/forcebi-answer/SKILL.md`): the ForceBI answer style for Claude (headline first, short numbered updates, amounts in RM, one next step) and the data rules (only totals that ForceBI returns, no invented figures, read-only). The skill is generated from the server guidance (by Force Tech from the server guidance); do not edit it by hand.

## Before you start

- A ForceBI company account, and your company has accepted the ForceBI AI Connector Agreement.
- Your 6-character company code (from your ForceBI administrator).
- Your own ForceBI login. ForceBI shows only the data that your role may see.

## Connect

1. Install the plugin (from the Claude directory, or for a test: Customize > Plugins > Upload plugin with the zip).
2. Open the ForceBI connector and click **Connect**.
3. Enter your company code, then log in on your company's own ForceBI site and allow read access (`bi.read`).
4. Ask a question, for example "How are our sales this month?" or "Who owes us the most?".

## Read-only scope

ForceBI in Claude reads data only. It cannot change, approve, delete, send or export data, and it gives no customer contact data. Make changes in ForceBI itself.

## Privacy Policy

See the Force Tech privacy policy: https://www.forcetechai.com/privacy/ (section on the ForceBI AI connector). ForceBI does not store your Claude conversations.

## Support

Support contact: **support@forcetechai.com**.

## Uninstall

Remove the plugin in Customize > Plugins (claude.ai) or with `claude plugin uninstall forcebi` (Claude Code). To stop all access, also disconnect ForceBI in the connector settings; your ForceBI administrator can revoke the AI connection too.

## Claude Code

Claude Code is out of scope for now: it needs a client that registers itself (CIMD or DCR), and the ForceBI broker accepts only fixed clients. The plugin installs in Claude Code, but the connector login works in claude.ai only.
