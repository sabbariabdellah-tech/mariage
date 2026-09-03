# Gestion Invités Mariage — V3 Online

V3 conserve l'interface de la V2 et ajoute une base de données cloud partagée.

## Architecture
- Frontend : HTML/CSS/JavaScript, compatible GitHub Pages.
- Données : Supabase Postgres + Auth.
- Synchronisation : les invités, l'historique et le placement des tables sont stockés dans `wedding_data`.
- Sécurité : Row Level Security limite les données à l'utilisateur connecté.

## Mise en ligne gratuite
1. Créer un projet Supabase.
2. Dans Supabase > SQL Editor, exécuter `supabase_schema.sql`.
3. Récupérer dans Supabase > Settings > API : Project URL et `anon` public key.
4. Ouvrir l'application et cliquer `Configuration Supabase` pour enregistrer ces deux valeurs.
5. Créer le compte depuis l'application.
6. Publier `index.html` sur GitHub Pages.

Ne jamais utiliser la `service_role key` dans le navigateur.

## Important
La première connexion sur un navigateur contenant encore les données V2 peut proposer automatiquement d'importer ces données si le compte Supabase est vide.
