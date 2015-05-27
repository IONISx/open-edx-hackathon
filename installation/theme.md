# Personnaliser le LMS

Il est possible de personnaliser l’interface du LMS à l’aide de thèmes.

En suivant le [guide d’installation de la plateforme](plateforme.html), vous avez le [thème IONISx](https://github.com/IONISx/edx-theme) installé par défaut.


## Thème IONISx

Le thème IONISx propose un nouveau thème pour Open edX en se basant sur [Bootstrap](http://getbootstrap.com).

Le code du thème se trouve, sur votre machine physique, dans le répertoire `themes/ionisx`.

### Environnement de développement

Le thème IONISx utilise un environnement de développement basé sur Node.js, en utilisant les outils [Grunt](http://gruntjs.com/) et [Bower](http://bower.io).

* Installez [Node.js](https://nodejs.org/).

* Installez les outils `grunt` et `bower` :

 ```shell
 npm install -g grunt-cli bower
 ```

* Installez les dépendances du thème :

 ```shell
 npm install
 bower install
 ```

Enfin, lancez `grunt` et laissez-le tourner dans un terminal.

Grunt va observer les changements sur les fichiers et automatiquement recompiler les fichiers qui seront utilisés par le LMS.

[Lancez le LMS](plateforme.html) et naviguez sur [http://localhost:8000](http://localhost:8000).

