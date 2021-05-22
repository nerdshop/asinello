---
title: "Client-Entwicklungen"
author: Maik
---

Der Client kommt langsam voran. Mittlerweile ist folgendes erreicht:

- MQTT-Verbindung mit TLS
- Integration des Drehgeberknopfes

Momentan arbeite ich an einem Konzept zur Abbildung verschiedener Nutzer-Ein-/Ausgabemodi. Es soll das Zusammenspiel aus Drehgeber-Eingaben und LED-Ring-Ausgaben in verschiedenen Situationen kapseln, um den Code übersichtlich und robust zu halten.
Mein Mangel an C++-Erfahrung macht das etwas mühsam, aber die kleinen Erfolge machen Spaß und es geht voran. Dennoch wäre hier etwas Starthilfe nicht schlecht.

# Prototyp

Für die Entwicklung stelle ich gerade drei Prototypen-Geräte zusammen. Dabei ergibt sich ein erstes Muster für die Verkabelung der Komponenten. Es wäre schön, wenn sich das Hardware-Team daran orientiert, sofern es keine plausiblen Gründe für Abweichungen gibt.

![PXL_20210521_202454320](https://user-images.githubusercontent.com/728958/119215653-40050700-bacf-11eb-91a5-69f745749a4a.jpg)

## Hardware

Für die Komponenten verwende ich männliche Dupont-Stecker. Die sind Breadboard-freundlich und außerdem habe ich von ihnen mehr über als von den weiblichen. ;)

Die Spannungversorgung des LED-Rings ist mit einem roten (5V) und einem schwarzen (GND) Kabel über einen gemeinsamen Dupont-Stecker angeschlossen. DI hat ein separates, blaues Kabel und wird bei mir aktuell an D7 angeschlossen. Hier müssen wir vielleicht noch einen Widerstand einplanen - das wird hier und da im Netz empfohlen.
DO ist optional und wird ggf. mit einem grauen Kabel mit weiblichem Stecker versehen. Auf die Art können hier weitere LEDs angeschlossen werden und falls nicht, baumelt kein blanker Stecke lose herum.

Beim Drehgeber ist ein Pin des Knopfes mit dem mittleren PIN des Drehgebers kurzgeschlossen, um beide mit einem separaten, schwarzen Kabel an GND anzuschließen. De facto verwende ich als Masse-Anschluss gerade einen auf OUPUT LOW konfigurierten D4. So spart man sich eine Hardware-Lösung, um den enizigen GND-PIN des D1 Mini aufzuteilen.
Die beiden Drehgeber-Anschlüsse (blau und lila) sowie der zweite Knopf-Anschluss (braun) werden mit einem gemeinsamen Stecker an D1, D2 (Drehgeber) und D3 (Knopf) angeschlossen. Die Pins sind alle als INPUT_PULLUP konfiguriert.

Für einen Buzzer habe ich noch keinen Anschlussstandard parat.

## Gehäuse

Am Entwicklergehäuse habe ich kleine Anpassungen vorgenommen, die ich demnächst noch im Projekt aktualisiere. Nett wäre ein zusätzlichen ansteckbares Modul mit einer Aufnahme für einen D1 Mini (und alternativ eins mit einer Aufnahme für einen NodeMCU). Ob sich das Entwicklergehäuse als Grundlage für einen ersten Prototyp eignet, weiß ich nicht. Aber zum Sammeln erster Erfahrungen reicht er allemal.
