# HEH Beamer

![Version](https://img.shields.io/badge/version-1.1.2-blue.svg)

Framework de la HEH pour faire vos présentations avec Beamer plus facilement.

<p align="center">
	<img src="preview.png" alt="Beamer (Preview)" width="320">
</p>

Pour le compiler et faire du LaTeX, je conseille **TeXStudio**.
Il faut utiliser le compilateur **XeLaTeX**.

Pour ce faire, installez TexStudio via le guide (voir fin de ce document), ouvrez-le et suivez les étapes ci-dessous :

1. Allez dans le menu "Options"
2. Cliquez sur "Configurer TexStudio". Une fenêtre s'ouvre.
3. Dans cette fenêtre à gauche, cliquez sur "Production".
4. Cliquez à droite sur "Compilation par défaut".
5. Changez "PDFLaTeX" par "XeLaTeX".



## Téléchargement

Cliquez sur ce lien pour télécharger le framework HEH-Beamer : [https://github.com/gquittet/HEH-Beamer/archive/1.1.2.zip](https://github.com/gquittet/HEH-Beamer/archive/1.1.2.zip)

## Installer LaTeX

### Windows

Téléchargez et installez les outils suivants :
- Miktex (la suite LaTeX) : [https://miktex.org/download](https://miktex.org/download)
- TexStudio (l'éditeur) : [https://www.texstudio.org/](https://www.texstudio.org/)

### Debian, Linux Mint, Ubuntu et autres dérivées de Debian

Veuillez taper la commande suivante :
```bash
sudo apt-get install -y texlive-full && sudo apt-get install -y texstudio
```

### Fedora

Veuillez taper la commande suivante :
```bash
sudo dnf install -y texlive-scheme-full && sudo dnf install -y texstudio
```


