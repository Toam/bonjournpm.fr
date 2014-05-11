---
layout: post
title:  "Mobile-icon-resizer"
subtitle: "Génère des icones pour les applications iOS et Android"
category: mobile
---

[Mobile-icon-resizer][mobile-icon-resizer] est un package NPM qui prend
une image en 1024x1024 et qui génère toutes les icones pour vos
applications iOS ou Android.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install mobile-icon-resizer -g
{% endhighlight %}

Il est possible d'utiliser ce package en ligne de commande ou de
l'inclure dans un projet node.js. La commande suivant permet de créer
des icones pour une applicaiton Android.
{% highlight bash %}
mobile-icon-resizer -i appicon_1024.png --iosprefix="Icon" --iosof=output/ios --androidof=output/android --config=custom-sizes.js
{% endhighlight %}

Plus d'information et la liste des options sont disponible sur [la page du package][mobile-icon-resizer].


[mobile-icon-resizer]: https://github.com/muzzley/mobile-icon-resizer
