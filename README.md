# SPAM Overlay

An unofficial fan tool for the card game SPAM: a small window that sits on top of the game and advises you during a match
(which card to play, what to buy in the shop, your chances). It is not affiliated with the game's studio, it does not modify the
game, and it ships nothing of the game's code or data.

*Français plus bas.*

## Download and install

Get the latest version from the [Releases page](../../releases/latest). Windows 10 or 11, 64-bit.

- **`SPAM-Overlay-Setup-<version>.exe`** (recommended): run it. It installs for your Windows user only, in
  `%LOCALAPPDATA%\Programs\SPAM Overlay`, with no administrator rights, and adds a Start menu entry.
- **`spam-overlay-<version>-win64.zip`** (portable): unzip it into a folder you own (not Program Files) and run
  `SPAM Overlay.exe`. Nothing is installed in Windows; everything stays in that folder.
- **`SHA256SUMS.txt`**: the checksum of each file. To check a download in PowerShell:
  `Get-FileHash .\<file> -Algorithm SHA256`.

**Windows SmartScreen.** The files are not code-signed, so on the first run Windows may say "Windows protected your PC". Choose
**More info**, then **Run anyway**. For the ZIP you can avoid it: right-click the downloaded ZIP, Properties, tick **Unblock**,
then unzip.

**First start.** A short setup finds your game, prepares the overlay's engine from your own copy of the game and explains the keys.

**Reading the match.** The overlay reads best from the game's network traffic, through [Npcap](https://npcap.com) (free for
personal use), which you install once: the setup's "Install Npcap for me" fetches Npcap's own installer from npcap.com and runs it
after a Windows prompt, or you install it yourself. Without Npcap it reads the game window instead, less precisely. The overlay
never ships Npcap.

## Privacy

- **It only reads.** It never clicks, types, injects code, reads the game's memory or changes a file of the game.
- **What goes online, and nothing else.**
  - Updates: at each start, and when you press "Check for updates", it reads the latest version from spam-meta.com. An
    installed copy then downloads it, checks it and installs it, never during a match.
  - Game data: after each match, and when you report an advice, it sends an anonymous record of the game (no name, no account,
    no file path) to reports.spam-meta.com. This collection is the condition of using the overlay, accepted at setup.
  - "Install Npcap for me" downloads Npcap's installer from npcap.com when you press it.
- **Your files.** Settings, logs and the engine prepared from your game stay in the overlay's own `data` folder. The overlay
  writes nothing to the registry.

## Uninstall

- **Installed with the Setup:** Windows Settings, Apps, *SPAM Overlay*, Uninstall. Or, in the overlay, *Setup and help*,
  *Remove SPAM Overlay*.
- **Portable ZIP:** in the overlay, *Setup and help*, *Remove SPAM Overlay*, then delete the folder if Windows kept it.
- Npcap, if you installed it, is a separate program: remove it from Windows Settings, Apps.

## Licences

The package carries the licence texts of everything it ships: the `LICENSES` folder (Electron, Chromium, the engine's libraries,
the fonts) and each runtime's own notices (`runtime\python`, `runtime\dotnet`). See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)
for the list. SPAM and its card art belong to their publisher.

This repository holds this README, the notices and the releases only. No source code is published here.

---

# SPAM Overlay (français)

Un outil de fan non officiel pour le jeu de cartes SPAM : une petite fenêtre posée au-dessus du jeu qui te conseille pendant
un match (quelle carte jouer, quoi acheter à la boutique, tes chances). Sans lien avec le studio du jeu, il ne modifie pas le jeu
et n’embarque ni le code ni les données du jeu.

## Télécharger et installer

Prends la dernière version sur la [page des versions](../../releases/latest). Windows 10 ou 11, 64 bits.

- **`SPAM-Overlay-Setup-<version>.exe`** (recommandé) : lance-le. Il s’installe pour ton utilisateur Windows seulement, dans
  `%LOCALAPPDATA%\Programs\SPAM Overlay`, sans droits d’administrateur, et ajoute une entrée au menu Démarrer.
- **`spam-overlay-<version>-win64.zip`** (portable) : décompresse-le dans un dossier à toi (pas dans Program Files) et lance
  `SPAM Overlay.exe`. Rien n’est installé dans Windows ; tout reste dans ce dossier.
- **`SHA256SUMS.txt`** : la somme de contrôle de chaque fichier. Pour vérifier dans PowerShell :
  `Get-FileHash .\<fichier> -Algorithm SHA256`.

**Windows SmartScreen.** Les fichiers ne sont pas signés : au premier lancement, Windows peut afficher « Windows a protégé votre
ordinateur ». Choisis **Informations complémentaires**, puis **Exécuter quand même**. Pour le ZIP, tu peux l’éviter :
clic droit sur le ZIP téléchargé, Propriétés, coche **Débloquer**, puis décompresse.

**Premier lancement.** Une courte installation trouve ton jeu, prépare le moteur de l’overlay à partir de ta propre copie du
jeu et explique les touches.

**Lecture de la partie.** L’overlay lit au mieux dans le trafic réseau du jeu, grâce à [Npcap](https://npcap.com) (gratuit pour
un usage personnel), que tu installes une fois : « Installer Npcap pour moi » télécharge l’installateur de Npcap sur npcap.com et
le lance après une demande de Windows, ou tu l’installes toi-même. Sans Npcap, il lit la fenêtre du jeu, de façon plus
approximative. Npcap n’est jamais fourni avec l’overlay.

## Vie privée

- **Il ne fait que lire.** Il ne clique jamais, ne tape rien, n’injecte rien, ne lit pas la mémoire du jeu et ne modifie aucun
  fichier du jeu.
- **Ce qui part en ligne, et rien d’autre.**
  - Mises à jour : à chaque démarrage, et quand tu appuies sur « Rechercher une mise à jour », il lit la dernière version sur
    spam-meta.com. Une copie installée la télécharge, la vérifie et l’installe, jamais pendant une partie.
  - Données de jeu : après chaque partie, et quand tu signales un conseil, il envoie un relevé anonyme de la partie (sans nom,
    sans compte, sans chemin de fichier) à reports.spam-meta.com. Cette collecte est la condition d’utilisation de l’overlay,
    acceptée à l’installation.
  - « Installer Npcap pour moi » télécharge l’installateur de Npcap depuis npcap.com quand tu appuies dessus.
- **Tes fichiers.** Réglages, journaux et moteur préparé à partir de ton jeu restent dans le dossier `data` de l’overlay.
  L’overlay n’écrit rien dans le registre.

## Désinstaller

- **Installé avec le Setup :** Paramètres Windows, Applications, *SPAM Overlay*, Désinstaller. Ou, dans l’overlay,
  *Installation et aide*, *Retirer SPAM Overlay*.
- **ZIP portable :** dans l’overlay, *Installation et aide*, *Retirer SPAM Overlay*, puis supprime le dossier si Windows l’a
  gardé.
- Npcap, si tu l’as installé, est un programme à part : retire-le depuis Paramètres Windows, Applications.

## Licences

Le paquet contient les licences de tout ce qu’il embarque : le dossier `LICENSES` et les notices des environnements d’exécution
(`runtime\python`, `runtime\dotnet`). Liste dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). SPAM et les illustrations de ses
cartes appartiennent à leur éditeur.

Ce dépôt ne contient que ce README, les notices et les versions publiées. Aucun code source n’est publié ici.
