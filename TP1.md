# TP 1 - Prise en main d’un micro-contrôleur

Ce TP a pour but deux objectifs : 1. Vous familiariser avec l’environnement de développement qui sera utilisé pendant tous les TP IoT. 2. Vous faire découvrir la programmation d’un micro-contrôleur.

## Exercice 1. Étude du système

— Utiliser les modules RF Sub-1Ghz de Techno-Innov.
http://techdata.techno-innov.fr/Modules/RF-Sub1G/System_Reference_Manual_RF_Sub1GHz_USB_v03.pdf

La première et la plus importante est celle du micro-contrôleur, mais vous aurez aussi besoin de celle du module RF et celles de l’EEPROM I2C et du capteur de température I2C


 
L’accès à cette liaison série se fera via un fichier spécial dont le nom devrait ressembler à "/dev/ttyUSB0", le "USB0"
Attention : La machine virtuelle que vous allez utiliser à une liaison du port /dev/ttyUSB0 de votre machine hôte vers le port /dev/ttyS3 de la distribution Linux virtuelle

## Exercice 2. Documentations techniques

### Question 1. Une chaîne de cross-compilation pour micro-contrôleurs ARM est déjà installée sur la VM fournie. Quelle est cette chaîne de cross-compilation ? Comment l’utilise-t-on ? Utilisez l’option -v de gcc (celui de la chaîne de cross-compilation) pour identifier la version et vérifier qu’il s’exécute correctement.

Pour permettre l’étude de l’exemple suivant et permettre le développement "linux embarqué" par la suite, nous avons aussi installé deux autres chaines de compilation pour ARM : gcc-arm-linux-gnueabi et gcc-arm-linux-gnueabih.

### Question 2. Quelles sont les différences entre ces trois chaînes de compilation croisée ?

Programmation : lpctools
disponible sur le dépôt GIT de Techno-Innov (http://git.techno-innov.fr/?p=lpctools), et est intégré depuis peu à la distribution Debian GNU/Linux.

Remarque. Comme vous n’avez pas les permissions nécessaires pour installer des paquets dans les machines CPE, vous pouvez aussi télécharger les sources de lpctools et les compiler pour l’utiliser depuis votre espace de travail.

## Exercice 3. Test du module

Dans la VM, l’utilitaire minicom est déjà installé, et il permet de récupérer ces messages. (La configuration de minicom est expliquée sur la page concernant le système de développement http://www.nathael.org/wiki_cpe/index.php/Dev/Host#Minicom).

Remarque. Le port USB de votre machine normalement apparaît sous le nom /dev/ttyUSB0, pour pouvoir l’utiliser dans ce TP, il est lié à la VM debian_aiot directement, il apparaît sous le nom /dev/ttyS3 dans votre VM.

Depuis votre VM testé la connexion avec minicom :
minicom -ow -D /dev/ttyS3
Vous devriez voir les messages suivants s’afficher :
Module RF-SUB 1GHz.
CPE Lyon.

Remarque. Pour sortir de minicom utiliser le raccourci Ctrl+A, puis Z et puis Q





