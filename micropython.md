---
layout: default
title: MicroPython
# KW: micropython
---

Das Kickstarter-Projekt [MicroPython](https://micropython.org) von Damien George ist eine zur Version 3 kompatible Python-Implementierung, die auf verschiedenen Architekturen wie zum Beispiel ARM oder dem Raspberry Pi Pico läuft. Das offizielle Entwicklungsboard nennt sich _pyboard_, es ist je nach Ausstattung ab ca. etwa 20 Euro zu bekommen. MicroPython funktioniert aber auch mit den beliebten ESP32- und ESP8266-Boards. Und die gibt es schon deutlich günstiger.

Das Open Source-Projekt **MicroPython** beinhaltet Compiler, Runtime, einen interaktiven Modus zur Befehlseingabe und verschiedene Pakete der Python Standard Library. Wie die Arduino-Plattform eignet sich MicroPython damit perfekt für Elektronikprojekte - iat aber grade für Einsteiger deutlich einfacher.

Die Kombination von Low-Level-Mikrocontrollerhardware mit einer höheren Programmiersprache wie Python hat verschiedene Vorteile. Der Code ist weniger an den Ziel-Controller gebunden und bekannte IDEs können zur Entwicklung genutzt werden. Die Entwicklungsgeschwindigkeit von Python erlaubt schnelles Prototyping - dank der Einfachheit von Python für Jedermann (und -frau).

Die Entwicklung findet auf dem Desktop-Rechner statt, der Code wird mithilfe eines USB-Kabels direkt aus einer IDE wie Thonny oder Mu auf den MicroController übertragen und dort ausgeführt. Wer Python auf dem Desktop kennt, findet sich also sofort zurecht.

Mit dem Fork [CircuitPython](https://circuitpython.org) von Adafruit wird speziell die Hardware dieses Anbieters, wie zum Beispiel das CircuitPlayground, unterstützt.

Mit MicroPython erobert sich Python ein ganz neues Aufgabengebiet. Die spanende Welt des Internet of Things.


<ul style="list-style-type:none;">

{% for post in site.categories['micropython'] %}
{% include teaser.html %}
{% endfor %}
</ul>
