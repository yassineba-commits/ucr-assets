# UNCROWNED — contexte complet du projet (à coller dans un nouveau compte Claude)

Tu reprends un projet en cours avec Yacine (Krealab, Algérie). Lis tout avant d'agir. Réponds en français, messages courts, pas de demande de confirmation inutile.

## 1. Le projet
- Film vitrine « UNCROWNED » pour le client **Impact Factory** (plateforme IA, impactfactory.ai). Objectif : réalisme tel que les gens disent « je ne peux pas croire que c'est de l'IA ». Chaque plan ≥ 9/10.
- Durée cible ≤ 3:30, en anglais. Dernière version livrée : **UNCROWNED_v11.mp4 (3:39)**.

## 2. Structure verrouillée (ne jamais changer)
1. **Cérémonie** — THE SOLSTICE AWARDS 2026 (prix inventé). Un **animateur** (smoking velours bleu nuit, ~50 ans) et une **co-animatrice** (robe soie émeraude, oreillette) parlent **à l'écran** (pas de voix off au début). « Best Short Film of 2026… Impact Factory Productions! » — pas de mention d'IA.
2. **Coulisses (making-of)** façon featurette Marvel : fonds verts, câbles, combinaisons mocap grises à marqueurs, vraie équipe (Steadicam, grue, drone, video village, pointeur). Gym et régime d'Atlas, maquillage, costumes, Blaze, Nova, FaceTime de Pip avec sa famille (même famille à la cérémonie), dîner du cast (2 tiramisus Orion/Aurelia, brocoli devant Atlas), actrice au sol « I can't anymore », Atlas qui essaie d'impressionner Aurelia (café + tournesol).
3. **Carton titre** : « After 6 months of work… » → UNCROWNED (Cinzel or) → « A few scenes from the film ».
4. **Le film = best-of** (comme les buts au Ballon d'Or). Équipe Atlas (Atlas, Blaze, Pip) vs équipe Aurelia (Aurelia, Nova, Orion). Pouvoirs = personnalité : Atlas (Superman original : vole, force cobalt rendue en onde de choc, jamais de laser néon) ; Pip (papillons mignons aux dégâts monstrueux) ; Orion (stratège pur, pièges, bat tout le monde sauf Atlas) ; Blaze (plus fort à chaque coup reçu) ; Nova (tempo/claquement de doigts) ; Aurelia (ce qui l'ennuie devient or ; main levée « stop » qui arrête une attaque avec onde visible). **Atlas gagne seul.** Climax : **coup de poing géant** → coupe au **noir total** sur l'image avant contact + **1,5 s de silence** → résonance → Atlas vole victorieux, Aurelia à genoux, couronne brisée.
5. **Nouvelle ovation** après le film (« I'd seen it already… but I hadn't realised until now. » / « Me neither. »).
6. **Best Actor = Atlas** : marche vers la scène, trophée, discours sur Aurelia (« Three months I trained to impress one person. I hope it worked. »). Aurelia impressionnée pour la première fois.
7. **Le date** (rooftop), réplique VERBATIM : ATLAS « What an irony… I had to punch you in the face for you to accept a date — and to finally be impressed. » AURELIA (éclate de rire, au bord des larmes) « …Okay. You finally got me. »
8. **Reveal** sur le plateau fond vert avec toute l'équipe : les personnages disent face caméra que ce n'est pas réel (Pip « Everything you just saw… isn't real. », Nova « Not the hall. Not the crowd. Not even us. », Atlas « It was made with Impact Factory. », Aurelia « Try it — for only ninety-nine cents. »).
9. **Fin** : logo Impact Factory **bleu** plein écran + « Try it for only $0.99 » + impactfactory.ai.

## 3. Personnages et costumes (verrou)
- ATLAS : 55 ans, cheveux argentés plaqués en arrière, lunettes rectangulaires écaille, barbe grise courte. Film : combinaison cobalt à panneaux usinés plats, bras droit qui devient or. Cérémonie/date : **smoking bleu nuit**, revers satin noir, nœud papillon, lunettes.
- AURELIA : ~35 ans, chignon bas, minuscule paillette or (3 mm) sur la pommette. Film : armure plumes d'or + cape champagne. Cérémonie/date : **robe satin champagne une épaule + manchette or** (jamais le costume du film hors film). **Jamais de halo / cercle autour de sa tête.**
- ORION : ~60 ans, asiatique, lunettes rondes, cardigan sombre ; smoking noir à la cérémonie.
- PIP : 30 ans, cheveux roux bouclés, taches de rousseur, barrette papillon cyan, pull moutarde + jean. Gala : robe velours prune.
- NOVA : jeune femme, peau foncée, coupe courte platine ; bomber satin marine avec phénix cramoisi. Gala : combinaison satin noire.
- BLAZE : 28 ans, cheveux bruns bouclés, sourcils épais ; hoodie noir sans manches, bandes de boxe cramoisies, casque autour du cou. Gala : costume anthracite.
- Trophée : flèche de cristal dans un anneau d'or sur socle noir.
- Famille d'Atlas : sa mère et sa sœur.
- Aucun personnage ne doit ressembler à un acteur/une célébrité réelle.

## 4. Règles de Yacine (toujours)
- Réalisme 10/10, jamais de look plastique/CGI, vrais ciels photographiques, pas de faux rayons.
- Un personnage qui parle doit être **vu en train de parler** (lip-sync généré), jamais en voix off. Ne **jamais couper une réplique** — vérifier par transcription que chaque mot est là. Les rires doivent s'entendre.
- **Aucune musique Seedance** (l'interdire dans chaque prompt ; au montage, garder seulement les voix isolées).
- Musique de montage : discrète dans le film, ne coupe jamais (sauf le noir du coup de poing), chaque scène est un hook vers la suivante.
- Bruitages ElevenLabs (attention : les VO/SFX actuels viennent de comptes ElevenLabs gratuits → à refaire sur un compte payant avant livraison).
- Blender pour les mouvements (previs en mannequins gris, utilisés **comme référence de mouvement uniquement**, jamais sur les plans de foule — sinon public de mannequins).
- Pas de noms de prophètes. Pas de musique générée. Pas de punch dans le vide. Pas d'obélisque/monument derrière les décors dorés.
- Toujours noter chaque clip /10 ; ne garder que ≥ 9.

## 5. Où sont les fichiers (GitHub public)
Dépôt : **https://github.com/yassineba-commits/ucr-assets** (branche main)
- `flow/` : visages et costumes de référence (FACE_*, CAST_*_HERO, FAM_*, FACE_HOST, FACE_COHOST…)
- `vref/` : vraie salle (hall_t4.jpg), podium, etc.
- `previs/` : animations Blender (PV_F01–PV_F40 combats, 19 PV_Rxx, PV_FIGHT_A/B, PV_PILLAR_SAVE, PV_HOST_*, PV_ENVELOPE)
- `handoff/FINAL_80.md` : **88 prompts Seedance 2.5 vérifiés** (48 combats + 40 réalisme) avec protocole de notation et liens des refs
- `handoff/QUALITY_RULES.md` : ce qui donne 9/10 vs 6–7/10
- `handoff/HANDOFF_v2.md`, `HF_PENDING_PROMPTS.md` : prompts cérémonie/date/reveal
- Pages avec boutons « Copier » : https://claude.ai/artifact/6YWVLTnd7Eq1K43awuHJBA (88 prompts) et https://claude.ai/artifact/Lxqofyi646jbZPXZSLWJhf (kit Higgsfield)
- À supprimer après livraison : le dépôt ucr-assets.

## 6. Génération
- Higgsfield (higgsfield.ai), Seedance 2.5, 720p, 16:9, mode **Unlimited**, projet UNCROWNED. **Ne jamais toucher au projet KAIROS** (concours Higgsfield de Yacine). Ne rien acheter. Les vérifications humaines (« Quick check ») sont pour Yacine.
- Unlimited ne marche que si le clic vient de Yacine ou de Claude in Chrome dans son Chrome.
- Impact Factory : plus de crédits (≈38). Google Flow : limites d'usage sur plusieurs comptes.

## 7. État actuel (27 nov, ~02:40)
- v11 livrée (3:39) : nouvelle ouverture (trophée + grue sur vraie salle), animateur qui dit l'enveloppe et « how it was made » à l'écran, ovation avec câlin, nouveau combat sous la pluie (coup de pied de Nova, « Hit me. », Nova qui s'écrase, « Thanks for the warm-up. »), papillons de Pip, nouvelle ovation après le film, coup de poing géant + noir + silence, Aurelia à genoux, Best Actor, date, reveal, logo bleu.
- ~38 clips générés cette nuit dans l'historique Higgsfield (combats F*, cérémonie). Il reste beaucoup des 88 prompts à générer.
- À faire ensuite : générer le reste des 88 prompts (≥ 9/10), intégrer les meilleurs, ramener sous 3:30 si demandé, refaire les voix/SFX ElevenLabs sur compte payant, P5 « Best Actor… Atlas! » dit à l'écran par l'animateur, reveal avec les personnages face caméra, date avec Aurelia en robe champagne.

## 8. Mémoire / préférences générales de Yacine
Il veut un travail de pro, rapide, sans gaspiller les crédits ; il corrige plan par plan avec des captures d'écran ; il déteste : voix off à la place des personnages, répliques coupées, musique Seedance, figurants/mannequins 3D, halos IA, coups dans le vide, incohérences de costumes, plans trop lents.
