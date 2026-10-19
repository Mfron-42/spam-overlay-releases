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
personal use), which you install yourself. Without Npcap it reads the game window instead, less precisely. The overlay never
ships or installs Npcap.

## Privacy

- **It only reads.** It never clicks, types, injects code, reads the game's memory or changes a file of the game.
- **It sends nothing.** No account, no telemetry, no analytics. What it reads stays on your PC. The only thing that can go
  online is "Check for updates", and only when you press it; it downloads and runs nothing by itself.
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

Un outil de fan non officiel pour le jeu de cartes SPAM : une petite fenêtre posée au-dessus du jeu qui vous conseille pendant
un match (quelle carte jouer, quoi acheter à la boutique, vos chances). Sans lien avec le studio du jeu, il ne modifie pas le jeu
et n'embarque ni le code ni les données du jeu.

## Télécharger et installer

Prenez la dernière version sur la [page des versions](../../releases/latest). Windows 10 ou 11, 64 bits.

- **`SPAM-Overlay-Setup-<version>.exe`** (recommandé) : lancez-le. Il s'installe pour votre utilisateur Windows seulement, dans
  `%LOCALAPPDATA%\Programs\SPAM Overlay`, sans droits d'administrateur, et ajoute une entrée au menu Démarrer.
- **`spam-overlay-<version>-win64.zip`** (portable) : décompressez-le dans un dossier à vous (pas dans Program Files) et lancez
  `SPAM Overlay.exe`. Rien n'est installé dans Windows ; tout reste dans ce dossier.
- **`SHA256SUMS.txt`** : la somme de contrôle de chaque fichier. Pour vérifier dans PowerShell :
  `Get-FileHash .\<fichier> -Algorithm SHA256`.

**Windows SmartScreen.** Les fichiers ne sont pas signés : au premier lancement, Windows peut afficher « Windows a protégé votre
ordinateur ». Choisissez **Informations complémentaires**, puis **Exécuter quand même**. Pour le ZIP, vous pouvez l'éviter :
clic droit sur le ZIP téléchargé, Propriétés, cochez **Débloquer**, puis décompressez.

**Premier lancement.** Une courte installation trouve votre jeu, prépare le moteur de l'overlay à partir de votre propre copie du
jeu et explique les touches.

**Lecture de la partie.** L'overlay lit au mieux dans le trafic réseau du jeu, grâce à [Npcap](https://npcap.com) (gratuit pour
un usage personnel), que vous installez vous-même. Sans Npcap, il lit la fenêtre du jeu, de façon plus approximative.
L'overlay ne fournit ni n'installe jamais Npcap.

## Vie privée

- **Il ne fait que lire.** Il ne clique jamais, ne tape rien, n'injecte rien, ne lit pas la mémoire du jeu et ne modifie aucun
  fichier du jeu.
- **Il n'envoie rien.** Pas de compte, pas de télémétrie, pas de statistiques. Ce qu'il lit reste sur votre PC. Seul
  « Rechercher une mise à jour » peut aller en ligne, et seulement quand vous appuyez dessus ; il ne télécharge et ne lance rien
  de lui-même.
- **Vos fichiers.** Réglages, journaux et moteur préparé à partir de votre jeu restent dans le dossier `data` de l'overlay.
  L'overlay n'écrit rien dans le registre.

## Désinstaller

- **Installé avec le Setup :** Paramètres Windows, Applications, *SPAM Overlay*, Désinstaller. Ou, dans l'overlay,
  *Installation et aide*, *Retirer SPAM Overlay*.
- **ZIP portable :** dans l'overlay, *Installation et aide*, *Retirer SPAM Overlay*, puis supprimez le dossier si Windows l'a
  gardé.
- Npcap, si vous l'avez installé, est un programme à part : retirez-le depuis Paramètres Windows, Applications.

## Licences

Le paquet contient les licences de tout ce qu'il embarque : le dossier `LICENSES` et les notices des environnements d'exécution
(`runtime\python`, `runtime\dotnet`). Liste dans [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). SPAM et les illustrations de ses
cartes appartiennent à leur éditeur.

Ce dépôt ne contient que ce README, les notices et les versions publiées. Aucun code source n'est publié ici.
