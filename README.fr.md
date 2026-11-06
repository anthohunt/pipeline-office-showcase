[English](README.md) · **Français**

**Anthony Hunt** · [Fiche du projet sur ingevision.cloud](https://ingevision.cloud/?p=pipeline-office) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [Profil GitHub](https://github.com/anthohunt)

> Dépôt vitrine : le code et les données de ce projet sont privés ; ce README le décrit.

# Pipeline Office (premier essai, 2026)

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
