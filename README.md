# Chatty — Twitch Chat Highlight Overlay

Système d'overlay pour mettre en avant un message du chat Twitch dans OBS.
Pur HTML/CSS/JS, sans bot, sans build, sans compilation.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Panneau de contrôle — chat défilant, clic pour sélectionner |
| `overlay.html` | Overlay OBS — affiche le message sélectionné (fond transparent) |

## Utilisation

1. Ouvrir `index.html` dans un navigateur ou comme dock OBS personnalisé.
2. Saisir le nom de la chaîne Twitch et cliquer **Connecter**.
3. Les messages du chat apparaissent en temps réel. Cliquer sur l'un d'eux pour le mettre en avant.
4. Les messages précédant le message sélectionné sont grisés.
5. Dans OBS, ajouter `overlay.html` comme **source navigateur** (browser source).

## Communication entre les pages

Les deux pages communiquent via `BroadcastChannel` (même navigateur / même domaine) avec un fallback `localStorage`.
Aucun serveur backend n'est nécessaire.

## GitHub Pages

Le site est automatiquement publié sur GitHub Pages à chaque push d'un tag `v*`.

- **Panneau de contrôle :** `https://vignemail1.github.io/chatty/`
- **Overlay OBS :** `https://vignemail1.github.io/chatty/overlay.html`
