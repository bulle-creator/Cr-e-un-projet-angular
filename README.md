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
Créer un composant :

```bash
ng generate component login
```

Dans le *login.html* :

```bash
<link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel="stylesheet">

<div class="center">
    <div class="container" [class.active]="isActive">
        <div class="from-box login">
            <form action="">
                <h1>Login</h1>
                <div class="input-box">
                    <input type="text" placeholder="Username" require>
                    <i class='bx bx-user'></i>
                </div>
                <div class="input-box">
                    <input type="password" placeholder="Password" require>
                    <i class='bx bxs-lock-alt' ></i>
                </div>
                <div class="forgot-link">
                    <a href="#">Mot de passe oublier?</a>
                </div>

                <a routerLink="/location-car" routerLinkActive="active">
                  <button type="submit" class="btn">Login</button></a>
            </form>
        </div>


        <div class="from-box register">
            <form action="">
                <h1>Registration</h1>
                <div class="input-box">
                    <input type="text" placeholder="Name and Lastname" require>
                    <i class='bx bx-user'></i>
                </div>
                <div class="input-box">
                    <input type="text" placeholder="Username" require>
                    <i class='bx bx-user'></i>
                </div>
                <div class="input-box">
                    <input type="text" placeholder="Telephhone" require>
                    <i class='bx bx-user'></i>
                </div>
                <div class="input-box">
                    <input type="email" placeholder="Email" require>
                    <i class='bx bxs-envelope'></i>
                </div>
                <div class="input-box">
                    <input type="password" placeholder="Password" require>
                    <i class='bx bxs-lock-alt' ></i>
                </div>


                  <button type="submit" class="btn">Register</button>
            </form>
        </div>

        <div class="toggle-box">
            <div class="toggle-panel toggle-left">
                <h1>Bienvenue!</h1>
                <p>Tu n'as pas de compte?</p>
                <button class="btn register-btn" (click)="register()">Register</button>
            </div>

            <div class="toggle-panel toggle-right">
                <h1>Bon retour!</h1>
                <p>Tu as déja un compte?</p>
                <button class="btn login-btn" (click)="login()">Login</button>
            </div>
        </div>
    </div>
</div>
```

Dans le *login.css* :

```bash
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family:'Poppins', sans-serif;
}
.center {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container{
    position: relative;
    width: 850px;
    height: 550px;
    background: #fff;
    border-radius: 30px;
    box-shadow: 0 0 30px rgba(0,0,0,.2);
    margin: 20px;
    overflow: hidden;
}

.from-box{
    position: absolute;
    right: 0;
    width: 50%;
    height: 100%;
    background: #fff;
    display: flex;
    align-items: center;
    color: #333;
    text-align: center;
    padding: 40px;
    z-index: 1;
    transition: .6s ease-in-out 1.2s, visibility 0s 1s ;
}

.container.active .from-box{
    right: 50%;
}

.from-box.register{
    visibility: hidden;
}

.container.active .from-box.register{
    visibility: visible;
}

form{
    width: 100%;
}

.container h1{
    font-size: 36px;
    margin: -10px 0;
}

.input-box{
    position: relative;
    margin: 30px 0;
}

.input-box input{
    width: 100%;
    padding: 13px 50px 13px 20px;
    background: #eee;
    border-radius: 8px;
    border: none;
    outline: none;
    font-size: 16px;
    color: #333;
    font-weight: 500;
}

.input-box input::placeholder {
    color: #888;
    font-weight: 400;
}

.input-box i{
    position: absolute;
    right: 20px;
    top: 50%;
    transform: translateY(-50%);
    font-size: 20px;
    color: #888;
}
.forgot-link{
    margin: -15px 0 15px;
}

.forgot-link a{
    font-size: 14.5px;
    color: #333;
    text-decoration: none;
}

.btn{
    width: 100%;
    height: 48px;
    background: #7994E7;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,.1);
    border: none;
    cursor: pointer;
    font-size: 16px;
    color: #fff;
    font-weight: 600;
}

.container p{
    font-size: 14.5px;
    margin: 15px 0;
}

.social-icons{
    display: flex;
    justify-content: center;
}

.social-icons a{
    display: inline-flex;
    padding: 10px;
    border: 2px solid #ccc;
    border-radius: 8px;
    font-size: 24px;
    color: #333;
    text-decoration: none;
    margin: 0 8px;
}

.toggle-box {
    position: absolute;
    width: 100%;
    height: 100%;
}

.toggle-box::before{
    content: '';
    position: absolute;
    left: -250%;
    width: 300%;
    height: 100%;
    background: #7494ec;
    border-radius: 150px;
    z-index: 2;
    transition: 1s ease-in-out;
}

.container.active .toggle-box::before {
    left: 50%;
}

.toggle-panel {
    position: absolute;
    width: 50%;
    height: 100%;
    color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 2;
    transition: .8s ease-in-out;
}

.toggle-panel.toggle-left {
    left: 0;
    transition-delay: 1s;
}

.container.active .toggle-panel.toggle-left {
    left: -50%;
    transition-delay: .5s;
}


.toggle-panel.toggle-right {
    right: -50%;
    transition-delay: .5s;
}

.container.active .toggle-panel.toggle-right {
    right: 0;
    transition-delay: 1s;
}

.toggle-panel p{
    margin-bottom: 20px;
}

.toggle-panel .btn{
    width: 160px;
    height: 46px;
    background: transparent;
    border: 2px solid #fff;
    box-shadow: none;
}

@media screen and (max-width:650px)  {
    .container{
        height: calc(100vh - 40px);
    }

    .from-box{
        bottom: 0;
        width: 100%;
        height: 70%;
    }

    .container.active .from-box{
        right: 0;
        bottom: 30%;
    }

    .toggle-box::before{
        left: 0;
        top: -270%;
        width: 100%;
        height: 300%;
        border-radius: 20vw;
    }

    .container.active .toggle-box::before{
        left: 0;
        top: 70%;
    }

    .toggle-panel{
        width: 100%;
        height: 30%;
    }

    .toggle-panel.toggle-left{
        top: 0;
    }

    .container.active .toggle-panel.toggle-left{
        left: 0;
        top: -30%;
    }

    .toggle-panel.toggle-right{
        right: 0;
        bottom: -30%;
    }

    .container.active .toggle-panel.toggle-right{
        bottom: 0;
    }
}

@media screen and (max-width: 400px)  {
    .from-box{
        padding: 20px;
    }
    .toggle-panel h1{
        font-size: 30px;
    }
}
```


Dans le *login.ts* :

```bash
export class LoginComponent {

    isActive = false;

  register() { this.isActive = true; }
  login() { this.isActive = false; }
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
