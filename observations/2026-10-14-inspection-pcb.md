# Inspection PCB — 14 octobre 2026

Douze photographies de face composants et de verso fournies et indexées : `20261014_110749.jpg`, `110759`, `110804`, `110816`, `110848`, `110928`, `110935`, `110956`, `111003`, `111009`, `111013`, `111017` (préfixe identique). Images conservées dans archive ZIP locale remise à l'utilisateur; transfert des JPEG originaux vers GitHub restant à effectuer.

## Observations
- Région M1/M2/M3 : régulations locales, MOSFET et condensateurs; connexions de puissance principales non établies.
- Verso : alignements de vias, tracés apparents, condensateurs CMS et contacts traversants; nombreuses liaisons internes invisibles en photo.
- Les pastilles cuivrées de fixation et plans visibles ne doivent pas être supposés reliés à GND.
- Aucun repérage sûr du réseau P1 +12 V à ce stade; P2/GND étayé par les mesures.
- Les contacts A1–C11 ne sont pas identifiés fonctionnellement; voir M17 à M19.

## Suite proposée, uniquement hors tension
1. Confirmer mécaniquement que les pads suivis appartiennent au connecteur arrière Management/Power et non aux mezzanines M1–M3.
2. Localiser le net P1 par continuité vers un via/testpoint accessible (éviter de toucher deux vias à la fois).
3. Localiser les masses P2 et les éventuelles protections en série.
4. Rechercher référence composants de contrôle d'alimentation; distinguer hypothèses et validation.
5. Pas d'injection du 12 V tant que la polarité n'est pas corroborée indépendamment.

Conserver les fichiers bruts et les mesures dans la sauvegarde complète de la conversation.
