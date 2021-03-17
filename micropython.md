---
layout: default
title: MicroPython
---

 Das Kickstarter-Projekt [MicroPython](https://micropython.org) von Damien George ist eine zur Version 3 kompatible Python-Implementierung, die auf verschiedenen Architekturen wie zum Beispiel ARM oder dem Raspberry Pi Pico läuft. Das Open Source-Projekt beinhaltet Compiler, Runtime, einen interaktiven Modus zur Befehlseingabe und verschiedene Pakete der Python Standard Library. Wie die Arduino-Plattform eignet sich MicroPython damit perfekt für Elektronikprojekte.

## Beiträge

<ul>
{% for post in site.categories['micropython'] %}
{% include teaser.html %}
{% endfor %}
</ul>
