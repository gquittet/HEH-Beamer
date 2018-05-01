# HEH Beamer
Template de la HEH pour faire vos présentations en Beamer.

Pour le compiler et faire du LaTeX, je conseille **TeXStudio**.
Il faut utiliser le compilateur **XeLaTeX**.

Pour ce faire, installez TexStudio via le guide (voir fin de ce document), ouvrez-le et suivez les étapes ci-dessous :

1. Allez dans le menu "Options"
2. Cliquez sur "Configurer TexStudio". Une fenêtre s'ouvre.
3. Dans cette fenêtre à gauche, cliquez sur "Production".
4. Cliquez à droite sur "Compilation par défaut".
5. Changez "PDFLaTeX" par "XeLaTeX".

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


