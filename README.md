# LaFabrik — Circuit iPad (version locale)

Application mobile en **fichier unique** (`index.html`) pour gérer un événement sur **un seul iPad**.

## Correctifs importants

- IDs produits/logs en **entiers incrémentaux** (plus de `Date.now()+Math.random()`).
- LocalStorage sécurisé avec fallback mémoire si erreur d'accès.
- Export CSV compatible Safari local via `data:` URI.
- Confirmation avant clôture journée et clôture week-end.

## UX / Fonctionnalités

- Annulation rapide depuis **Ventes** (bouton `↺` par carte).
- Stock restant + vendu affichés en temps réel sur les cartes vente.
- Filtres de catégories dans Ventes (pour éviter de scroller tout).
- Catégorie fusionnée : **Calendriers & Circuits** (F1 + MotoGP ensemble).
- Historique clair dans Résumé (heure + modèle + statut + annulation ligne).
- Gestion week-end déplacée dans **Résumé**.
- Résumé affiche **CA journée** et **CA événement**.
- Export CSV débloqué **uniquement après clôture week-end**.

## Clôtures

- **Clôturer la journée**
  - Passe au jour suivant (Jour 1, Jour 2, Jour 3...).
  - Conserve le stock restant réel.
- **Clôturer le week-end**
  - Bloque les ventes.
  - Débloque l'export CSV final.

## Déploiement

1. Copier `index.html` sur l'iPad.
2. Ouvrir dans Safari/Chrome.
3. Utiliser hors-ligne (données en localStorage).

Aucune installation, aucun build, aucune dépendance.
