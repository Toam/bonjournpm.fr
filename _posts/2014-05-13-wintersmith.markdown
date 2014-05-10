---
layout: post
title:  "Wintersmith"
subtitle: "Un générateur de sites statiques"
category: outils 
---

[Wintersmith][wintersmith] est un package NPM qui permet de réaliser des
sites statiques. Les sources du site sont compilées au moment de la
génération pour que les visiteurs n'intéragissent qu'avec des fichiers
html. Le site est beaucoup plus rapide et il y a moins de risques de
sécurités.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install wintersmith -g
{% endhighlight %}

Wintersmith permet de créer un site grâce à la commande :
{% highlight bash %}
$ wintersmith new <chemin>
{% endhighlight %}

Ensuite, une commande permet de lancer la génération du site statique et
le rend disponible à l'addresse `http://localhost:8080`
{% highlight bash %}
$ cd <chemin>
$ wintersmith preview
{% endhighlight %}

Toutes les informations pour créer un site complet sont disponible sur
[la page du package][wintersmith].


[wintersmith]: https://github.com/jnordberg/wintersmith
