# Installation

La dernière *release* stable de Open edX en date est [Birch](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/birch.html).

Pour plus d’information sur l’installation d’Open edX, rendez-vous sur la [documentation officielle](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/index.html).

## Applications

La plateforme Open edX est composée de plusieurs applications.

Le code des différents composants se trouve sur [GitHub](https://github.com/edx/).


### LMS (Learning Management System)

LMS est l’application principale d’Open edX, permettant aux apprenants (utilisateurs) de suivre les cours.

Il s’agit d’une application Django (Python).

[Installer le LMS](installation/plateforme.md).


### Studio (CMS – Content Management System)

Studio est l’application de création des cours et des contenus.

Il s’agit d’une application Django (Python).

[Installer Studio](installation/plateforme.md).

### Forum

Le forum est très étroitement liée au LMS. Il s’agit d’une API [REST](http://fr.wikipedia.org/wiki/Representational_State_Transfer) en Ruby, exposant des donnés de discussions.

Ces donnés sont ensuite affichées dans le LMS sous la forme de forums (un par cours).

[Installer le forum](installation/plateforme.md).