# Projet DevOps – Ahlam

##  Description
Ce projet a pour objectif de mettre en place une chaîne **CI/CD** simple pour une application **Node.js**, en utilisant **GitHub**, **GitHub Actions**, **Jenkins** et **Docker**.

L’application Node.js affiche un message simple et sert de support pour tester l’intégration continue et le workflow DevOps.



##  Technologies utilisées
- **Node.js**
- **Git & GitHub**
- **GitHub Actions** (CI)
- **Jenkins** (Pipeline CI)
- **Docker** (exécution de Jenkins)



##  Structure du projet

├── .github/workflows/ci.yml
├── Jenkinsfile
├── server.js
├── package.json
└── README.md



##  Workflow DevOps mis en place

###  Gestion du code avec Git
- Branche **main** : branche principale
- Branche **dev** : développement
- Utilisation de **Pull Request** pour intégrer `dev` vers `main`



### Intégration Continue avec GitHub Actions
- Un workflow CI est déclenché automatiquement à chaque `push`
- Vérifie le bon fonctionnement de l’application Node.js
- Les checks doivent être **valides (✔️)** avant le merge



###  Jenkins Pipeline
- Jenkins est exécuté dans un **conteneur Docker**
- Le pipeline est défini dans le fichier `Jenkinsfile`
- Étapes principales :
  - Récupération du code depuis GitHub
  - Exécution du pipeline CI
  - Vérification du succès du build


###  Docker
- Jenkins est déployé via **Docker Desktop**
- L’utilisation de Docker permet un environnement isolé et reproductible



## ▶️ Lancer l’application Node.js
```bash
npm install
node server.js
