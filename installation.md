# Installation

Open edX release environ une fois par semaine.

Il existe des releases *stables*, la dernière en date est [Birch](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/birch.html).

Open edX est composé de plusieurs applications, principalement LMS, Studio et des workers.

Le code se trouve sur [GitHub](https://github.com/edx/edx-platform).

Pour plus d’information sur l’installation d’Open edX, rendez-vous sur la [documentation officielle](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/index.html).


## Environnement de développement

Que vous soyez sur Mac, Windows ou Linux, nous vous conseillons d’utiliser une box [Vagrant](https://www.vagrantup.com/) pour installer votre environnement.

Pour ce faire, installez [VirtualBox](https://www.virtualbox.org/wiki/Downloads), puis [Vagrant](https://www.vagrantup.com/downloads.html).

Une box Vagrant est simplement une machine virtuelle pré-configurée. Il est possible d’avoir des dossiers partagés entre votre machine physique et la machine virtuelle, ceci vous permettant de travailler sur votre machine et d’executer Open edX sur la machine virtuelle.

Enfin, utiliser une box Vagrant vous permettra d’éviter d’installer toutes les dépendances d’Open edX sur votre machine.


Créez un nouveau répertoire de travail :

```shell
mkdir devstack && cd devstack
```

Installez votre environnement de développement :

```shell
curl -sL http://hack.ioni.sx/birch | sh
```