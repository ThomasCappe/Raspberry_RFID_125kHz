# Raspberry_RFID_125kHz
Programme permettant de connecter le capteur RFID 125 kHz à une Raspberry en utilisant une GrovePi.  

Allumage d'une led lorsque l'id correspond.

##titreBranchement:
Utilisation avec GrovePi, le branchement du capteur Rfid est sur le port RPISER de la GrovePi, la led sur le port D3 de la GrovePi.
Utilisation sans GrovePi, le branchement du capteur (RFID_125mHz -> Raspberry): Vcc -> 5V ; GND -> GND ; RX -> RX ; TX -> TX


## Initialisation:

### 1.installation de GrovePi : 
```python
curl -kL dexterindustries.com/update_grovepi | bash 
```
### 2.clone du programme 
```python
git clone https://github.com/ThomasCappe/Raspberry_RFID_125kHz.git
```
### Conseil: Utiliser cette commande avant de lancer le programme
```python
sudo systemctl stop serial-getty@ttyS0.service
```
### 3.Lancer le programme
```python
sudo python2 RFID_Reader.py
```

## Erreur possible lors de l'utilisation:

```python
nano ^@^CTraceboack (most recent call last):
  File "RFID_Reader.py", line 10, in <module>
    read_byte = PortRF.read()
  File "/usr/lib/python2.7/dist-packages/serial/serialposix.py", line483, in read
    ready, _, _ = select.sekect([self.fd, sekf.pipe_abort_read_r], [], [], timeout.time_left())
KeyboardInterrupt
```
Pour résoudre ce probléme utilisez la commande suivante : 
```python
sudo systemctl stop serial-getty@ttyS0.service
```
![alt text](https://github.com/ThomasCappe/Raspberry_RFID_125kHz/blob/7744bbae006db7484f188b4d730c773c4ac9c4aa/Montage.jpg?raw=true)
