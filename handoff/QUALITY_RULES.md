# UNCROWNED — Seedance 2.5 QUALITY RULES (what gives 9+/10 in THIS project)
Source: 60+ Higgsfield Seedance 2.5 takes of 26 Nov (CLIPS_STATUS, GEN_log, QA_FINAL_v6, EDIT v9/v10), and contact sheets of the 5–7 and 9/10 clips.

## A. What the 9/10 clips have in common
(HF_M17_t2, HF_M05_t4, HF_CER_A2_t1, HF_CER_A1_t4, HF_M18a_t2, HF_M10_t2, HF_M07_t2, HF_DATE_t1, HF_HOST_P2_t1, HF_R6_t4, HF_R1_t2, HF_M20_t1)
1. **One idea per clip.** 1 shot (or at most 2 shots with a hard cut) for 4–5 s. Max 3 shots in 8 s. Every 9/10 BTS clip is a single shot, a single gag (2 tiramisu + 1 broccoli box; coffee + sunflower; one line said to camera).
2. **≤ 2 characters doing an action, ≤ 3 named characters in frame.** Extras are fine only as a background "crowd/crew" that does nothing specific.
3. **Countable props.** "exactly 2 tiramisu, one in front of X, one in front of Y; Z holds ONLY a clear box of broccoli". Numbers and ownership are always followed.
4. **Real places, described by real objects.** "lived-in home kitchen, wood cabinets, fridge with magnets and a child's drawing, pendant lamp" → 9. "studio space" → 8 (concrete set).
5. **Line on camera.** "<WHO> faces camera 3/4, lips clearly visible and in sync, says: "…"" + hands DOWN / nothing near the mouth. Short lines (≤ 12 words per 3 s).
6. **Image refs only for faces + costumes + (clean) location.** No keyframe that carries a prop you do not want (KF_F16 carried the obelisk; the IF_CER_A1 frame carried the dummy audience).
7. **Physical powers = physical consequences.** R6_t4 (9) = "pushed backward into a gold column that crumbles into real stone and dust", energy never drawn. R6_t1 (7.5) = "light spill / heat lane" → neon beam + drawn rings.
8. **Short negative list that names the exact failure**, not a generic one ("NO obelisk, NO tower, NO stone slab", "no beam, no rings"). It works: t2/t3/t4 retakes that named the failure fixed it each time.

## B. The prompt template (fill in order; 90–170 words for 4–5 s, ≤ 230 words for 8 s)
```
[GENRE line] Live-action <fantasy feature film | BTS documentary | live broadcast> footage, <N> seconds, <1 continuous shot | 2 shots, hard cut at X s>, <lens> <camera move>.
[MOTION-REF line, only if a PV_ video is attached] (wording in §D)
[IDENTITY] Image 1 = <NAME>'s face (identity: <age>, <3–4 traits>), image 2 = <NAME>'s costume (<exact costume as in the CAST image>). ... Nobody resembles any real actor or celebrity.
[WARDROBE LOCK] <NAME> wears ONLY <costume>, same in every shot.
[LOCATION + LIGHT] <real place with 3 concrete objects>. <real light: time of day + source + direction>. <sky wording §G>.
[TIMED BEATS] 0–X s: <one action, who, where in frame>. X–Y s: ... (max 3 beats)
[LINE] <NAME> says on camera, lips clearly in sync, face visible: "<line>".
[EXCLUSIONS] (only the ones that apply, §F)
STYLE: 35 mm film, natural film grain, real skin with pores, real fabric, physically correct light, natural grade, no CG look, no text.
AUDIO: no music, no score, no soundtrack; only <listed real sounds> and the spoken line.
```

## C. Shot / character budget
| clip length | max shots | max beats | max characters with an action |
|---|---|---|---|
| 4 s | 2 | 2 | 2 |
| 5 s | 2 | 3 | 2 (3 if one only reacts) |
| 8 s | 3 | 4 | 2 |
| 10 s+ | split it into two prompts (a/b) |
- A fight exchange (strike + block + reaction) counts as 1 beat per ~1.2 s. More than 5 strikes in 8 s = the stiff, wide "stage fight" of rain_t2/t6 (7–8). Keep ≤ 4 strikes per 8 s and frame at medium/medium-wide, not full wide.
- Never ask for two separate locations or a time jump in one prompt.

## D. Motion refs (PV_xx Blender mannequin previs)
- Problem seen: CER_A1_t1/t2/t3 = 5–7 — the ref's grey dummy audience was COPIED. RAIN_t2 (7) followed the ref but became dry, wide and stiff like the previs.
- Use a PV only for **camera path + blocking of ≤ 2 bodies**. Never for crowds, never for a location.
- Exact wording (paste as is, right after the genre line):
  `The video reference is ONLY a timing and camera-path guide built with grey placeholder mannequins in an empty grey space. Copy ONLY its camera movement and the body positions over time. Do NOT copy its look, colours, lighting, set, empty space or figures: every person is a real human actor with real skin, hair and clothes, in the real location described below. No mannequins, no grey figures, no faceless bodies, no dummies anywhere in frame.`
- Repeat the look in the text (location, rain, light) because the ref's look tends to win: describe the real scene in MORE detail when a PV is attached.
- Crowds/audiences: NO video ref. Use a still of a REAL packed audience (vref/hall_t4.jpg) and write "every seat filled with real black-tie guests of varied ages, moving naturally; no empty seats, no repeated faces, no rows of identical figures". (CER_A1_t4 = 9.)

## E. Identity and wardrobe locks
- Image order = the order you name them in the text. Refs: FACE_<NAME>_flow_nbpro_v1_OK.png + CAST_<NAME>_HERO_flow_nbpro_v1_OK.png (film), FACE_ only + wardrobe text (BTS/ceremony).
- **The wardrobe text must describe what is IN the CAST image.** Nova's CAST image is a navy satin bomber with a crimson phoenix on the back, black tee, black cargo pants, black boots — every prompt that said "navy-silver suit" produced the bomber anyway (rain_t1/t3/t6, R2_t3). Use the bomber wording.
- Identity text (paste):
  - ATLAS: exactly 55, swept-back silver-grey hair, dark tortoise rectangular glasses, short grey stubble, light skin. Film costume: fitted navy-cobalt suit with flat machined chest and shoulder panels, black boots. Ceremony: midnight-navy tuxedo, black satin lapels, black bow tie, same glasses.
  - AURELIA: early 30s, olive-light skin, dark brown hair in a low bun, a single tiny 3 mm square gold flake on her left cheekbone. Film costume: gold leaf-feather bodice, champagne satin gown with a long cape, gold gauntlets. Ceremony/date: champagne satin one-shoulder gown, gold cuff bracelet. No halo, no crown of rays.
  - ORION: about 65, East Asian, short grey hair, round thin metal glasses, calm. Costume: long charcoal cable-knit cardigan coat over a grey shirt, black trousers. Ceremony: black tuxedo.
  - PIP: exactly 30, long curly copper-red hair, dense freckles, cyan butterfly hair clip, big smile. Costume: mustard knit sweater, light ripped jeans, olive crossbody bag, white sneakers. BTS: grey mocap suit with markers + lanyard.
  - NOVA: mid 20s, deep brown skin, short platinum-blonde crop, small gold hoops. Costume: navy satin bomber jacket with a crimson phoenix on the back, black tee, black cargo pants, black boots.
  - BLAZE: 28, dark curly hair, thick brows, short beard, silver chain. Costume: black sleeveless hooded vest with leather panels, black joggers, crimson hand wraps, black headphones around the neck, white sneakers.
- Always: "Nobody resembles any real actor or celebrity." The HOST/co-host Soul batch produced a Clooney-like face → masters from Nano Banana Pro only.
- Duplicates: "exactly one <NAME> in frame; no twins, no lookalikes, no reflections of other people". Avoid mirrors entirely (F22 mirror = duplicate Pip twice → dropped).

## F. Powers, fights and contact — physical wording only
| want | write | never write |
|---|---|---|
| gold power | "his right forearm and fist are solid polished gold metal up to the shoulder, reflecting the sun" | "glowing", "energy", "aura", "melts", "liquid gold forms" |
| blast / push | "an invisible shove: dust and her cape blow back, he is thrown backward 3 m into a column that cracks and crumbles into real stone chunks and dust" | "beam", "ray", "light lane", "shockwave ring", "ripple", "heat lane" |
| speed | "a motion-blurred figure, real motion blur only" | "light trail", "streak of light" |
| flight | "lands feet-first, knees bending, dust kicks up" | "hovers", "floats" |
| punch | "his fist lands on <exact target: her raised forearm / his gloves / ribs>, visible contact, spray/dust on impact" and both bodies within 1 m in the same frame | a fist toward the camera with the target off-frame / far away |
| giant scale | "seen from the ground, worm's-eye, the 12 m statue's foot fills the frame" | "colossal glowing" |
- Contact rule: name the target body part, put both fighters in the same frame within arm's reach, and add "no punches into empty air, every strike makes visible contact". (QA C3/C4: air punches.)
- Physics rule: the person HIT moves back, not the striker. Add "the striker stays planted" when needed (rain_t1: kicker flew 10 m).
- Ban drawn VFX: "no beams, no glowing outlines, no drawn rings or ripples, no sparkles, no lens flares, no halo, no rays behind any head, no portal, no vortex" (R1_t3 vortex, R6_t1 beam/rings, final_run halo).
- If Higgsfield flags NSFW on a fight: replace "punch her face / jaw / blood" by "swings at her / his fist stops a hand-width from her face" and "is thrown back", resubmit once.

## G. Sky, light, weather
- Name the light source and direction: "low golden sunset sun from frame left, long shadows", "overcast dusk, cold blue-grey key from behind".
- Location ban that MUST be in every gold-square/bridge/colonnade prompt: `No obelisk, no monument, no tower, no stone slab, no skyscrapers in the background; open sky and distant mountains only.` (R1_t1, R2_t1, R3, R9_t1 all got one.)
- Bridge: "an ancient stone bridge of pale carved stone blocks with gold inlay, no guardrails, no asphalt" (R9_t3 read as a highway).
- RAIN (rain_t5 = no rain, t2/t3 = haze): Seedance renders rain only when it is the subject of a sentence and the light is behind it: `HEAVY REAL RAIN pouring the whole time: thick vertical rain streaks backlit by a low cold light behind the actors, rain splashing on the stone, a mirror-wet marble floor with puddles reflecting the columns, soaked hair stuck to faces, water spraying off clothes on every impact, breath vapour.` Never write "golden" or "sunset" in a rain prompt (t5 turned into a dry sunset). Wide rain shots peaked at 8–8.5 (small figures, dry floor); medium shots and close-ups with backlit rain (rain_t6 Blaze CU, rain_t1 CU) reached 9. Keep rain fights at medium / medium-wide, with the backlight behind the actors.

## H. Dialogue
- Put the line on a visible face: "<NAME> faces the camera 3/4, face fully visible, lips clearly in sync, hands away from the mouth, says: "…"". (C7 hand over mouth; C8 faceless artist; C9 pencil in mouth; M06_t2 profile.)
- One line per clip, ≤ 12 words; or two speakers max in 8 s.
- Spell any number as a word in the line only if it must be spoken that way; keep names that Seedance can pronounce.
- Never an off-screen line: if nobody's lips are visible at that moment, cut the line.

## I. Audio (every prompt, last line)
`AUDIO: no music, no score, no soundtrack, no drum hits, no tonal pad; only <real sounds> and the spoken line.`
(R6_t4 had the loudest Seedance music of the film; R2_t2/R5_t2/R9_t3 were music-only. The editor still mutes/stems, but this line reduces it.)

## J. Top failure modes → exact fix wording
| # | failure (clip) | cause | paste this fix |
|---|---|---|---|
| 1 | dummy/grey crowd copied (CER_A1_t1–t3, 5–7) | video ref or a frame from a previs/IF clip with dummies | drop the video ref; image ref = hall_t4.jpg; "every seat filled with real black-tie guests of varied ages, ethnicities and hairstyles, moving naturally; no empty seats, no mannequins, no rows of identical figures" |
| 2 | obelisk / monument / slab (R2_t1, R3, R9_t1, R1_t1) | KF keyframes + "classical gold square" priors | drop KF_F16/KF_F12; §G location ban |
| 3 | duplicate character (R7 mirror Pip, REVEAL two Aurelias) | mirrors, "two shots of X", crowded frames | no mirrors; "exactly one <NAME>; no twins, no lookalikes" |
| 4 | static / stiff (R8_t1, R2_t3 T-pose, M09) | no verb in the first second; "she stands" | start at 0 s with an action verb and a camera move: "0–1 s: already mid-<action>, camera pushing in" |
| 5 | weak or no rain (rain_t2/t3/t5) | rain as an adjective, golden light | §G rain block, no "golden/sunset" |
| 6 | CG vortex / portal / beam / rings / halo (R1_t3, R6_t1, final_run) | abstract power words ("wall of cobalt light", "energy") | §F physical wording + ban list |
| 7 | punch into air (R1_t2 F15, R6_t4) | target off-frame, OTS from far | both in frame ≤ 1 m, named target, "visible contact" |
| 8 | celebrity-looking face (Soul host) | model priors on "handsome host" | NBP masters + "Nobody resembles any real actor or celebrity" |
| 9 | costume inconsistency (Nova bomber vs suit, Aurelia gown vs feathers at the date, Pip civilian in R2_t1) | text contradicts CAST image / no lock | §E wardrobe text identical to the ref image, "wears ONLY …, same in every shot" |
| 10 | mannequins bleed from motion refs | PV look wins | §D wording + more scene detail |
| 11 | off-screen dialogue (M06_t1, M07_t1, M09 count, DATE) | speaker not described on camera | §H wording |
| 12 | Seedance music | default | §I audio line |
| 13 | glowing knuckles / ember lines (rain_t3, rain_t1) | "fire", "ember", "heat" words | "plain skin, no glowing skin, no ember lines, no fire" |
| 14 | extra hard cut / extra angle (R3_t1 4.2 s) | 3+ beats in 5 s | respect §C budget; "one continuous shot, no other cuts" |
| 15 | NSFW false positive (R6_t2, M05_t2, R4_t2, M17_t3) | "sweaty", "strike her", body words, no refs | remove body/violence nouns, keep refs attached, resubmit once |

## K. Self-score before generating (expected score)
Start at 10, subtract: >3 shots −2 · >2 characters acting −1.5 · crowd with a video ref −3 · PV attached without §D wording −2 · no location ban on gold sets −1.5 · power words (glow/energy/beam) −1.5 · line not tied to a visible face −1 · rain without the §G rain block −1.5 (with the block, framed medium/MCU with backlight: −0.5; a wide rain shot stays ≤ 8.5, so keep rain shots medium or tighter) · mirror −3 · no audio line −0.5 · wardrobe text ≠ CAST image −1 · >2 named props without counts −0.5. Ship only prompts at ≥ 9.
