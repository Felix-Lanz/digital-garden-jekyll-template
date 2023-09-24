---
tags:
  - it-sec
title: 3DES
aliases:
  - Triple-DES
---
Kaskadiert [[DES]]. Kann in drei Modi laufen. Entweder mit 3 Unique Keys, wodurch die Schlüssellänge auf 168Bit ansteigt, wobei ein [[meet-in-the-middle attack]] die Schlüssellänge effektiv auf 112 Bit reduziert, oder mit 2 Unique Keys, daher 112Bit, wobei diese Variante auch anfällig für den  [[meet-in-the-middle attack]] ist.

Mit einem unique Key als backwards compatibility modus für DES Systeme. 

Bei der Ausführung von Triple des wird folgender Algorithmus angewandt: E(D(E(M,Ki),Kj),Kk) = C

3DES ist langsam als Softwareimplementierung.