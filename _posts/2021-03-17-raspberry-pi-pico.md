---
layout: default
title: "MicroPython auf dem Raspberry Pi Pico"
image: /static/2021-03-16-raspberry-pi-pico/raspberry-pi-pico.jpg
category: micropython   
tags: Pico
vgwort: 4711
---

Die Raspberry Pi Foundation hat nach den bisherigen Raspberry Pis, die ja eher "komplette Computer" sind, nun ein Mikrocontroller-Board  herausgebracht. Der **[Raspberry Pi Pico](https://www.raspberrypi.org/products/raspberry-pi-pico/)** steht in Konkurrenz zu Arduino- oder ESP32-Boards und lässt sich wie diese in C oder MicroPython Programmieren. In diesem Beitrag wird gezeigt, wie man das Board in Betrieb nimmt und ersten Python-Code darauf ausführt.

<img src="/static/2021-03-16-raspberry-pi-pico/raspberry-pi-pico.jpg" alt="Der neue Raspberry Pi Pico mit dem RP2040-Mikrocontroller" class="responsive">

## Installieren von MicroPython

Zur Installation von MicroPython auf dem Raspberry Pi Pico ist zunächst ein UF2-File zu laden, man erhält es [hier](https://www.raspberrypi.org/documentation/pico/getting-started/). Diese Datei muss nun auf den Pico gebracht werden. Dazu wird das Board per USB mit dem PC oder Mac verbunden, und dabei der weiße BOOTSEL-Schalter gedrückt werden. Er befindet sich in der Nähe des USB-Anschlusses auf dem Board. Der Pico wird dadurch unter dem Namen RPI-RP2 ins Dateisystem eingehängt. Das UF2-File wird dann einfach über Drag-and-drop in dieses Verzeichnis geschoben. Der Raspberry Pi Pico bootet danach automatisch und ist einsatzbereit.

## Verbinden mit REPL

Hat das geklappt, kann man sich mit *REPL* (Read Evaluate Print Loop), dem interaktiven Python Prompt von MicroPython auf dem Mikrocontroller verbinden. Das geschieht mit Hilfe eines Terminal Emulators, unter MacOS beispielsweise mit screen:

    screen  /dev/tty.usbmodemFA141 115200

Wichtig: Nach dem Bestätigen des Kommandos mit Return muss man nochmal Return drücken (also insgesamt 2x). Die erfolgreiche Verbindung wird dann durch den REPL-Prompt (>>>) angezeigt. Hier lassen sich nun Python-Kommandos direkt ausführen:

![In REPL lassen sich Python-Kommandos direkt ausühren.](/static/2021-03-16-raspberry-pi-pico/repl-raspberry-pi-pico.jpg)

Mit ein paar Zeilen Code lässt sich zum Beispiel die grüne LED auf dem Board aktivieren, sie wird über PIN 25 angesprochen:

    >>> from machine import Pin
    >>> led = Pin(25, Pin.OUT)
    >>> led.value(1)


