# 🏛️ Les douze maisons du développement

Ce projet est né afin de me permettre d'expérimenter avec le web hosting Nginx, Linux (Alpine), Laravel, Docker, Devcontainer... et tout ce que le cosmos brûlant de ce Chevalier de Bronze a en elle!

Au terme de cette quête, j'espère avoir franchit les douze maisons du Zodiaque/développement web et mériter mon armure d'or!

---
## ♈ **Maison du Devcontainer**

#### 📖 **Documentation**

👉 [Documentation officielle](https://containers.dev/)
👉 [Documentation officielle (pour VS Code)](https://code.visualstudio.com/docs/devcontainers/containers)
👉 [Dev Containers CLI](https://github.com/devcontainers/cli)

#### 📋 **Résumé**
###### 🤷‍♀️ **Quoi?**
Un devcontainer est un environnement de développement conteneurisé. Il permet à une équipe de développeurs de faciliter l'onboarding de nouveaux membres sur un projet, ou de se remettre rapidement au travail, peu importe la machine de développement utilisé. Développé par Microsoft, un devcontainer est en parfaite synergie avec l'IDE Visual Studio Code et fonctionne avec Docker.
###### 🙎‍♀️ **Pourquoi?**
Dans mon cas, je voulais pouvoir passer facilement de mon laptop (Windows 10) à mon desktop (Windows 11) pour travailler sans me casser le pon-pon. Comme j'ai plusieurs projets personnels et que je ne veux pas perdre du temps à setup mes deux machines, la réalisation d'un devcontainer me semblait tout à fait appropriée pour mon cas d'usage.
###### 👷‍♀️ **Comment?**
J'utiliserai exclusivement VS Code à des fins de développement sauf pour explorer les limites du Devcontainer CLI.

#### 👩‍🔧 **Sous le capot**
- `devcontainer.json` : Le fichier principal de configuration d'un devcontainer. 

---
## ♉ **Docker (du Taureau)**

#### 📖 **Documentation**

👉 [Installer Docker sur WSL2 sans Docker Desktop](https://dev.to/felipecrs/simply-run-docker-on-wsl2-3o8)

---

## ♊ **Laravel (des Gémeaux)**

#### 📋 **Résumé**

#### 👩‍🔧 **Sous le capot**

#### 🦸‍♀️ **Au secours!**
- `Fatal error: Uncaught Error: Failed opening required '.../vendor/autoload.php'` 
	👉 Tu as oublié de faire `composer install` pour généré le dossier vendor et tous ses accessoires!
- `500 Server Error` dans le browser 
	👉 Tu as oublié de générer la clé d'application avec `php artisan key:generate`

---

## ♋ Nginx (du Cancer)

## ♌ Linux (du Lion)

## ♍ Alpine (de la Vierge)