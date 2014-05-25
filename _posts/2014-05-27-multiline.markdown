---
layout: post
title:  "Multiline"
subtitle: "Permet d'ecrire des chaines sur plusieurs lignes sans
concaténations"
category: code 
---

[Multiline][multiline] est un package NPM qui utilise une astuce pour
vous permettre d'écrire des chaines sur plusieurs lignes sans utiliser
de concaténation ou de join().

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install multiline
{% endhighlight %}

Sans le package, on écrivait les chaines de cette façon :
{% highlight js %}
var str = '' +
'<!doctype html>' +
'<html>' +
'   <body>' +
'       <h1>❤ unicorns</h1>' +
'   </body>' +
'</html>' +
'';
{% endhighlight %}

Il est maintenant possible de le faire de cette façon :
{% highlight js %}
var str = multiline(function(){/*
<!doctype html>
<html>
    <body>
        <h1>❤ unicorns</h1>
    </body>
</html>
*/});
{% endhighlight %}

Attention, bien que cette méthode soit plus simple à lire et a écrire,
il y a un impact non négligeable sur les performances.

Plus d'information sur [la page du package][multiline].


[multiline]: https://github.com/sindresorhus/multiline
