# Q90033/Q90034/Q90035 — AON6500 (Alpha & Omega Semiconductor)

Identification apportée par l'utilisateur le 2026-10-14, avec datasheet **AON6500.PDF** de six pages, rév. 0 janvier 2012. Conserver le PDF original dans le dossier documentaire lors du prochain transfert des binaires.

## Brochage constructeur — DFN 5×6, vue de dessus selon repère PIN1

- Broches 1, 2, 3 : **Source (S)**
- Broche 4 : **Gate (G)**
- Broches 5, 6, 7, 8 et plage drain : **Drain (D)**
- Ne pas identifier une broche à partir du seul côté gauche de la photo sans orienter le marquage du boîtier et localiser la broche 1.

## Caractéristiques datasheet, pages 1–2

- MOSFET N 30 V, ID 200 A à Tc=25°C (limite spécifiée en conditions particulières)
- RDS(on) max 0,95 mΩ à VGS=10 V, 1,3 mΩ à VGS=4,5 V
- VGS max ±20 V; seuil VGS(th) 1–2 V à ID=250 µA, ce n'est pas la tension garantissant l'état passant à fort courant
- VSD diode de corps typ. 0,7 V, max 1 V à IS=1 A
- Ciss typ. 7036 pF; Qg typ. 107 nC à 10 V

## Constat issu des mesures

- M26: trois grandes terminaisons dites « D » reliées au réseau rouge NET-31-R puis P1 à 0,4 Ω ; la référence AON6500 permet maintenant de vérifier que ces grandes terminaisons sont bien les drains *si orientation conforme au boîtier illustré*.
- M27: anciennes « G1 » communent à 0,4 Ω entre boîtiers ; elles sont à 3,76 kΩ de NET-31-R, à 4,44 kΩ de NET-31-P. **ATTENTION : « G1 » était un repère géométrique, et non la grille constructeur.** Si le point était réellement la broche supérieure du groupe gauche en vue orientée avec PIN1 en haut à gauche, il s'agit de S1, non de G4. Valider orientation avant renommage définitif.
- M24: NET-31-P pointe positive, NET-31-R négative en mode diode donne ~0,456 V. Compatible avec diode de corps d'un N MOS (anode Source, cathode Drain) si NET-31-P = Source et NET-31-R = Drain, mais le circuit in situ offre d'autres chemins. À confirmer par test de chaque source et grille à la masse, selon orientation et isolation.

## Rectification méthodologique

**L'ancien protocole M28 de simple dénombrement des pattes est devenu obsolète.** La prochaine campagne doit orienter physiquement le boîtier, identifier broche 4 G et broches 1–3 S, puis mesurer chaque sous-réseau sans jamais forcer la grille. Ne pas injecter de 12 V sur P1 : polarité nominale et rôle de l'étage toujours à documenter.
