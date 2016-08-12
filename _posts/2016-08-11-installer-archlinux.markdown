--- layout: post
title: "Guide d'installation d'ArchLinux"
date: 2016-08-11 19:43:23
categories: linux, archlinux
---

# Guide d'installation d'Archlinux

## Introduction
Pour commencer, j'imagine que si vous êtes tombés sur cet article, il y a de bonnes chances
pour que vous soyez déjà au courant de ce qu'est [Archlinux][archlinux], GNU/Linux et la sphère
[FOSS][foss] en général. Cette introduction que je vous fais d'Archlinux a donc plus pour but
de vous faire comprendre ce qu'implique que de choisir une distribution comme Archlinux, et
plus en général quels en sont les avantages et inconvénients. Il est a noté que étant moi même
sous Archlinux depuis maintenant 2 ans, il me sera difficile d'être particulièrement objectif,
mais dans la mesure où je m'y complait, je pense mon avis pas complétement absurde.

Une des grosse spécificité d'Archlinux consiste en sont système de release qui est dit "rolling
release". C'est à dire que contrairement à Ubuntu, Debian, ou en réalité la grosse majorité des
distributions existantes, Archlinux observe un rythme de sortie de version assez élevé, les
incrémentation sont relativement mineures au vu de leur fréquences, mais en retour, chaque mise
à jour ne requiert aucune réinstallation pour l'utilisateur final. C'est à dire que vous
pourrez garder la même installation d'Archlinux depuis la première, en faisant toutes les mises
à jour au travers du gestionnaire de paquets. 

Un autre avantage d'Archlinux est justement son gestionnaire de paquets, Pacman. Enfin en
réalité pas tellement sont gestionnaire de paquets integré, mais plutôt la facilité avec
laquelle il est possible de partager un paquet. La sphère communautaire Archlinux possède un
dépôt de paquets alternatifs qui s'apelle [AUR (Archlinux User Repository)][aur]  qui comme
sont nom l'indique consiste en un ensemble de paquets qui sont publiés et gérés par la
communauté. Et il est facilement possible de télécharger un gestionnaire de paquet alternatif
qui permet de gérer ses paquets tiers de la même manière qu'avec Pacman. Mais nous reverrons
tout cela lors de la phase de post-installation d'archlinux.

En parlant de [AUR][aur], un autre avantage (et pas des moindres), et justement sa communauté.
Le wiki d'Arch est sans aucun doute le wiki sur linux le plus fourni et précis, sans compter
les forums officiels qui restent d'une aide inégalée.

Il est également à noter que grace à ce système de rolling release, Archlinux est probablement
la distribution qui permet d'avoir assez systématiquement les dernières versions des logiciels.
Ça peut être une raison pour certains de choisir Archlinux.

D'autre part, Archlinux demande un certain investissement pour des néophytes à installer ou
même à gérer. Ce qui veut aussi dire qu'il y a des tonnes de choses à apprendre rien qu'en
l'installant. Archlinux se veut être une distribution [minimale et légère][moto] et c'est
probablement la raison qui m'a vraiment poussé dans sa direction. Manipuler une distribution si
"dépouillée" de logiciels tiers, de services inconnus, d'encombrement visuel, oblige donc
l'utilisateur à faire son choix. Et c'est en faisant ce genre de choix que l'on se rend compte
de comment un ordinateur et Linux marchent, et même simplement de tout ce que l'on peut faire
avec.

La question du dépouillement est à double tranchant, car bien qu'elle permettent d'apprendre
tout un tas de choses sur tout un tas de trucs différent, cela veut aussi dire qu'il y a une
courbe de progression avant d'y être suffisament à l'aise. Alors maintenant il est toujours
possible d'installer Archlinux au travers d'un script existant, ou en installant son petit
frère [Manjaro][manjaro] avec un installeur graphique, mais en faisant une installation
complète d'Archlinux, on sait exactement ce qu'il faut pour que notre distribution marche, et
ce qu'il y a à l'intérieur. Cela signifie également que les problèmes que l'on peut rencontrer
(similaire à ceux que l'on peut retrouver dans les autres distributions) sont plus facilement
résolvable car le système de base est plus simple, et que l'on sait ce qu'il y a à l'intérieur
justement.

J'espère que ces quelques paragraphes vous auront permis de vous faire une idée sur Archlinux,
mais aussi que la courbe de progression (qui n'est certainement pas la plus complexe) est, pour
un néophyte comme pour quelqu'un de relativement à l'aise, reste bénéfique.

## Partitionnement
## Installation
## Configuration


**half-shell**

[foss]:
[aur]:
[archlinux]:
[moto]:
[manjaro]:
