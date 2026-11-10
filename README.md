# Agent Social

**Make a whole film or TV series from one idea, with the same faces in every shot.**

Agent Social is a complete AI film and TV series studio inside a chat. Tell it an idea, a story or a full script, and it does what a whole crew does:

- 📝 **Writes the screenplay**, chapter by chapter, and you can change any line.
- 🎭 **Casts the characters** and locks their faces, clothes and voices, so they never change from shot to shot or episode to episode.
- 🏙️ **Builds the places**, so every room, street and city looks the same each time the story returns to it.
- 🎬 **Films every shot as video**, cinematic and photoreal or animated, from anime to cartoon.
- 🗣️ **Adds dialogue, voices, music and subtitles**, then joins it all into one finished episode you can download and post.
- 📺 **Carries a series on.** Episode 2 starts straight from the last shot of Episode 1, with the same cast and world.

**Made with it:** *OVERCLOCK*, a sci-fi monster series set in India, every episode made by one person with no camera, crew or actors. Watch it at https://agentsocial.dev/overclock?utm_source=skills

**Ask for anything, in plain words:**

- "Make an AI movie: a kaiju rises from the sea off Mumbai in the monsoon, with the same hero in every scene."
- "Start a TV series about three sisters who run a bakery in Pune, with the same faces in every episode."
- "Make Episode 2 of my series and carry straight on from the last shot of Episode 1."
- "Turn my script into a film in anime style."
- "Review chapter 1 of my episode and fix what's off."

This repository holds the Agent Social skill for AI agents such as Claude Code, Codex, Cursor and OpenClaw. With it, your agent can make, review and fix films and TV series, short videos, memes, research and social posts in your [Agent Social](https://agentsocial.dev/?utm_source=skills) account straight from a conversation.

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
