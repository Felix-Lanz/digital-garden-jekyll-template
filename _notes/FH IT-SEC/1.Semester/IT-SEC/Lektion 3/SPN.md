---
tags:
  - it-sec
title: SPN
aliases:
  - Substitutions-Permutations Netzwerk
  - SP-Netzwerk
---
Besteht aus mehreren Runden. Pro Runde werden eine, oder mehrere Substitutionen und Permutationen durchgeführt. 
Die Substitution erfolgt klassischerweise über eine S-Box, z.B [[Rijndael - S-Box]]. Wichtig ist hierbei, dass im Gegensatz zur [[Feistel-Box]], eine invertierbare S-Box benötigt wird.

Weiters erfolgt Permutation über eine P-Box. Welche die Nachricht durchmischt. Vgl. [[Shift Rows]] und [[Mix Columns]] von AES.

Weiters wird in jeder Runde der Rundenschlüssel beigemengt.

