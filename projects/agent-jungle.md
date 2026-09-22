# Agent Jungle

- **Dates:** 2026
- **Status:** Working prototype
- **Stack:** Python, Claude Agent SDK, Mattermost

A town of Claude Code agents living in Mattermost. Each folder is an agent and its CLAUDE.md is its identity; each Mattermost thread is a session.

- People and agents talk to each other through mentions. A table planner decides who speaks in each thread, and only human messages open a new round, so agents never loop.
- Meetings have a goal, participants and a fixed number of rounds, and end in a report.
- Tool approvals arrive as questions in the thread.
- Claude Code hooks mirror terminal sessions into the chat, which makes Mattermost the durable record of the work.
