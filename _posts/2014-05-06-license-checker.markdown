---
layout: post
title:  "license-checker"
subtitle: "Pour avoir des informations sur les licences des dépendances"
category: outils
---

[license-checker][license-checker] est un package NPM qui permet de
connaitre les licences utilisées dans vos projets. 

Il est possible d'installer ce package grâce à la commande :
{% highlight bash %}
$ npm install license-checker -g
{% endhighlight %}

La commande `license-checker` permet d'avoir des informations sur les licences des dépendances du
projet. 

Voici par exemple ce qu'on obtient sur les dépendances de `yui-lint`

{% highlight bash %}
scanning ./yui-lint
├─ cli@0.4.3
│  ├─ repository: http://github.com/chriso/cli
│  └─ licenses: MIT
├─ glob@3.1.14
│  ├─ repository: https://github.com/isaacs/node-glob
│  └─ licenses: UNKNOWN
├─ graceful-fs@1.1.14
│  ├─ repository: https://github.com/isaacs/node-graceful-fs
│  └─ licenses: UNKNOWN
├─ inherits@1.0.0
│  ├─ repository: https://github.com/isaacs/inherits
│  └─ licenses: UNKNOWN
├─ jshint@0.9.1
│  └─ licenses: MIT
├─ lru-cache@1.0.6
│  ├─ repository: https://github.com/isaacs/node-lru-cache
│  └─ licenses: MIT
├─ lru-cache@2.0.4
│  ├─ repository: https://github.com/isaacs/node-lru-cache
│  └─ licenses: MIT
├─ minimatch@0.0.5
│  ├─ repository: https://github.com/isaacs/minimatch
│  └─ licenses: MIT
├─ minimatch@0.2.9
│  ├─ repository: https://github.com/isaacs/minimatch
│  └─ licenses: MIT
├─ sigmund@1.0.0
│  ├─ repository: https://github.com/isaacs/sigmund
│  └─ licenses: UNKNOWN
└─ yui-lint@0.1.1
   ├─ licenses: BSD
      └─ repository: http://github.com/yui/yui-lint
{% endhighlight %}

Il est aussi possible d'utiliser `--json fichier.json` pour exporter les
données dans un fichier.

Plus d'information sur [la page du package][license-checker].

[license-checker]: https://github.com/davglass/license-checker
