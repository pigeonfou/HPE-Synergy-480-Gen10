# Résultats M18 et M19 — 2026-10-14

Mesures réalisées hors tension sur HPE Synergy 480 Gen10. Les lectures ont été transcrites à partir des feuilles manuscrites fournies; toujours conserver les originaux.

## M18 — résistance des contacts vers P1

|Contact|M17 vers P2|M18 vers P1|
|---|---:|---:|
|A2|OL|OL|
|A5|61 kΩ|82,6 kΩ|
|A6|61 kΩ|82,6 kΩ|
|A8|OL|OL|
|A9|OL|OL|
|A11|OL|OL|
|B1|10 kΩ|13,5 kΩ|
|B3|10 kΩ|13,5 kΩ|
|B4|10 kΩ|13,5 kΩ|
|B6|OL|OL|
|B7|9,2 kΩ|9,7 kΩ|
|B9|10 kΩ|13,5 kΩ|
|B10|10 kΩ|13,5 kΩ|
|C2|OL|OL|
|C3|OL|OL|
|C5|84 kΩ|82,6 kΩ|
|C6|84 kΩ|82,6 kΩ|
|C8|OL|OL|
|C9|OL|OL|
|C11|OL|OL|

## M19 — résistance entre contacts

|ID|Points|Résultat|
|---|---|---:|
|M19-A|A5–A6|74,3 kΩ|
|M19-B|C5–C6|74,3 kΩ|
|M19-C|B1–B3|20 kΩ|
|M19-D|B3–B4|20 kΩ|
|M19-E|B9–B10|20 kΩ|

## Interprétation provisoire

Aucun des 20 contacts non-GND de M17 ne présente de connexion de faible résistance à P1. Les contacts B1/B3/B4/B9/B10 présentent un comportement symétrique ~10 kΩ vers P2, ~13,5 kΩ vers P1, ~20 kΩ entre deux lignes testées. Hypothèse : polarisation similaire de plusieurs signaux indépendants, non confirmation d'un bus ou d'une fonction.

A5/A6 et C5/C6 sont chacun mesurés 74,3 kΩ intercontacts, avec des résistances vers GND différentes entre les deux groupes. Les mesures in-circuit ne permettent pas d'établir le schéma des réseaux.

**Ne pas alimenter P1 ni injecter de tension dans les contacts : +12 V n'est toujours pas confirmé sur P1.**

## À compléter

Archiver les photos manuscrites originales de M18 et M19; réaliser mesures de polarité croisée en mode diode ciblées et confirmation indépendante du chemin de puissance P1.
