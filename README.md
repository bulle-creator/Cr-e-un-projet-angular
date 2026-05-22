# Tutoriel Angular

## Introduction

Ce tutoriel explique comment créer et lancer un projet avec Angular.

---

# Prérequis

Avant de commencer, installer :

* [Node.js](https://nodejs.org?utm_source=chatgpt.com)
* npm (installé avec Node.js)

Vérifier les versions :

```bash
node -v
npm -v
```

---

# Installation d’Angular CLI

Installer Angular CLI globalement :

```bash
npm install -g @angular/cli
```

Vérifier l’installation :

```bash
ng version
```

---

# Création du projet

Créer un nouveau projet Angular :

```bash
ng new mon-projet
```

Le terminal demandera :

* Activation du routing
* Choix du format de style (CSS, SCSS, etc.)

Entrer ensuite dans le dossier du projet :

```bash
cd mon-projet
```

---

# Lancer le projet

Démarrer le serveur de développement :

```bash
ng serve
```

Application accessible sur :

```text
http://localhost:4200
```

---

# Structure du projet

Exemple de structure générée :

```text
mon-projet/
├── src/
├── app/
├── angular.json
├── package.json
└── tsconfig.json
```

---

# Commandes utiles

Créer un composant :

```bash
ng generate component mon-composant
```

Version courte :

```bash
ng g c mon-composant
```

Créer un service :

```bash
ng g service mon-service
```

Build de production :

```bash
ng build
```

---

# Documentation officielle

* [Angular Documentation](https://angular.dev?utm_source=chatgpt.com)
* [Angular CLI](https://angular.dev/tools/cli?utm_source=chatgpt.com)

---

# Auteur

Tutoriel Angular de base pour débutants.
