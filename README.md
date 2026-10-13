# HPE Synergy 480 Gen10 — rétro-ingénierie sans châssis
État au 2026-10-13. Étude passive, **aucune mise sous tension hors châssis documentée**.

## Identification
HPE Synergy 480 Gen10, commercial **871940-B21**, réglementaire **HSTNS-TB14-S**, plaque signalétique **12 VDC / 40 A MAX** (480 W). Deux CPU, 24 emplacements DIMM, PCH C621, iLO, extensions M1–M3.

## Outillage
Alimentation laboratoire 0–15 V / 3 A avec limitation de courant; oscilloscope, multimètre; pas d'analyseur logique. **L'alimentation 3 A ne convient pas au démarrage complet.**

## Repères
Connecteur Management/Power vu de face, deux lames de puissance à droite : **P1 lame gauche**, **P2 lame droite**. Matrice de contacts 3 colonnes A, B, C de gauche à droite × 11 rangées du haut vers le bas. Contacts fins et larges; ces numéros sont internes à l'étude, non issus du constructeur.

## Hypothèses / confirmations
- P2 en continuité franche avec masse USB, microSD, châssis ⇒ **GND forte confiance**.
- P1 est **+12 V plausible MAIS NON CONFIRMÉ**; interdiction de l'alimenter sur cette seule hypothèse.
- C5788 et C5791 (270 µF / 16 V) : leurs pôles (+) sont communs; pôles (−) à P2; leurs pôles (+) ne sont pas directement reliés à P1.
- L220, L221, L222 : extrémités reliées à faible résistance en circuit; ~97 Ω apparents vers GND; ~3,1 kΩ vers P1. Pas de conclusion certaine sur topologie dynamique.
- U200 : marquage SN1701022, extrait de schéma fourni par l'utilisateur (broches SMB_DIO, SMB_CLK, AVR_EN, AVR_RDY, PWM, VPP_SENSE); provenance et correspondance avec révision PCB **à vérifier**.
- Aucune identification fonctionnelle des contacts A1–C11 autre que GND probable; ne pas forcer les lignes.

## Dossier
- [Journal des mesures M1–M16](mesures/journal.md)
- [Matrice M17](mesures/M17.md)
- [Protocole M18/M19](protocoles/M18_M19.md)
- [Schéma de principe](schemas/architecture.mmd)
- Photographies et schéma SN1701022 dans [l'archive locale du dossier](../../releases) lorsqu'elle sera publiée. **Les photos ne sont pas encore transférées dans ce dépôt**.

## Confidentialité
L'une des photographies originales porte le mot de passe iLO. **Ne jamais publier l'original** ; l'archive de sauvegarde fournie dans la conversation contient une version masquée.

## Sécurité
Pas d'injection de 12 V tant que la polarité P1 et la topologie d'entrée ne sont pas corroborées indépendamment. Les mesures de résistance et de capacité in-circuit sont des valeurs apparentes. Ne jamais placer la masse d'un oscilloscope relié à la terre de protection sur un net inconnu.
