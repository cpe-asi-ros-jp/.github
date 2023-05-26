# ASI adaptée à la Robotique
- Partie 1 : [github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX1](https://github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX1/)
- Partie 2 : [github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX2](https://github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX2/)
- Partie 3 : [github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX3](https://github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX3/)
- Partie 4 : [github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX4](https://github.com/cpe-asi-ros-jp/4IRC_ASIROS_PLANCHON_EX4/)

## Cahier des charges
### Les besoins
#### Principaux
- (a) Remonté information contrôle (start/stop sur un équipement)
- (b) Remonté d’information sporadique (appuie bumper)
- (c) Remontée de flux d’information (flux video, flux audio)

#### Annexes
- (d) Des besoins d’Interface Homme Robot (Controller le lancement des traitements quand nécessaire)
- (e) Une nécessité de Déploiement
- (f) L’importance des Test, surtout à un niveau système/intégration
- (g) Le Paramétrage des traitements
- (h) La Remonté information de debug en fonctionnement
- (i) La Problématique de conservation et distribution de log
- (j) L’authentification et les droits d’accès qui est généralement un problème centrale de la distribution mais malheureusement pas encore en robotique

### Scénario
Une installation de type domotique ou équivalent (ca pourrait aussi être un robot) comporte les équipements suivants :
- 2 sondes de températures envoyant des informations toutes les 10s
- 5 sondes à déclenchement de proximité
- Dix actionneurs en tout ou rien
- 2 moteurs contrôlés en position et qui peuvent renvoyer une erreur en cas de problème (surchauffe ou impossibilité d’atteindre la position après un timeout à définir)
- 2 caméras ( flux camera entre 10 et 30 images par secondes )
- Un microphone et 2 hauts parleurs (On considère donc 3 flux audio, 1 flux microphone et 2 flux à destinations des hauts parleurs)
- Une logique d’affichage sous forme d’écran

L’objectif du système est de pouvoir créer des applications permettant la mise en œuvre de ses capteurs/actionneurs.  

Un cas typique est de considérer un contrôleur qui permet de controller les actionneurs et de récupérer les informations des capteurs. Dans le cas des flux videos et audio , on souhaite les coupler à des outils d’intelligence artificielles, en particulier de la détection d’objets ou de la reconnaissance de visage ou encore un système de chatbot. Ces différentes applications doivent pouvoir être facilement distribués.
