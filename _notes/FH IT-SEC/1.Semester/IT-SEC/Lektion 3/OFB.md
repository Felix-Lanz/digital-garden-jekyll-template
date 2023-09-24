---
tags:
  - it-sec
title: OFB
aliases:
  - Output Feedback Mode
---
Arbeitet so wie [[CFB]] Zeichenorientiert. 
Der Byteoutput von E(), wird mit dem Klartext Bit XORed. Weiters wird der Byteoutput von E() als Eingangsbit für die nächste E() Funktion verwendet. E() wird dadurch zu einem Pseudo-Zufallszahlengenerator und kreiert Pseudo One-Time-Pads welches mit dem Klartext Byte XORed werden.

Anfangs wird ein Initialisierungsvektor benötigt. Da, diese Betriebsart wieder Byteorientiert ist, wird aus der Blockchiffre wieder eine Stromchiffre.

Im Gegensatz zu [[CFB]] wird bei einem korrumpierten Byte, der Gesamte nachfolgende Bytestrom korrumpiert. 
![[Pastedimage20230923204338.png]]

