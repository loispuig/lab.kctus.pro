+++
date = "2015-11-24T15:08:31+01:00"
draft = true
title = "jekyll on ispconfig3"

comments = true     # set false to hide Disqus comments
share = true        # set false to share buttons
menu = ""
+++

Faire fonctionner [Jekyll](http://jekyllrb.com/) dans un environement chrooté, avec ISPConfig + Jailkit sur une Debian Wheezy.

###Installation de Ruby via RVM
En tant qu'utilisateur root :
<script src="https://gist.github.com/7788411.js?file=install_rvm.sh"></script>

###Installation de Jekyll
<script src="https://gist.github.com/7788411.js?file=install_jekyll.sh"></script>

###Installation de Pygment (pour la coloration syntaxique)
<script src="https://gist.github.com/7788411.js?file=install_pygment.sh"></script>

###Configuration de Jailkit pour les futurs utilisateurs ssh chrootés
<script src="https://gist.github.com/7788411.js?file=edit_jk_init.sh"></script>

<script src="https://gist.github.com/7788411.js?file=jk_init.ini"></script>

Puis aller sur ISPConfig en tant qu'admin > Système > Configuration Serveur > Cliquez sur votre serveur.
Dans l'onglet "Jailkit", ajoutez "jekyll" à la fin du champ "Sections des applications chrootées Jailkit".

![Add Jekyll to ISPConfig Jailkit config]({{ site.url}}/assets/img/posts/ispconfig-jekyll.png)

Vous pouvez maintenant créer un autilisateur ssh chrooté via ISPConfig.

###Si l'utilisateur chrooté est déjà créé 

Vous pouvez tout de même ajouter ce qu'il faut à son environnement chrooté.

<script src="https://gist.github.com/7788411.js?file=jk_add_python_ruby.sh"></script>

###Connectez-vous avec votre utilisateur chrooté

###Créez un dépôt git
<script src="https://gist.github.com/7788411.js?file=git_create_repo.sh"></script>

###Configurez le hook post-receive
<script src="https://gist.github.com/7788411.js?file=git_create_post_receive_hook.sh"></script>
<script src="https://gist.github.com/7788411.js?file=git_jekyll_post_receive_hook.sh"></script>

Vous pouvez maintenant cloner votre dépôt via ssh, ajoutez-y votre arborescence jekyll et poussez le tout à nouveau sur le dépôt.
Voilà, votre site web doit se mettre à jour à chaque push sur votre dépôt.