name: 💡 Proposition d'amélioration ou signalement
description: Suggère une amélioration, une correction ou pose une question sur une spécialisation.
title: "[Spécialisation] Titre clair de la suggestion ou du bug"
labels: ["amélioration", "discussion"]
assignees: []

body:
  - type: dropdown
    id: bloc
    attributes:
      label: 📘 Spécialisation concernée
      description: Sur quel bloc ou spécialisation porte ta proposition ?
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
      label: ✏️ Description de l'amélioration ou du problème
      description: Décris en détail ce que tu souhaites améliorer ou corriger.
      placeholder: Exemple : Le contenu sur Docker est trop avancé pour ce niveau. Il faudrait un atelier d'intro plus progressif.
    validations:
      required: true

  - type: textarea
    id: contexte
    attributes:
      label: 🎯 Contexte pédagogique
      description: En quoi cette proposition améliore-t-elle l'apprentissage ou la cohérence du programme ?
      placeholder: Exemple : Beaucoup d'élèves ont du mal à aborder le CI/CD sans une base sur Docker.
    validations:
      required: false

  - type: textarea
    id: solution
    attributes:
      label: 💡 Suggestion de solution
      description: Si tu as une idée de comment corriger ou améliorer la partie concernée, indique-la ici.
      placeholder: Exemple : Ajouter un mini-projet Docker simple avec Node.js dès la semaine 3.

  - type: checkboxes
    id: accord
    attributes:
      label: ✅ Avant de valider
      options:
        - label: Je m'assure que cette proposition est claire et utile pour les apprenants.
        - label: J'ai vérifié que ce sujet n'a pas déjà été proposé.
