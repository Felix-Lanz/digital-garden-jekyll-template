---
title: GCM
aliases: []
tags:
  - it-sec
---
Betriebsart, welche [[AEAD|Authenticated Encryption with Associated Data]] bietet. 
Dadurch wird auch [[Datenintegrität - Integrity|Integrität]] und [[Authentizität - Authenticity|Authentizität]] gewährleistet.

Funktioniert grundsätzlich wie der [[CTR|Counter Mode]]. 128 Bit IV, 96Bit Pseudo Random, 32 Bit inkrementeller Teil. 

Encryption: Key wird mit IV XORed und ist Input für AES. der Output wird mit dem Plaintext XORed. Der Geheimtext wird gehashed und mit dem Hash der Associated Data XORed, dieser Output wird wiederum als Hash für den nächsten Block verwendet. Auf diese Art und weise propagiert der Hash durch die gesamte Nachricht.

Associated Data: ein 128 Bit 0 Block wird encrypted und dient als Ausgangshash, dieser wird mit dem ersten Plaintextblock XORed, wobei dieser output wieder mit dem nächsten Plaintextblock XORed wird usw. Dieses Ergebnis dient dann als Ausgangsahsh zum Encrypten. 

Authentication Tag: Dieser besteht aus dem IV, der länge der Associated Data, länge des Ciphertextes sowie dem letzten Hashblock. 

![[Pastedimage20230923232238.png]]