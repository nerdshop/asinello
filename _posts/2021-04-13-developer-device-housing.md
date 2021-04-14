---
title: Entwicklergehäuse
author: Maik
---

Ich habe eine Halterung für die Ein- und Ausgabegeräte des Spiel-Clients gebaut. Die Ziele dabei:
* Erstes Gefühl für die Steuerung bekommen
* Weniger zerbrechliches Testgerät zum Entwickeln

Im Wesentlichen habe ich eine erste Umsetzung von https://github.com/nerdshop/asinello/issues/13 durchgeführt.

## Modellierung

Der LED-Ring wird mit 4 M2 * 6 Schrauben in einen passenden Rahmen geschraubt. Die Löcher habe ich etwas zu eng modelliert - dafür brauchte ich keine Muttern. ;) Er wird von unten angeschraubt, um einen ersten Eindruck der Lichtdiffusion durch das Gehäuse zu erhalten. Für die Anschlusskabel gibt es eine Aussparung.

Der Drehgeber ragt oben aus dem Gehäuse und wird mit der zugehörigen Unterlegscheibe und Mutter befestigt. Ein Rahmen für das untere Gehäuse verhindert das Mitdrehen beim Bedienen.

Drei Standfüße sorgen für einen sicheren Stand und genügend Spielraum für die Anschlusskabel. In einer späteren Iteration könnten z.B. an deren Innenseite Schnappnase modelliert werden, die in Halterungen für verschiedene ESP-Varianten greifen können, um ein rudimentäres Gesamtpaket zu bilden.

![Oberansicht](/media/PXL_20210413_183755438.jpg "Oben")
![Unteransicht](/media/PXL_20210413_183814257.jpg "Unten")

https://user-images.githubusercontent.com/728958/114712105-030b5f00-9d30-11eb-8003-d3fe7714e469.mp4

## Erkenntnisse

Es bedient sich wunderbar! Allergins sollte das finale Gehäuse schwerer und / oder rutschfester sein, um eine einhändige Bedienung zu erleichtern.

Die Diskrepanz aus LED-Anzahl und Drehgeberschritten für eine Umdrehung ist kein Problem. Es fühlt sich sehr intuitiv an.

Für die Lichtdiffusion empfehle ich Experimente mit Hohlkammern. Bei meinem Aufbau liegen die LEDs unmittelbar am Gehäuse an. Dadurch erkennt man z.B. in verschiedenen Richtungen die RGB-Komponenten.
Außerdem sähe eine weniger punktuelle, durch einen Hohlraum definierte Leuchtform (z.B. Flächen oder Symbole) sicher schicker aus.

Wie bereits oben erwähnt wäre es nett, wenn das hier entworfene Bedienteil mit einer Aufnahme für ein Entwicklerboard (D1 Mini / NodeMCU) kombinieren könnte. Dann hätte man ein kompaktes Entwicklergerät.

Die Bohrungen für die Schrauben sollten etwas vergrößert werden, auch wenn es praktisch ist, dass man bei der aktuellen Version keine Muttern benötigt. :)
