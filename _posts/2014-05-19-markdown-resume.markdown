---
layout: post
title:  "Markdown-resume"
subtitle: "Générez votre cv à partir d'un fichier en markdown"
category: 
---

[Markdown-resume][markdown-resume] est un package NPM qui permet de générer un CV à partir d'un fichier en markdow. Le rendu est assez sympa, voici [un exemple][cv].

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install -g markdown-resume
{% endhighlight %}

A partir du fichier en markdown, il est ensuite très simple de générer un CV en HTML ou en PDF :
{% highlight bash %}
# Generate HTML file
md2resume my-resume-file.md

# Generate PDF file
md2resume --pdf my-resume-file.md
{% endhighlight %}

Plus d'information sur [la page du package][markdown-resume].


[cv]: http://bitlyfieddotcom.files.wordpress.com/2013/03/name-surname-cv.pdf
[markdown-resume]: https://github.com/c0bra/markdown-resume-js
