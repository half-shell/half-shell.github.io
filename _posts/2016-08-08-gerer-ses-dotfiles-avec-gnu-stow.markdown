--- layout: post
title: "Gérer ses dotfiles avec GNU Stow"
date: 2015-08-08 17:25:53
categories: linux, configuration
---

# Un gestionnaire de dotfiles

Depuis quelques années maintenant, de concert avec mon passage permanent à  Archlinux , je me
suis mis à versionner mes fichiers de configuration, les fameux "dotfiles". Cela me permet de
les porter sur d'autres systèmes si j'en ai besoin, d'incrémenter les changements que j'opère
vis-à-vis de ma configuration, et surtout de les partager parmis mes différents systèmes
personnels. 

La plupart des fichiers de configuration sont généralement placés dans votre dossier
d'utilisateur ($HOME), et par conséquent, en faire un dépôt VCS, n'est pas forcément une
solution idéale. Par conséquent, tous les héberger à part dans un dossier spécifique parait
pratique. Mais le problème qui apparait devient celui du "déploiement" des fichiers sur une
machine. Et c'est en cela que [Stow][stow] rentre en jeu. Vous pouvez retrouver l'article
original en anglais qui me l'a fait découvrir [ici][brandon.invergo].

Si vous avez assez de chance pour être linux, vous pouvez retrouver stow dans votre
gestionnaire de paquet: ’’’ # pour Archlinux $ pacman -S stow # ou pour Debian/Ubuntu $ apt-get
install stow # ou même Fedora $ ynf install stow ’’’

Stow est un gestionnaire de liens symboliques. Il est utilisé pour répliqué l'arborescence d'un
paquet ou de données d'un dossier à l'autre, et ce justement, à l'aide de liens symboliques.
Dans notre cas, on l'utilise donc pour nos dotfiles.  Stow respecte l'arborescence existante au
sein d'un dossier, et cela nous permet de "déployer" nos fichier de configurations comme on le
souhaite, à savoir par environnement (personnel, travail...), par programme concerné (bash,
vim, awesome, termite...) ou n'importe quel système qui vous arrange.

Pour cet exemple, et parce que c'est de cette manière là que mes dotfiles dont arrangés, je
présenterai l'organisation par programme. 

Venons en à la pratique maintenant. Imaginons que j'ai envie de versionner ma configuration
bash, et par conséquent mon .bashrc. Normalement, ce fichier est directement à $HOME/.bashrc.
Mais pour utiliser Stow à son avantage, je vais créer un dossier bash dans mon répertoire
dotfiles, qui contiendra le .bashrc. De cette manière, quand je suis dans mon dossier dotfiles,
je peux effectuer la commande ’’’stow bash’’’, et un lien symbolique sera créé dans mon
répertoire personnel, et bash pourra l'exploiter à sa prochaine session.

Utilisant Git comme mon système de versionning, Je créé un dossier dotfiles: ’’’mkdir
doftiles’’’, j'initialise mon repository avec ’’’git init’’’, et j'y mets mon fichier de
configuration.  Maintenant, tout ce qu'il me reste c'est de supprimer mon fichier original
($HOME/.bashrc donc), de me déplacer dans le dossier contenant le même fichier versionné, et de
faire un coup de ’’’stow .bashrc.

Voila pour le fonctionnement de base. Maintenant, il ya plusieurs manières de gérer ce
déploiement. On peut par exemple l'exercer en fonction de l'environnement (Développement,
Personnel, Réseau...), ou même, et c'est la solution que j'ai utilisé, par portée des fichiers
de configurations, c'est à dire par programme.

Donc pour continuer avec l'exemple précédent et en y rajoutant des fichiers de configurations
pour vim, l'arborescence de mon repo ressemblera à: ’’’ dofiles/ -- bash/ -- .bashrc -- vim/ --
.vimrc -- .git/ ’’’ Et ainsi, au lieu de taper ’’’stow .bashrc’’’, je n'ai plus qu'à taper
’’’stow bash’’’, et mon un lien symbolique vers mon fichier .bashrc sera fait dans mon
répertoire principal.

On peut généraliser cette organisation facilement, et un coup d'oeil à [mes dotfiles] pourra
vous donner une idéé de ce que cela peut donner.

On peut également imaginer une organisation du repo

Stow nous permet donc d'avoir un moyen facile pour gérer ces liens symboliques qui constituent
désormais notre configuration. 

**half-shell**

[stow]: https://gnu.org/software/stow
[brandon.invergo]: brandon.invergo.net/news/2012-05-26-using-gnu-stow-to-manage-your-dotfiles.html
