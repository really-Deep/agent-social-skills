# Agent Social

**AI film and TV series studio: the same faces and places in every shot, from idea to finished episode.**

This repository holds the Agent Social skill for AI agents such as Claude Code, Codex, Cursor and OpenClaw. With it, your agent can make, review and fix films and TV series in your [Agent Social](https://agentsocial.dev/?utm_source=skills) account straight from a conversation.

## What it does

Your agent reads your series, episodes, chapters and clips, watches the rendered clips frame by frame, and compares them with the pictures and story they were made from. It asks your Agent Social studio for every change — new films and episodes, rewritten clips, characters, places, voices, rendering, music and subtitles — follows the work until it is done, and checks what came back before telling you.

## Install

1. Add the skill:

   ```bash
   npx skills add really-Deep/agent-social-skills
   ```

   In Claude Code you can also add it as a plugin:

   ```
   /plugin marketplace add really-Deep/agent-social-skills
   /plugin install agent-social@agent-social
   ```

2. Connect the Agent Social connector once, and sign in with your Agent Social account:
   - **Claude (web, Desktop, mobile, Cowork):** Settings → Connectors → Add custom connector, name it Agent Social, paste `https://mcp.agentsocial.dev/mcp`, then Connect and Allow.
   - **Claude Code:** run `claude mcp add --transport http agentsocial https://mcp.agentsocial.dev/mcp`, then `/mcp` → agentsocial → Authenticate.
   - **Other agents:** add `https://mcp.agentsocial.dev/mcp` as a streamable HTTP MCP server.

   The skill tells your agent to load its instructions from the connector at the start of each session, so it always works the current way without you updating anything.

## Use it

Ask in plain words:

- "Review chapter 1 of my episode and fix what's off."
- "Make the next episode, carrying straight on from the last shot."
- "Start a TV series about three sisters who run a bakery in Pune, with the same faces in every episode."

Follow along live: your agent shares the link to the episode's chat in Agent Social, where every change appears as it happens.

Reading and watching are free. The studio's work — rendering, new pictures, music, voiceover and the rest — uses your Agent Social credits, exactly as in the app, and your agent asks for it only when you did.

## Data

The skill talks only to your own Agent Social account, through the Agent Social connector you sign in to. It stores nothing itself. What your agent changes is recorded in your episode's chat, labelled as coming from your agent.

Support: support@agentsocial.dev · [agentsocial.dev](https://agentsocial.dev/?utm_source=skills)
