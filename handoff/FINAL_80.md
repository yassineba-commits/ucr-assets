# UNCROWNED — FINAL 80 Seedance 2.5 prompts (QA-gated, ready to paste)
Reviewed by PROMPT-QA against `QUALITY_RULES.md` (same folder). Every prompt below is expected to score ≥ 9/10. Settings unless stated: Higgsfield Seedance 2.5, 720p, 16:9, project UNCROWNED. Refs are in the `ucr-assets` repo: `flow/` (FACE_*, CAST_*, KF_*), `vref/` (hall_t4.jpg etc.), `previs/` (PV_*.mp4, attached as the VIDEO reference = motion only). Upload images in the order listed: image 1, image 2, ... must match the text.

## RATING PROTOCOL (for the generating chat — mandatory)
1. After each clip: make a contact sheet at 3 fps (`ffmpeg -i clip.mp4 -vf "fps=3,scale=320:-1,tile=6x4" sheet.jpg`) and look at EVERY frame. Listen once (or STT) for the line and for music.
2. Check the top failure modes, in this order. Any one = the clip is below 9:
   1. grey mannequins / dummy crowd / empty seats / faceless figures
   2. a duplicate or extra lookalike character, a mirror twin
   3. obelisk, monument, tower, stone slab, skyscraper behind a gold set
   4. CG look: beam, ray, glowing outline, drawn rings/ripples, vortex/portal, halo or rays behind a head, glowing knuckles/ember lines, lens-flare streaks
   5. punch or kick into empty air; the striker flying instead of the target; floating props
   6. a face that is not the master (or looks like a celebrity); wrong costume vs the WARDROBE LOCK
   7. the line said off-screen, with a hand/prop over the mouth, cut mid-word, or repeated twice
   8. static/stiff clip (nothing moves in the first second), extra unwanted cuts
   9. rain prompt with no visible rain; dry floor in a "wet" scene
   10. Seedance music / tonal pad in the audio
3. Score /10. **If < 9: regenerate ONCE**, pasting the "If < 9 →" fix line listed under that prompt (add it to the end of the prompt, before AUDIO), and change nothing else.
4. Keep the better take only if it is ≥ 9. **Never keep a clip under 9.** If both takes are < 9, stop on that ID, log both URLs + scores + the failure numbers, and move on (do not burn a 3rd take without Yacine).
5. Log every take: time | ID | take | URL | score | failure numbers | credits.
6. Music in the audio alone does not fail a clip that is otherwise 9+ (the editor strips it with the vocal stem), but write it in the log.

## HOW TO USE THE REFS ON HIGGSFIELD
1. Every ref is a full raw GitHub URL (repo `yassineba-commits/ucr-assets`, branch `main`). Download each image URL and upload it to the **References** slots **in the order listed** (image 1, image 2, ...). The prompt text refers to "image 1", "image 2" in that same order, so a wrong order swaps faces. After uploading, check that the slot thumbnails are in the right order (a UI glitch once put FACE_ATLAS stuck in slot 1).
2. A **PV_xx.mp4** (Blender previs with grey mannequins) goes in the **video / motion reference** slot, never in an image slot. When a PV is attached, paste this MOTION line as the 2nd line of the prompt, right after the first sentence:
   > `The video reference is ONLY a timing and camera-path guide built with grey placeholder mannequins in an empty grey space. Copy ONLY its camera movement and the body positions over time. Do NOT copy its look, colours, lighting, set, empty space or figures: every person is a real human actor with real skin, hair and clothes, in the real location described below. No mannequins, no grey figures, no faceless bodies, no dummies anywhere in frame.`
3. If a PV URL returns **404**, the previs is not rendered yet: generate without the video ref, using the timed beats in the prompt.
4. **Never attach previs to crowd or audience shots**, and never use a frame from an old clip that has dummies as an image ref. That is how HF_CER_A1_t1/t2/t3 got grey dummy audiences (5–7/10). For crowds, `vref/hall_t4.jpg` alone is enough.
5. Never attach `flow/KF_F*` keyframes unless a prompt asks for one: they carry the obelisk and slab (R2_t1).
6. Settings: Seedance 2.5 · 720p · 16:9 · the duration given in the prompt · project UNCROWNED (never KAIROS). Paste the prompt from inside its code block only.

**Count:** 88 prompts. FIGHTS: 40 IDs became 48 prompts (8 split into a/b), all rewritten. REALISM: 40 prompts, all reviewed; 13 had real fixes, and the rest had PV/audio normalised.

---

# PART 1 — FIGHTS (F01–F40)

**Shared notes for every F prompt**
- Image refs: `flow/FACE_<NAME>_flow_nbpro_v1_OK.png` then `flow/CAST_<NAME>_HERO_flow_nbpro_v1_OK.png`, per character, in the order written in the prompt.
- Previs: no `PV_F01…PV_F40` was in `ucr-assets/previs/` at review time (26 Nov, 21:50); only `PV_FIGHT_A`, `PV_FIGHT_B`, `PV_PILLAR_SAVE` and `PV_RAIN_FIGHT` exist. Each unsplit F prompt lists its `PV_Fxx` URL as optional. A split prompt (a/b) gets no PV, because the original previs covers both halves.
- Changes applied to all 40 originals:
  - Nova's "navy-silver suit" became the bomber shown in her CAST image.
  - "shockwave / dust rings / ripple rings / air barrier" became physical contact plus blown dust (drawn rings showed up in R6_t1/t3).
  - "gold bridge with marble deck" became an ancient carved-stone bridge with gold inlay (R9_t3 looked like a highway).
  - The full location ban was added (obelisk, monument, tower, slab).
  - The rain block was added on the rain terrace.
  - The §D motion line was added.
  - Each audio line now reads "no music".

## OPENING CLASH

### F01a — Two Teams Collide (the charge)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F01 would not match its timing, so generate from the timed beats.
- **Original F01 score:** 5.5/10. Risks: 6 characters, 12 images, 4 beats, an FPV dive. Expect duplicate or missing heroes, tiny faces, an obelisk and a drawn "shock ring". **Split** into F01a (Blaze vs Nova collide) and F01b (Atlas lands).
- **Expected score:** 9 · **If < 9 →** `One continuous shot, only two people in the whole square, both faces clearly visible at the clash.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot: a low drone skims the marble then rises to a 28 mm medium-wide at chest height.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people in frame.
Location: a sunlit classical square of white marble veined with gold, gold colonnades around it; open pale sky and distant mountains only; no obelisk, no monument, no tower, no stone slab, no skyscrapers. Light: low late-afternoon sun from frame left, hard long shadows.
0–3 s: BLAZE and NOVA sprint at each other from opposite sides, footfalls slapping the marble, real motion blur.
3–5 s: they meet in the centre: BLAZE's wrapped fist lands on NOVA's crossed forearms, visible contact; the impact blows a burst of marble dust off the floor around their feet, her bomber and his hood flap back, the camera shakes once.
No beams, no glow, no drawn rings or ripples, no sparkles, no lens flares, no mannequins, no punches into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real fabric, physically correct sunlight, natural grade, no CG look, no text.
AUDIO: no music, no score, no soundtrack; only wind, running footsteps on marble, a heavy forearm smack and debris patter.
```

### F01b — Two Teams Collide (Atlas drops in)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F01 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `He lands on his feet and one knee only, no hovering; Aurelia stays small and still in the background, exactly one of each.`
```
Live-action superhero feature film footage, 4 seconds, ONE continuous shot, 24 mm low angle at knee height on the marble square.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined chest and shoulder panels, black boots. AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, one tiny 3 mm square gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly one ATLAS, exactly one AURELIA.
Location: a sunlit classical square of white marble veined with gold, gold colonnades; open pale sky and distant mountains only; no obelisk, no monument, no tower, no stone slab, no skyscrapers. Light: low late-afternoon sun, hard shadows.
0–1.5 s: ATLAS drops from above feet-first into frame and lands on one knee and one fist; the marble cracks outward under him along the gold veins and a burst of dust and chips blows toward the lens.
1.5–4 s: he rises slowly, adjusts his glasses and looks up; far behind him on the colonnade steps AURELIA stands still, cape moving in the wind, unimpressed.
No glow, no blue light on his body, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real brushed metal and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; only a rush of air, a heavy landing crack, chips clinking, wind.
```

## BLAZE vs NOVA — THE RAIN TERRACE

### F02 — Nova Snaps the Rain
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F02.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_RAIN_FIGHT.mp4 (fallback if PV_F02 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7. Risks: the frozen-rain "field of beads" plus walking through tunnels plus 3 strikes in 8 s is overloaded; "halo of drops" invites a CG halo; the bomber did not match.
- **Expected score:** 9 · **If < 9 →** `The frozen raindrops are ordinary clear water drops hanging still, like a high-speed photograph; nothing glows.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 40 mm Steadicam slowly circling NOVA at eye level, medium shot.
Image 1 = NOVA's face, image 2 = NOVA's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold balustrade and gold columns behind; no obelisk, no tower, no monument. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, rain splashing on the stone, mirror-wet marble with puddles reflecting the columns, soaked hair, breath vapour. Cold blue-grey dusk light.
0–2 s: NOVA, soaked, raises her hand and snaps her fingers: instantly every raindrop stops and hangs still in the air like clear glass beads; BLAZE stops mid-step, frozen.
2–6 s: she walks calmly through the hanging drops, which burst into real spray where they touch her shoulders, and plants one open-palm strike on BLAZE's chest: visible contact, a burst of water flies off his vest.
No glow, no sparkles, no halo, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; heavy rain hiss that cuts to silence on the snap, a sharp finger snap, one wet palm impact, breathing.
```

### F03 — Balustrade Breaker
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F03.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_FIGHT_A.mp4 (fallback if PV_F03 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7.5. Risks: a cartwheel plus a Phantom ramp plus a whip-pan is 3 camera ideas; the target flying 4 m is fine.
- **Expected score:** 9 · **If < 9 →** `Her heel lands flat on his raised forearms; she stays planted after the kick; only he flies back.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = NOVA's face, image 2 = NOVA's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, a low white-marble balustrade, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble with puddles, water spraying off clothes on every impact, soaked hair. Cold blue-grey dusk light.
0–3 s (50 mm medium, slow motion): NOVA spins and her heel kick lands flat on BLAZE's raised crossed forearms, visible contact; a sheet of water bursts off his sleeves and wraps.
3–6 s (28 mm wide, real speed): he is knocked back 3 m into the marble balustrade, which cracks, chunks dropping into the puddles; he slides down against it and shakes his head. NOVA stays in her stance.
No glow, no drawn rings, no sparkles, no lens flares, no mannequins, no strikes into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; rain, kick whoosh, forearm thud, a body hitting stone, marble cracking, splashes.
```

### F04 — Slow Punch
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F04.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: two speeds in one frame plus a torso snorricam (gives warped bodies) plus a knee slide in 8 s; "blood" is an NSFW risk.
- **Expected score:** 9 · **If < 9 →** `Only the raindrops and Blaze's fist are in slow motion; Nova moves at normal speed.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous handheld shot, 35 mm medium two-shot in profile.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble with puddles, soaked hair, breath vapour. Cold blue-grey dusk light.
0–2 s: BLAZE throws a heavy right hook; NOVA snaps her fingers: his fist and the rain around it slow to a crawl.
2–4 s: at normal speed she ducks under the slow fist and drives her knee into his ribs: visible contact.
4–6 s: speed snaps back to normal: his body folds over her knee, a burst of water flies off his vest, he drops to one knee on the wet marble, sliding a little.
No glow, no drawn rings, no sparkles, no lens flares, no mannequins, no strikes into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; muffled slowed rain, a finger snap, a knee impact, a grunt, a wet skid.
```

### F05 — Hit Me
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F05.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Line on camera:** BLAZE: "Hit me."
- **Original score:** 8.5. Risks: "blood on lip" (NSFW flag), the bomber wording, no rain block.
- **Expected score:** 9.5 · **If < 9 →** `Blaze's face fills a third of the frame, lips clearly visible when he says "Hit me."`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 85 mm slow push-in over NOVA's out-of-focus shoulder onto BLAZE, handheld micro-breathing.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA (seen only from behind, soft focus): short platinum-blonde crop, navy satin bomber jacket. Nobody resembles any real actor or celebrity.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind him, rain splashing on the stone, his soaked curls stuck to his forehead, breath vapour. Cold blue-grey dusk light.
0–2 s: BLAZE on one knee in the pouring rain spits out water and looks up.
2–4 s: he rises slowly, rolls his shoulders and raises his crimson-wrapped fists low and open.
4–6 s: close on his face, he looks at NOVA and says on camera, lips clearly in sync, a cocky half-smile: "Hit me."
No glowing skin, no ember lines, no fire, no glow, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; pouring rain, breath, a creak of wet hand wraps, his line.
```

### F06 — The Flurry
- **Duration:** 8 s (was 9) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F06.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_FIGHT_B.mp4 (fallback if PV_F06 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: "about twelve" strikes gives the stiff stage fight of rain_t2/t6; a chest snorricam warps the body; "growing water rings" invites drawn rings.
- **Expected score:** 9 · **If < 9 →** `Only five strikes, each clearly landing on his chest or forearms; medium shot, both faces visible.`
```
Live-action superhero feature film footage, 8 seconds, 2 shots with a hard cut at 5.5 s.
Image 1 = NOVA's face, image 2 = NOVA's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble with puddles, water spraying off clothes on every impact, soaked hair. Cold blue-grey dusk light.
0–5.5 s (35 mm medium two-shot, handheld): NOVA unloads five fast strikes, jab, cross, hook, knee, elbow, each one landing on BLAZE's chest and raised forearms with a burst of spray; he does not step back; the wet marble under his sneakers cracks a little more with every hit.
5.5–8 s (85 mm close-up on NOVA): breathing hard, she stares at him, eyes widening: he hasn't moved.
No glow, no drawn rings or ripples, no sparkles, no lens flares, no mannequins, no strikes into empty air; the striker stays planted.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; rain, five wet impacts rising in weight, marble cracking, her breathing.
```

### F07 — The Catch
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F07.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7.5. Risks: a macro-to-wide crash zoom plus frozen rain plus a backflip is too much; a backflip gives limb errors.
- **Expected score:** 9 · **If < 9 →** `Drop the flip: she pulls her fist free and steps back into guard.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble, soaked hair. Cold blue-grey dusk light.
0–3 s (85 mm close-up on the two fists): the raindrops hang still in the air; NOVA's punch drives through them and BLAZE's open hand catches her fist, palm on knuckles, visible contact; water squeezes out of his wraps as he grips.
3–6 s (35 mm medium two-shot): the hanging rain crashes down all at once; he squeezes, she twists her fist free and springs back into guard, both breathing hard, staring at each other.
No glow, no sparkles, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; silence, a palm-catch slap, rain crashing back, heavy breathing.
```

### F08 — Counter Punch
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F08.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: "a perfect expanding ring of clear air" is exactly the drawn-ring failure; a 10 m skid; a Phantom ramp.
- **Expected score:** 9 · **If < 9 →** `No ring shape anywhere: the rain is simply blown sideways in one gust.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 35 mm low dolly that rushes backward with NOVA after the impact.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble with puddles, water spraying off clothes on every impact. Cold blue-grey dusk light.
0–2 s: BLAZE plants his feet and throws his first real punch; NOVA crosses her forearms and his fist lands on them, visible contact.
2–6 s: the blow sends a sideways gust that whips the rain and a sheet of puddle water away from them; NOVA skids back 5 m on her heels across the wet marble, two wakes of water spraying behind her boots, and stops, still in guard. BLAZE stays planted.
No glow, no ring shapes, no ripples drawn in the air, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a deep thump, a forearm crack, a long wet heel skid, rain.
```

### F09a — Tempo Gambit (the axe kick)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F09 would not match its timing, so generate from the timed beats.
- **Original F09 score:** 5.5. Risks: wall-run, inverted leap, axe kick, crater, ankle grab and a swing into a column in 9 s; a straight-down overhead; the location jumps from the rain terrace to the sunny colonnade. **Split** F09a/F09b, both on the sunny colonnade with no rain.
- **Expected score:** 9 · **If < 9 →** `She jumps from the column base, not running up it; the kick lands on his shoulder, visible contact.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 28 mm side angle, medium-wide.
Image 1 = NOVA's face, image 2 = NOVA's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a gold colonnade over wide white marble steps veined with gold; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low sun raking through the columns as a hard key, soft bounce off the marble.
0–2 s: NOVA kicks off the base of a gold column and leaps high above BLAZE.
2–5 s: she drives a downward axe kick onto his shoulder, visible contact; he takes it, knees bending, and the marble step cracks and sinks under his sneakers with a puff of dust.
No glow, no drawn rings, no sparkles, no lens flares, no mannequins, no strikes into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a footstep on metal, a whoosh, a heavy shoulder impact, stone cracking.
```

### F09b — Tempo Gambit (the column)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F09 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `He throws her by the ankle into the column base; her back hits it, visible contact; she gets up.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 35 mm medium-wide, handheld.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a gold colonnade over white marble steps veined with gold; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low sun through the columns, hard key, long shadows.
0–2 s: still half-crouched from her kick, BLAZE grabs NOVA's ankle with one wrapped hand.
2–5 s: he swings her round and throws her back-first into a gold column, visible contact: the gold surface dents, flakes of gold leaf shower down, she drops to the marble, dazed, and pushes herself up.
No glow, no drawn rings, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real fabric and dented metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a grunt, a whoosh, a metallic dent clang, gold leaf pattering, her breath.
```

### F10 — Stronger
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F10.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8. Risks: "heat haze rising off his shoulders" plus "vibrating from pressure" invites the glowing-ember look (rain_t1/t3).
- **Expected score:** 9.5 · **If < 9 →** `Plain wet skin, only white steam, no orange or red light on his body.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 100 mm slow tilt from his fists up to his eyes on a locked tripod.
Image 1 = BLAZE's face, image 2 = BLAZE's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity.
Location: a rain-soaked white marble terrace at dusk, gold columns soft in the background; no obelisk, no tower. HEAVY REAL RAIN: thick vertical rain streaks backlit by warm lamps behind him, rain bursting on his skin. Cold blue-grey dusk light.
0–2.5 s: macro on his crimson wraps tightening around his fists, knuckles whitening, veins rising on his forearms, rain bouncing off his skin.
2.5–5 s: the tilt reaches his face: he rolls his neck, white steam rising off his wet shoulders into the cold air, the puddle at his feet trembling, his eyes calm and dangerous.
Plain skin, no glowing skin, no ember lines, no fire, no orange glow, no lens flares.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores and veins, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; heartbeat thumps, rain, a knuckle crack, a slow breath.
```

### F11 — Thanks for the Warm-up
- **Duration:** 8 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F11.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_FIGHT_B.mp4 (fallback if PV_F11 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Line on camera:** BLAZE: "Thanks for the warm-up."
- **Original score:** 8. Risks: a frozen tempo plus an uppercut plus a POV shot plus the line; the POV hides Blaze's lips.
- **Expected score:** 9 · **If < 9 →** `Shot 2 is a 3/4 medium close-up of Blaze from the front, not her POV; his lips are visible on the line.`
```
Live-action superhero feature film footage, 8 seconds, 2 shots with a hard cut at 4 s.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = NOVA's face, image 4 = NOVA's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical terrace of white marble veined with gold, gold columns behind; no obelisk, no tower. HEAVY REAL RAIN at dusk: thick vertical rain streaks backlit by warm lamps behind the actors, mirror-wet marble with puddles, water spraying off clothes on every impact, soaked hair, breath vapour. Cold blue-grey dusk light.
0–4 s (24 mm low angle, medium-wide): NOVA charges; BLAZE steps in and drives an uppercut into her crossed forearms, visible contact; she is lifted off her feet and lands on her back in a puddle with a big splash.
4–8 s (65 mm 3/4 medium close-up of BLAZE from the front): rain pouring, he stands over her, unwraps one hand slowly and says on camera, lips clearly in sync, cocky grin: "Thanks for the warm-up."
No glowing knuckles, no glow, no drawn rings, no sparkles, no lens flares, no mannequins, no strikes into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real wet fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; rain, a heavy impact, a big splash, his line.
```

## MID-BATTLE WIDE

### F12 — Battlefield From Above
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  5. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  6. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F12.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: 4 tiny characters from 30 m (identity unreadable, duplicates); a "long dust trail" behind a flying man reads as a CG trail; Aurelia on a bridge inside the square mixes two locations.
- **Expected score:** 9 · **If < 9 →** `Crane stops at 12 m; Pip and Orion clearly readable; Atlas lands instead of flying through.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 21 mm crane rising from 3 m to 12 m over the square with a slow rotation.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = PIP's face, image 4 = PIP's costume, image 5 = ORION's face, image 6 = ORION's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses; navy-cobalt suit with flat machined panels. PIP: 30, long curly copper-red hair, freckles, cyan butterfly clip; mustard knit sweater, light ripped jeans. ORION: about 65, East Asian, short grey hair, round thin glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly one of each, no other people.
Location: a classical square of white marble veined with gold, gold colonnades, a fallen gold column and scattered marble debris; open pale sky and distant mountains only; no obelisk, no monument, no tower, no stone slab, no skyscrapers. Light: low late-afternoon sun, hard raking shadows.
0–3 s: PIP stands beside the fallen column, a small cloud of matte cyan butterflies fluttering around her raised hands; ORION walks calmly between the debris, hands behind his back.
3–6 s: ATLAS sweeps in low across the frame, motion-blurred, and the wind of his pass whips dust off the marble and blows PIP's curls and ORION's coat sideways.
Butterflies look like real insects with paper-thin matte wings, no glow. No light trails, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; wind, a distant rumble, wing flutter, a fly-by air rip.
```

## PIP — THE BUTTERFLIES

### F13 — Cute Is Dangerous
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F13.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risks: a crash-zoom plus a rack focus; a "marble bench" can turn into a slab or monument.
- **Expected score:** 9 · **If < 9 →** `One butterfly only, matte; the bench explodes into real stone chunks; Pip's face stays in frame and smiling.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3.5 s.
Image 1 = PIP's face, image 2 = PIP's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans, olive crossbody bag, white sneakers. Nobody resembles any real actor or celebrity. Exactly one person.
Location: a classical square of white marble veined with gold, gold colonnades, a low carved white-marble bench; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun, hard shadows, warm skin tones.
0–3.5 s (85 mm close-up): PIP opens her cupped hands; three small matte cyan butterflies unfold their wings on her palms; she smiles sweetly and blows on them; they flutter away.
3.5–6 s (35 mm medium-wide, PIP in the foreground): one butterfly settles on the marble bench and the bench bursts apart into heavy stone chunks and a rolling cloud of dust; PIP does not flinch, still smiling.
Butterflies look like real insects with paper-thin matte wings, no glow, no sparkles. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores and freckles, real knit fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; soft wing flutter, a gentle breath, a sudden heavy stone blast, chips raining down.
```

### F14 — Swarm Hammer
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F14.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7. Risks: "hundreds of butterflies form a dense column" plus tiles peeling like a wave is CG-heavy; the bomber did not match; 4 beats.
- **Expected score:** 9 · **If < 9 →** `The swarm is a thick cloud like a murmuration of starlings, not a solid shape; Nova is pushed back by it with her guard up.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 28 mm shoulder rig with a whip-pan from PIP to NOVA.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = NOVA's face, image 4 = NOVA's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans, white sneakers. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble veined with gold, gold colonnades; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun, hard shadows.
0–2 s: NOVA sprints at PIP; PIP flicks her wrist and a thick cloud of thousands of matte cyan butterflies pours from behind her like a murmuration of starlings.
2–6 s: the dense swarm slams into NOVA's raised forearms like a wave of water and drives her backward, her boots skidding and scraping the marble, until her back hits the base of a gold column; the butterflies scatter calmly into the air.
Butterflies are real insects with paper-thin matte wings, no glow, no sparkles. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a dense roar of wings, a guard impact thud, boots scraping, a metallic thump against the column.
```

### F15 — Frozen Swarm
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F15.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: frozen rain plus a frozen swarm plus slipping between them plus a strike plus a crater is 4 beats of VFX; light rain gets lost.
- **Expected score:** 9 · **If < 9 →** `Drop the rain: only the butterflies hang frozen in the air.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous Steadicam follow shot, 40 mm medium.
Image 1 = NOVA's face, image 2 = NOVA's costume, image 3 = PIP's face, image 4 = PIP's costume. NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops; navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans, white sneakers. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical marble terrace veined with gold, gold columns; overcast dusk with cold blue-grey light and warm lamps behind; no obelisk, no tower.
0–3 s: NOVA snaps her fingers: dozens of matte cyan butterflies stop dead and hang motionless in the air between her and PIP, like a high-speed photograph; NOVA slips sideways between them, careful, millimetres from the wings.
3–6 s: she reaches PIP and lands an open palm on PIP's shoulder, visible contact; PIP stumbles back a step, then grins as the butterflies start moving again.
Butterflies are real insects with paper-thin matte wings, no glow, no sparkles. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a finger snap, sudden silence, a single wing tick, a palm hit, wings resuming.
```

### F16 — Column Cut
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F16.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risk: a clean diagonal shear can look CG-sliced.
- **Expected score:** 9 · **If < 9 →** `The column cracks and breaks like real stone (rough fracture), not a clean cut.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 2.5 s.
Image 1 = PIP's face, image 2 = PIP's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans, white sneakers. Nobody resembles any real actor or celebrity. Exactly one person.
Location: a gold colonnade over wide white marble steps veined with gold; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low sun through the columns, hard key, long shadows.
0–2.5 s (100 mm): a single matte cyan butterfly flutters lazily and lands on a massive fluted gold column.
2.5–6 s (24 mm wide, PIP in the mid-ground): the column cracks across with a rough fracture, its top half tilts and topples onto the marble steps in a wave of dust and gold-leaf flakes; PIP covers her mouth with both hands, laughing, eyes wide.
Butterfly is a real insect with paper-thin matte wings, no glow. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, real metal and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; one wing flutter, a groan of metal, an enormous crash, debris raining.
```

### F17 — Swarm Versus Trap
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F17.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7. Risks: 3 setups; "a slab tilts up as a shield" brings the forbidden slab look; "pinning the swarm" is an abstract logic beat.
- **Expected score:** 9 · **If < 9 →** `Orion stays in frame the whole time; the floor tile flips up like a heavy marble trapdoor.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 2.5 s.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = ORION's face, image 4 = ORION's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans. ORION: about 65, East Asian, short grey hair, round thin metal glasses, calm; long charcoal cable-knit cardigan coat over a grey shirt, black trousers. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble floor tiles veined with gold, gold colonnades; open pale sky; no obelisk, no monument, no tower. Light: low late-afternoon sun, hard shadows.
0–2.5 s (35 mm over PIP's shoulder): PIP throws her arm forward and a thick cloud of matte cyan butterflies rushes at ORION, who stands calmly with his hands behind his back.
2.5–6 s (50 mm on ORION): he taps one floor tile with the toe of his shoe; the heavy marble tile flips up on its edge in front of him like a trapdoor; the swarm smashes into it and the tile bursts into chunks and dust; ORION, untouched, adjusts his glasses.
Butterflies are real insects with matte wings, no glow. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real wool and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a roar of wings, a shoe tap, stone grinding, a shatter, dust settling.
```

### F18a — Giant Fist of Wings (the strike)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F18 would not match its timing, so generate from the timed beats.
- **Original F18 score:** 6. Risks: "thousands of butterflies form a giant fist shape" is pure CG; a crater plus a pre-cut chain plus a lantern rig in 9 s. **Split** into F18a (the swarm hammer misses) and F18b (the bronze lantern trap).
- **Expected score:** 9 · **If < 9 →** `The swarm is a dense dark-cyan cloud falling like a waterfall, not a fist shape.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 18 mm low wide angle.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = ORION's face, image 4 = ORION's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble veined with gold, gold colonnades; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun, hard shadows.
0–2 s: PIP, angry, swings both arms down; a huge dense cloud of thousands of matte cyan butterflies rises behind her and arcs over like a breaking wave.
2–5 s: the mass crashes down onto the spot where ORION stands; at the last instant he takes one calm step aside; the marble where he stood smashes into a crater, stone fragments and dust flying; he brushes dust off his sleeve.
Butterflies are real insects with matte wings, no glow, no solid shapes. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a massive roar of wings, a crater boom, stone fragments falling.
```

### F18b — Giant Fist of Wings (the lantern trap)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F18 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `The bronze lantern frame drops straight down between them with real weight; nothing floats.`
```
Live-action superhero feature film footage, 4 seconds, ONE continuous shot, 35 mm medium-wide.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = ORION's face, image 4 = ORION's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: under a gold colonnade on the marble square; a heavy bronze lantern frame hangs on a chain between two columns; open pale sky; no obelisk, no tower. Light: low sun, hard shadows.
0–1.5 s: ORION, calm, flicks a small chain hook with one finger.
1.5–4 s: the heavy bronze lantern frame drops on its chain and slams onto the marble right between PIP and her cloud of matte cyan butterflies, cutting her off; dust bursts up; PIP stops, mouth open, then frowns at ORION.
No glow, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real bronze and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a chain snap, a heavy bronze clank, dust, Pip's frustrated gasp.
```

## ORION — THE STRATEGIST

### F19 — The Board
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F19.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risk: a crane to 25 m with nobody in frame becomes the empty-square / miniature look (R8).
- **Expected score:** 9 · **If < 9 →** `The crane stops at 10 m; Orion stays clearly visible at the edge of the frame.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = ORION's face, image 2 = ORION's costume. ORION: about 65, East Asian, short grey hair, round thin metal glasses, calm; long charcoal cable-knit cardigan coat over a grey shirt, black trousers. Nobody resembles any real actor or celebrity. Exactly one person.
Location: a classical square of white marble tiles in a regular grid, veined with gold, gold colonnades, a low marble balustrade; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun, hard shadows; dust drifting in the air from a fight off-screen.
0–3 s (100 mm macro): ORION's fingers place a small black wooden chess knight on the marble balustrade; dust settles on it; his glasses reflect the square.
3–6 s (crane rising to 10 m, ORION at the edge of frame): the square's tile grid reads like a chessboard with debris as pieces; ORION turns calmly and walks away.
No glow, no drawn lines on the floor, no text, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real wool and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a distant fighting rumble, a chess-piece click, wind.
```

### F20 — Tile Slide
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F20.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risk: "drops waist-deep" gives impossible geometry; "mud" contradicts the marble.
- **Expected score:** 9 · **If < 9 →** `The tile tips and Blaze falls hard onto his side on the marble; no hole.`
```
Live-action superhero feature film footage, 6 seconds, ONE continuous shot, 28 mm low tracking shot behind BLAZE that ends on a side angle.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = ORION's face, image 4 = ORION's costume. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble floor tiles veined with gold, gold colonnades; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun, hard shadows.
0–2.5 s: BLAZE charges at ORION with a big right hand cocked back; ORION calmly steps back one tile.
2.5–6 s: the tile under BLAZE's front foot tips up on a hinge; he loses his footing and slams down on his side, his swinging fist cracking the tile edge into pieces; dust bursts; he looks up and ORION is already three tiles away, hands behind his back.
No glow, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; running footsteps, stone grinding, a heavy body thud, stone shattering.
```

### F21 — Bell Drop
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F21.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risk: Pip disappears under the bell, so her identity is only checkable in beat 1; a bell that "cracks but holds" is ambiguous.
- **Expected score:** 9.5 · **If < 9 →** `Pip's face clearly visible in the first 2 s; the bell lands with real weight and rings.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3.5 s.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = ORION's face, image 4 = ORION's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a gold colonnade arch over white marble, a huge bronze bell hanging on a rope inside the arch; open pale sky; no obelisk, no tower. Light: low sun through the columns, hard shadows.
0–3.5 s (21 mm low angle): PIP backs under the arch, a few matte cyan butterflies around her, facing ORION; ORION calmly pulls a rope tied to a column; the huge bronze bell drops over PIP and slams onto the marble, dust bursting from under its rim.
3.5–6 s (85 mm): the bell rings and shudders from thuds inside; ORION places his palm flat on the bronze to stop the hum and smiles faintly.
No glow, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real bronze and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a rope whir, a colossal bronze clang, a long ring, muffled thuds inside.
```

### F22a — Checkmate Setup (the trap)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  5. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  6. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F22 would not match its timing, so generate from the timed beats.
- **Original F22 score:** 5.5. Risks: 3 characters in a top-down domino chain (pole, column, lattice) over 9 s; top-down hides faces. **Split** F22a/F22b, 3/4 high angle instead of top-down.
- **Expected score:** 9 · **If < 9 →** `The pole falls straight across Pip's path; she stops in time; both faces readable.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 24 mm high three-quarter crane angle (not top-down), slowly lowering.
Image 1 = ORION's face, image 2 = ORION's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume, image 5 = PIP's face, image 6 = PIP's costume. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. BLAZE: 28, dark curly hair, short beard; black sleeveless hooded vest, black joggers, crimson hand wraps, headphones around his neck. PIP: 30, long curly copper-red hair, freckles, cyan butterfly clip; mustard knit sweater, light ripped jeans. Nobody resembles any real actor or celebrity. Exactly three people.
Location: a classical square of white marble tiles veined with gold, gold colonnades, a tall gold banner pole; open pale sky; no obelisk, no monument, no tower. Light: low late-afternoon sun, hard shadows.
0–2.5 s: BLAZE and PIP circle ORION from two sides; ORION walks three tiles diagonally, calm.
2.5–5 s: BLAZE follows and steps on a raised tile; with a clunk the tall gold banner pole tips and falls across PIP's path; she skids to a stop just in front of it.
No glow, no drawn lines, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, metal and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; footsteps, a stone clunk, a metal pole clang, sneakers skidding.
```

### F22b — Checkmate Setup (the pin)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F22 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `Only the cracked column falls; Blaze is pinned by its weight across his legs and strains; Orion untouched.`
```
Live-action superhero feature film footage, 5 seconds, ONE continuous shot, 28 mm medium-wide at eye level.
Image 1 = ORION's face, image 2 = ORION's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: the marble square, a fallen gold banner pole on the floor, a cracked gold column standing; open pale sky; no obelisk, no monument, no tower. Light: low late-afternoon sun.
0–2 s: BLAZE swings a big punch at ORION, who leans back; BLAZE's fist hits the cracked gold column instead, visible contact.
2–5 s: the column breaks and falls onto the banner pole, pinning BLAZE's legs under a heavy lattice of gold; he strains and pushes; ORION stands on the one clear tile, untouched, and adjusts his cardigan.
No glow, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real metal and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a fist on metal, a column groan, a heavy crash, strained breathing.
```

### F23 — You Can't Predict Work
- **Duration:** 8 s (was 9) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F23.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Line on camera:** ATLAS: "You can predict talent. You can't predict work."
- **Original score:** 8. Risks: the word "slab" (R-series slab/monument); an R3-style extra cut; the glasses falling off and coming back.
- **Expected score:** 9 · **If < 9 →** `No other cuts; his glasses stay on the whole time; he says the line facing the camera 3/4.`
```
Live-action superhero feature film footage, 8 seconds, 2 shots with a hard cut at 4 s, no other cuts.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = ORION's face, image 4 = ORION's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses (they stay on), short grey stubble; fitted navy-cobalt suit with flat machined chest and shoulder panels, black boots. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble veined with gold, gold colonnades behind; open pale sky; no obelisk, no monument, no tower, no skyscrapers. Light: low late-afternoon sun, dust floating in the light.
0–4 s (35 mm low angle): ATLAS lies under a broken block of marble floor; ORION turns to walk away; the block lifts as ATLAS pushes it off with one arm and gets up, dust pouring off his suit.
4–8 s (85 mm slow push-in, ATLAS 3/4 to camera, ORION's back soft in the foreground): ATLAS straightens his glasses and says on camera, lips clearly in sync, face fully visible: "You can predict talent. You can't predict work." ORION stops walking.
No glow, no blue light, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real brushed metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; grinding stone, a block dropping, a dusty breath, his line.
```

### F24 — Strategy Ends
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F24.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6. Risks: "a gold beam swings" (the word beam produces a light beam); "cobalt force shows as a heat-haze shockwave" (energy wording); traps swept away is abstract.
- **Expected score:** 9 · **If < 9 →** `The girder is a solid gold metal I-beam on two chains; his fist dents it, visible contact.`
```
Live-action superhero feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = ORION's face, image 4 = ORION's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined panels, black boots. ORION: about 65, East Asian, short grey hair, round thin metal glasses; long charcoal cable-knit cardigan coat. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a classical square of white marble veined with gold, gold colonnades; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low late-afternoon sun.
0–3 s (28 mm whip-pan): ORION pulls a hidden rope; a heavy solid-gold metal girder hanging on two chains swings at ATLAS like a pendulum; ATLAS plants his feet and punches it, visible contact: the girder bends around his fist with a deep dent and stops.
3–6 s (50 mm locked two-shot): the bent girder sways on its chains; ORION sighs, sits down on a marble step and folds his hands; ATLAS shakes out his hand.
No glow, no beams of light, no heat-haze effects, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real bent metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a rope whip, chains rattling, a massive metal crunch, a quiet settle.
```

## TEAM-UP & THE QUEEN ARRIVES

### F25a — Team-Up Launch (catapult)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F25 would not match its timing, so generate from the timed beats.
- **Original F25 score:** 5.5. Risks: a butterfly catapult, twin flight past a 20 m wall, a double punch and a collapse in 8 s; "cobalt force… bends the light". **Split** F25a (Pip launches Blaze) and F25b (the wall breaks).
- **Expected score:** 9 · **If < 9 →** `Pip cups her hands, Blaze steps into them and she boosts him upward like a gymnastics throw; the butterflies only swirl around them.`
```
Live-action superhero feature film footage, 4 seconds, ONE continuous shot, 24 mm low angle, medium-wide.
Image 1 = PIP's face, image 2 = PIP's costume, image 3 = BLAZE's face, image 4 = BLAZE's costume. PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip; mustard knit sweater, light ripped jeans, white sneakers. BLAZE: 28, dark curly hair, thick brows, short beard, silver chain; black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: the marble square in front of a tall smooth gold wall that blocks the way; open pale sky above it; no obelisk, no monument, no tower. Light: low late-afternoon sun.
0–2 s: BLAZE sprints toward PIP; she crouches with both hands cupped low; a whirl of matte cyan butterflies swirls up around them.
2–4 s: he steps into her hands and she launches him upward with all her strength; he shoots up out of the top of the frame, the butterflies and dust blown up after him; PIP looks up, grinning.
Butterflies are real insects with matte wings, no glow. No beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; running footsteps, a grunt, a whoosh, wings.
```

### F25b — Team-Up Launch (the wall falls)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F25 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `Both fists visibly hit the gold wall at the same time; the wall cracks into large panels and falls away from camera.`
```
Live-action superhero feature film footage, 5 seconds, 2 shots with a hard cut at 2 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = BLAZE's face, image 4 = BLAZE's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined panels, black boots. BLAZE: 28, dark curly hair, thick brows, short beard; black sleeveless hooded vest, black joggers, crimson hand wraps, headphones around his neck. Nobody resembles any real actor or celebrity. Exactly two people.
Location: the top of a tall smooth gold wall above the marble square; open pale sky; no obelisk, no monument, no tower. Light: low late-afternoon sun, hard shadows.
0–2 s (35 mm, both rising into frame side by side in mid-air at the top of the wall, wind tearing at their clothes): they pull back their right fists.
2–5 s (24 mm wide from below): both fists slam into the gold wall at the same instant, visible contact; the wall cracks into huge panels that tilt and fall outward with clouds of dust and gold-leaf flakes; sunlight floods through the gap.
No glow, no blue light, no beams, no heat-haze effects, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; wind rush, a double impact boom, a huge metal-wall collapse, debris raining.
```

### F26a — The Queen Arrives (the walk)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F26 would not match its timing, so generate from the timed beats.
- **Original F26 score:** 5. Risks: 6 characters and 12 refs; "a visible pressure wave like a sound barrier" gives drawn rings; 5 bodies shoved at once. **Split** F26a (Aurelia alone) and F26b (the push hits three heroes).
- **Expected score:** 9.5 · **If < 9 →** `Plain sky behind her head; nothing behind her except the canyon.`
```
Live-action fantasy feature film footage, 5 seconds, ONE continuous shot, 35 mm low Steadicam backing away in front of her.
Image 1 = AURELIA's face, image 2 = AURELIA's costume. AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, one tiny 3 mm square gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets. No crown, no headdress, no halo, no rays behind her head. Nobody resembles any real actor or celebrity. Exactly one person.
Location: an ancient bridge of pale carved stone blocks with gold inlay and a low gold balustrade over a deep sandstone canyon; no guardrails, no asphalt, no cables; open sky; no obelisk, no monument, no tower. Light: low sunset sun from frame left as a hard warm key, long shadows, natural orange-to-pale-blue sky, no god-rays.
0–3 s: AURELIA walks slowly toward the camera along the bridge, cape trailing over the stone, the gold flake on her cheek catching the sun, her expression bored.
3–5 s: she stops and raises one open hand, palm out; a sudden gust blasts dust and loose gold leaf away from her across the bridge, her cape snapping back.
No glow, no drawn rings or ripples, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real satin and metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; slow footsteps on stone, canyon wind, a deep gust.
```

### F26b — The Queen Arrives (the push)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  5. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  6. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F26 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `Only three people; all three shoved back by wind and dust, faces visible, nothing drawn in the air.`
```
Live-action fantasy feature film footage, 4 seconds, ONE continuous shot, 24 mm wide from slightly in front of the three heroes.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = BLAZE's face, image 4 = BLAZE's costume, image 5 = PIP's face, image 6 = PIP's costume. ATLAS: 55, swept-back silver-grey hair, dark tortoise glasses; navy-cobalt suit with flat machined panels. BLAZE: 28, dark curly hair, short beard; black sleeveless hooded vest, crimson hand wraps, headphones around his neck. PIP: 30, long curly copper-red hair, freckles, cyan butterfly clip; mustard knit sweater, light ripped jeans. Nobody resembles any real actor or celebrity. Exactly three people.
Location: the same ancient carved-stone bridge with gold inlay over a sandstone canyon at sunset; no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–1 s: the three stand side by side, ready, looking ahead.
1–4 s: a violent blast of wind and dust hits them from the front: all three are shoved back 2 m, boots skidding on the stone, arms up to shield their faces, Pip's curls and Blaze's hood whipping back; a crack runs along the bridge toward them.
No glow, no drawn rings or ripples, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a deep pressure boom, a wind blast, boots skidding, stone cracking.
```

## ATLAS vs AURELIA — THE CLIMAX

**Bridge + duel lock (in every prompt below):** Atlas is on the LEFT of frame and Aurelia on the RIGHT in every two-shot (QA H7: the 180° flip). Atlas's RIGHT forearm and fist are gold from F29 on, and the gold climbs: wrist (F29) → elbow (F30–F33) → shoulder (F34–F40). Aurelia never wears a crown, halo or rays.

### F27 — Atlas Lands
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F27.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7.5. Risks: an FPV chase 1 m above the deck turns into a long low hover (H3: hovering/CG); a 10 m gap makes faces tiny; the bridge reads as a highway.
- **Expected score:** 9 · **If < 9 →** `He drops into frame from above and lands; no flying along the bridge.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 2.5 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined chest and shoulder panels, black boots; both arms normal. AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, one tiny 3 mm square gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient bridge of pale carved stone blocks with gold inlay and a low gold balustrade over a deep sandstone canyon; no guardrails, no asphalt, no cables; open sky; no obelisk, no monument, no tower, no stone slab. Light: low sunset sun from frame left, hard warm key, natural orange-to-pale-blue sky, no god-rays.
0–2.5 s (14 mm low on the bridge deck): ATLAS drops from the sky feet-first and lands on one knee; the stone cracks outward under him, a burst of dust and chips blows across the deck, his suit creasing with the impact.
2.5–6 s (50 mm locked two-shot, ATLAS frame left, AURELIA frame right, 4 m apart): he rises and adjusts his glasses; she tilts her head, unimpressed, her cape still settling.
No glow, no blue light on his body, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real brushed metal, satin and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a rush of air, a heavy landing boom, chips clinking, canyon wind.
```

### F28 — The Stop Hand
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F28.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_FIGHT_A.mp4 (fallback if PV_F28 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 5.5. Risks: an "invisible wall 10 cm from her palm" plus "air rippling outward in rings" is exactly QA C4 (a punch into air, a flick with no contact) and the R6 rings.
- **Fix:** real palm-to-knuckle contact.
- **Expected score:** 9 · **If < 9 →** `Her bare palm touches his knuckles; his fist stops dead on her palm; the wind blows back only behind HIM.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined panels, black boots; both arms normal. AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, one tiny 3 mm square gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key, natural sky.
0–3 s (50 mm profile two-shot, ATLAS frame left, AURELIA frame right, an arm's length apart): ATLAS throws a full-weight straight right at her face; without looking at him she raises her open palm and his fist lands flat on her palm, visible contact, and stops dead; a blast of dust and loose gold leaf blows off the deck behind HIM, his sleeve rippling back.
3–6 s (85 mm on the fist pressed into her palm, her bored face behind it): he pushes, jaw clenched, his arm trembling; she does not move an inch and slowly yawns.
No beams, no glow, no invisible walls, no drawn rings or ripples, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real metal, satin and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a punch whoosh, a deep thump of a fist on a palm, a wind blast, his strained breath, her soft yawn.
```

### F29 — Boring
- **Duration:** 6 s (was 7) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F29.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Line on camera:** AURELIA: "Boring."
- **Original score:** 7. Risks: gold "spreads… like liquid metal" is QA H7 (liquid-CG gauntlet); a macro on the wrist then a rack focus makes her line easy to miss.
- **Expected score:** 9 · **If < 9 →** `Cut straight from the touch to his hand already turned to solid cast gold; no visible melting.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = AURELIA's face, image 2 = AURELIA's costume, image 3 = ATLAS's face, image 4 = ATLAS's suit. AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, one tiny 3 mm square gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown, gold gauntlets; no crown, no halo. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; open sky; no obelisk, no monument, no tower. Light: low sunset sun, warm side key.
0–3 s (100 mm macro): ATLAS's fist still pressed into AURELIA's palm; she touches two fingertips to his right wrist; his right hand is now solid polished cast gold up to the wrist, heavy and reflective, like a gold statue's hand, fine cracks at the edge where it meets the skin.
3–6 s (85 mm close-up of AURELIA, 3/4 to camera, face fully visible): she looks at him and says on camera, quiet, lips clearly in sync, hands away from her mouth: "Boring."
No liquid, no melting, no glow, no sparkles, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real polished metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a soft metallic creak, canyon wind, her line.
```

### F30 — Gold Creep
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F30.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8. Risks: "creeps… hardening" is an animated transformation (CG); 3 camera moves.
- **Expected score:** 9 · **If < 9 →** `His right forearm is already solid gold to the elbow from the first frame.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; fitted navy-cobalt suit with flat machined panels, black boots. His RIGHT hand and forearm, up to the elbow, are solid polished gold metal, heavy; his left arm is normal. Nobody resembles any real actor or celebrity. Exactly one person.
Location: an ancient carved-stone bridge with a low gold balustrade over a sandstone canyon; no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–3 s (35 mm handheld): ATLAS staggers back clutching his gold right forearm with his left hand, staring at it; then he slams the gold forearm into the gold balustrade, visible contact: the rail buckles and bends outward over the canyon, bolts popping.
3–6 s (65 mm on his face and shoulder): breathing hard, he lets the arm hang; its weight drags his right shoulder down.
No glow, no liquid metal, no sparkles, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real polished and bent metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a metal creak, a heavy clang, bolts popping, ragged breath.
```

### F31a — Into the Sky (lift-off)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F31 would not match its timing, so generate from the timed beats.
- **Original F31 score:** 5.5. Risks: grab, fly up, an orbit spin, a palm blast, a canyon-wall crater and an FPV orbit plus a dive in 9 s; the spin gives tangled limbs. **Split** F31a (he drives her up) and F31b (she shoves him into the canyon wall).
- **Expected score:** 9 · **If < 9 →** `Camera stays on the bridge looking up; they rise out of frame together.`
```
Live-action fantasy feature film footage, 4 seconds, ONE continuous shot, 24 mm low angle from the bridge deck tilting up.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; his RIGHT forearm and fist are solid polished gold to the elbow. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; open sunset sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm key.
0–1.5 s: ATLAS lunges and grabs AURELIA by her armoured shoulders, both hands gripping the gold feathers, visible contact.
1.5–4 s: he drives them both straight up off the bridge into the open sky, her cape whipping around them, dust blown off the deck below; they rise out of the top of the frame.
No glow, no light trails, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real metal and satin, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a grunt, wind roar, a cape flapping.
```

### F31b — Into the Sky (the canyon wall)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F31 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `Her palm visibly lands on his chest plate; he flies back and hits real sandstone; she stays in place.`
```
Live-action fantasy feature film footage, 5 seconds, 2 shots with a hard cut at 2 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT forearm and fist solid polished gold to the elbow. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: high in the open sunset sky above a deep sandstone canyon; no obelisk, no monument, no tower. Light: low sunset sun, warm key, natural sky.
0–2 s (35 mm medium two-shot in mid-air, wind tearing at hair and cape): AURELIA, calm, places her open palm flat on ATLAS's chest plate, visible contact, and pushes.
2–5 s (24 mm wide on the canyon wall): ATLAS is hurled down and back into the sandstone canyon wall; the rock cracks into a crater and a cloud of orange dust bursts out; stones fall.
No glow, no beams, no drawn rings or ripples, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real metal, satin and sandstone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; wind roar, a soft palm thump, a rock impact boom, falling stones.
```

### F32 — Golden Column
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F32.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_PILLAR_SAVE.mp4 (fallback if PV_F32 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7.5. Risks: the column "turns to gold mid-fall" (a transformation); 3 beats plus a shove; a deep tonal "metal tone" in the audio list invites music.
- **Expected score:** 9 · **If < 9 →** `The column is gold from the start; Aurelia only taps it to make it fall.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 2.5 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT forearm and fist solid polished gold to the elbow. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: a gold colonnade over white marble steps veined with gold; open pale sky; no obelisk, no monument, no tower, no stone slab. Light: low sun through the columns, hard key.
0–2.5 s (24 mm low angle up): AURELIA, bored, taps a massive solid-gold column with one finger; it cracks at the base and topples toward ATLAS.
2.5–6 s (50 mm on ATLAS): he catches it on his left shoulder and gold forearm, visible contact; his knees buckle, his boots sink into the cracking marble step, dust spurting out of the cracks; he holds it, trembling, veins on his neck, then shoves it aside and it slams into the floor.
No glow, no blue light, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real metal and marble, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; stone groaning, a heavy catch thud, steps cracking, a final ground-shaking impact.
```

### F33 — Five Punches
- **Duration:** 6 s (was 9) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F33.mp4 (optional, only if it exists) · https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_FIGHT_B.mp4 (fallback if PV_F33 is 404)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6. Risks: 5 punches into "air-barrier ripples" (punches into air plus rings); a 360° orbit during a fight breaks screen direction (H7 180° flip); a 5 m slide.
- **Expected score:** 9 · **If < 9 →** `Three punches only, each landing on her palm; camera fixed in profile.`
```
Live-action fantasy feature film footage, 6 seconds, ONE continuous shot, 35 mm profile two-shot with a slow dolly, ATLAS frame left, AURELIA frame right.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT forearm and fist solid polished gold to the elbow. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–4 s: ATLAS throws three fast punches, gold right, left, gold right; each one lands on AURELIA's open palm, visible contact, with a puff of dust blown off the deck behind him; with each block she steps forward and he steps back.
4–6 s: she flattens her palm on his chest plate and pushes: he slides back 3 m on the stone deck, his heels carving two lines in the dust.
No glow, no invisible walls, no drawn rings or ripples, no sparkles, no lens flares, no mannequins, no punches into empty air.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real metal, satin and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; three heavy palm thumps rising, a long boot skid, canyon wind.
```

### F34a — Training Ghosts (on the bridge)
- **Duration:** 5 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F34 would not match its timing, so generate from the timed beats.
- **Original F34 score:** 6. Risks: 3 flashback locations plus the bridge with 6-frame flash cuts in one prompt (Seedance merges locations, adds extra cuts). **Split** F34a (the bridge) and F34b (the gym flashback); the editor intercuts them.
- **Expected score:** 9.5 · **If < 9 →** `One continuous close shot, no cuts.`
```
Live-action fantasy feature film footage, 5 seconds, ONE continuous shot, 85 mm slow push-in from medium close-up to extreme close-up.
Image 1 = ATLAS's face, image 2 = ATLAS's suit. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; his RIGHT arm is solid polished gold metal from the fingers up to the shoulder; left arm normal. Nobody resembles any real actor or celebrity. Exactly one person.
Location: an ancient carved-stone bridge over a sandstone canyon; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key, dust floating in the light.
0–2.5 s: ATLAS kneels on one knee on the bridge, head down, his heavy gold arm resting on the stone, dust settling on his glasses, breathing hard.
2.5–5 s: the camera pushes into his eyes; his eyes lift behind the glasses, his jaw sets, and he breathes out slowly.
No glow, no blue light, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores and sweat, real polished metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a heartbeat, his breath, canyon wind.
```

### F34b — Training Ghosts (the gym flashback)
- **Duration:** 4 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/C2_ATLAS_GYM_flow_nbpro_v2_OK.png
- **Motion ref:** none. This is a split shot: the original PV_F34 would not match its timing, so generate from the timed beats.
- **Expected score:** 9 · **If < 9 →** `One location only, the gym; no costume, grey T-shirt; face visible.`
```
Live-action film flashback footage, 4 seconds, 2 shots with a hard cut at 2 s, handheld 50 mm.
Image 1 = ATLAS's face, image 2 = the gym. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; sweat-soaked grey T-shirt, black training shorts, normal arms. Nobody resembles any real actor or celebrity. Exactly one person.
Location: a dim old boxing gym like image 2, worn heavy bag on a chain, tungsten work lights, concrete floor, grey dawn through a high window.
0–2 s: ATLAS pounds the worn heavy bag with a combination, visible contact, the bag jumping on its chain, sweat flying off his face on each impact.
2–4 s: he drops to the concrete and does fast push-ups, breath fogging, face toward the camera, jaw clenched.
No glow, no lens flares, no mannequins.
STYLE: 35 mm film, natural film grain, gritty practical light, real skin with pores and sweat, real fabric and leather, no CG look, no text.
AUDIO: no music, no score, no soundtrack; heavy-bag thuds, a chain rattle, breathing, push-up grunts.
```

### F35 — Heavy Arm
- **Duration:** 6 s · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F35.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5. Risk: the gold extent was not stated (continuity); otherwise simple.
- **Expected score:** 9.5 · **If < 9 →** `Aurelia's reaction is a clear front 3/4 medium close-up; she uncrosses her arms.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3.5 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT arm solid polished gold from fingers to shoulder, left arm normal. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–3.5 s (28 mm low, slow dolly in, ATLAS frame left): he stands up, lifting the heavy gold arm; its weight pulls him sideways; he plants his feet and the stone under each boot cracks; he raises the gold fist to guard height.
3.5–6 s (85 mm on AURELIA, frame right, facing camera 3/4): for the first time she uncrosses her arms, one eyebrow raised, slightly interested.
No glow, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real polished metal and satin, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a metal creak, stone cracking, breath, wind.
```

### F36 — Everyone Watches
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  5. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  6. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F36.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6.5. Risks: 4 characters plus 3 separate actions plus frozen drops; "heat haze in the distance" gives a CG vortex; the bomber did not match. Orion is removed (he is in F19–F24).
- **Expected score:** 9 · **If < 9 →** `Only the three of them, side by side, seen from behind then from the front; no effects.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = BLAZE's face, image 2 = BLAZE's costume, image 3 = PIP's face, image 4 = PIP's costume, image 5 = NOVA's face, image 6 = NOVA's costume. BLAZE: 28, dark curly hair, short beard, silver chain; black sleeveless hooded vest, black joggers, crimson hand wraps, headphones around his neck. PIP: 30, long curly copper-red hair, freckles, cyan butterfly clip; mustard knit sweater, light ripped jeans. NOVA: mid 20s, deep brown skin, short platinum-blonde crop; navy satin bomber jacket with a crimson phoenix on the back, black cargo pants. Nobody resembles any real actor or celebrity. Exactly three people.
Location: the edge of a gold colonnade above a sandstone canyon at sunset; far away the stone bridge with a column of dust rising from it; open sky; no obelisk, no monument, no tower. Light: low sunset sun, warm, gusts of wind.
0–3 s (135 mm from behind them, slow push): the three stand at the edge, hair whipping in the gusts, watching the dust rise over the distant bridge.
3–6 s (50 mm from the front): PIP steps forward to run toward the bridge; BLAZE grabs her shoulder and holds her back; NOVA stares, hand over her heart, worried.
No glow, no vortex, no beams, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real fabric, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a deep distant rumble, gusting wind.
```

### F37 — Vertical Launch
- **Duration:** 5 s (was 7) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F37.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7. Risks: a "sonic-boom ring" plus a "condensation cone" (drawn rings, CG); an FPV vertical chase past the bridge (portal/vortex risk like R1_t3).
- **Expected score:** 9 · **If < 9 →** `Camera stays on the ground looking up; he leaves frame upward; only dust and stones react.`
```
Live-action fantasy feature film footage, 5 seconds, ONE continuous shot, 14 mm ground-level camera looking up.
Image 1 = ATLAS's face, image 2 = ATLAS's suit. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels, scuffed and dusty; RIGHT arm solid polished gold from fingers to shoulder. Nobody resembles any real actor or celebrity. Exactly one person.
Location: the floor of a deep sandstone canyon among broken rocks; high above, the underside of an ancient stone bridge crosses the strip of sunset sky; no obelisk, no monument, no tower. Light: warm bounced sunset light on the canyon walls, cool shade at the bottom.
0–2 s: ATLAS crouches among the broken sandstone, gold fist braced on the ground, looking up.
2–5 s: he launches straight up: the ground cracks under him, a burst of dust and pebbles blasts out and rocks jump into the air and fall back; he shrinks fast toward the bridge high above and leaves the top of the frame.
No glow, no light trails, no rings, no condensation cone, no portal, no vortex, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin, real metal and rock, physically correct light, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a deep boom, rocks clattering, wind roar.
```

### F38 — The Wall Bends
- **Duration:** 6 s (was 8) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F38.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6. Risks: the "air wall… ripple bends inward around his knuckles" (drawn ripple plus air punch); a Phantom ramp; the bun loosening (identity drift).
- **Expected score:** 9 · **If < 9 →** `His gold fist lands on her palm (contact) and her whole body is driven back; she stays the same person, bun intact.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT arm solid polished gold from fingers to shoulder. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–3 s (50 mm profile two-shot, ATLAS frame left, AURELIA frame right): ATLAS vaults over the balustrade and drives his gold fist into her raised open palm, visible contact; this time her arm buckles and her heels skid back across the stone.
3–6 s (24 mm wide from behind her): behind her the stone deck shatters in a fan of cracks, her cape blasts flat, a few strands come loose from her bun; she stares at him, shocked for the first time.
No glow, no invisible walls, no drawn rings or ripples, no sparkles, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real metal, satin and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a heavy fist-on-palm thump, a boot skid, stone shattering, wind.
```

### F39 — The Build-Up
- **Duration:** 6 s (was 9) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F39.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 6. Risks: "debris sucked in a slow spiral toward his fist" is exactly the R1_t3 CG VORTEX; "the bridge flexes, cables vibrating" is a suspension-bridge/highway look; 9 s.
- **Expected score:** 9 · **If < 9 →** `No spiral: dust and pebbles only skitter across the deck toward his boots.`
```
Live-action fantasy feature film footage, 6 seconds, 2 shots with a hard cut at 3.5 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT arm solid polished gold from fingers to shoulder. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets; no crown, no halo. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge with gold inlay over a sandstone canyon; no cables, no guardrails, no asphalt; open sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–3.5 s (35 mm slow Steadicam move around ATLAS, frame left): he draws his gold arm back in one long wind-up; the stone deck cracks under his boots; dust, pebbles and loose gold leaf skitter across the deck toward him; the air above his fist shimmers like heat over hot asphalt.
3.5–6 s (100 mm on AURELIA's eyes): her eyes widen for the first time; she raises her hand and her fingers tremble.
No spiral, no vortex, no portal, no glow, no drawn rings, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real metal and stone, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a rising low rumble, wind pulling inward, stone cracking.
```

### F40 — The Last Frame
- **Duration:** 4 s (was 6) · 16:9 · 720p
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_F40.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7. Risks: a crash-zoom along the arm with "snorricam on the fist" hides who is where; "air rippling" gives rings. This is the CLIMAX F15 v3 beat: both must be in one frame, the fist reaching her face (QA C3).
- **Expected score:** 9 · **If < 9 →** `Both in the same frame in profile, 1 m apart; the fist stops a hand-width from her cheek; her hair blown back.`
```
Live-action fantasy feature film footage, 4 seconds, 2 shots with a hard cut at 2 s.
Image 1 = ATLAS's face, image 2 = ATLAS's suit, image 3 = AURELIA's face, image 4 = AURELIA's costume. ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble; navy-cobalt suit with flat machined panels; RIGHT arm solid polished gold from fingers to shoulder. AURELIA: early 30s, dark brown hair in a low bun, tiny 3 mm gold flake on her left cheekbone; gold leaf-feather bodice, champagne satin gown with a long cape, gold earrings; no crown, no halo, no rays behind her head. Nobody resembles any real actor or celebrity. Exactly two people.
Location: an ancient carved-stone bridge over a sandstone canyon; open sunset sky; no obelisk, no monument, no tower. Light: low sunset sun, hard warm side key.
0–2 s (35 mm profile two-shot, ATLAS frame left, AURELIA frame right, 1 m apart): he lands in front of her and drives a huge gold right punch at her face.
2–4 s (85 mm close-up on AURELIA, the gold fist entering frame left and filling a third of the frame): the fist stops a hand-width from her cheek; the wind of it blows her hair, earrings and cape hard back; her eyes are wide; the shot ends on the frame just before contact.
No glow, no neon, no drawn rings or ripples, no halo, no lens flares, no mannequins.
STYLE: 35 mm anamorphic film, natural film grain, real skin with pores, real polished metal, physically correct sunlight, no CG look, no text.
AUDIO: no music, no score, no soundtrack; a rising roar of wind, then sudden silence on the last frame.
```



---

# PART 2 — REALISM (R01–R40)
The writer of REALISM_40 already applied QUALITY_RULES, so most prompts only needed small fixes:
- off-screen lines removed
- halo/crown and bell-tower triggers removed
- crowd shots stripped of previs
- crowds reduced
- audio line normalised

**New wardrobe locks for Yacine to approve** (set by the REALISM writer):
- Gala: Pip in a plum velvet midi dress, Nova in a black satin jumpsuit, Blaze in a charcoal suit with an open collar.
- Trophy: a crystal spire inside a gold ring.
- Atlas's family: his mother and his SISTER.

Making-of = grey mocap suits with markers.

### R01 — Jib sweep over the packed hall (opening light cue)
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: Crowd from hall_t4 only (good). Risk: "beams visible in haze" can turn into CG lasers; a PV with dummy seats would be copied. **Change:** Remove the PV. Keep the stage beams as real haze beams.
- **If < 9 →** `The moving-head lights are real stage fixtures; the beams are soft haze light, not lasers; every seat filled with real people.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot on a 30-foot broadcast jib with a 24 mm lens. Image 1 = the real awards hall (architecture and stage only).
0-2 s: the jib starts high above the back rows and sweeps down and forward over the heads of the audience; warm house lights dim to half.
2-4.5 s: a lighting cue: a row of real moving-head spotlights tilts up from the stage floor, beams visible in light haze; the audience murmurs and settles.
4.5-6 s: the jib lands at stage height behind the front rows; the stage glows warm white, the giant LED screen behind it shows only a soft dark-blue gradient.
Every seat filled with real black-tie guests of varied ages, ethnicities and hairstyles, moving naturally (whispering, adjusting jackets, a phone lowered); no empty seats, no repeated faces, no rows of identical figures, no mannequins.
STYLE: real broadcast camera, natural grain, light haze, practical stage lights, real fabric and skin, natural grade. No CG look, no text, no logos, no lens-flare streaks.
AUDIO: no music, no score, no soundtrack, no drum hits; only a large hall murmur, seats creaking, a few coughs, the hum of the lights.
```

### R02 — Backstage wings, ten seconds to air
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_HOST.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/host_face.jpg
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_COHOST.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/cohost_face.jpg
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R02.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Three people and one line on a visible face. Low risk. **Change:** Audio line normalised.
- **If < 9 →** `The stage manager faces the camera 3/4 and her lips are clearly visible on "Ten seconds. Have fun."`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous handheld shot, 35 mm, in the dark backstage wings of a gala awards show. Image 1 = the HOST's face (exactly 50, light olive skin, salt-and-pepper hair with a side part, light stubble, hazel eyes), image 2 = his look (midnight-blue velvet tuxedo jacket, black satin lapels, bow tie), image 3 = the CO-HOST's face (exactly 35, warm medium-brown skin, dark hair in a low side bun, diamond studs), image 4 = her look (emerald silk gown, tiny earpiece). Nobody resembles any real TV host or celebrity.
Location: black velour curtains, a cable-taped floor, a lighting rig, blue cue lights, a small monitor showing the stage; the bright stage spills in from frame right.
0-2 s: the CO-HOST presses her earpiece and smooths her gown; the HOST shakes out his hands and breathes slowly.
2-4 s: a stage manager (woman, 40s, headset, black clothes, clipboard) faces camera 3/4 and says, lips clearly in sync: "Ten seconds. Have fun."
4-6 s: the HOST and CO-HOST exchange a quick nervous smile, then walk into the light; the camera stays in the wings.
Exactly these 3 people, no duplicates. STYLE: real skin with pores, real velvet and silk, practical blue cue lights, film grain, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only muffled hall applause through the curtain, headset chatter, footsteps, the stage manager's line.
```

### R03 — Broadcast camera operator in the aisle
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_HOST.png
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: The host is small in the background (identity loose, acceptable). Crowd shot: never attach a PV. **Change:** Removed the PV.
- **If < 9 →** `The operator in the foreground is sharp; the host on stage is the HOST of image 2 in the velvet tux; every seat filled.`
```
Live-action documentary footage of a real televised awards show, 5 seconds, ONE continuous shot, 50 mm, slow lateral dolly. Image 1 = the awards hall, image 2 = the HOST (midnight-blue velvet tuxedo), seen small on stage.
0-2.5 s: in the foreground, a broadcast camera operator (man, 40s, black clothes, headset) works a large studio camera on a pedestal in the side aisle, zooming with his right hand, red tally light on; his face lit by the viewfinder.
2.5-5 s: the camera dollies past him to reveal the stage in the background: the HOST at the glass podium in a warm spotlight, gesturing; between them, rows of guests in black tie, heads and shoulders soft in the foreground.
Every seat filled with real guests of varied ages and ethnicities, no empty seats, no repeated faces, no mannequins. Real cables on the aisle carpet, gaffer tape.
STYLE: real broadcast production, natural grain, haze in the stage light, real skin and fabric, no CG look, no readable text, no logos.
AUDIO: no music, no score, no soundtrack; only the HOST's distant voice through the PA (unintelligible), audience laughter, the camera's pan-head creak, headset chatter.
```

### R04 — Nominee row, the glance Aurelia ignores
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R04.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: At 200 mm, both faces must stay sharp. Low risk. **Change:** Audio normalised.
- **If < 9 →** `Both faces sharp in the same focal plane; she never looks at him.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 200 mm long lens from the side of the hall, shallow depth of field, slight operator drift. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, dark brown hair in a low bun, tiny gold flake on her left cheekbone), image 3 = the hall. Nobody resembles any real actor or celebrity.
WARDROBE: ATLAS wears ONLY a midnight-navy tuxedo, black satin lapels, black bow tie. AURELIA wears ONLY a champagne satin one-shoulder gown and a gold cuff.
0-2 s: they sit side by side in the third row, faces lit by the warm stage spill; she watches the stage, still.
2-4.5 s: ATLAS glances at her, smiles hopefully, leans slightly toward her; she keeps her eyes on the stage, one eyebrow lifts a millimetre.
4.5-6 s: he straightens his bow tie and looks back at the stage, pretending nothing happened; guests behind them out of focus.
Exactly one of each, no lookalikes. STYLE: real skin with pores, satin highlights, natural grain, no CG, no text.
AUDIO: no music, no score, no soundtrack; only the hall's hush, the HOST's distant PA voice, a cough.
```

### R05 — Pip's family, suspense before the envelope
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FAM_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: FAM_PIP is a 3-person sheet, so only these 3 must appear. Crowd: no PV. **Change:** Removed the PV; locked to exactly three family members.
- **If < 9 →** `Exactly the three family members of image 1; the boy has red curls and a missing front tooth.`
```
Live broadcast footage of a real gala awards ceremony, 5 seconds, ONE continuous shot, 135 mm long lens, slow push-in. Image 1 = Pip's family (mum: curly copper hair, red glasses, turquoise beads, emerald velvet dress; dad: big ginger-white beard, tuxedo, tweed flat cap held in his lap; brother about 8: red curls, missing front tooth, tuxedo, gold bow tie), image 2 = the hall. Nobody resembles any real person. Exactly these three family members, no duplicates.
0-2 s: the three sit in a middle row, warm stage spill on their faces; the mum grips the dad's hand, knuckles white; the boy crosses the fingers of both hands and squeezes his eyes shut.
2-5 s: the dad whispers something to the boy and the boy nods fast; the mum holds her breath, lips pressed, eyes fixed on the stage.
Guests around them in black tie, softly out of focus, every seat filled, varied faces, no repeats, no mannequins.
STYLE: real skin with pores and freckles, velvet texture, natural grain, practical light, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only a tense hush, the paper of an envelope tearing far away through the PA, one cough.
```

### R06 — Best Short Film win: confetti cue over the cast row
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: Gala looks for Pip and Nova have no image ref (text lock only; Yacine to approve the plum and the black jumpsuit). Confetti could sparkle. Crowd: no PV. **Change:** Removed the PV.
- **If < 9 →** `Confetti is matte paper falling with gravity; Pip in plum velvet, Nova in a black satin jumpsuit, faces as images 1-2.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 24 mm on a broadcast jib rising over the cast row. Image 1 = PIP's face (exactly 30, long curly copper-red hair, dense freckles, cyan butterfly clip), image 2 = NOVA's face (mid 20s, deep brown skin, short platinum-blonde curly crop, winged liner, small gold hoops), image 3 = the hall. Nobody resembles any real actor or celebrity.
WARDROBE: PIP wears ONLY a deep plum velvet long-sleeve midi dress. NOVA wears ONLY a black satin wide-leg jumpsuit with a deep V and gold hoops.
0-1.5 s: already mid-eruption: the row jumps to its feet; PIP screams with joy, both hands on her head.
1.5-4 s: real confetti cannons fire from the stage edge: thousands of small matte gold and white paper squares drift down through the warm spotlights; PIP and NOVA hug, bouncing.
4-6 s: the jib rises above them to show the whole hall standing and applauding under falling confetti.
Every seat filled with real guests of varied ages and ethnicities, no repeated faces, no mannequins. Confetti is real paper with gravity, no sparkles.
STYLE: broadcast camera, grain, haze, practical lights, real fabric, no CG, no text, no logos, no lens-flare streaks.
AUDIO: no music, no score, no soundtrack; only a roar of applause and cheers, two confetti-cannon pops, PIP's scream.
```

### R07 — Pip's family crying with pride
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FAM_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 8/10. Risks: The boy's line "That's my sister!" was only in the AUDIO list (off-screen line risk). 3 actions in 5 s. **Change:** The line is now on the boy's visible face; removed the PV.
- **If < 9 →** `The boy faces the camera 3/4 when he shouts, lips clearly in sync.`
```
Live broadcast footage of a real gala awards ceremony, 5 seconds, ONE continuous handheld shot, 85 mm, close on Pip's family. Image 1 = Pip's family (mum: curly copper hair, red glasses, turquoise beads, emerald velvet dress; dad: big ginger-white beard, tuxedo, tweed flat cap in hand; brother about 8: red curls, missing front tooth, gold bow tie), image 2 = the hall. Nobody resembles any real person.
0-2 s: all three are on their feet; the mum cries with pride, lifting her glasses to wipe a real tear with a knuckle, laughing at the same time.
2-3.5 s: the dad waves his flat cap high in the air and whistles with two fingers.
3.5-5 s: the boy stands on his seat, faces the camera 3/4, points at the stage and shouts, lips clearly in sync, gap-toothed grin: "That's my sister!"; the dad steadies him with one hand.
Small matte gold paper confetti drifting in the light. Guests around them clapping, varied faces, no repeats.
STYLE: real tears on real skin with pores, freckles, velvet, natural grain, practical stage light, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only applause, the dad's whistle, the mum's laughing sob, the boy's shouted line.
```

### R08 — Video village: "That's the one."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_C_flow_nbpro_v2_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_D_flow_nbpro_v2_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R08.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5/10. Risks: An off-screen "Cut!" in the audio (no visible speaker). The monitor image of a wire flight is fine. **Change:** Replaced the off-screen "Cut!" with crew murmur.
- **If < 9 →** `The director turns 3/4 to camera for "That's the one."; his face is fully visible.`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous handheld shot, 35 mm, at the video village of a big film set. Image 1 = the DIRECTOR (crew member from image 1: keep the face and clothes), image 2 = the SCRIPT SUPERVISOR (from image 2). Nobody resembles any real person.
Location: a black pop-up tent beside a huge green-screen stage; three monitors on a cart with sun hoods, director's chairs, a walkie on the table, tangled cables, half-drunk coffee cups.
0-2.5 s: over their shoulders, the main monitor shows a man in a grey mocap suit flying on a wire across green screen; the director leans in, headphones on one ear.
2.5-4.5 s: the take ends; the director slaps the table, turns to the script supervisor, faces camera 3/4 and says, lips in sync: "That's the one."
4.5-6 s: she laughs and writes a note in her binder (no readable text).
Real monitor glow on faces, the soft daylight of the stage doors behind. No duplicates.
STYLE: real skin with pores, real fabric, natural grain, practical monitor light, no CG look, no readable text, no logos.
AUDIO: no music, no score, no soundtrack; only stage ambience, walkie chatter, distant crew murmur, the director's line, a laugh.
```

### R09 — Steadicam operator backing through the green stage
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_RIG1_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R09.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5/10. Risks: "Watch the cable." is an off-screen or back-turned line. 3 people moving. **Change:** Removed that line from the audio.
- **If < 9 →** `Pip runs toward the lens and her face is readable; the operator walks backward smoothly.`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous shot, 28 mm handheld following from the side. Image 1 = the STEADICAM OPERATOR and his rig (keep his face and the rig), image 2 = PIP's face (exactly 30, long curly copper-red hair, dense freckles, cyan butterfly clip). Nobody resembles any real actor.
WARDROBE: PIP wears ONLY a grey mocap suit with white ball markers. The operator wears a black Steadicam vest and arm with a cinema camera.
Location: a huge green-screen stage, green floor with white tape crosses, a light grid overhead, softboxes, a grip in a black t-shirt.
0-3 s: the operator walks backward fast, gliding, framing PIP who runs toward him with her arms pumping; a grip walks behind him with one hand flat on his back to guide him.
3-6 s: PIP stops on her mark and bends over laughing, out of breath; the operator lowers the rig and grins.
Exactly one PIP, no duplicates, nobody standing still in rows.
STYLE: real skin with sweat sheen, real green-screen spill on skin, natural grain, practical overhead lights, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only footsteps on the stage floor, the rig's soft clicks, PIP's breathing and laugh
```

### R10 — Focus puller, marks and a rack to Aurelia
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_E_flow_nbpro_v2_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R10.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5/10. Risks: "Rolling!" from an unseen 1st AD is an off-screen line. **Change:** Replaced it with a stage bell.
- **If < 9 →** `A real optical rack focus: the focus puller is sharp first, then Aurelia sharp, with the gold flake on her cheek.`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous shot, 50 mm, slow push past the camera. Image 1 = the FOCUS PULLER (keep his face and clothes), image 2 = AURELIA's face (early 30s, olive-light skin, dark brown hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: AURELIA wears ONLY a grey mocap suit with white ball markers and a lanyard.
0-2.5 s: close on the focus puller's hands turning a wireless follow-focus wheel with white tape marks drawn in marker; he glances between the cinema camera and the actress.
2.5-6 s: the shot racks focus over his shoulder to AURELIA, 3 m away on a coloured tape mark on the green floor; she runs her line silently, then rolls her shoulders, waiting.
Location: green-screen stage, a cinema camera on a dolly, a matte box, an LED panel on a stand, real cables.
STYLE: real skin with pores, real metal and rubber on the gear, real optical rack focus with breathing, natural grain, no CG, no readable text, no logos.
AUDIO: no music, no score, no soundtrack; only stage ambience, a stage bell ringing once far away, the follow-focus clicks.
```

### R11 — Wire rig rehearsal with the stunt coordinator
- **Duration:** 7 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_RIG2_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R11.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5/10. Risks: The coordinator is not in the refs while image 2 is the rigging crew (Seedance may give her a rigger's face). 3 beats. **Change:** States that she is a different person from the riggers.
- **If < 9 →** `The coordinator faces camera 3/4 for the count; the cable is visible; Atlas rises only 1 m.`
```
Live-action behind-the-scenes documentary footage, 7 seconds, ONE continuous handheld shot, 35 mm. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = the RIGGING CREW (keep faces and gear). Nobody resembles any real actor.
WARDROBE: ATLAS wears ONLY a grey mocap suit with white ball markers and a black stunt harness with steel rings.
Location: a green-screen stage, a black truss overhead with pulleys, two riggers holding a rope, crash mats on the floor.
0-3 s: the STUNT COORDINATOR (a different person from the riggers: woman, 40s, black cap, headset) checks the carabiner on ATLAS's back with a hard tug, faces camera 3/4 and says, lips in sync: "On three. One, two, three."
3-5.5 s: the riggers pull together; ATLAS lifts 1 m off the mat, wobbling, arms out, and laughs nervously; the cable is clearly visible.
5.5-7 s: he gives a shaky thumbs-up; the coordinator lowers him with a hand signal.
Exactly one ATLAS. Real cable tension, real body weight.
STYLE: real skin with pores, real nylon webbing and steel, natural grain, practical overhead light, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the pulley squeak, the rope, ATLAS's laugh, the coordinator's count.
```

### R12 — Mocap markers applied to Pip's face
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R12.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: The technician's face is "at the edge of frame" while she speaks (weak lip-sync). Mirror out of frame (good). **Change:** Her face is now visible 3/4 beside Pip and the line is on camera.
- **If < 9 →** `The technician's face is fully visible beside Pip when she says "Don't you dare."`
```
Live-action behind-the-scenes documentary footage, 5 seconds, ONE continuous shot, 85 mm close-up, slight handheld drift. Image 1 = PIP's face (exactly 30, long curly copper-red hair pulled back under a wig cap, dense freckles, cyan butterfly clip). Nobody resembles any real actor.
WARDROBE: PIP wears ONLY a grey mocap suit with white ball markers and a lanyard.
Location: a makeup trailer, a mirror edged with round bulbs (the mirror is out of frame), brushes in a jar, a tray of tiny white tracking dots.
0-2.5 s: a mocap technician's gloved hand (woman, 50s, reading glasses, her face clearly visible in 3/4 beside PIP) places a tiny white dot on PIP's chin with tweezers; PIP holds very still, eyes crossed trying to look at it.
2.5-5 s: PIP's nose twitches; she fights a sneeze and bursts into giggles; the technician laughs and says on camera, lips clearly in sync: "Don't you dare."
Exactly one PIP, no mirror reflections, no duplicates.
STYLE: real freckled skin with pores, peach fuzz, warm bulb light, natural grain, no CG, no plastic skin, no text, no logos.
AUDIO: no music, no score, no soundtrack; only trailer hum, tweezers clicks, PIP's giggle, the technician's line.
```

### R13 — Atlas tries to impress: the foam column
- **Duration:** 7 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R13.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Three people and a sight gag. Low risk. **Change:** Audio normalised.
- **If < 9 →** `The props assistant carries the column under ONE arm; the column bends slightly like foam.`
```
Live-action behind-the-scenes documentary footage, 7 seconds, 2 shots, hard cut at 4.5 s, handheld 35 mm. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: both wear ONLY grey mocap suits with white ball markers and lanyards.
Location: the edge of a green-screen stage, a props area with painted "marble" columns, a coffee cart.
0-4.5 s (medium wide): AURELIA walks past with a coffee; ATLAS quickly squats and lifts a 2 m white-and-gold marble column onto his shoulder with a huge fake strain, glancing at her to see if she noticed.
4.5-7 s (medium): she does not look; a young props assistant (man, 20s, cap) takes the same column from ATLAS with ONE hand, tucks it under his arm like a pillow and walks away; ATLAS stares at his own hands; AURELIA, now in the background, hides a smile behind her cup.
The column is light foam: it flexes slightly. One of each person, no duplicates.
STYLE: real skin, real fabric, natural grain, practical stage light, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only ATLAS's fake grunt, crew laughter, footsteps.
```

### R14 — Costume department, the armour on the rack
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R14.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: A "sunburst crown" prop reads as a halo (flagged in EDIT_v10). A "radio murmuring" invites music. **Change:** Removed the crown and the radio.
- **If < 9 →** `No crown anywhere; one seamstress; steam in the window light.`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous slow dolly, 50 mm. Image 1 = AURELIA's film costume ONLY (gold leaf-feather bodice, champagne satin gown, long cape): it hangs on a dress form; nobody wears it.
Location: a real costume workshop: rolling rails of costumes in garment bags, a cutting table with chalk and pins, a sewing machine, a steamer, a tray of spare gold feathers.
0-3 s: the camera glides along the rail and stops on the gold feather bodice on the dress form; a seamstress (woman, 60s, measuring tape around her neck, glasses on a chain) steams the champagne cape; the steam rises in window light.
3-6 s: she sets the steamer down and, with pliers, bends one gold feather back into line, checks it, and nods to herself.
Real metal feathers with scratches and fingerprints, real satin creases. Exactly one seamstress.
STYLE: soft daylight from a tall window on the left, dust in the air, natural grain, real textures, no CG look, no halo, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the steamer hiss, pliers click, a sewing machine in the background.
```

### R15 — Pip FaceTime: the family's screen up close
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FAM_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R15.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: A phone UI is fine. The boy's line is on the phone screen, lips visible. **Change:** Audio normalised.
- **If < 9 →** `Phone screen fills half the frame; the boy's lips visible on "I drew you!"`
```
Live-action behind-the-scenes documentary footage, 6 seconds, ONE continuous handheld shot, 50 mm, pushing in until the phone screen fills most of the frame. Image 1 = Pip's family (mum: curly copper hair, red glasses, turquoise beads; dad: big ginger-white beard, tweed flat cap; brother about 8: red curls, missing front tooth), image 2 = PIP's face (exactly 30, curly copper-red hair, dense freckles, cyan butterfly clip). Nobody resembles any real person.
WARDROBE: PIP wears ONLY a grey mocap suit with white markers and a lanyard; at home the family wear casual sweaters.
0-2 s: PIP sits in a makeup chair holding her phone up; on the screen, a real video call: the family squeezed into frame in their warm-lit home kitchen.
2-4.5 s: the boy pushes his face close to his camera and holds up a crayon drawing of a red-haired hero; he says on screen, lips visible: "I drew you!"
4.5-6 s: the camera tilts to PIP's face: she laughs with glistening eyes and presses her free hand to her chest.
Slight hand shake, real screen glare and pixels, no readable interface text.
STYLE: real skin with pores and freckles, natural grain, warm practical light, no CG, no logos.
AUDIO: no music, no score, no soundtrack; only the phone's small speaker voices, the family laughing, the boy's line, trailer hum.
```

### R16 — The Gilded City, aerial drone establishing
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  none: text only (do NOT attach KF keyframes; they bring the obelisk back)
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R16.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: "church-like bells" invites a bell tower (the obelisk/tower failure); from a drone, people look miniature (R8). **Change:** Removed the bells; added "no bell tower".
- **If < 9 →** `Fly lower: rooftops fill the frame; no tower of any kind.`
```
Live-action fantasy feature film footage, 8 seconds, ONE continuous aerial drone shot, 24 mm, flying forward and slowly descending.
A real-looking ancient city on a hill by the sea: white marble buildings with gold-leaf domes and gold-trimmed cornices, terracotta roofs between them, narrow streets with real people as tiny moving dots, laundry lines, cypress trees, a wide central square of white marble veined with gold surrounded by a gold colonnade.
0-4 s: the drone flies low over the roofs toward the square; seagulls cross the frame; shadows of clouds slide over the domes.
4-8 s: it tilts down to the square where hundreds of real people walk, stalls with awnings, a fountain.
SKY: real photographic sky: soft overcast morning with a break of sun from frame right, layered grey-white clouds, natural haze toward the sea; no painted sky, no god-rays.
No obelisk, no monument, no tower, no bell tower, no stone slab, no skyscrapers; open sky and distant mountains only.
STYLE: real aerial cinematography, 35 mm film grain, physically correct light, real stone weathering and dirt, real gold with patina (not shiny CG), no CG look, no glow, no lens flare, no text, no logos.
AUDIO: no music, no score, no soundtrack; only wind, distant city crowd, seagulls, waves.
```

### R17 — Square at street level, a real sky
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R17.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Crowd market: risk of repeated extras. The text handles it. **Change:** Audio normalised.
- **If < 9 →** `Pip in the mustard sweater stays the clear subject; extras all different.`
```
Live-action fantasy feature film footage, 6 seconds, ONE continuous Steadicam shot, 28 mm, walking backward in front of PIP. Image 1 = PIP's face (exactly 30, long curly copper-red hair, dense freckles, cyan butterfly clip), image 2 = her costume (mustard knit sweater, light ripped jeans, olive crossbody bag, white sneakers). Nobody resembles any real actor.
WARDROBE: PIP wears ONLY the costume of image 2.
0-3 s: PIP walks through a crowded market on a white marble square veined with gold, eating an apple, dodging a porter carrying a crate of oranges.
3-6 s: she stops, looks up at the gold colonnade and squints at the sky; behind her, real townspeople in simple linen clothes pass, buy bread, argue, a child chases a pigeon.
SKY: real photographic late-afternoon sky, warm sun low from frame left, broken cumulus clouds, long shadows on the marble; no painted sky, no god-rays.
No obelisk, no monument, no tower, no stone slab; open sky and distant mountains only. Crowd: varied faces, ages, clothes, no repeated people, no frozen extras.
STYLE: 35 mm anamorphic, natural grain, real skin with pores, real worn marble with dirt in the joints, no CG look, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the market crowd, footsteps, the apple crunch, pigeons, a cart wheel.
```

### R18 — Aurelia's throne room
- **Duration:** 7 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R18.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 7.5/10. Risks: A "matte gold sunburst crown of thin metal blades" behind her head reads as a halo or rays; "hard shafts with dust" are god-rays. **Change:** Crown removed; sunlight is patches on the floor.
- **If < 9 →** `Plain hair in a low bun, nothing behind her head; sunlight only as patches on the floor.`
```
Live-action fantasy feature film footage, 7 seconds, ONE continuous slow dolly-in on a 40 mm lens down the centre of a throne room. Image 1 = AURELIA's face (early 30s, olive-light skin, dark brown hair in a low bun, tiny gold flake on her left cheekbone), image 2 = her costume (gold leaf-feather bodice, champagne satin gown, long cape, gold gauntlets). Nobody resembles any real actor.
WARDROBE: AURELIA wears ONLY the costume of image 2. No crown, no headdress, nothing behind her head.
Location: a long hall of white marble with gold-veined columns, tall arched windows on the left, a worn red carpet, a throne carved from white stone with gold inlay on three steps; two guards in bronze armour stand still by the doors, far back.
0-4 s: she sits sideways on the throne, legs over the armrest, bored, flipping one gold coin into the air and catching it.
4-7 s: she stops, catches the coin, and slowly looks straight into the lens, unimpressed.
Light: real afternoon sunlight from the windows falling in bright patches on the floor, dust floating in the air, cool fill from the far end; no god-rays painted, no halo, no glow behind her head.
STYLE: 35 mm film, grain, real skin with pores, real metal with scratches, real satin, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the coin flicks, the echo of the hall, wind at the windows.
```

### R19 — Pip and Atlas, the quiet step
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9.5
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_PIP_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R19.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9.5/10. Risks: Two people, a quiet beat. Very low risk. **Change:** Audio normalised.
- **If < 9 →** `Both faces visible in profile 3/4; the apple hand-off is clear.`
```
Live-action fantasy feature film footage, 6 seconds, ONE continuous shot, 50 mm, slow push-in at seated eye level. Image 1 = PIP's face (exactly 30, curly copper-red hair, dense freckles, cyan butterfly clip), image 2 = her costume (mustard knit sweater, ripped jeans, olive crossbody bag), image 3 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 4 = his costume (fitted navy-cobalt suit with flat machined chest and shoulder panels). Nobody resembles any real actor.
Location: wide marble steps at the edge of the square at dusk, a few lit oil lanterns, dust on the steps.
0-3 s: they sit side by side on the steps, tired; his suit is scuffed and dusty, a small cut on his cheekbone. PIP pulls a second apple from her bag and holds it out without looking at him.
3-6 s: he takes it, turns it in his fingers, and they both laugh quietly; she bumps his shoulder with hers.
SKY: real dusk sky, deep blue above, a thin band of orange on the horizon, no painted sky.
No obelisk, no tower, no glow on his hands or suit. Exactly one of each.
STYLE: 35 mm, grain, real skin with pores, real dust, warm lantern practicals, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only distant city murmur, crickets, a lantern's flame, their soft laugh.
```

### R20 — Victory: Atlas flies over the city, Aurelia kneels below
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ATLAS_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_AURELIA_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R20.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: A top-down far shot makes Aurelia a tiny figure (miniature look); horizontal flight risks a stiff hover (H3); the gold arm should reach the shoulder at the end. **Change:** Shot 2 is now a high 3/4 crane; gold to the shoulder.
- **If < 9 →** `Shot 1: real motion blur and wind on him; shot 2: a high 3/4 angle with Aurelia readable, cape spread.`
```
Live-action fantasy feature film footage, 8 seconds, 2 shots, hard cut at 4 s. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 2 = his costume (fitted navy-cobalt suit with flat machined panels; his right arm is solid polished gold metal from fingers to shoulder), image 3 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her cheekbone), image 4 = her costume (gold feather bodice, champagne gown, cape). Nobody resembles any real actor.
0-4 s (aerial, 35 mm, camera flying alongside him): ATLAS flies forward over the gold-domed rooftops at sunset, body horizontal, suit fabric rippling in the wind, hair blown back; real motion blur only.
4-8 s (high three-quarter crane, 35 mm, slowly rising): far below on the white marble square, AURELIA kneels alone, cape spread on the stone; her sunburst crown lies broken in metal pieces around her; the small shadow of ATLAS passes over her.
SKY: real sunset: low sun from frame right, orange-to-violet gradient, scattered clouds lit from below; no god-rays, no painted sky.
No glow, no energy, no light trail, no halo, no obelisk, no tower, no monument; open sky and distant mountains only.
STYLE: 35 mm film, grain, physically correct light, real metal and stone, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only strong wind, cloth flapping, a distant crowd starting to cheer.
```

### R21 — The team looks up at the real sky
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_NOVA_HERO_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_BLAZE_HERO_flow_nbpro_v1_OK.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CAST_ORION_HERO_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R21.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Four people, but passive and mostly from behind. Image 1 is FACE_PIP and images 2-4 are CAST sheets (they include faces). **Change:** Audio normalised.
- **If < 9 →** `Backs to camera, then all four readable from above; exactly one of each.`
```
Live-action fantasy feature film footage, 6 seconds, ONE continuous shot, 35 mm, slow crane up from behind four people. Image 1 = PIP (exactly 30, curly copper-red hair, freckles, cyan clip, mustard knit sweater, ripped jeans), image 2 = NOVA (mid 20s, deep brown skin, platinum crop, gold hoops, navy satin bomber with a crimson phoenix on the back, black cargo pants), image 3 = BLAZE (28, dark curly hair, short beard, black sleeveless hooded vest, crimson hand wraps, headphones around the neck), image 4 = ORION (about 65, East Asian, short grey hair, round metal glasses, long charcoal cable-knit cardigan coat). Nobody resembles any real actor.
0-3 s: the four stand on the marble square, backs to camera, dusty and tired, looking up; BLAZE drapes an arm over NOVA's shoulders.
3-6 s: the camera rises over them: a small dark figure crosses the sky far away; PIP raises both fists; ORION smiles and polishes his glasses.
SKY: real photographic sunset: overcast lifting, warm light leaking under a grey cloud deck, natural gradient; no god-rays, no painted sky.
No obelisk, no tower, no monument; open sky and distant mountains only. Exactly one of each.
STYLE: 35 mm anamorphic, grain, real fabric and dust, no CG look, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only wind, distant cheering, PIP's whoop.
```

### R22 — Standing ovation after the film
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: Crowd from hall_t4, everyone moving differently. Low risk. **Change:** Audio normalised.
- **If < 9 →** `Every seat filled, everyone moving differently; no empty seats.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 24 mm from the stage edge looking out over the audience, slow push back. Image 1 = the real awards hall.
0-2 s: the giant screen's light fades on the audience's faces; a beat of stunned silence; a woman in row two slowly puts her hand over her heart.
2-4 s: applause starts in pockets and spreads; people rise row by row.
4-6 s: the whole hall stands: real people of varied ages and ethnicities, some clapping above their heads, an older man wiping his eyes, two friends hugging, a young man filming on his phone.
Every seat filled, then everyone standing; no empty seats, no repeated faces, no rows of identical figures, no mannequins, everyone moving differently.
STYLE: broadcast camera, natural grain, warm house lights rising, haze, real fabric and skin, no CG look, no text, no logos, no lens-flare streaks.
AUDIO: no music, no score, no soundtrack; only silence turning into a building roar of applause, cheers, whistles.
```

### R23 — "I'd seen it already… but I hadn't realised until now."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: Two strangers, one line on a visible face. Crowd: no PV. **Change:** Removed the PV.
- **If < 9 →** `Woman A faces camera 3/4, lips clearly in sync.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 85 mm, two-shot of two women in the audience during a standing ovation. Image 1 = the awards hall (background only). Neither woman resembles any real actress or celebrity.
WOMAN A: about 45, light-brown skin, short dark wavy bob, emerald earrings, black velvet dress. WOMAN B: about 60, pale freckled skin, silver hair in a chignon, pearl necklace, navy gown.
0-2 s: both are standing and clapping among the crowd; WOMAN A slows her clapping, eyes wet, still looking at the screen.
2-5 s: she leans to WOMAN B, faces camera 3/4, lips clearly in sync, hands away from her mouth, and says softly: "I'd seen it already... but I hadn't realised until now."
5-6 s: WOMAN B nods slowly, squeezes her arm, and keeps clapping.
Guests around them standing and clapping, out of focus, varied faces, no repeats.
STYLE: real skin with pores, a real tear on mascara, velvet texture, natural grain, warm stage spill, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only loud applause around them, WOMAN A's line clear and close.
```

### R24 — Host's suspense before Best Actor (side angle)
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_HOST.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/host_face.jpg
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_COHOST.png
  4. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/cohost_face.jpg
  5. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R24.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Two presenters; lips closed (good, no line). Low risk. **Change:** Audio normalised.
- **If < 9 →** `Exactly two presenters; the envelope has no readable text.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 135 mm long lens from the side of the stage, profile two-shot, very slow push. Image 1 = the HOST's face (exactly 50, light olive skin, salt-and-pepper hair, side part, light stubble, hazel eyes), image 2 = his look (midnight-blue velvet tuxedo jacket, black satin lapels, bow tie), image 3 = the CO-HOST's face (exactly 35, warm medium-brown skin, dark hair in a low side bun, diamond studs), image 4 = her look (emerald silk gown, tiny earpiece), image 5 = the hall. Nobody resembles any real TV host.
0-2 s: the HOST holds a sealed cream envelope against his chest with both hands and looks out over the audience, smiling, saying nothing.
2-4.5 s: the CO-HOST leans in and whispers in his ear; he shakes his head slowly with a playful smile, making the hall wait.
4.5-6 s: he slides one finger under the flap; the CO-HOST presses her palms together.
Exactly two presenters, no duplicates, no readable text on the envelope. Lips closed while waiting.
STYLE: real broadcast camera, grain, haze in the white spotlight, real velvet and silk, real paper, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack, no drum roll; only a total hush, a single cough, the envelope paper.
```

### R25 — "...Atlas!" — his frozen reaction
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R25.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: 3 characters, but only Atlas acts (the others react). Low risk. **Change:** Audio normalised.
- **If < 9 →** `Atlas sharp and centred; Orion and Aurelia one each.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous shot, 200 mm long-lens close-up on ATLAS in his seat, shallow depth of field. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her left cheekbone), image 3 = ORION's face (about 65, East Asian, short grey hair, round thin metal glasses). Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo, black satin lapels, bow tie. AURELIA: champagne satin one-shoulder gown, gold cuff. ORION: black tuxedo.
0-2 s: the hall erupts; ATLAS is frozen, mouth slightly open, not believing it.
2-4 s: ORION, behind his shoulder, grips it and shakes it, laughing; ATLAS exhales, puts a hand flat on his chest.
4-6 s: in the soft foreground, AURELIA turns her head and looks at him for a long second, surprised, lips parted.
Exactly one of each, no lookalikes.
STYLE: real skin with pores, the glasses catching the spotlight, natural grain, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only a roar of applause and cheers, ATLAS's shaky breath.
```

### R26 — Atlas's mother and sister stand up
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FAM_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: FAM_ATLAS sheet. Crowd: no PV. **Change:** Removed the PV.
- **If < 9 →** `Exactly the mother and the sister from image 1; the cane is real.`
```
Live broadcast footage of a real gala awards ceremony, 5 seconds, ONE continuous handheld shot, 85 mm. Image 1 = Atlas's family: his MOTHER (about 82, white bob, glasses, black velvet jacket, silver bird brooch, wooden cane) and his SISTER (about 50, long grey-brown hair, navy sleeveless gown). Image 2 = the hall. Nobody resembles any real person.
0-2.5 s: the MOTHER pushes herself up from her seat with her cane; the SISTER jumps up to steady her elbow, laughing and crying.
2.5-5 s: standing, the MOTHER lifts her cane high in the air like a trophy, chin trembling, eyes shining; the SISTER claps with her hands above her head.
Guests around them standing and applauding, varied faces, no repeats, no empty seats.
STYLE: real aged skin with pores and wrinkles, a real tear, velvet texture, warm stage spill, natural grain, no CG, no plastic skin, no text, no logos.
AUDIO: no music, no score, no soundtrack; only applause, the SISTER's laugh-sob, the cane tapping the seat.
```

### R27 — Steadicam follows the winner down the aisle
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: 8 s Steadicam through a crowd: risk of repeated faces. Crowd: no PV. **Change:** Removed the PV.
- **If < 9 →** `Every guest different; Atlas in the navy tux, glasses on.`
```
Live broadcast footage of a real gala awards ceremony, 8 seconds, ONE continuous Steadicam shot, 28 mm, following behind and then beside ATLAS. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = the hall. Nobody resembles any real actor.
WARDROBE: ATLAS wears ONLY a midnight-navy tuxedo, black satin lapels, black bow tie.
0-3 s: ATLAS walks down the centre aisle toward the bright stage; guests reach out from the rows: a handshake, a pat on the back, a woman squeezes his arm.
3-6 s: the Steadicam swings around to his side: he laughs, overwhelmed, wipes one eye under his glasses with a knuckle.
6-8 s: he climbs the five stage steps, buttoning his jacket; the white spotlight catches him.
Audience standing on both sides, all different real people, no repeated faces, no mannequins.
STYLE: broadcast camera, grain, haze in the spotlight, real skin with pores, real satin lapels, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only applause and cheers, footsteps on the carpet, then on the wooden steps.
```

### R28 — The trophy hand-off, hands shaking
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_COHOST.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/cohost_face.jpg
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R28.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Macro hands plus a trophy design lock. Low risk. **Change:** Audio normalised.
- **If < 9 →** `Exactly one trophy: a crystal spire inside a gold ring on a black base.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, 2 shots, hard cut at 3 s. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 2 = the CO-HOST's look (emerald silk gown, tiny earpiece), image 3 = her face (exactly 35, warm medium-brown skin, low side bun, diamond studs). Nobody resembles any real person.
WARDROBE: ATLAS: midnight-navy tuxedo, black satin lapels, bow tie.
0-3 s (100 mm macro insert): the CO-HOST's hands pass the trophy into ATLAS's hands: a slim faceted crystal spire set inside a polished gold ring, on a black stone base. His fingers tremble visibly; he grips it tighter; the crystal throws small real reflections.
3-6 s (50 mm medium): he holds it with both hands, looks down at it, then up at the hall, breathes out a laugh; the CO-HOST kisses his cheek and steps back, clapping.
Exactly one trophy, one ATLAS, one CO-HOST. The trophy has weight; no floating.
STYLE: real skin with veins and pores on the hands, real crystal and gold, white spotlight, grain, no CG, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only applause dropping to murmurs, his breath, the base touching the podium glass.
```

### R29 — The speech: "Three months I trained to impress one person."
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9.5
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/podium_back.jpg
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R29.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9.5/10. Risks: One line on a visible face. Very low risk. **Change:** Audio normalised.
- **If < 9 →** `Face fully visible, lips clearly in sync, the trophy steady against his chest.`
```
Live broadcast footage of a real gala awards ceremony, 8 seconds, ONE continuous shot, 85 mm close-up from the front, very slow push-in. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = the glass podium. Nobody resembles any real actor.
WARDROBE: ATLAS wears ONLY a midnight-navy tuxedo, black satin lapels, black bow tie; he holds the trophy (crystal spire inside a gold ring, black base) against his chest.
0-1.5 s: he stands at the glass podium, swallows, the trophy trembling slightly; the hall is silent.
1.5-6.5 s: he faces camera 3/4, face fully visible, lips clearly in sync, hands away from his mouth, and says slowly: "Three months I trained to impress one person. I hope it worked."
6.5-8 s: he looks off to his right, into the audience, searching for someone, a nervous half-smile.
STYLE: real skin with pores, a wet glint in his eyes, white key spotlight with warm edge, haze, grain, no CG, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the hall's silence, his voice through the PA with a slight room echo, then scattered "aww" and laughter.
```

### R30 — From the podium: Aurelia, impressed for the first time
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/vref/hall_t4.jpg
- **Motion ref:** none. This is a crowd shot: NEVER attach a previs here (it brings back the grey dummy audience).
- **Original score:** 9/10. Risks: Rack focus to Aurelia among the guests. Crowd: no PV. **Change:** Removed the PV.
- **If < 9 →** `Rack focus lands on her face; exactly one Aurelia, in the champagne gown.`
```
Live broadcast footage of a real gala awards ceremony, 6 seconds, ONE continuous over-the-shoulder shot from behind ATLAS at the podium, 135 mm, with a rack focus. Image 1 = ATLAS's face (seen only as his back, silver hair and the edge of his glasses), image 2 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her left cheekbone), image 3 = the hall. Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo. AURELIA: champagne satin one-shoulder gown, gold cuff on her right wrist.
0-2 s: ATLAS's shoulder and silver hair sharp in the foreground; the audience in soft focus.
2-6 s: the focus racks to AURELIA in the third row: she slowly stands, alone for a second among seated guests; she presses her lips together, looks at him for the first time with real admiration, gives one small nod, then starts to clap slowly; a tear catches the light.
Exactly one AURELIA, no lookalikes. Guests around her varied, no repeats.
STYLE: real optical rack focus, grain, haze in the spotlight, real satin, real skin, no CG, no halo, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only a quiet hall, then her slow claps joined by the audience.
```

### R31 — Rooftop wide, the city behind
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R31.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Two people plus a waiter; no bottle (good). **Change:** Audio normalised.
- **If < 9 →** `Only two wine glasses, two dessert plates and one candle on the table; no bottle.`
```
Live-action romantic film footage, 6 seconds, ONE continuous shot, 35 mm, slow lateral dolly along the parapet. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo, bow tie loosened. AURELIA: champagne satin one-shoulder gown, gold cuff. NEVER the film armour.
Location: a real restaurant rooftop at night, one small round table with a white cloth, ONE candle in a glass, two wine glasses, two dessert plates, warm string lights overhead, potted olive trees; behind them a real city skyline as soft bokeh.
0-3 s: a waiter (man, 50s, white jacket) pours red wine into her glass and leaves frame.
3-6 s: they sit facing each other in profile; she listens with her chin on her hand; he talks with his hands; the camera keeps sliding.
Exactly these 3 people, no other diners. No water bottle.
STYLE: real 35 mm night photography, fast lens, creamy bokeh, candle and string lights as the only key, grain, real skin, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only city traffic far below, wind, the wine pour, cutlery.
```

### R32 — Atlas close-up: "What an irony…"
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R32.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: A long line (22 words). The same line already STT-verified in IF_DATE. **Change:** Audio normalised.
- **If < 9 →** `Split delivery is OK: keep his face 3/4 with lips visible the whole time.`
```
Live-action romantic film footage, 8 seconds, ONE continuous shot, 85 mm close-up over AURELIA's soft shoulder, slow push-in. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble). Nobody resembles any real actor.
WARDROBE: midnight-navy tuxedo, black satin lapels, bow tie loosened.
Location: night rooftop, one candle between them, warm string lights, city bokeh behind him.
0-1 s: he turns his wine glass by the stem, smiling to himself.
1-7.5 s: he looks up at her, faces camera 3/4, lips clearly in sync, hands away from his mouth, and says with a dry smile: "What an irony... I had to punch you in the face for you to accept a date, and to finally be impressed."
7.5-8 s: he raises an eyebrow, waiting.
In the foreground: the blurred edge of her champagne satin shoulder and her dark bun (no face).
STYLE: real skin with pores and stubble, candlelight flicker on the glasses, grain, shallow focus, no CG, no glow, no text, no logos.
AUDIO: no music, no score, no soundtrack; only distant city traffic, a light wind, his voice close.
```

### R33 — Reverse OTS on Aurelia: "…Okay. You finally got me."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9.5
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R33.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9.5/10. Risks: A replacement for HF_DATE_t1 with the correct gown. Nothing near her mouth (good). **Change:** Audio normalised.
- **If < 9 →** `Hands on the table while she speaks; champagne one-shoulder gown.`
```
Live-action romantic film footage, 6 seconds, ONE continuous shot, 85 mm over ATLAS's soft shoulder (midnight-navy tuxedo, silver hair at the edge of frame) onto AURELIA. Image 1 = AURELIA's face (early 30s, olive-light skin, dark brown hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: champagne satin one-shoulder gown, gold cuff on her right wrist.
Location: night rooftop, one candle, warm string lights, city bokeh.
0-2.5 s: she bursts out laughing, eyes filling with tears from laughing, leaning back; she wipes under one eye with a fingertip.
2.5-5.5 s: she lowers her hands to the table, faces camera 3/4, face fully visible, lips clearly in sync, and says, still laughing near tears: "...Okay. You finally got me."
5.5-6 s: she shakes her head, smiling.
Nothing near her mouth while she speaks.
STYLE: real skin with pores, glistening eyes, candlelight on satin, grain, shallow focus, no CG, no halo, no text, no logos.
AUDIO: no music, no score, no soundtrack; only her laugh, the city far below, her line close.
```

### R34 — Two-shot laughing, the boom dips in
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R34.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8.5/10. Risks: The "grey fluffy boom" can render as a strange creature or blob. **Change:** Described as a real boom microphone.
- **If < 9 →** `If the boom still looks odd, drop beat 3 and end on the pull-back.`
```
Live-action film footage, 6 seconds, ONE continuous shot, 40 mm, slow crane back and up from the table. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, tortoise rectangular glasses, short grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, dark hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo, bow tie loosened. AURELIA: champagne satin one-shoulder gown, gold cuff.
0-3 s: both laugh, clink their wine glasses over the single candle, city bokeh behind.
3-5 s: the camera keeps pulling back and up; the city lights look perfect.
5-6 s: a real boom microphone in a grey furry windshield on a black telescopic pole dips into the top of the frame by mistake and quickly lifts out again.
Exactly one of each, no other diners, no water bottle.
STYLE: real night photography, string lights and candle as the only key, grain, bokeh, real fabric and skin, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only their laughter, the glass clink, city ambience, a tiny bump of the boom pole.
```

### R35 — "Cut!" — the rooftop is a set
- **Duration:** 7 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/CREW_C_flow_nbpro_v2_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R35.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: "about 20 crew members" is the REVEAL failure (extras like mannequins, lookalikes); 3 beats with a fast crane. **Change:** Crew reduced to about 10, each doing something different.
- **If < 9 →** `About ten crew, all different; exactly one Atlas and one Aurelia.`
```
Live-action behind-the-scenes documentary footage, 7 seconds, ONE continuous shot, 24 mm, a fast crane pull-back. Image 1 = ATLAS's face (exactly 55, silver-grey hair, tortoise glasses, grey stubble), image 2 = AURELIA's face (early 30s, olive-light skin, low dark bun, tiny gold flake on her cheekbone), image 3 = the DIRECTOR (keep his face and clothes). Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo. AURELIA: champagne satin one-shoulder gown, gold cuff.
0-3 s: the camera pulls back from the candlelit table: the rooftop is a small wooden platform with one table, potted olive trees and a string of lights, surrounded by green-screen walls, a light grid, C-stands, sandbags.
3-5 s: the DIRECTOR stands up from his chair at the monitors, faces camera 3/4, lips in sync, and shouts: "Cut!"
5-7 s: the work lights bang on; about ten crew members of varied ages, each doing something different, start clapping and cheering; ATLAS and AURELIA laugh at the table.
Exactly one of each actor, no lookalikes, no mannequins.
STYLE: real skin, real green spill, real stage gear, grain, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only the "Cut!", the clunk of work lights, applause, cheers.
```

### R36 — Pip to camera: "Everything you just saw… isn't real."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9.5
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R36.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9.5/10. Risks: One person, one line to camera. Very low risk. **Change:** Audio normalised.
- **If < 9 →** `Straight to lens, lips clearly in sync.`
```
Live-action behind-the-scenes footage, 6 seconds, ONE continuous handheld shot, 35 mm, PIP walks toward the lens on a green-screen stage. Image 1 = PIP's face (exactly 30, long curly copper-red hair, dense freckles, cyan butterfly clip). Nobody resembles any real actor.
WARDROBE: PIP wears ONLY a deep plum velvet long-sleeve midi dress and the cyan clip.
Location: a huge green-screen stage, light grid, C-stands, a crew member carrying a foam "marble" column in the background, others coiling cables.
0-2 s: PIP walks up to the camera with a grin, as if letting us in on a secret, stops close in a medium close-up.
2-5.5 s: she faces the camera straight on, face fully visible, lips clearly in sync, hands away from her mouth, and says: "Everything you just saw... isn't real."
5.5-6 s: she raises her eyebrows and bites her lip, holding back a laugh.
Exactly one PIP.
STYLE: real freckled skin with pores, velvet texture, green spill on her hair, practical work lights, grain, no CG look, no text, no logos.
AUDIO: no music, no score, no soundtrack; only stage ambience, crew chatter (unintelligible), PIP's line clear.
```

### R37 — Nova to camera: "Not the hall. Not the crowd. Not even us."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_NOVA_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_BLAZE_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R37.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Two people, a line counted on her fingers. Low risk. **Change:** Audio normalised.
- **If < 9 →** `Nova's face fully visible on the line; Blaze in the background.`
```
Live-action behind-the-scenes footage, 6 seconds, ONE continuous shot, 50 mm, slow push-in. Image 1 = NOVA's face (mid 20s, deep brown skin, short platinum-blonde curly crop, winged liner, small gold hoops), image 2 = BLAZE's face (28, dark curly hair, thick brows, short dark beard, thin silver chain). Nobody resembles any real actor.
WARDROBE: NOVA: black satin wide-leg jumpsuit with a deep V, gold hoops. BLAZE: charcoal suit, black open-collar shirt, no tie, silver chain.
Location: green-screen stage, light grid, a rolling rack of the film costumes behind them, a grip pushing a camera dolly past.
0-1 s: NOVA turns from BLAZE to the camera; BLAZE leans on her shoulder, eating an apple.
1-5 s: NOVA faces camera, face fully visible, lips clearly in sync, and says with a confident smile, counting on her fingers: "Not the hall. Not the crowd. Not even us."
5-6 s: BLAZE pinches his own arm, pretends to be shocked; she laughs.
Exactly one of each.
STYLE: real skin with pores, satin highlights, green spill, grain, no CG, no text, no logos.
AUDIO: no music, no score, no soundtrack; only stage ambience, the apple crunch, NOVA's line clear, their laugh.
```

### R38 — Atlas to camera: "It was made with Impact Factory."
- **Duration:** 6 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ORION_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R38.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9/10. Risks: Two people, one line; the cup lowered (good). **Change:** Audio normalised.
- **If < 9 →** `Cup away from his mouth on the line.`
```
Live-action behind-the-scenes footage, 6 seconds, ONE continuous shot, 50 mm medium close-up, slight handheld. Image 1 = ATLAS's face (exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble), image 2 = ORION's face (about 65, East Asian, short grey hair, round thin metal glasses). Nobody resembles any real actor.
WARDROBE: ATLAS: midnight-navy tuxedo, bow tie undone and hanging, holding the crystal-and-gold-ring trophy loosely by its base. ORION: black tuxedo.
Location: green-screen stage, behind them crew members applauding, a light grid, a camera on a crane.
0-1.5 s: ORION hands ATLAS a paper coffee cup; ATLAS takes it and turns to the camera.
1.5-5 s: ATLAS faces the camera 3/4, face fully visible, lips clearly in sync, cup lowered, and says with a calm smile: "It was made with Impact Factory."
5-6 s: ORION raises his own cup to the lens in a small toast.
Exactly one of each, no lookalikes.
STYLE: real skin with pores, real satin lapels, practical work lights, green spill, grain, no CG, no text on cups, no logos.
AUDIO: no music, no score, no soundtrack; only applause and chatter behind, ATLAS's line clear.
```

### R39 — Aurelia to camera: "Try it — for only ninety-nine cents."
- **Duration:** 5 s · 16:9 · 720p · **Expected score:** 9.5
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R39.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 9.5/10. Risks: One person, one line. Very low risk. **Change:** Audio normalised.
- **If < 9 →** `Straight to lens, hands down.`
```
Live-action behind-the-scenes footage, 5 seconds, ONE continuous shot, 85 mm close-up, the camera static. Image 1 = AURELIA's face (early 30s, olive-light skin, dark brown hair in a low bun, tiny gold flake on her left cheekbone). Nobody resembles any real actor.
WARDROBE: AURELIA wears ONLY the champagne satin one-shoulder gown and a gold cuff on her right wrist.
Location: green-screen stage, softly out of focus behind her: crew in black, a C-stand, the work lights.
0-1 s: she steps into her close-up, tucks a loose strand of hair behind her ear, and looks straight into the lens.
1-4 s: she faces the camera straight on, face fully visible, lips clearly in sync, hands down, and says with a slow, amused smile: "Try it... for only ninety-nine cents."
4-5 s: she winks once and walks out of frame to the right.
Exactly one AURELIA. No halo, no crown.
STYLE: real skin with pores, a 3 mm gold flake catching the light, satin highlights, grain, no CG look, no plastic skin, no text, no logos.
AUDIO: no music, no score, no soundtrack; only soft stage ambience and her line, close and clear.
```

### R40 — Wrap: props out, hugs, the blue light bank
- **Duration:** 8 s · 16:9 · 720p · **Expected score:** 9
- **Refs (upload in this order: image 1, 2, ...):**
  1. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_ATLAS_flow_nbpro_v1_OK.png
  2. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_AURELIA_flow_nbpro_v1_OK.png
  3. https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/flow/FACE_PIP_flow_nbpro_v1_OK.png
- **Motion ref (video, motion only):** https://raw.githubusercontent.com/yassineba-commits/ucr-assets/main/previs/PV_R40.mp4 (optional, only if it exists)
  If the PV URL returns 404 (previs not rendered yet), generate without the video ref using the timed beats. When a PV is attached, paste the MOTION line (see "How to use the refs") as the 2nd line of the prompt.
- **Original score:** 8/10. Risks: Too much in beat 1 (a group hug, grips with a column, the trophy in a case) plus a crane to the grid plus an LED blue flood (may read as beams). **Change:** Beat 1 simplified; the blue described as a flat panel.
- **If < 9 →** `Only the hug and the crew clapping; the blue is a flat wall of LED panels.`
```
Live-action behind-the-scenes documentary footage, 8 seconds, ONE continuous shot, 24 mm, a crane rising from floor level to the lighting grid. Image 1 = ATLAS (exactly 55, silver-grey hair, tortoise glasses, midnight-navy tuxedo), image 2 = AURELIA (early 30s, olive-light skin, low dark bun, champagne one-shoulder gown), image 3 = PIP (exactly 30, curly copper-red hair, freckles, cyan clip, plum velvet dress). Nobody resembles any real actor.
0-3 s: on the green-screen stage, PIP runs in and hugs ATLAS and AURELIA together; around them crew of varied ages clap.
3-6 s: the crane rises: the whole stage below, crew moving naturally, cables, monitors, a coffee cart; nobody stands in a line.
6-8 s: at the grid, a bank of LED panels switches to a deep cobalt blue, a flat, even wall of deep blue panels filling the top of the frame (no beams).
Exactly one ATLAS, one AURELIA, one PIP; no twins, no lookalikes, no mannequins, no strangers in costumes.
STYLE: real stage, grain, practical lights, no CG look, no beams, no lens flare, no text, no logos.
AUDIO: no music, no score, no soundtrack; only cheers, applause, crew laughter, the click of the LED panels switching on.
```

---

## QA SUMMARY
- **88 ready prompts** (F: 48 · R: 40), each expected at ≥ 9.
- **Split (8):** F01, F09, F18, F22, F25, F26, F31, F34 → a/b.
- **Most frequent fixes in FIGHTS:**
  - Nova bomber matching her CAST image (every Nova film prompt).
  - "Air barrier / ripple rings / shockwave" replaced by palm-to-fist contact (F28, F33, F38, F40).
  - The vortex/spiral removed (F39).
  - "Gold beam" renamed a girder (F24).
  - Liquid-gold transformation replaced by cast gold (F29, F30, F32).
  - Mixed locations split (F09, F34).
  - Strike counts cut (F06, F33).
  - Bridge and location bans added everywhere.
- **Expected weakest spots** (if a take misses, use its "If < 9" line):
  - Nova's frozen-rain or frozen-swarm VFX (F02, F07, F15).
  - The butterfly-swarm mass (F14, F18a).
  - The boom-dip gag (R34).
  - Rain in general: keep shots medium or tighter.
