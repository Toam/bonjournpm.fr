---
layout: post
title:  "Sentiment"
subtitle: "Analysez le contenu d'un message"
category: analyse
---

[Sentiment][sentiment] est un package NPM qui permet de faire une
analyse du sens d'une phase ou d'un bloc de texte en anglais.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install sentiment
{% endhighlight %}

L'analyse du texte permet de voir si le message est plutôt positif ou
négatif comme dans l'exemple suivant :

{% highlight js %}
var sentiment = require('sentiment');

var r1 = sentiment('Cats are stupid.');
// Score: -2, Comparative: -0.666

var r2 = sentiment('Cats are totally amazing!');
// Score: 4, Comparative: 1
{% endhighlight %}

Plus d'information sur [la page du package][sentiment].


[sentiment]: https://github.com/thisandagain/sentiment
