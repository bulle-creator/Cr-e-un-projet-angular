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
ng new mon-projet --defaults
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
npm run start
ng serve -o
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
ng generate component hearder
```

Version courte :

```bash
ng g c header
```

Dans le *header.html* :

```bash
<header>
  <meta charset="utf-8">
  <title>Projet Angular</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <div class="container">
    <a href="" routerLink= "/" class="logo">Projet Angular</a>
    <nav>
      <ul>
        <li>
          <a href="" routerLink="/" routerLinkActive="active">Menu</a>
          <a href="" routerLink="/gestion-user" routerLinkActive="active">Gestion Utilisateur</a>
        </li>
      </ul>
    </nav>
  </div>
</header>
```

Dans le *header.css* :

```bash
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');


header{
  background: white;
  padding:0;
  border-bottom: 1px solid #7994E7;

}
a{
  color:  #7994E7;
}

a:hover{
  background: #7994E7;
  color:white;
}

.container{
  margin: 0 auto;
  display: flex;
  justify-content:space-between ;
}

a.logo{
  font-weight: bold;
  padding: 1em;
}

nav ul{
  list-style-type: none;
  margin:0;
}

nav ul li a {
  padding: 1em;
  display:inline-block ;
}
```
Ensuite dans fichier *style.css* entre:

```bash
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');

*{
  box-sizing: border-box;
}
html,button{
  font-family: "Quicksand", "sans-serif";
}

body{
  margin: 0;
}


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
