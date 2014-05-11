---
layout: post
title:  "Asyncawait"
subtitle: "Ecrivez du code asynchrone plus facilement"
category: code
---

[Asyncawait][asyncawait] est un package NPM qui permet de gérer
facilement des flux asynchrones et d'avoir du code lisible simplement.

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install asyncawait
{% endhighlight %}

Le package permet de transformer ce code :
{% highlight js %}
function foo2(callback) {
    firstAsyncCall(function (err, resultA) {
        if (err) { callback(err); return; }
        secondAsyncCallUsing(resultA, function (err, resultB) {
            if (err) { callback(err); return; }
            thirdAsyncCallUsing(resultB, function (err, resultC) {
                if (err) {
                    callback(err);
                } else {
                    callback(null, doSomethingWith(resultC));
                }
            });

        });
    });
}
{% endhighlight %}

Grâce au package, on peut écrire ce même code de la façon suivante : 
{% highlight js %}
var foo = async (function() {
    var resultA = await (firstAsyncCall());
    var resultB = await (secondAsyncCallUsing(resultA));
    var resultC = await (thirdAsyncCallUsing(resultB));
    return doSomethingWith(resultC);
});
{% endhighlight %}

Plus d'information sur [la page du package][asyncawait].


[asyncawait]: https://github.com/yortus/asyncawait
