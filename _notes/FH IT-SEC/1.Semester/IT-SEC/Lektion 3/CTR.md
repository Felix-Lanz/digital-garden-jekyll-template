---
aliases:
  - Counter Mode
tags:
  - it-sec
title: CTR
---
Hier wird ein Initialisierungsvektor verwendet, welcher mit jedem Block erhöht wird. Der IV sowie der symm. Key dienen als Parameter der Funktion E(). Der Output wird mit dem Klartextblock XORed. 

Der Vorteil ist hierbei, dass ein beliebiger Block entschlüsselt werden kann, weder die vorhergehenden noch die nachfolgenden Blöcke müssen entschlüsselt werden. Weiters kann das ver/entschlüsseln parallelisiert werden. 
![[Pastedimage20230923210108.png]]
Hängt stärke des ciphers vom IV ab?