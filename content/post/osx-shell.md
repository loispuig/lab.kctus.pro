+++
date = "2015-11-24T15:04:49+01:00"
draft = false
title = "osx shell"

+++

Quelques commandes shell utiles sur Mac OS X.
<!--more-->

### Recherche dans la liste des processus en cours

```sh
ps aux|grep "Nom de l'application"
ps aux|grep nom_du_processus
```

### Fermer une application desktop à partir du shell

```sh
osascript -e 'tell application "safari" to quit'
```

### Vider le menu contextuel "Ouvrir avec..."

```sh
/System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user
```

### Rendre visible un dossier caché

```sh
sudo chflags nohidden Library/
```