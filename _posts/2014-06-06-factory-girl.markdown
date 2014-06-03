---
layout: post
title:  "Factory girl"
subtitle: "gerez simplement les données de vos tests unitaires"
category: tests
---

[Factory-girl][factory-girl] est un package NPM qui permet de générer
des données pour vos tests. Ce package est inspiré du très célèbre
factory-girl de Ruby on Rails.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install factory-girl
{% endhighlight %}

On peut ensuite générer des données, comme par exemple ici des
utilisateurs avec une adresse mail unique et un mot de passe :
{% highlight js %}
var factory = require('factory-lady'),
    User    = require('../../app/models/user'),

var emailCounter = 1;

factory.define('user', User, {
  state: 'active',
  email: function() {
    return 'user' + emailCounter++ + '@example.com';
  },
  password: '123456'
});
{% endhighlight %}

On a ensuite un objet User qu'il est possible d'utiliser dans un test :
{% highlight js %}
factory('user', function(err, post) {
  // test
});
{% endhighlight %}

Plus d'information sur [la page du package][factory-girl].


[factory-girl]: https://github.com/
