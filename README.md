**English** · [Français](README.fr.md)

> Showcase repository: the code and data of this project are private; this README describes it.

# Pipeline Office, OpenClaw

A Discord server where a team of AI agents guided a software project from the idea to the specification, then to the build.

## The problem

Going from a vague idea to built software means asking the right questions, making mockups, keeping notes and splitting the work. Pipeline Office was meant to do this inside a chat channel, with one or several people. Each project had its own channel. It was a personal experiment in multi-agent orchestration, run from February to April 2026.

## How it works

- A "Manager" agent creates the project channel, asks the questions, challenges weak ideas but follows the user's decision.
- A "Storm" agent produces HTML mockups for each section; a "NoteBot" agent keeps the notes thread and the project memory.
- A bot with no language model handles setup (language, tone, new or existing project), voice transcription and navigation between steps.
- The flow follows a file of steps: brainstorm, then a specification, which must be explicitly approved before the build.
- The build goes epic by epic: a coding agent works on its own, reports completion or error in the channel, and the user reviews.

## What is built

- An OpenClaw gateway that runs the agents, with hooks that inject context and memory.
- A service Discord bot: `/where`, `/step`, `/project-memory`, `/listen`, `/debug` commands, alerts when the main agent's memory reaches 70% then 85%.
- French voice transcription through a local faster-whisper server.
- Static tests and live tests on Discord.
- The main repository has 86 commits and 13 agent workspaces; it also holds two trial applications (an economic indicators dashboard, a beer game).

Status: stopped. Shutting down the gateway was decided on 12 April 2026; the project was replaced by Flux, the pipeline engine that followed.

## What is public

Only this showcase is public; the code stays private.

## Tech stack

- Node.js, TypeScript, JavaScript
- OpenClaw
- discord.js, @discordjs/voice
- faster-whisper (large-v3 model)
- PowerShell
- Playwright (trial applications)
