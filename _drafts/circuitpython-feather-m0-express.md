## Feather M0 Express einrichten

UF2-File Laden (adafruit-circuitpython-feather_m0_express-de_DE-6.3.0.uf2)
Feather über USB mit dem Rechner Verbinden
Knopf doppelt klicken (größere LED leuchtet grün, ein Gerät FEATHERBOOT taucht auf)
uf2 File nach  FEATHERBOOT kopieren, Feather startet automatisch neu und ein Laufwerk namens CIRCUITPY ist vorhanden

## Mu
Mu is designed for CircuitPython
installieren uns starte



Mode CircuitPython auswählen
BILD


in der rechten unteren Ecke sollte circuitypythn stehen und der Prozi kein rotes x drauf haben
BILD



Beispielcode eingeben:

import board
import digitalio
import time

led = digitalio.DigitalInOut(board.LED)
led.direction = digitalio.Direction.OUTPUT

while True:
 		print("Hello, CircuitPython!")
    led.value = True
    time.sleep(0.5)
    led.value = False
    time.sleep(0.5)

Speichern auf CIRCUITPY unter code.py

Code wird sofot ausgeführt, rote LED blinkt

Aber wo landet die Print-Ausgabe -> Verbinden mit der seriellen Konsole

BILD
