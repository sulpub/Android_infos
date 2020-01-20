# Android Informations

## ADB list commands

Android Debug Bridge

Voici une liste des commandes ADB qui nous retrouvons le plus souvent sur internet quand il s'agit de modifier son appareil ou d’effectuer des actions diverses.


### adb help

Cette commande permet d'avoir la liste des commandes disponibles via l'ADB, cette dernière est très utile lorsque nous oublions les paramètres à passer aux commandes.


### adb-help

### adb logcat

Cette commande permet de visualiser le log spécifique à l'appareil ou à l'émulateur.

### adb devices

Cette commande permet d'afficher la liste des émulateurs (lancés via le SDK Android) et des appareils branchés en USB à l'ordinateur et pouvant être administrés avec l'ADB.

### adb-devices

### adb kill-server

Cette commande a pour but d'éteindre le serveur ADB. Une fois cette commande tapée, il vous faudra relancer la commande adb devices pour remettre en ligne le serveur adb.

### adb-kill-server

### adb start-server

Cette commande permet de s'assurer qu'un serveur est toujours en cours d'exécution.

### adb-start-server

### adb wait-for-device

Cette commande permet de bloquer toute exécution jusqu'à ce qu'un appareil ou un émulateur soit connecté.

 ### adb get-state

Cette commande permet de connaître en temps souhaité l'état de l'appareil ou de l'émulateur connecté : hors-ligne (offline), bootloader, normal (device).

### adb get-serialno

Cette commande permet d'obtenir le numéro de série de l'appareil connecté.

### adb -s "device"  "commande"

Cette commande permet d'appliquer une commande spécifique sur un des terminaux listés. 
Ex : adb -s emulator-5554 install proofofconcept.apk

### adb install "chemin-accès-fichier-apk"

Cette commande permet lorsque nous sommes en possession du fichier .apk d'une application, de pouvoir l'installer sur l’appareil ou émulateur connecté.

### adb pull "chemin-accès-fichier-appareil" "chemin-accès-placer-fichier-ordinateur"

Cette commande permet de déplacer un fichier se trouvant sur un appareil ou un émulateur vers l'ordinateur directement sans passer par la gestion de la carte mémoire.

### adb push "chemin-accès-placer-fichier-ordinateur" "chemin-accès-fichier-appareil"

Cette commande permet de déplacer un fichier se trouvant sur l'ordinateur vers l'appareil ou l'émulateur connecté sans passer par la gestion de la carte mémoire.

### adb -s "device" shell

Cette commande permet d'ouvrir une saisie de commande shell, comme si nous étions sur le terminal Linux. De cette façon nous pouvons utiliser les commandes shell basiques de Linux. 
Ex : adb -s emulator-5554 shell

### adb-shell-terminal

    adb -s -d "device" shell "commande shell"

Cette commande permet d'utiliser les commandes shell basiques de Linux directement sur le terminal sélectionné, sans passer par l'application Terminal Emulator. 
Ex :  adb -s emulator-5554 shell ls

### adb-shell-commande

### adb install "C:cheminaccesapplicationnom-de-l'application".apk

Cette commande, en indiquant le chemin d'accès entier vers le fichier .apk à installer permet d'installer l'application souhaitée sur le téléphone connecté à l'ordinateur ou bien sur l'émulateur directement. Cela peut être pratique pour tester son application avant déploiement final sur le Play Store.

Ex : adb install C:Usersmarshallino16Documentsproofofconcept.apk

### adb uninstall nom-application.apk

Cette commande permet de supprimer de l'appareil ou de l'émulateur un package sans passer par l'interface graphique. Il est également possible d'utiliser le paramètre "-k" afin de garder la mémoire cache de l'application si à l'avenir vous souhaitez réutiliser cette dernière.

### adb bugreport

Cette commande permet de reporter toutes les données de l'appareil ou de l'émulateur pouvant avoir été incluses dans le bug report.

### adb reboot "mode souhaité"

Cette commande permet de rebooter (NDLR : redémarrez) votre appareil ou l'émulateur dans le mode souhaité. Cela est souvent utilisé pour flasher une nouvelle ROM ou un nouveau packlage .zip.
Ex : adb reboot recovery ou encore adb reboot bootloader.

Vous voici désormais en possession des principales commandes ADB faites en bon usage ! 
