---
tags:
  - it-sec
title: CBC
aliases:
  - Cipher Block Chain Mode
---
Hier wird jeder Klartextblock vor dem Verschlüsseln mit dem vorhergehenden Geheimtextblock verXORed. Der erste Block wird mit einem Initialisierungsvektor XORed, da es noch keinen vorhergehen Geheimtextblock gibt.

Wird ein Block korrumpiert, ist nur der nachhergehende Block betroffen, die anderen zukünftigen sind nicht mehr korrumpiert.
Durch diese Eigenschaft werden allerdings Cut&Paste Angriffe ermöglicht, da der Angreifer Blöcke ersetzen kann, ohne dass die gesamte Nachricht davon betroffen ist.
![[Pastedimage20230923200715.png]]

