from grovepi import *
import time
import serial
import RPi.GPIO as GPIO
GPIO.setmode(GPIO.BCM)
led = 3
pinMode(led,"OUTPUT") 
Tag1 = str('5700B8A0D29D')
PortRF = serial.Serial('/dev/ttyS0',9600)
while True:
    #print(PortRF.read())
    ID = ""
    read_byte = PortRF.read()
    if read_byte=="\x02":
        for Counter in range(12):
            read_byte=PortRF.read()
            ID = ID + str(read_byte)
       # print (ID)
        if ID == Tag1:
            print ("matched")
            try:
                #Blink the LED
                digitalWrite(led,1)     # Send HIGH to switch on LED
                time.sleep(5)
                digitalWrite(led,0)
            except KeyboardInterrupt:   # Turn LED off before stopping
                digitalWrite(led,0)
                break
            except IOError:             # Print "Error" if communication error encountered
                print "Error"
        else:
            print ("Access Denied")
            time.sleep(5)
