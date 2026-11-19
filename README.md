# VPS Hardening MCP

A free, read-only MCP server with research-backed security checklists for people who run their own server or ship vibe-coded apps. Ask your AI "how do I lock down my VPS?" or "check my Stripe webhook setup" and it answers from this library, with links to the sources behind every point.

Hosted on [NoteSupreme](https://notesupreme.com/?ref=github). Nothing to install.

## What's inside

**🛡️ VPS Hardening**
- **Research Findings (Nov 2026):** how servers actually got hacked (open databases, open Docker ports, API keys leaking from odd places) and the setup most people agree on.
- **Round 2 Findings:** locking a private server behind Cloudflare Tunnel + Access service tokens, why Docker skips the UFW firewall and the `127.0.0.1:PORT:PORT` fix, and getting API keys off the box (Infisical, sops + age).
- **Tailscale vs Cloudflare:** a plain-English comparison, including Tailscale's non-commercial free plan.
- **Sources:** every video and thread the research used.

**🔐 App Security Checklists** — 9 plain-English checklists, each with its sources:

1. Free trial & API abuse
2. Database security (Supabase RLS, exposed databases, leaked service keys)
3. Bad packages & supply chain (Shai-Hulud worm waves, safe install settings)
4. AI agent & MCP risks (prompt injection, the lethal trifecta, least privilege)
5. Backups & recovery
6. Monitoring & alerts
7. Login & auth (BOLA, sessions, password resets, OAuth)
8. Payments & Stripe (fake webhooks, card testing, Radar)
9. Safe deployments & rollbacks

## Try asking

- "Using the VPS hardening MCP, give me a hardening checklist for a new Hetzner server running Docker."
- "Which of the database security mistakes apply to a Supabase app?"
- "Should I use Tailscale or Cloudflare Tunnel for a business?"

## Connect it

It's a remote MCP server (Streamable HTTP). No install, no API key, no sign-up: the link below includes its access token.

```
https://notesupreme.com/p/vps-hardening?token=nsp_6bmDN1j4mZCnQJCfL0rgDA
```

**Claude (claude.ai / Desktop):** Settings → Connectors → Add custom connector → paste the URL.

**Claude Code:**
```bash
claude mcp add --transport http vps-hardening "https://notesupreme.com/p/vps-hardening?token=nsp_6bmDN1j4mZCnQJCfL0rgDA"
```

**Cursor / VS Code / Windsurf** (`mcp.json` or the app's MCP settings):
```json
{
  "mcpServers": {
    "vps-hardening": { "url": "https://notesupreme.com/p/vps-hardening?token=nsp_6bmDN1j4mZCnQJCfL0rgDA" }
  }
}
```

**ChatGPT and any other MCP app:** add a remote MCP server / custom connector and paste the same URL.

Opened in a browser, the link explains how to connect.

## Disclaimer

General information compiled from public videos, posts and docs, not professional security advice. Test changes on a server you can rebuild.

## About NoteSupreme

[NoteSupreme](https://notesupreme.com/?ref=github) is long-term memory for your AI. You keep notes, specs and research as plain markdown, and every project gets its own MCP URL. Your AI searches what you already know instead of guessing, and uses up to 97% fewer tokens doing it than reading the files raw.

**One account, many Ships.** A Ship is one project: a vault of markdown notes with its own MCP URL and its own chat history. The Free plan includes 5 Ships, no card. Paid plans are unlimited.

**Every Ship gets three MCPs:**

| MCP | Who it's for | What it does |
|---|---|---|
| **Code Mode MCP** | you | One tool. Your AI writes a few lines of JavaScript, a sandbox walks the whole Ship, and only the answer comes back into your context. |
| **Regular MCP** | you, in any app | 23 plain tools (search, read, write, frontmatter, version history…) for apps that don't support Code Mode yet. |
| **Read-only MCP** | other people | Publish a Ship and give the link away. Guests get the whole knowledge graph and none of the write tools. **This repo's MCP is one of these.** |

**Built-in RAG on Google's Open Knowledge Format ([OKF](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md)), no vector database.** Each note is a markdown file that carries a type, a one-line description and tags, and notes link to each other. Your AI keyword-matches the right entry note, then follows the links a few hops, so it reads a small, relevant slice instead of everything. Nothing to embed or re-index, so a note you saved a second ago is already searchable. A short "how this Ship is organized" note tells every AI how to search that Ship.

**Also in the box:** a desktop workspace with AI chat beside your docs, 30-day version history on every write, import/export of markdown folders, a phone app with voice, and a 3D "2nd Brain" view of your whole account.

Build your own: **[notesupreme.com](https://notesupreme.com/?ref=github)**
