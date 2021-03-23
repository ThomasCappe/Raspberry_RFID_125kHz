# Raspberry_RFID_125kHz
Programme permettant de connecter le capteur RFID 125 kHz à une Raspberry en utilisant une GrovePi.  

Allumage d'une led lorsque l'id correspond.

Branchement:
Utilisation d'une GrovePi, le branchement du capteur Rfid est sur le port RPISER de la GrovePi, la led sur le port D3 de la GrovePi.

Initialisation:
installation de GrovePi : curl -kL dexterindustries.com/update_grovepi | bash

Erreur possible lors de l'utilisation:

![alt text](https://github.com/ThomasCappe/[Raspberry_RFID_125kHz/blob/main/image_error1.jpg?raw=true)

Pour résoudre ce probléme utilisez la commande suivante : sudo systemctl stop serial-getty@USB0.service
