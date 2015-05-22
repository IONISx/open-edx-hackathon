# Installation

Open edX release environ une fois par semaine.

Il existe des releases *stables*, la dernière en date est [Birch](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/birch.html).

Open edX est composé de plusieurs applications, principalement LMS, Studio et des workers.

Le code se trouve sur [GitHub](https://github.com/edx/edx-platform).

Pour plus d’information sur l’installation d’Open edX, rendez-vous sur la [documentation officielle](http://edx.readthedocs.org/projects/edx-installing-configuring-and-running/en/latest/index.html).

## tl;dr

```shell
curl -sL https://ionisx.fr-1.storage.online.net/hack/go | sh
```

## Environnement de développement

Que vous soyez sur Mac, Windows ou Linux, nous vous conseillons d’utiliser une box [Vagrant](https://www.vagrantup.com/) pour installer votre environnement.

Pour se faire, installez [VirtualBox](https://www.virtualbox.org/wiki/Downloads), puis [Vagrant](https://www.vagrantup.com/downloads.html).

Une box Vagrant est simplement une machine virtuelle pré-configurée. Il est possible d’avoir des dossiers partagés entre votre machine physique et la machine virtuelle, ceci vous permettant de travailler sur votre machine et d’executer Open edX sur la machine virtuelle.

Enfin, utiliser une box Vagrant vous permettra d’éviter d’installer toutes les dépendances d’Open edX sur votre machine.

## Installer Open edX Birch

* Créez un nouveau dossier de travail sur votre machine :

 ```shell
 mkdir devstack && cd devstack
 ```

* Téléchargez le [Vagrantfile](https://ionisx.fr-1.storage.online.net/hack/Vagrantfile) (fichier de configuration de la box Vagrant) :

 ```shell
 curl -sL https://ionisx.fr-1.storage.online.net/hack/Vagrantfile > Vagrantfile
 ```

* Installez le plugin [vbguest](https://github.com/dotless-de/vagrant-vbguest) de Vagrant :

 ```shell
 vagrant plugin install vagrant-vbguest
 ```
 
* Définissez la variable d’environnement `OPENEDX_RELEASE` (détermine la version d’Open edX à installer) :

 ```shell
 export OPENEDX_RELEASE="named-release/birch"
 ```
 Si vous ne définissez pas cette variable, la dernière version d’Open edX sera installée.

* Créez et démarrez la machine virtuelle :

 ```shell
 vagrant up
 ```

* Il se peut que le mot de passe administrateur de votre machine soit demandé, si c’est le cas, saisissez-le.