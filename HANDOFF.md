# Mozvane Game – Project Handoff Brief
_Prepared Oct 11, 2026 for Eric (mozvane / ericmoz). Use this to pick the project up in any tool (ChatGPT, another assistant, or a human dev/artist)._

## Links
- **Playable prototype (phone-friendly):** https://raw.githack.com/EricMoz/mozvane-impound-prototype/main/index.html  (tap "Open the page" on the first visit, then play in landscape)
- **Permanent link once GitHub Pages is switched on:** https://ericmoz.github.io/mozvane-impound-prototype/ (turn on at https://github.com/EricMoz/mozvane-impound-prototype/settings/pages → Deploy from a branch → main → / (root) → Save)
- **Code repo (public):** https://github.com/EricMoz/mozvane-impound-prototype
- **Original art (OneDrive, Ep 3/Artifacts):** https://1drv.ms/f/c/a8ce9a24a3eb2899/IgD7Mmv5P0xtSLuRRwWbRhpvATGJ4FEVOE6z2qlls0H011E  (Characters: 45 files, Backdrops by Scene: 96 files, Sounds, Video Raw)
- **DaCat site / arcade where it would live:** https://dacat.fun/arcade/

## Eric's verdict on the prototypes (read this first)
Eric dislikes almost all of the game built so far, including the controls. **Only the backdrops/environment look (rainy neon street, lighting, reflections) is worth keeping. Everything else needs a full overhaul:** gameplay design, controls and game feel, characters (look and animation), combat, UI/HUD, and level design. Treat the existing prototypes as reference for what NOT to repeat, not as a base to polish.

## The goal
A fun, unique browser game for the DaCat arcade (dacat.fun, an Ethereum community/“Cryptotainment” IP) built from Eric's **Mozvane** animated series – not a rushed arcade toy. Must:
- Play well **on phone (landscape)** first, desktop too.
- Feel modern: fluid, intuitive controls, readable camera, strong feedback ("not a 90s arcade game").
- Look like Eric's art. Quality bar is high: anything off-model or cheap-looking is a no.
- Have replay value (high score / leaderboard idea fits the arcade's existing "Hall of Legends").
- Stand out from the existing arcade games (mostly runners/shooters).

### Look & feel target
- **Hades** (Supergiant): tilted top-down camera, painted environments, very responsive controls.
- **Mark of the Ninja**: stealth that's easy to read (vision cones, noise rings) – optional layer.
- Eric's own backdrops: rainy neon cyber-noir city at night, deep blue/black, cyan neon, warm amber lights, wet reflective streets.
- **Style prefix Eric requires at the start of every image prompt:**
  > Late-90s 2D cel-shaded anime. Bold ink outlines, flat fills, hard shadow edges, matte surfaces

## The world (from Ep 1–3; use themes, don't copy the script literally)
- **Mozvane** (Moz): white cat, navy ribbed suit with light-blue armor plates, mechanical eye with a **yellow beam** powered by a **Zafus Chip** (also powers his suit). The beam is **powerful but limited** – in Ep 2 it destroyed 3 toads at once, then the chip burned out.
- **Vesper**: black cat with tan muzzle, scar, black scarf, rusty pauldrons/bracers, belt pouches with tools, ragged brown tunic, clawed feet, orange-tipped tail. Moves when Moz would stop.
- **Nox**: teen grey cat, goggles pushed UP on forehead, olive jacket, white shirt, dog tag, satchel, cargo shorts, boots with red laces. Guide/trickster, not a fighter.
- **Toad soldiers ("the frogs")**: work for the Dark Lord. Big toads: hunched, dark green, glowing red eyes, gunmetal plate armor, black chains crossed on chest, armored backpack with a fin. Small toads: crouched, dark slate tactical armor with pouches/backpack, no chains. Cyan energy guns.
- **Dark Lord**: bigger toad in a dark chair, appears as a hologram only (art from Ep 2 still to come). Wants Moz **alive** + the Ghost Shard.
- **The city (planet Kafkaesk)**: bureaucratic lizards – **Clerk Reed** (Registrar, dark hooded mantle with blue lining and a round clasp), **Cult lizard** (black/charcoal robes, on the street), **Lil Clip** (short, funny lot clerk with a clipboard). The city stops Moz with paperwork but ignores the frogs.
- **Props**: Ghost Shard (stolen data device), Zafus Chip (dead/charged), Veinrunner (their ship; two designs exist in the art – sleek grey shuttle in the lot shots vs. boxy hover ship in Scene 5.1 – Eric to pick).
- Tone: melancholic, unfair, a little funny; short lines; rain. Series under daCAT / Clowder After Dark; yellow end card with the name.

## What was built
1. **"Impound" level** (first prototype): 3D browser game (Three.js) – stealth past toad vision cones and searchlights, city stamp checkpoints, Zafus chip pickups for a one-shot piercing beam, Ghost Shard, escape on the Veinrunner from the impound lot, score + yellow end card, touch controls.
2. **Movement + combat sandbox** (in progress at time of writing): one rainy street block, temporary rigged stand-in character in Moz colors that actually runs/dashes, a basic melee combo that works from second one, eye beam as a meter-charged power move, toad waves, phone-first controls.

## What wasn't working (be honest about this)
- **Gameplay was confusing.** Eric: "I don't get how to kill an enemy." Attacking needed a rare chip pickup and the game never made that clear. Too much was taken literally from the episode script (stamps, windows, impound) before the core moment-to-moment fun was proven.
- **Character looked bad and didn't animate.** The 3D models were made with free AI image-to-3D tools; textures were smeared/glitchy, and even after a flat-color cleanup the shapes were wrong (missing armor plates, wrong poses, painted-on chains). No rig → characters slid instead of walking.
- **AI-generated character angles drifted off-model** (wrong armor/colors on toads, Vesper got boots and an all-black head, Nox's goggles over his eyes). Rejected. The image tool used here couldn't hold Eric's designs.
- **What Eric liked:** the environment/background look (rainy neon street, lighting, reflections).

## Key learning (how Hades actually does it)
- Hades does **not** render 3D in real time. Characters are 3D models (sculpted over the 2D art, flat-colored, ink lines hand-painted) rendered out as **2D sprite frames** from many angles; environments are **hand-painted 2D** pieces for one fixed camera.
- Nobody ships auto-textured AI 3D. Every good-looking game has an artist or carefully controlled shader between model and final image.
- Implication: get the **art right in 2D first** (Eric's GPT workflow made all originals, so it should make the missing angles), then either (a) 2D sprites with directional frames, or (b) hire a stylized 3D character artist (~80–150 hrs estimated) for Moz + a shared toad base.

## Art still needed (priority order)
Use existing views as references every time, plus the style prefix.
1. **Lizards** – Clerk Reed, Cult lizard, Lil Clip: 3/4, side, back (only fronts exist).
2. **Back 3/4** for Moz, Vesper, Nox (everything else exists; Vesper/Nox side views can be cropped from "Crew - Sideways Right.png").
3. **Toads** – one clean isolated front 3/4 of a big toad and a small toad, no gun (front/side/back can be cropped from the group shots).
4. **Veinrunner** – pick the real design; top-down + front view.
5. Later for animation: a few run/attack poses for Moz.

## Recommended next steps
1. Eric makes the missing angles (above) in GPT and drops them in the OneDrive folder.
2. Prove the core fun on phone with the movement + combat sandbox: does running, dashing, hitting and the beam feel good? Iterate only on that.
3. Then decide the game: e.g. short replayable runs in Kafkaesk (melee + limited Zafus beam vs. toad squads, city lizards as obstacles/comedy), leaderboard for the DaCat arcade.
4. Swap in real characters built from approved art (2D directional sprites, or a hired 3D artist).
5. Expand environments from the backdrops (rain street, poster wall, No Signal corner, Registrar Hall, impound lot).

## Inventory of work files (on Grok Bot's computer – ask Gaming bot to zip/upload any of these)
- Downloaded art: /workspace/mozvane-art/Characters, /workspace/mozvane-art/Backdrops
- On-model reference crops from Eric's art: /workspace/mozvane-art/Crops
- Game source + screenshots: /workspace/mozvane-game (sandbox + Impound level), research report: /workspace/mozvane-game/research/art_pipeline.md
- AI 3D models (not approved): /workspace/mozvane-game/assets/models
