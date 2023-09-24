tags: #it-sec 

1. Was versteht man unter einem [[Symmetric Cipher|symmetrischen Verschlüsselungsverfahren]]?
2. Erklären Sie folgende Definition mit eigenen Worten: ∀M ∈ M : D(E(M, KA,B ), KA,B ) =
D(C, KA,B ) = M
Es gilt dass für alle Nachrichten M, das die Umkehrfunktion von E D ist, wobei der input von D, output von E ist, sowie in beiden Fällen, der Symmetrische Schlüssel KA,B.

3. Was ist eine [[Blockchiffre]]?
4. Was ist eine [[Stromchiffre]]?
5. Zählen Sie wichtige Aufgaben einer [[S-Box]] auf.
6. Erläutern Sie das „[[Strict Avalanche Criterion]]“.
7. [[Feistel-Box]]: Erklären Sie folgende Definition mit eigenen Worten:
Fs(Fs(l, r)) = Fs(l ⊕ S(r), r) = (l ⊕ S(r) ⊕ S(r), r) = (l, r)


Welches Problem wird dadurch elegant gelöst bzw. beseitigt?
- Das Problem, dass eine nicht invertierbare Funktion S, es nicht möglich machen würde den Geheimtext wieder zu entschlüsseln. Die Feistel-Box löst genau dieses Problem

8. Was versteht man unter einem [[Rundenschlüssel]]?
9. Was ist eine [[Produktchiffre]]?
10. Nennen Sie die wesentlichen Merkmale eines [[Feistel-Netzwerk|Feistel-Netzwerks]].
11. Nennen Sie die wesentlichen Merkmale eines [[SPN]].
12. Wozu dienen im Zusammenhang mit symmetrischen Blockchiffren die [[Betriebsarten]]?
Was wird dadurch verhindert?
13. Erläutern Sie die Betriebsarten [[ECB]], [[CBC]], [[CFB]],[[OFB]], [[CTR]] bzw. unterscheiden Sie die
ab Unterabschnitt 3.1.7 dargestellten Blockschaltbilder.
14. Erläutern Sie die Betriebsarten [[ECB]] und [[CBC]]. Was ist der Vorteil von [[CBC]]?
15. Welches Sicherheitsproblem gibt es im Zusammenhang mit der Betriebsart [[CBC]]?
16. Nennen Sie die Besonderheit des[[CTR| Counter Mode]].
17. Warum kann über den Counter Mode eine Block- wie eine Stromchiffre betrieben werden?
18. Nennen Sie die Besonderheit des [[GCM]].
19. Gegeben sind zwei Blöcke (l,r) mit je 32 Bits Breite. Skizzieren Sie eine Runde eines
Feistel-Netzwerks [[DES]] unter Verwendung eines Rundenschlüssels.
![[Pastedimage20230923211007.png]]
20. Erläutern Sie Eigenschaften/Funktionsweise/Vor- und Nachteile von [[3DES]] mit eigenen
Worten.
21. Welche Schlüssellängen gibt es bei [[3DES]]. Skizzieren Sie die kaskadierten Durchläufe.
22. ![[Pastedimage20230923223539.png]]
23. Welche symmetrischen Blockchiffren kennen Sie neben [[DES]] bzw. 3DES? Erläutern Sie
diese kurz!
-  [[AES]], [[Camellia]], [[IDEA]], [[Blowfish]], [[Twofish]]
23. Was ist der wesentliche Unterschied zwischen einer [[Blockchiffre|Block]]- und einer [[Stromchiffre]]?
Blockchiffren sind blockbasiert, Stromchiffren sind Zeichenbasiert. 
24. Erläutern Sie das Funktionsprinzip einer [[Stromchiffre]].
25. Stromchiffren: Erklären Sie folgende Definition mit eigenen Worten:
C1 ⊕ C2 = M1 ⊕ KStrom ⊕ M2 ⊕ KStrom = M1 ⊕ M2 , da x ⊕ KStrom ⊕ KStrom = x
Welches Problem ergibt sich daraus?
Wird zweimal der gleiche Schlüssel verwendet, kann durch XORen der Geheimtexte der XORte Klartext gewonnen werden. Ist dem Angreifer ein Klartext bekannt, kann er den anderen durch XORen herleiten. Vgl. [[chosen-plaintext attack]]
26. Warum darf bei Stromchiffren ein bereits verwendeter Schlüsselstrom nicht erneut ein-
gesetzt werden? Vgl. 25.
27. Welches Problem ergibt sich bei dem zu klein bemessenen [[Initialisierungsvektor]] im [[WEP]]-
Standard? Was ist die Konsequenz?
Ein gleicher Initialisierungsvektor ergibt gleiche Schlüssel ua. auch weil der WEP key immer gleich bleibt. Da der Initialisierungsvektor nur 3Byte=24Bit lang ist, werden nach nur 2^24 = ca. 7MB wieder gleiche Schlüssel verwendet.
28. Was ist [[ChaCha20]], und was ist der wesentliche Vorteil im Vergleich zu [[AES]]?
[[ChaCha20]] ist eine Stromchiffre und ist optimiert um in Software noch schneller zu sein als AES.

