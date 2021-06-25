# CircuitPython mit dem Adafruit Feather M0 Expres

TEASER

BILD VOM Feather
## Feather M0 Express einrichten

UF2-File Laden (adafruit-circuitpython-feather_m0_express-de_DE-6.3.0.uf2)
Feather über USB mit dem Rechner Verbinden
Knopf doppelt klicken (größere LED leuchtet grün, ein Gerät FEATHERBOOT taucht auf)
uf2 File nach  FEATHERBOOT kopieren, Feather startet automatisch neu und ein Laufwerk namens CIRCUITPY ist vorhanden

## Mu
Mu is designed for CircuitPython
installieren uns starte

Mode CircuitPython auswählen

<img src="/static/circuitpython-feather-m0-express/mode-circuitpython.PNG" alt="Modus CircuitPython" class="img-fluid">


Danach öffnet sich die IDE. In der Statusbar ganz unten soltte rechts  CircuityPython stehen und das Microcontroller-Symbol daneben kein rotes X drauf haben:

<img src="/static/circuitpython-feather-m0-express/mu-connected.PNG" alt="Mu ist mit dem Feather M0 verbunden" class="img-fluid">

Ist das der Fall wird es Zeit für einen ersten Programmierversuch. Dazu wird das folgende Codestück in Mu eingegeben oder kopiert:

```Python
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
```

Nach dem Speichern auf CIRCUITPY unter dem Namen code.py wirde der Code sofort  ausgeführt, die rote LED blinkt.
Um die print-Ausgabe sehen zu können verbindet man Mu mit der seriellen Konsole (Klick auf den Button _Seriell_.)

<img src="/static/circuitpython-feather-m0-express/serielle-konsole.PNG" alt="Mu ist mit dem Feather M0 verbunden" class="img-fluid">


##

BMP280 anschliessen



lib.Sammlung (adafruit-circuitpython-bundle-6.x-mpy-20210623) runterladen, entpacken

dier erford4lrichen lib-Ordner (adafruit_bme280, noch einer) in den Ordner lib auf dem Feather kopieren

```Python
import board
from adafruit_bme280 import basic as adafruit_bme280
i2c = board.I2C()  # uses board.SCL and board.SDA
bme280 = adafruit_bme280.Adafruit_BME280_I2C(i2c, address=0x76)

print("\nTemperature: %0.1f C" % bme280.temperature)
print("Humidity: %0.1f %%" % bme280.humidity)
print("Pressure: %0.1f hPa" % bme280.pressure)
```
