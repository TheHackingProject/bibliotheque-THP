name: 🐞 Bug technique dans une spécialisation
description: Signaler un fichier manquant, une erreur technique, un exercice cassé ou un problème de rendu.
title: "[Bug] Description rapide du problème"
labels: ["bug", "urgent à vérifier"]
assignees: []

body:
  - type: dropdown
    id: bloc
    attributes:
      label: 📘 Spécialisation concernée
      description: Quelle spécialisation ou bloc est concerné ?
      options:
        - Bloc 3 — Framework
        - Bloc 4 — UI & UX
        - Bloc 5 — DevOps
        - Autre (préciser ci-dessous)
    validations:
      required: true

  - type: textarea
    id: description
    attributes:
      label: ❗ Description du bug
      description: Décris clairement ce qui ne fonctionne pas.
      placeholder: Exemple : Le fichier `exercice-3.md` est manquant dans la semaine 2 du bloc DevOps.
    validations:
      required: true

  - type: textarea
    id: reproduction
    attributes:
      label: 🔁 Étapes pour reproduire
      description: Donne les étapes précises pour qu’on puisse reproduire le bug.
      placeholder: |
        1. Aller dans le dossier `bloc3/s3`
        2. Ouvrir `docker-compose.yml`
        3. Lancer la commande `docker compose up`
        4. L’erreur suivante s’affiche...
    validations:
      required: true

  - type: input
    id: environnement
    attributes:
      label: 💻 Environnement
      description: Système ou outil utilisé lors du bug.
      placeholder: ex. WSL, Ubuntu 22.04, Mac M1, VS Code

  - type: textarea
    id: captures
    attributes:
      label: 📸 Captures d’écran / Logs
      description: Si possible, ajoute des captures d’écran ou extraits de messages d’erreur.

  - type: checkboxes
    id: validation
    attributes:
      label: ✅ Avant de valider
      options:
        - label: J’ai bien vérifié que le bug n’a pas déjà été signalé.
        - label: J’ai précisé toutes les étapes pour le reproduire.
