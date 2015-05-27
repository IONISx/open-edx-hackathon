# Plateforme

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

La commande ci-dessus va installer une *devstack* Open edX, comprenant les composants de la plateforme suivants :

* [LMS](https://github.com/edx/edx-platform)
* [Studio](https://github.com/edx/edx-platform)
* [Forum](https://github.com/edx/cs_comments_service)