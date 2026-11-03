> Showcase repository: the code and data of this project are private; this README describes it. / Dépôt vitrine : le code et les données de ce projet sont privés ; ce README le décrit.

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
- A service Discord bot: `/where`, `/step`, `/project-memory`, `/listen`, `/debug` commands, alerts when the main agent's memory reaches 70 % then 85 %.
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

---

## Version française

# Pipeline Office, OpenClaw

Un serveur Discord où une équipe d'agents IA accompagnait un projet logiciel, de l'idée au cahier des charges puis à la construction.

## Le problème

Passer d'une idée floue à un logiciel construit demande de poser les bonnes questions, de faire des maquettes, de tenir des notes et de découper le travail. Pipeline Office devait faire ce chemin dans un salon de discussion, avec une ou plusieurs personnes. Chaque projet avait son propre salon. C'était un essai personnel d'orchestration multi-agents, mené de février à avril 2026.

## Comment ça marche

- Un agent « Manager » crée le salon du projet, pose les questions, conteste les idées faibles mais suit la décision de l'utilisateur.
- Un agent « Storm » produit les maquettes HTML de chaque section ; un agent « NoteBot » tient le fil de notes et la mémoire du projet.
- Un bot sans modèle de langage gère la configuration (langue, ton, projet neuf ou existant), la transcription de la voix et la navigation dans les étapes.
- Le déroulé suit un fichier d'étapes : brainstorm, puis cahier des charges, qui doit être validé explicitement avant la construction.
- La construction se fait épopée par épopée : un agent de code travaille seul, annonce la fin ou l'erreur dans le salon, et l'utilisateur relit.

## Ce qui est construit

- Une passerelle OpenClaw qui fait tourner les agents, avec des crochets d'injection de contexte et de mémoire.
- Un bot Discord de service : commandes `/where`, `/step`, `/project-memory`, `/listen`, `/debug`, alertes quand la mémoire de l'agent principal atteint 70 % puis 85 %.
- Une transcription vocale en français par un serveur faster-whisper local.
- Des tests statiques et des tests en direct sur Discord.
- Le dépôt principal compte 86 commits et 13 espaces de travail d'agents ; il contient aussi deux applications d'essai (un tableau de bord d'indicateurs économiques, un jeu de la bière).

État : arrêté. L'arrêt de la passerelle a été décidé le 12 avril 2026 ; le projet a été remplacé par Flux, le moteur de pipelines qui a suivi.

## Ce qui est public

Seule cette vitrine est publique ; le code reste privé.

## Pile technique

- Node.js, TypeScript, JavaScript
- OpenClaw
- discord.js, @discordjs/voice
- faster-whisper (modèle large-v3)
- PowerShell
- Playwright (applications d'essai)
