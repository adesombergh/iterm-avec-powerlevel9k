# iTerm2, OhMyZsh et Powerlevel9K sur MacOS
Un guide de comment installer iTerm2, OhMyZsh et Powerlevel9K, étape par étape, sur mac, via le terminal.
Pour info ce guide installe tout dans le dossier racine.

## Vue d'ensemble

1. Installer iTerm2 avec brew
2. Télécharger et installer les polices et les palettes de couleur
3. Installer OhMyZsh
4. Installer Powerlevel9k
5. Configurer iTerm

## Etapes

### Brew

Il faut tout d'abord avoir Brew, un gestionnaire de paquets pour MacOs.
Assurez vous d'avoir brew en tapant:

	brew -v

Si le terminal ne renvoie pas la version installée suivez ces instructions: [Installer Brew](https://brew.sh/index_fr.htm)

### Fonts

Installer les polices:

	git clone https://github.com/powerline/fonts.git

	cd fonts/

	./install.sh

### Color Scheme

Installer les palettes de couleur:

	git clone https://github.com/nathanbuchar/atom-one-dark-terminal.git

### Installer Oh My Zsh

Assurez vous de bien effacer ces fichers/dossiers avant tout:

	.zshrc .zsh-update .zsh_history .zcompdump .oh-my-zsh

Installer OhMyZsh:

	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

OhMyZsh se lance automatiquement mais pour l'instant il faut sortir:

	exit


### Installer Powerlevel9k

Installer PowerLevel9k:

	git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k

Et editer le fichier . zshrc dans le dossier Home (ou racine):

	nano .zshrc

changer la valeur de cette ligne

	 ZSH_THEME="robbyrussell"

par celle ci

	 ZSH_THEME="powerlevel9k/powerlevel9k"

et enregistrer!

### Configurer iTerm
#### Couleurs

Lancez iTerm et allez dans:

	Menu Pomme > Préférences > Profiles > Colors

En bas à droite choisissez Import et pointer vers la color palette installer au point 3 qui normalement devrait se trouver dans:

	~/atom-one-dark-terminal/scheme/iterm/One Dark.itermcolors

#### Fonts

Dans iTerm allez dans:

	Menu Pomme > Préférences > Profiles > Text

Décochez la case "Use a diferent font for non-ASCII text"

Cliquez sur Change Font et choisissez une police pour Powerline. Je vous conseil la 

	Meslo LG M for Powerline

### Et voila...