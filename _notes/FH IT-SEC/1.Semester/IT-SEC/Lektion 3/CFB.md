---
tags:
  - it-sec
title: CFB
aliases:
  - Cipher Feedback Mode
---
Die ersten 64 Bit werden durch einen Initialisierungsvektor generiert, da zumindest 8 Byte benötigt werden, um mit dem Verschlüsseln der Nachricht zu beginnen. Diese 64 Bit befinden sich in einem Schieberegister, welches im Laufe der verschlüsselung mit den verschlüsselten Bytes befüllt wird. 

Der Inhalt des Registers sowie der symmetrische Schlüssel sind Parameter der Verschlüsselungsfunktion E(). Vom Output von E(), wird nur das Most Significant Byte ausgewählt und mit dem zu verschlüsselnden Klartextbyte XORed. Diese Byte wird nun einerseits Teil des Geheimtexts, andererseits kommt es nun an der Least Significant Byte Stelle des Schieberegisters. Das MSB des Schieberegisters "fällt" hinaus.
![[Pastedimage20230923201750.png]]

Das Schieberegister ist von allen vorhergehenden Blöcken abhängig. Dadurch werden Muster im Klartext verwischt. 

Weiters, ermöglicht diese Betriebsart eine Blockchiffre als Stromchiffre zu betreiben. 
Da der Cipher auf Basis einzelner Bytes fungiert, ist es möglich sehr kleine Datenmengen zu verschlüsseln, ohne auf einen ganzen Block zu benötigen. Z.B interaktive Terminals



