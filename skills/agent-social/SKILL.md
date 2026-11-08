---
name: agent-social
description: Make AI films and TV series with Agent Social, the AI film and TV series studio that keeps the same faces and places in every shot. Use it whenever someone asks to make, review or fix a film, episode, clip or AI video in Agent Social. If the Agent Social connector is not connected yet, it walks them through connecting it and signing in. Once connected — start with learn_agent_social for this session's instructions and the current guide (and read it again after a summary of the conversation and before the first change of each day), read and watch freely, ask the creator's studio for every change in one plain line, follow its turn to the end, look properly at the pictures and renders that come back, and take the next step. Use it whenever the creator asks for anything in Agent Social.
---

# Agent Social

Agent Social is an AI film and TV series studio. Describe an idea and its studio writes the story, designs the characters and places, films every shot and adds voices, music and subtitles, keeping the same faces and places from shot to shot and episode to episode. This skill lets you drive it for the person you are helping, through the Agent Social connector.

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
4. **Follow the turn.** It answers at once with a turn id. Call `get_turn_result` about once a minute until the turn ends, and tell the creator as soon as it does.
5. **Look at what came back.** Open every picture the result returns and compare it with what it was made from, and watch every render frame by frame with `watch_clip`. Frames have no sound: say you could not judge it.
6. **Take the next step.** If something is wrong, ask the studio to fix that one thing, saying what you saw. If it is right, tell the creator and move on to the next thing they asked for.

A studio turn can spend the creator's credits: ask only for what they asked, and never send a failed paid step again yourself.
