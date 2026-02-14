# Movie App

Une application mobile (Expo + React Native) affichant des films provenant de l'API TMDB.

## Fonctionnalités principales
- Liste et cartes de films populaires / tendances
- Page de détails d'un film (affiche, titre, date, durée, note, synopsis, genres, sociétés de production)
- Recherche de films
- Interface optimisée pour mobile (simulator / device)

## Technologies
- Expo (React Native)
- TypeScript
- Expo Router (file-based routing)
- NativeWind (Tailwind pour React Native)
- TMDB API (The Movie Database)
- Axios / fetch pour les requêtes réseau
- Appwrite (présent dans `services/appwrite.ts` — optionnel selon votre configuration)

## Structure du projet
- `app/` : pages et routes
- `components/` : composants réutilisables (`MovieCard`, `SearchBar`, `TrendingCard`, ...)
- `services/` : appels API et hooks (`api.ts`, `useFetch.ts`, `appwrite.ts`)
- `constants/` : images et icônes
- `tailwind.config.js` : configuration NativeWind / Tailwind

## Installation & exécution
1. Installer les dépendances :

```bash
npm install
```

2. Créer un fichier `.env` à la racine (il est ignoré par git via `.gitignore`) et ajouter vos clés :

```
TMDB_API_KEY=your_tmdb_api_key_here
# si vous utilisez Appwrite
APPWRITE_ENDPOINT=...
APPWRITE_PROJECT_ID=...
```

3. Lancer l'application :

```bash
npx expo start -c
```

Puis ouvrir sur un simulateur iOS/Android ou sur un appareil.
