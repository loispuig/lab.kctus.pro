+++
date = "2015-11-24T15:10:43+01:00"
draft = true
title = "kolab3 on debian wheezy"

+++

Dans ma quête pour me défaire de Google Apps & Co. je cherche désespérement une nouvelle plateforme de travail collaboratif, stable et compatible avec les standards WebDav, WebCal et WebCard. Pas si facile à trouver !

Au menu d'aujourd'hui, l'installation de [Kolab 3.1](http://kolab.org) sur une Debian wheezy minimal toute neuve.

###Pré-requis (OpenVZ)
Si vous êtes sur une VM OpenVZ, n'oubliez pas d'activer les quotas sur celle-ci.
Puis sur votre hôte virtualiseur :

101 étant l'id de votre VM

<script src="https://gist.github.com/dae57e7b29c494363c38.js?file=debian7-kolab3-configure-vz.sh"></script>

###Installation

Lancez la commande suivante en tant que root :

<script src="https://gist.github.com/dae57e7b29c494363c38.js?file=debian7-kolab3-start.Sh"></script>

Qui téléchargera et exécutera le sript suivant :

<script src="https://gist.github.com/dae57e7b29c494363c38.js?file=debian7-kolab3-setup.sh"></script>

###Sources
* [Blupgnup's Tavern : Installation du Groupware Kolab](http://blupgnup.com/installation-groupware-kolab/)
* [Official Kolab doc](http://docs.kolab.org/)