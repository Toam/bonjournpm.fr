---
layout: post
title:  "Config-node"
subtitle: "Un chargeur de configuration simple et flexible"
category: 
---

[Config-node][config-node] est un package NPM qui permet de gérer
plusieurs configurations suivant l'environement.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install config-node
{% endhighlight %}

On peut ensuite charger des paramètres simplement :
{% highlight js %}
var config = require('config-node')();
console.log(config.server.port);
{% endhighlight %}

Dans cette exemple `config` contiendra les informations relatives à
l'environement. Il est possible de configurer son comportement :

{% highlight js %}
var config = require('config-node')({
    dir: 'config', 
    env: 'development'
});
{% endhighlight %}

Il est possible d'utiliser des fichiers de configurations en JSON, YAML,
INI, XML, etc.  Plus d'information sur [la page du package][config-node].


[config-node]: https://github.com/flesler/config-node
