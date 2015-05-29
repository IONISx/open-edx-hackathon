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

* [LMS](https://github.com/edx/edx-platform) avec le [*responsive theme* IONISx](https://github.com/IONISx/edx-theme)
* [Studio](https://github.com/edx/edx-platform)
* [Forum](https://github.com/edx/cs_comments_service)
 
Pour installer une devstack sans le thème utilisez le script suivant :

```shell
curl -sL http://hack.ioni.sx/birch-themeless | sh
```

## Gestion

Une fois votre *devstack* Open edX installée, vous avez trois nouveaux répertoires dans votre dossier courant :

* `edx-platform`
* `themes`
* `cs_comments_service`

Ces répertoires sont les dépôts [Git](https://git-scm.com/) des différentes applications listées ci-dessus.
Ils sont synchronisés avec votre machine virtuelle.

Pour vous connecter à la machine virtuelle, entrez

```shell
vagrant ssh
```

### LMS

Pour lancer le LMS, depuis votre machine virtuelle, connectez-vous avec l’utilisateur `edxapp` :

```shell
sudo su edxapp
```

Vous allez automatiquement être placé dans le répertoire `/edx/app/edxapp/edx-platform` (synchronisé avec le répertoire `edx-platform` sur votre machine physique).

Lancez le LMS avec la commande suivante :

```shell
paver devstack lms
```

Vous pouvez maintenant naviguer sur le LMS, sur votre machine physique, en vous rendant sur [http://localhost:8000](http://localhost:8000).

Vous pouvez vous authentifier avec un des utilisateurs suivants :

| Nom d’utilisateur | Mot de passe |
| -- | -- |
| staff@example.com | edx |
| honor@example.com | edx |
| audit@example.com | edx |

### Studio

Pour lancer Studio, de la même manière que pour le LMS, lancez

```shell
paver devstack studio
```

Accédez à Studio, sur votre machine physique, en vous rendant sur [http://localhost:8001](http://localhost:8001).

Les bases de donnés sont partagées entre LMS et Studio, vous pourrez donc vous authentifier avec les mêmes identifiants.