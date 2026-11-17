[English](README.md) · **Français**

# Pipeline Office

**Un serveur Discord où un Manager IA menait un projet logiciel de la première idée au code construit, une étape à la fois, une personne cliquant « Étape suivante » entre chacune.**

[![Un passage réel dans l'architecture, flèche par flèche, avec les livrables que le système a vraiment produits (cliquer pour la vidéo complète)](docs/demo.gif)](https://drive.google.com/file/d/1AgtCbBvHznlDH22xS-a1iaI28_zPqnuS/view)

*Un passage dans le système, flèche par flèche, avec de vrais livrables de ses projets de test (mars et avril 2026) (animation en anglais). [Vidéo complète (1:20)](https://drive.google.com/file/d/1AgtCbBvHznlDH22xS-a1iaI28_zPqnuS/view)*

## Ce qu'on fait avec

- **Un salon par projet.** `/create-project` l'ouvre ; un bot sans IA demande la langue, puis affiche un bouton Commencer.
- **Un Manager mène.** Il lit l'étape en cours et pose les questions, toujours avec une proposition d'abord, sans jargon.
- **Claude Code fait le travail.** Carte d'architecture, maquettes, histoires d'utilisateur, feuille de route, puis le code, épopée par épopée ; les résultats reviennent dans le salon et les maquettes sont mises en ligne.
- **Vous donnez le rythme.** Une barre de boutons sous chaque réponse : *Je suis perdu*, *Feedback*, *Save checkpoint*, *Next step* (avec une courte notation). `/where`, `/step` et `/project-memory` disent où on en est.
- **La voix aussi.** `/listen` transcrit ce qu'on dit dans un salon vocal.

## Architecture

![Architecture de Pipeline Office : vous écrivez dans le salon du projet ; le bot Pipeline-System gère les réglages et les boutons ; le Manager, porté par une passerelle OpenClaw, lit l'étape en cours et pose les questions ; il confie les tâches à une session Claude Code propre au salon, qui met les maquettes en ligne et renvoie les résultats par un webhook ; « Étape suivante » fait avancer le déroulé](docs/architecture.svg)

*Sept étapes : accueil, concept et conception de l'appli, cahier des charges et feuille de route, préparation, construction, rapprochement des histoires, recette et remise. Schéma en anglais : [architecture.en.svg](docs/architecture.en.svg).*

## État

- **Arrêté.** Construit du 4 février au 3 avril 2026 (514 commits), sur un PC Windows ; l'arrêt de la passerelle a été décidé le 12 avril 2026.
- **Essayé sur des projets de test.** Un planificateur de Gantt, un gestionnaire de tournois de jeux rétro, une appli web pour un cours d'une journée.
- **Deux architectures.** D'abord un bot par rôle (maquettes, notes, code) ; à partir du 2 avril 2026, une seule session Claude Code par salon les a remplacés.
- **Code privé.** Seule cette vitrine est publique.

---

**Anthony Hunt** · [ingevision.cloud](https://ingevision.cloud/?p=pipeline-office) · [LinkedIn](https://www.linkedin.com/in/anthony-hunt-3948a9196) · [GitHub](https://github.com/anthohunt)
