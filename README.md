# Robot-Tout-Terrain
Ce programme est conçu pour contrôler un robot mobile à 4 moteurs via une connexion Bluetooth à l’aide d’un module (comme HC-05) connecté au port série de l’Arduino. Le robot peut effectuer plusieurs mouvements selon les caractères reçus : avancer, reculer, tourner à gauche/droite, virer ou s'arrêter.

⚙️ Composants matériels utilisés :
Carte Arduino UNO (ou similaire)

8 relais pour inverser la polarité des moteurs (4 relais par côté pour le contrôle H-bridge manuel)

Carte de variation de vitesse (contrôle PWM, connectée à la broche D11)

Module Bluetooth (ex. HC-05 ou HC-06)

Abaisseur de tension (buck converter) pour adapter la tension batterie (12V) à 5V pour l’Arduino et le module Bluetooth

Batterie (ex. 12V)

Caméra Cognex

⚡ Principe de fonctionnement :
Les relais servent à inverser la polarité des moteurs pour les faire tourner dans un sens ou dans l’autre.

Le signal PWM sur la broche D11 (via analogWrite) est envoyé à la carte de variation de vitesse, qui ajuste la vitesse des moteurs.

Le module Bluetooth reçoit des caractères depuis une application smartphone et les transmet à l’Arduino.

Le code Arduino lit le caractère reçu et exécute la fonction de mouvement correspondante (ex: fwd(), left(), rev(), etc.).


![image](https://github.com/user-attachments/assets/94d1632f-f6cb-4afd-813a-df71025fc6b5)
