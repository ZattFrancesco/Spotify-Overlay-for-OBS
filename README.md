# Overlay Spotify pour OBS

Appli Windows qui affiche dans OBS le titre que tu écoutes sur Spotify : pochette, titre, artistes et progression. Rien à configurer : elle lit ce que joue Spotify sur ton PC. Tout se règle dans l'appli, et chaque changement s'applique en direct dans OBS.

## Télécharger

Prends l'installeur `Overlay-Spotify-Setup-x.y.z.exe` dans la **[dernière version](https://github.com/ZattFrancesco/Spotify-Overlay-for-OBS/releases/latest)**. Ensuite, l'appli se met à jour toute seule.

## Ce qu'elle fait

- **Sans compte à connecter** : elle lit le titre en cours dans les commandes média de Windows. Spotify seulement, ou n'importe quel lecteur (lecteur web, YouTube, Deezer…).
- **Overlay en source Navigateur** : 5 dispositions (compacte, grande pochette, minimale, bandeau, verticale).
- **Couleurs automatiques** : le fond et l'accent peuvent prendre les couleurs de la pochette en cours.
- **Comportement** : masquer en pause après un délai, n'apparaître qu'au changement de titre, animations d'entrée, ancrage dans la source.
- **Réglages en direct** : avec un aperçu toujours visible, dans la fenêtre de l'appli ou dans un dock OBS.
- **Profils** : un overlay différent par scène, chacun avec sa propre adresse.
- **Discrète** : l'appli vit dans la zone de notification et peut se lancer au démarrage de Windows.
- **Script OBS** : lance l'appli avec OBS, la ferme avec lui et ajuste tout seul la taille des sources.
- **Mises à jour automatiques** : installées en silence à la fermeture de l'appli, ou tout de suite avec le bouton « Rechercher une mise à jour ».

## Installation

1. Lance l'installeur. L'appli n'est pas signée : si Windows SmartScreen s'affiche, clique sur **Informations complémentaires → Exécuter quand même**.
2. Lance Spotify sur ce PC : le titre en cours s'affiche tout seul dans l'appli.
3. Dans OBS, ajoute une source **Navigateur** (décoche *Fichier local*) avec l'adresse `http://127.0.0.1:8888/`.
4. Facultatif : page **OBS** de l'appli → **Afficher** le script, puis dans OBS **Outils → Scripts → +** pour l'ajouter.

Réglages rapides dans OBS : **Docks → Docks de navigateur personnalisés**, adresse `http://127.0.0.1:8888/settings?dock`.

La musique doit être jouée sur le même PC que l'overlay. Pour suivre un autre appareil, la page **Source** propose aussi l'**API Spotify** (il faut alors créer une app sur le [dashboard Spotify](https://developer.spotify.com/dashboard), Redirect URI `http://127.0.0.1:8888/callback`).

## Dépannage

- **Rien ne s'affiche** : Spotify doit tourner sur ce PC. Avec le lecteur web de Spotify, choisis « Tous les lecteurs » dans la page **Source**.
- **Pas de barre de progression** : certains lecteurs (souvent les navigateurs) ne donnent pas la durée du morceau à Windows.
- **Rien ne s'affiche dans OBS** : l'appli doit tourner (icône dans la zone de notification).

## Configuration

Windows 10 ou 11 (64 bits), OBS Studio, Spotify.

## Licence

© 2026 zattfrancesco, tous droits réservés. Le code source n'est pas public : voir [LICENSE](LICENSE).
