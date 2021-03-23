# Raspberry_RFID_125kHz
Programme permettant de connecter le capteur RFID 125 kHz à une Raspberry en utilisant une GrovePi.  

Allumage d'une led lorsque l'id correspond.

Branchement:
Utilisation d'une GrovePi, le branchement du capteur Rfid est sur le port RPISER de la GrovePi, la led sur le port D3 de la GrovePi.

Initialisation:
installation de GrovePi : 
''' 

curl -kL dexterindustries.com/update_grovepi | bash 

'''

Erreur possible lors de l'utilisation:

![alt text](https://github.com/ThomasCappe/Raspberry_RFID_125kHz/blob/9f252e324406910a58d6b7846abd2699ed609ae1/image_error1.jpg?raw=true)

Pour résoudre ce probléme utilisez la commande suivante : sudo systemctl stop serial-getty@ttyS0.service


![alt text](https://github.com/ThomasCappe/Raspberry_RFID_125kHz/blob/5358fd666b5e124ec6cd88bf7660bc3ddba9dc99/Montage_1.jpg?raw=true)
![alt text](https://github.com/ThomasCappe/Raspberry_RFID_125kHz/blob/5358fd666b5e124ec6cd88bf7660bc3ddba9dc99/Montage.jpg?raw=true)
