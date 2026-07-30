# Issues GitHub Project — Lorcana Pocket

Colonnes : `Backlog` → `Sprint courant` → `En cours` → `À tester/review` → `Terminé`
Labels : `backend` `mobile` `design` `devops` `data`

---

## Épic 0 — Cadrage & setup

1. **[devops] Initialiser les repos `api` et `mobile`**
   Créer les deux repos GitHub, README de base (stack, prérequis), `.gitignore` adaptés Node/Expo.

2. **[devops] Configurer le GitHub Project (Kanban)**
   Colonnes, labels, milestones par épic.

3. **[devops] Setup Docker Compose (node, mysql, adminer)**
   `docker-compose.yml` avec service Node (hot-reload), MySQL, Adminer pour l'inspection de la BDD.

4. **[devops] Pipeline CI de base (GitHub Actions)**
   Lint + tests automatiques sur push/PR pour `api` et `mobile`.

---

## Épic 1 — Données Lorcana

5. **[data] Modéliser `Card` et `Set` dans Prisma**
   Champs : nom, ink, coût, rareté, texte, image, set, classifications.

6. **[data] Script d'import LorcanaJSON → MySQL**
   Script Node/TS qui télécharge/lit les fichiers LorcanaJSON et peuple la base via Prisma.

7. **[data] Commande de synchronisation périodique**
   Vérifier `metadata.json` de LorcanaJSON pour détecter les mises à jour et ne réimporter que si nécessaire.

---

## Épic 2 — API cœur (NestJS)

8. **[backend] Module `cards` (endpoints liste + détail + filtres)**
   `GET /cards`, `GET /cards/:id`, filtres par ink/rareté/set.

9. **[backend] Module `sets`**
   `GET /sets`, `GET /sets/:id`.

10. **[backend] Auth JWT (module `auth` + `users`)**
    Inscription/connexion, protection des routes utilisateur.

11. **[backend] Module `collection` (cartes possédées par utilisateur)**
    `GET /me/collection`, ajout/retrait de cartes.

12. **[backend] Documentation API (Swagger/OpenAPI via NestJS)**
    Génération auto de la doc pour faciliter le dev mobile.

---

## Épic 3 — Design UI/UX

13. **[design] Wireframe écran Accueil**
    Statut du prochain booster disponible, accès rapide collection.

14. **[design] Wireframe écran Ouverture de booster**
    Séquence pack → cartes révélées une à une.

15. **[design] Wireframe écran Collection**
    Grille de cartes, filtres (set, rareté, ink), indicateur possédé/manquant.

16. **[design] Wireframe écran Détail carte**
    Image grande taille, stats, exemplaires possédés.

---

## Épic 4 — App mobile : navigation & collection

17. **[mobile] Setup navigation (React Navigation ou Expo Router)**
    Structure des écrans + tab bar.

18. **[mobile] Écran Collection (grille + filtres)**
    Connexion à `GET /me/collection`, React Query pour le cache.

19. **[mobile] Écran Détail carte**

20. **[mobile] Service API centralisé (client HTTP + gestion du token JWT)**

---

## Épic 5 — Logique boosters

21. **[backend] Endpoint `POST /boosters/open`**
    Vérifie le cooldown 12h, tire les cartes selon les taux de rareté, enregistre dans `PullHistory`.

22. **[backend] Modèle de taux de drop par rareté**
    Table/config des probabilités par type de booster.

23. **[mobile] Écran Accueil : cooldown en temps réel**
    Countdown jusqu'au prochain booster disponible.

---

## Épic 6 — Animations d'ouverture

24. **[mobile] Setup Reanimated + Skia**

25. **[mobile] Animation : pack qui s'ouvre**

26. **[mobile] Animation : révélation carte par carte + effet holo sur les rares**

---

## Épic 7 — Fonctionnalités sociales/méta

27. **[backend][mobile] Cartes recherchées / progression de collection**
    % de complétion par set, cartes manquantes mises en avant.

28. **[backend] Statistiques d'ouverture (historique des pulls)**

---

## Épic 8 — DevOps avancé

29. **[devops] Déploiement staging (Railway ou Fly.io)**

30. **[devops] Monitoring/logs (Sentry pour le crash reporting mobile)**

---

## Épic 9 — Polish & tests

31. **[backend][mobile] Tests unitaires modules critiques (boosters, collection)**

32. **[mobile] Tests E2E parcours principal (ouverture de booster)**
