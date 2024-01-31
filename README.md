# install-jdk
Ce script shell permet d'installer JDK ou JRE en spécifiant une des version LTS suivantes : **8, 11 , 17 , 21**

### **Installation JDK || JRE 8,11,17,21**

Pour installer JDK ou JRE en spécifiant une des versions LTS suivantes [8,11,17,21] sur votre système d'exploitation suivez ce guide :

### Pour quel fin vous avez besoin installer JDK ou JRE ?

>Vous avez besoin d'installer **JDK** lorsque vous développez des applications Java (JEE, JSE, Android, ...), vous avez besoin du JDK car il contient tous les outils de développement.  Il comprend le **JRE** et tous les outils nécessaires pour développer, compiler (__javac__ : le compilateur Java), déboguer et exécuter des applications Java.

>Vous avez besoin d'installer **JRE** (Java Runtime Environment) lorsque vous ne développez pas mais souhaitez exécuter des applications Java existantes, le JRE est suffisant. C'est-à-dire si vous avez un bytecode (Code intermédiaire, code compilé qui est appelé à être interprété et exécuté par la **JVM**). Le JRE contient le JVM (Java Virtual Machine) qui permet d'exécuter le code java compilé.

>Sur les distributions Red Hat Enterprise Linux (RHEL) et CentOS, le **JRE** (Java Runtime Environment) est généralement inclus dans le paquet OpenJDK. OpenJDK est la version open source de Java et est largement utilisé dans les distributions basées sur Red Hat.


### Clonez le script à partir de GitHub

**Nota** : Rassurez-vous d'avoir git installé, au cas contraire, il faut tout d'abord l'installer.

### Installation Git sur les distros basée sur RHEL

`sudo dnf install git-all`

### Installation Git sur les distros basée sur debian

`sudo apt install git-all`

### Clonez le script 

`git clone https://github.com/devops-shell/install-jdk.git`

Après avoir cloné le repository contenant le script, allez dans le répertoire **install-jdk** si vous n'avez pas nommé le répertoire dans le quel vous voulez cloner ledit script.

`cd install-jdk`

### Rendre le script exécutable

Assurez-vous de rendre le script exécutable avec la commande :

`chmod +x install-jdk.sh`

 Cette commande précédente va donner à l'utilisateur en cours le droit d'exécution du script


### Exécution du script

**Nota** : Vous devez être en mode sudo ou votre session shell doit avoir le droit super utilisateur puisque certaines commandes que contient ce script demandent d'avoir des droits super utilisateur.

#### Prérequis pour les distributions Red Hat Enterprise Linux (RHEL) et CentOS

**Nota** : Si vous utilisez une distribution Red Hat Enterprise Linux et vous avez déjà une version JDK installée. Vous devez d'abord la supprimer en saisissant cette commande : 

`dnf remove java-* -y`

### Guide d'exécution du script 


**-h**, **--helps**               Afficher l'aide

 Global Options :

  **-d**, **--jdk**          Installer jdk \
  **-r**, **--jre**          Installer jre \
  **-v**, **--version** <**number_version**> entier      Numero version jdk ou jre

  **Nota**: Les versions prises en charge sont **8 , 11 ,  17 et 21**


### 1. Afficher le guide d'installation

`sudo ./install-jdk.sh --helps`

ou 

`sudo ./install-jdk.sh -h`

 
**==========================**

### 2. Installation JDK


[1]  **Première possibilité**

`sudo ./install-jdk.sh --jdk --v 21`

[2] **Deuxième possibilité**

`sudo ./install-jdk.sh -d -v 21`


[3] **Troisième possibilité**

`sudo ./install-jdk.sh -dv 21`


**=========================**


### 3. Installation JRE

[1] **Première possibilité**

`sudo ./install-jdk.sh --jre --v 21`

[2] **Deuxième possibilité**

`sudo ./install-jdk.sh -r -v 21`


[3] **Troisième possibilité**

`sudo ./install-jdk.sh -rv 21`


**=========================**

**Nota** : Après avoir exécuté le script, le JDK ou le JRE sera installé. Et pour vérifier faites : 

#### Vérification de la version du compilateur installé 

`javac -version`

**Nota** : Cette commande ci-dessus n'est valable que si vous avez installé le JDK.

#### Vérification de la version Java installé 

`java -version`





