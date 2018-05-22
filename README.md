# HEH Beamer

![Version](https://img.shields.io/badge/version-1.1.3-blue.svg)

Framework de la HEH pour faire vos présentations avec Beamer plus facilement.

<p align="center">
	<img src="preview.png" alt="Beamer (Preview)" width="320">
</p>

Pour le compiler et faire du LaTeX, je conseille **TeXStudio**.
Il faut utiliser le compilateur **XeLaTeX**.

Pour ce faire, installez `TexStudio` via le guide (voir fin de ce document), ouvrez-le et suivez les étapes ci-dessous :

1. Allez dans le menu `Options`
2. Cliquez sur `Configurer TexStudio`. Une fenêtre s'ouvre.
3. Dans cette fenêtre à gauche, cliquez sur `Production`.
4. Cliquez à droite sur `Compilation par défaut`.
5. Changez `PDFLaTeX` par `XeLaTeX`.

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

---

## Utilisation

### Nouvelle partie

Dans le dossier `slide`, ajoutez un nouveau fichier latex (_e.g._ `nom_du_fichier.tex`).
Ensuite, éditez le fichier `presentation.tex` et ajoutez une nouvelle partie
dans le document :

```latex
\begin{document}
%%% ...

\partie{Nom de la partie}{nom_du_fichier}

%%% ...
\end{document}
```

### Nouvelle section

Éditez le fichier `.tex` présent dans le dossier `slide` et modifiez ce bloc de
code :

```latex
\begin{slide}[Titre de mon slide]
  \begin{center}
    \huge{Mon texte}
  \end{center}
\end{slide}
```

**NOTE:** la création d'un slide se définit entre les balises `slide`.

### Ajout d'une liste d'éléments

Chaque élément doit se trouver dans l'environnement `itemize`. Ces éléments sont
reconnaissables par la définition de l'environnement `item`.

```latex
\begin{slide}[Liste d'éléments]
  \begin{itemize}
    \item Un élément
    \pause
    \item Un autre élément
    \pause
    \item Un troisième élément
    \pause
    \item \ldots
  \end{itemize}
\end{slide}
```

**NOTE:** la commande `\pause` permet de faire une pause au niveau de la présentation.

### Ajout d'une image

Les images doivent être placées dans le dossier `images/`. Il est possible de créer les vôtres à l'intérieur de ce dernier. Créons par exemple le dossier `test/`.

Pour inclure l'image se trouvant dans ce dossier, il suffit de faire :

```latex
% Inclus une image qui a comme nom `mon_image.png` et qui fait 60% de la place disponible
\includegraphics[scale=0.6\linewidth]{test/mon_image.png}
```

Pour ajouter une image avec une légende :

```latex
\begin{slide}[Ajout d'une image]
  \begin{figure}[ht]
    % Permet de centrer une image
    \centering
    % Inclus une image qui fait 60% la place disponible
    \includegraphics[scale=0.6\linewidth]{images/mon_image.png}
    % Ajoute une légende
    \caption{Ma légende}
    % Ajoute une référence pour pouvoir citer l'image (optionel)
    \label{fig:mon_image}
  \end{figure}
\end[slide]
```

L'usage d'un label permet d'aisément référencer la figure
dans votre code, de la manière suivante : `\ref{fig:mon_image}`. Attention à
compiler plus d'une fois pour mettre à jour les références.
