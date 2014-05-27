---
layout: post
title:  "lazy-install"
subtitle: "Gérer efficacement les dépendances de vos projets"
category: code
---

[Lazy-install][lazy-install] est un package NPM qui permet de gérer les dépendances au démmarage d'un projet node.js. Les modules sont mis en cache et ré-utilisable entre les projets.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install lazy-install
{% endhighlight %}

La définition des dépence se fait toujours dans le fichier `package.json` :
{% highlight js %}
{
  "name": "myProject",
  "lazyDependencies": {
    "server": {
      "express": "4.0.0"
    },
    "test": {
      "mocha": "1.18.2"
    }
  }
}
{% endhighlight %}

On peut ensuite gérer directement l'instalation des modules depuis le code.
{% highlight js %}
var lazy = require("lazy-install");
lazy.install(function (err, installed) {
  if (err) throw new Error(err);
  console.log(installed.count, installed.time);
});
{% endhighlight %}

Plus d'information sur le package et la gestion fine des dépendances sur [la page du package][lazy-install].


[lazy-install]: https://github.com/adamrenklint/lazy-install
