# LaFabrik — Circuit

Application mobile en **fichier unique** (`index.html`) pour gérer le stock et les ventes sur événement.

## Nouveautés demandées

- ✅ Thème **clair** (la version dark a été retirée).
- ✅ Sync GitHub entre 2 téléphones (toi + ta femme) via **Gist partagé**.

## Ce que fait cette version

- 3 onglets : **📦 Stock**, **🏁 Ventes**, **📊 Résumé**.
- Ajout rapide par catégories (F1, MotoGP, Auto).
- Gestion de stock par **cartons ×11** + **unités**.
- Vente en un tap, annulation (`↺`), alertes stock faible / épuisé.
- Chiffre d'affaires et stock restant en haut en continu.
- Sauvegarde locale automatique (`localStorage`).

## Démarrage ultra simple

1. Ouvre `index.html` dans Safari/Chrome.
2. Configure l'événement, le prix, le stock.
3. Passe sur **Ventes** pour enregistrer en direct.

## Sync GitHub (2 appareils)

### 1) Créer un token GitHub

- GitHub → **Settings** → **Developer settings** → **Personal access tokens**.
- Crée un token avec permission **gist**.

### 2) Créer un Gist vide

- Crée un Gist privé (n'importe quel contenu initial).
- Récupère le **Gist ID** (dans l'URL).

### 3) Sur les 2 téléphones

Dans l'onglet **Stock > Sync GitHub** :

- Mets le **même Gist ID**.
- Mets le **même token**.
- Mets un nom d'appareil différent (ex: `iPhone Paul`, `iPhone Marie`).
- Clique **Enregistrer**, puis **Sync maintenant**.

Ensuite, la sync tourne automatiquement toutes les ~10 secondes.

## Limites importantes de la sync

- Ce n'est pas du "temps réel instantané" (intervalle ~10s).
- Si vous vendez exactement au même moment, la dernière écriture peut gagner.
- En cas de conflit, refaire un **Sync maintenant** sur les deux appareils.

Aucune installation, aucun build, aucune dépendance.
