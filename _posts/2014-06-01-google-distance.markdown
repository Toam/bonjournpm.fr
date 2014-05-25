---
layout: post
title:  "Google-distance"
subtitle: "Permet de calculer simplement la distance entre deux points"
category: outils 
---

[Google-distance][google-distance] est un package NPM qui permet
d'utiliser l'API de Google pour calculer la distance entre deux points. 

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install google-distance
{% endhighlight %}

On peut ensuite faire simplement des requêtes en utilisant la puissance
de l'API de Google pour déterminer le points de départs et celui de
destinations :
{% highlight js %}
var distance = require('google-distance');

distance.get(
  {
    origin: 'San Francisco, CA',
    destination: 'San Diego, CA'
  },
  function(err, data) {
    if (err) return console.log(err);
    console.log(data);
});
{% endhighlight %}

La requête ci-dessus donne le résultat suivant :
{% highlight js %}
{
  index: null,
  distance: '807 km',
  distanceValue: 807366,
  duration: '7 hours 30 mins',
  durationValue: 26981,
  origin: 'San Francisco, CA, USA',
  destination: 'San Diego, CA, USA',
  mode: 'driving',
  units: 'metric',
  language: 'en',
  avoid: null,
  sensor: false
}
{% endhighlight %}

Plus d'information sur [la page du package][google-distance].


[google-distance]: https://github.com/edwlook/node-google-distance
