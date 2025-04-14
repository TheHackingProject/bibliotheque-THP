[Index Bibliothèque THP](https://github.com/TheHackingProject/bibliotheque-THP/wiki) > [SOMMAIRE OUTILS]((https://github.com/TheHackingProject/bibliotheque-THP/wiki/sommaire_outils)) > Outils Github

___

# Outils Github

![](https://picsum.photos/1024/400)

## 📄 Description et/ou objectif

Cette liste permet d'afficher les outils mis en avant par THP pour nos étudiants

## Le .github

Le dossier `.github` dans un dépôt GitHub est un répertoire spécial qui permet de centraliser la configuration et la personnalisation du fonctionnement du dépôt, notamment pour améliorer la collaboration et l'automatisation.

Il permet de :

- Personnaliser les Issues et Pull Requests : via des templates (issue_template.md, pull_request_template.md), on peut guider les contributeurs pour qu’ils fournissent des informations claires et structurées, ce qui facilite le tri, la compréhension et le traitement rapide des contributions.
- Automatiser avec GitHub Actions : en y ajoutant des fichiers de workflows dans .github/workflows, on peut automatiser des tâches comme les tests, les déploiements, ou la mise à jour de documentation à chaque push ou pull request.
- Configurer les fichiers de communauté : comme le CODE_OF_CONDUCT.md, CONTRIBUTING.md, ou FUNDING.yml, pour structurer l'engagement communautaire autour du projet.
- Ajouter des Webhooks : bien que les webhooks ne soient pas définis directement dans .github, ce dossier peut contenir des scripts ou des workflows (via GitHub Actions) qui envoient des notifications vers des services comme Discord, Slack ou autres via des requêtes HTTP. Par exemple, on peut déclencher une notification sur Discord à chaque nouvelle PR ou issue ouverte, en utilisant un webhook Discord dans une GitHub Action.

---

### 🔐 Gestion des **Secrets** GitHub

Pour que certains **workflows GitHub Actions** fonctionnent correctement (par exemple pour envoyer des messages sur Discord, déployer une app, ou accéder à une API externe), il est souvent nécessaire de **définir des variables secrètes** appelées **secrets**.

#### ➕ Ajouter un secret dans un **repository individuel**

1. Va dans l’onglet **"Settings"** du repository concerné.
2. Clique sur **"Secrets and variables" > "Actions"**.
3. Clique sur **"New repository secret"**.
4. Renseigne le nom (ex: `DISCORD_WEBHOOK_URL`) et la valeur (le token ou l'URL) puis valide.

Ce secret ne sera utilisable que dans **ce repository**.

#### 🏢 Ajouter un secret **dans une organisation** (commun à tous les repos)

Si tes dépôts font partie d'une **organisation GitHub** (comme c’est le cas pour THP), tu peux centraliser les secrets pour tous les repos :

1. Va dans les **Settings de l’organisation**.
2. Dans le menu latéral, clique sur **"Secrets and variables" > "Actions"**.
3. Clique sur **"New organization secret"**.
4. Choisis à quels dépôts ce secret est accessible (tous ou sélection).
5. Renseigne nom et valeur du secret, comme pour un repo classique.

Cela permet d’éviter de répéter les mêmes secrets dans chaque dépôt.

---

### 📁 Déployer le dossier `.github` dans d’autres dépôts

Même si THP met à disposition un dossier `.github` centralisé dans [ce dépôt](https://github.com/TheHackingProject/.github), il peut être nécessaire de le **copier dans certains repositories spécifiques** si :

- Tu veux **surcharger** ou personnaliser certains comportements uniquement pour ce repo.
- Tu veux **ajouter des workflows spécifiques** dans `.github/workflows` propres à ce projet.
- Tu veux **tester un nouveau fonctionnement sans impacter les autres dépôts**.

Dans ce cas, tu peux créer un dossier `.github/` à la racine du repo concerné, et y ajouter uniquement les fichiers nécessaires (workflow, template, etc.). GitHub utilisera en priorité le `.github` local au repo plutôt que celui de l’organisation.

---

## le README originel

Ce repositorie spécial, nommé comme mon **nom d'utilisateur GitHub**, permet d’afficher un **README personnalisé directement sur ma page de profil**.

### 🔍 À quoi ça sert ?

Grâce à ce fichier `README.md`, je peux :
- Me présenter aux visiteurs de mon profil GitHub,
- Mettre en avant mes projets, compétences ou liens utiles,
- Ajouter des visuels, des statistiques, ou des badges dynamiques,
- Créer une **identité de développeur** claire et professionnelle.

### ⚙️ Fonctionnement

Il suffit de créer un repositorie public avec exactement le **même nom que ton nom d’utilisateur GitHub** (ex. `mon-pseudo/mon-pseudo`) et d’y ajouter un fichier `README.md`. Le contenu de ce fichier s’affichera en haut de ton profil GitHub.

> Pour activer l'affichage, pense à cocher l’option **"Public"** lors de la création du repo.

### 🛠 Quelques idées de contenu

- Une présentation rapide (qui je suis, ce que je fais)
- Un résumé de mes projets clés
- Des badges (langages, stats, contributions, etc.)
- Des liens vers mon portfolio, LinkedIn, etc.
- Une section fun : GIF, blague de dev, chatbot, etc.

## 📚 Liste des Outils Github
- Générateur de README => [readme.so](https://readme.so/fr)

<div align="center">

[Précédent](https://github.com/TheHackingProject/bibliotheque-THP/wiki/outil_html)

</div>