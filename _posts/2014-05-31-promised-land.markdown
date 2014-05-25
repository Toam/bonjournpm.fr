---
layout: post
title:  "Promised-land"
subtitle: "Fini les events, vive les Promises"
category: code
---

[Promised-land][promised-land] est un package NPM qui permet
d'utiliser des Promises plutôt que des évènements.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install promised-land
{% endhighlight %}

Dans l'exemple ce-dessous, on peut voir qu'une promise attend la
connexion à la base de données avant de s'exécuter :
{% highlight js %}
// Dans notre code, il est possible de place un bout de code qui ne sera exécuté que lorsque la connexion à la base de données sera effectué.
var Land = require('promised-land');
Land.promise('databaseConnected').then(function(db) {
    doSomethingWithDatabase();
});

// dans la gestion de la connexion à la base, on appele databaseConnected lorsque la connexion a marché. 
var Land = require('promised-land');
Land.emit('databaseConnected', db);
{% endhighlight %}

Plus d'information sur [la page du package][promised-land].


[promised-land]: https://github.com/FredyC/promised-land/
