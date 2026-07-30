# Lorcana TCG Pocket

Monorepo npm workspaces pour l'application Lorcana TCG Pocket.

## Stack

- **API** (`apps/api`) : [NestJS](https://nestjs.com/) (TypeScript) + [Prisma](https://www.prisma.io/) sur MySQL.
- **Mobile** (`apps/mobile`) : [Expo](https://expo.dev/) (TypeScript) avec [Expo Router](https://docs.expo.dev/router/introduction/).
- **Shared** (`packages/shared`) : types TypeScript partagés entre l'API et le mobile.
- **Base de données** : MySQL 8.0, administrable via [Adminer](https://www.adminer.org/).

## Structure

```
apps/
  api/       # NestJS + Prisma
  mobile/    # Expo + Expo Router
packages/
  shared/    # Types partagés (ex: Card)
docker-compose.yml
```

## Prérequis

- Node.js 22+
- Docker et Docker Compose

## Lancer le projet en local

1. Installer les dépendances (une seule fois, à la racine) :

   ```bash
   npm install
   ```

2. Démarrer MySQL et Adminer (et optionnellement l'API en conteneur) :

   ```bash
   docker compose up
   ```

   - MySQL est exposé sur `localhost:3306` (voir les identifiants dans `docker-compose.yml`).
   - Adminer est accessible sur [http://localhost:8080](http://localhost:8080).

3. Lancer l'API en développement (hors conteneur, avec hot-reload) :

   ```bash
   npm run dev:api
   ```

4. Lancer l'application mobile Expo :

   ```bash
   npm run dev:mobile
   ```

## Prisma

Le schéma se trouve dans `apps/api/prisma/schema.prisma`. Une fois le schéma défini :

```bash
cd apps/api
npx prisma migrate dev
```
