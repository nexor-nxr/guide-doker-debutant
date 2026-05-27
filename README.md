#  Guide Docker pour Débutants

Ce dépôt contient le code source Python et la structure HTML/CSS permettant de générer un guide pédagogique complet, moderne et professionnel sur **Docker** au format PDF. Le document inclut une mise en page de type livre (couverture personnalisée, table des matières automatique, blocs de code stylisés et boîtes de message informatives).

La compilation est gérée de manière fluide par la bibliothèque **WeasyPrint**, qui transforme le code HTML/CSS moderne (incluant le support des règles `@page` pour l'impression) en un document PDF A4 parfait.

---

##  Sommaire du Guide

Le document généré couvre l'intégralité des notions indispensables pour débuter sereinement avec la conteneurisation :

1. **Introduction à Docker** : Définition, fonctionnement et tableau comparatif complet avec les Machines Virtuelles (VM).
2. **Installation** : Prérequis système et tutoriel pas à pas pour Debian / Ubuntu (configuration des dépôts, clés GPG, et post-installation sans `sudo`).
3. **Commandes essentielles** : Synthèse sous forme de tableaux pour la gestion des images, des conteneurs et le diagnostic en temps réel (`logs`, `stats`, `exec`).
4. **Zoom sur `docker run`** : Syntaxe globale et fiches explicatives des options du quotidien (`-d`, `-p`, `-v`, `-e`, etc.).
5. **Volumes & Réseaux** : Concepts de persistance des données et d'isolation réseau avec exemples pratiques (déploiement MySQL).
6. **Docker Compose** : Automatisation d'architectures multi-tiers à l'aide de fichiers YAML (`compose.yml`).
7. **Portainer** : Déploiement et configuration de l'interface graphique d'administration web.
8. **Dépannage & Bonnes pratiques** : Guide de résolution des erreurs courantes, commandes de nettoyage de disque (`system prune`) et les 5 Règles d'Or du bon praticien.

---

## 🛠️ Prérequis et Dépendances

Pour exécuter le script et générer le PDF, vous devez disposer de **Python 3** et installer la bibliothèque **WeasyPrint**. 

### 1. Dépendances système (requises par WeasyPrint)
WeasyPrint nécessite des bibliothèques système pour le rendu des polices et des graphiques (Pango, Cairo, GdkPixbuf).

* **Sur Ubuntu / Debian :**
  ```bash
  sudo apt update
  sudo apt install build-essential python3-dev python3-pip python3-setuptools libcairo2 libpango-1.0-0 libpangocairo-1.0-0 libgdk-pixbuf2.0-0 libffi-dev shared-mime-info
