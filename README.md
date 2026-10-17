# Overlay Spotify pour OBS

Appli Windows qui affiche dans OBS le titre que tu écoutes sur Spotify : pochette, titre, artistes et progression. Tout se règle dans l'appli, et chaque changement s'applique en direct dans OBS.

## Télécharger

Prends l'installeur `Overlay-Spotify-Setup-x.y.z.exe` dans la **[dernière version](https://github.com/ZattFrancesco/Spotify-Overlay-for-OBS/releases/latest)**.

## Ce qu'elle fait

- **Overlay en source Navigateur** : 5 dispositions (compacte, grande pochette, minimale, bandeau, verticale).
- **Couleurs automatiques** : le fond et l'accent peuvent prendre les couleurs de la pochette en cours.
- **Comportement** : masquer en pause après un délai, n'apparaître qu'au changement de titre, animations d'entrée, ancrage dans la source.
- **Réglages en direct** : dans la fenêtre de l'appli ou dans un dock OBS, sans recharger la source.
- **Profils** : un overlay différent par scène, chacun avec sa propre adresse.
- **Discrète** : l'appli vit dans la zone de notification et peut se lancer au démarrage de Windows.
- **Script OBS** : lance l'appli avec OBS, la ferme avec lui et ajuste tout seul la taille des sources.

## Installation

1. Lance l'installeur. L'appli n'est pas signée : si Windows SmartScreen s'affiche, clique sur **Informations complémentaires → Exécuter quand même**.
2. Crée ton app sur le [dashboard Spotify](https://developer.spotify.com/dashboard) : **Create app**, Redirect URI `http://127.0.0.1:8888/callback`, coche **Web API**.
3. Dans l'appli, page **Compte Spotify** : colle le **Client ID** et le **Client Secret** de ton app, enregistre, puis clique sur **Se connecter**.
4. Dans OBS, ajoute une source **Navigateur** (décoche *Fichier local*) avec l'adresse `http://127.0.0.1:8888/`.
5. Facultatif : page **OBS** de l'appli → **Afficher** le script, puis dans OBS **Outils → Scripts → +** pour l'ajouter.

Réglages rapides dans OBS : **Docks → Docks de navigateur personnalisés**, adresse `http://127.0.0.1:8888/settings?dock`.

## Dépannage

- **L'overlay reste vide** : ajoute ton adresse e-mail Spotify dans l'onglet **User Management** de ton app, sur le dashboard Spotify.
- **« INVALID_CLIENT: Invalid redirect URI »** : la Redirect URI de ton app Spotify doit être exactement `http://127.0.0.1:8888/callback`.
- **Rien ne s'affiche dans OBS** : l'appli doit tourner (icône dans la zone de notification).

## Configuration

Windows 10 ou 11 (64 bits), OBS Studio, un compte Spotify.

## Licence

© 2026 zattfrancesco, tous droits réservés. Le code source n'est pas public : voir [LICENSE](LICENSE).
