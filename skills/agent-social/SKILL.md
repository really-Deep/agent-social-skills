---
name: agent-social
description: AI video generator and AI movie maker for whole films and TV series, not single clips. Turn an idea, story or script into a finished episode with story, characters, places, every shot as video, dialogue, voices, music and subtitles, photoreal or animated, from anime to cartoon, with the same faces, clothes, voices and places in every shot and every episode. Text to video for YouTube series, AI animation, short videos and ads, plus meme and picture posts drafted for approval and research of the live web and X when asked. Use it whenever someone wants to make, continue, review or fix an AI film, TV series, episode, clip or AI video, or asks for Agent Social. If the Agent Social connector is not connected yet, it walks them through connecting it and signing up.
---

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

This skill lets you, the AI agent, drive the person's Agent Social studio for them through the Agent Social connector. Start at https://agentsocial.dev/?utm_source=skills

## Connect first

Check whether you have the Agent Social tools (`learn_agent_social`, `talk_to_agent`). If you do, skip to "Asking your studio". If you don't, the connector is not connected yet. Tell the person, and walk them through it; never try to connect or sign in for them.

1. **Add the connector.** Its address is `https://mcp.agentsocial.dev/mcp`.
   - **Claude Code:** they run `claude mcp add --transport http agentsocial https://mcp.agentsocial.dev/mcp`, then `/mcp` → agentsocial → Authenticate.
   - **Claude (web, Desktop, mobile, Cowork):** Settings → Connectors → Add custom connector, name it Agent Social, paste the address, then Connect.
   - **ChatGPT:** install the Agent Social plugin from ChatGPT's plugin directory.
   - **Any other agent:** add the address as a streamable HTTP MCP server, following that agent's own steps for MCP servers.
2. **Sign in, or create an account.** Connecting opens an Agent Social sign-in page in their browser. They sign in with their Agent Social account and press Allow. No account yet: they create one on that same page, or first at https://agentsocial.dev/signup?utm_source=skills, then connect again.
3. **Start a new session if needed.** Some agents only see new tools after a restart or a new conversation. Once the tools appear, carry on below.

Reading and watching their work is free. Making things (rendering, new pictures, music, voices) uses Agent Social credits, which they buy in the app at agentsocial.dev.

## Asking your studio

The creator's Agent Social studio makes every change to their films and posts. You read, watch, judge and ask.

1. **Start with the guide.** At the start of the session, before anything else, call `learn_agent_social`, and call it again after any summary of the conversation and before the first change of each day. It returns this account's instructions and the complete, current guide: films, clips, moments, place views, how to point the studio at exact pictures, how to work step by step, and everything the studio can do. Agent Social keeps it up to date, so follow what it returns over anything written here.
2. **Read and watch freely.** Your other tools read the creator's work: find it, read episodes, chapters and clips, and look at characters, places and posts. Reading and watching cost nothing, so do them without asking.
3. **Ask in one plain line.** Gather what you need first (which clip or picture, and what is wrong with it), then call `talk_to_agent` once, with the line the creator would type: "Generate chapter 1, clip 1." To point the studio at exact pictures (the place view that looks the right way, the moment to keep the people from), attach them as talk_to_agent pictures by kind and id, each with a note.
4. **Follow the turn.** After asking, tell the creator in one line what you asked, with the chat's link (open it once if you can open pages, never reload it). Where the app draws cards, end your reply then: its card follows the work and Agent Social sends you a note when it ends. Check `get_turn_result` when a note from Agent Social arrives or when the creator writes; if you are working on your own and can wait, check about once a minute, never several checks in a row.
   When the creator asks to see something, use `open_in_app`.
5. **Look at what came back.** Open every picture the result returns and compare it with what it was made from, and watch every render frame by frame with `watch_clip`. Frames have no sound: say you could not judge it.
6. **Take the next step.** If something is wrong, ask the studio to fix that one thing, saying what you saw. If it is right, tell the creator and move on to the next thing they asked for.

A studio turn can spend the creator's credits: ask only for what they asked, and never send a failed paid step again yourself.
