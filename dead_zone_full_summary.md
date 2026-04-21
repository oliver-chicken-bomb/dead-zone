# DEAD ZONE — Complete Game Reference

---

## 1. THE MUTANT ZOMBIE KING (Wave 10 Boss)

**Stats:** 300 HP, takes 1 damage per bullet. Large radius of ~45px.

### Entrance
Wave 10 has no regular zombies. Instead, the camera slowly pans to the center of the map while an intro screen fades in reading **"WAVE 10 — MUTANT ZOMBIE KING rises from the earth..."** After the pan completes, the boss erupts from the ground at the map's center, leaving behind a permanent **death pit** — a dark circular hole in the concrete. Dirt stain splatter marks scatter around the crater in all directions.

### The Death Pit
The hole left by the boss's entrance is lethal. If you walk into it, you die instantly with no boss death description — just the normal YOU DIED screen. It sits permanently at the center of the map for the entire wave and the boss will move around it during the fight.

### Appearance
The boss is a massive bloated mutant humanoid with layered grotesque details. It has a rotten, torn-open torso with exposed muscle tissue and gore patches, visible ribs through the skin, boils and pustules weeping across the body, and electric lattice veins glowing faintly through the flesh. A ring of 10 mushroom growths orbits its body and 14 spore dots orbit further out. Its elongated skull has a fungi crown splitting the top, with blood seeping from the cracks and eye sockets. The eyes shift between cyan and purple with slit pupils that flare bright when attacking. It has a forked tongue, jagged yellowed molars, face scars, and two massive clawed arms with fungal bumps dripping blood. Dual aura rings pulse around it — electric cyan on the outside and purple closer in.

### Abilities

**Electric Dash** — Triggers when the player is far away (more than ~320px). The boss launches itself toward the player at high speed, leaving electric cyan afterimage trails and zap particles behind it. It stops roughly 15–20 tiles short of the player. If it collides with you during the dash it deals 8 damage and zaps you. Cooldown: ~6.7 seconds.

**Ground Slam** — Triggers when the player is nearby (under ~200px) and the slam cooldown is ready. The boss goes through three phases: a fast windup where it rises upward (~10 frames), a hover where it floats with purple smoke puffing out (~40 frames), then a crash where it slams down in ~12 frames. On landing, 8 ground cracks radiate outward and an expanding electric shockwave ring pulses out. If the ring hits you it deals 5 damage and applies a shock stack (3 damage per tick for 5 seconds). The crash causes heavy screen shake. Cooldown: 10 seconds.

**Fungi Spawn** — Triggers when nearby and the spawn cooldown is ready. The boss enters a spawn phase lasting ~10 seconds, during which purple smoke puffs from its body and a dashed ring shows the spawn radius. It spawns up to 8 fungi zombies total in groups of 4 every ~3.5 seconds. These fungi are tagged as boss-spawned. When the boss dies, every one of these tagged fungi instantly dies in a burst of purple particles — they do not persist after the boss falls. Cooldown: ~11.7 seconds.

**Fungi Slash** — Triggers when the player is directly in front of the boss within its arc. The right arm sweeps a wide arc with a glowing magenta blade trail — thick outer glow, solid bright inner line, white edge highlight, and gore chunk particles flung along the arc. Deals 45 damage if it catches you. Cooldown: 10 seconds, shared conceptually with slam so they don't both fire simultaneously.

### Boss HUD
A health bar appears at the top center of the screen showing the boss name, percentage, and exact HP out of 300. The bar color shifts from purple to orange to red as health drops.

### Ammo Drops During Fight
Every 60 seconds during the boss fight, a crate drops near the player granting **+80 ammo**. This keeps the fight from stalling out completely if you run dry.

### Boss Death
When the boss reaches 0 HP it tilts and falls over with a death tilt animation. All boss-spawned fungi die instantly. After a short delay, a **shotgun pickup** spawns near the boss's body. Walking over it triggers the **WIN screen** — it's the win condition for the entire game.

### Death Description Screen (Wave 10 only)
If the boss kills you — through any means except falling in the pit — the screen goes through a horror death sequence instead of the normal death screen. The game world freezes behind the effect. Phase 1 is ~90 frames of rapid black flickering with red static noise lines. Phase 2 is a slow fade to pure black. Phase 3 fades in pitch-black text with the title **"THE KING HAS CONSUMED YOU"** and one of four randomized horror descriptions:

> *"The King's jaws closed around you like a vice. You never even had time to scream. Every bone folded inward under a thousand pounds. It didn't even slow down. You were nothing to it."*

> *"It caught you mid-run. One hand. That was all. The pressure was total — cold, mechanical, absolute. The last sound you heard was a sickening crunch. Then silence. Then darkness. Then nothing at all."*

> *"The Mutant Zombie King didn't even stop moving. It scooped you up mid-stride like a ragdoll. Its molars came together with terrible, grinding finality. You were gone before the echo faded."*

> *"You ran. It covered the distance in an instant. Its jaws locked around you like a car compactor. Under a thousand pounds of rot and fury, you were snuffed out like a candle in a storm."*

After a moment, "click to continue" appears. Clicking advances to the normal death screen, and the wave panel locks again.

---

## 2. ZOMBIE TYPES

### Normal Zombie
The standard enemy, appearing from wave 1 onward. Humanoid with shambling walking animation, rotting green-toned skin in four different skin tone variants, tattered dark clothing, visible hair, and glowing red eyes. They have 2 HP and deal 10 damage when touching the player, hitting every ~0.5 seconds. Movement speed is the baseline (0.55 px/frame). Worth 10 points × wave number when killed.

**Wave counts:** Wave 1 = 20, Wave 2 = 25, Wave 3 = 30, Wave 4 = 35, Wave 5 = 20 normal + 20 fungi exactly.

### Fungi Zombie
A bloated, slow-moving humanoid with a purple mushroom crown on its head, 5 orbiting mushroom growths, and a ring of 14 spore dots orbiting its body. Its skin is dark purple-gray. The fungi zombie sways side to side as it moves. It has 4 HP and deals 20 damage per hit every ~0.67 seconds, making it hit harder and take more shots than normal zombies — but its speed is half the normal zombie's. Worth 30 points × wave number. Debuts in wave 5 (exact 20/20 split with normals) then appears in all subsequent waves.

### Electric Zombie
A fast, charred humanoid with standing-on-end hair from the voltage, cyan glowing eyes, a screaming open mouth, and a dark navy-charred torso with burn holes glowing from inside. Arcs of electricity fire off its outstretched arms every few frames. Has only 1 HP — one shot kills it — but moves at 2× normal speed (1.1 px/frame), making it the fastest enemy in the game. It deals 2 damage per hit and applies a **shock stack**: 1 damage per second for 5 seconds. Shock stacks are cumulative — multiple electric zombies can stack the damage-over-time. Getting hit by an electric zombie also produces the cyan shock aura around the player. Worth 25 points × wave number. Debuts in wave 7 and appears in all subsequent waves including wave 9.

**Wave mix from wave 7 onward:** roughly 45% normal, 30% fungi, 25% electric.

---

## 3. THE MAP & DUMPSTER FIRES

### The Map
The world is 1800×1400 pixels displayed through a 700×560 scrolling camera viewport (the camera follows the player with smooth lerp interpolation). The ground is light concrete with a tile grid overlay. Scattered across the map are dark tile patches, painted crack details, and graffiti tags in red, green, blue, orange and purple — words like NO HOPE, RUN, DEAD END, ZONE X, HELP, THEY'RE HERE, DON'T STOP, and LOST. Manhole covers are dotted around with cross-hatch details. The map has a thick crumbled wall border.

**Abandoned cars** — 22 cars are placed randomly across the map, avoiding the center zone where the boss spawns. They come in six muted colors and about 40% of them are wrecked with cracked/dimmed windshields. Cars are fully solid obstacles: bullets stop on impact with them (producing a spark particle), zombies pathfind around them using a three-step collision resolution system, the player slides smoothly along their edges, and the boss also navigates around them.

**Minimap** — A small map in the bottom-right corner of the screen shows the full world at a glance. Orange dots = dumpster fires, gray bars = cars, green dots = normal zombies, purple dots = fungi zombies, cyan dots = electric zombies, yellow squares = pickups/crates, blue square = player, purple dot = boss. A rectangle on the minimap shows the current camera viewport.

### Dumpster Fires
Between 7 and 9 dumpster fires are placed randomly across the map. Each dumpster is a green metal container with a layered fire animation on top — five flame layers in concentric sizes from dark orange outer glow to bright white-yellow center, with organic wobble and flicker applied per flame. Embers float upward from the flame constantly.

The dumpster fires have a flame radius of ~28px. If the player walks into this radius, a **burn stack** is applied: 2 damage per second for 5 seconds. Multiple entries stack. The burn aura (orange ring) shows around the player while burning. The HUD displays "BURNING x[count] -[total]/sec" in orange. Dumpsters also appear on the minimap as orange dots so you can avoid them.

---

## 4. WEAPONS, AMMO, HEALTH & CRATES

### The Pistol
The player's only weapon. It rotates to face the mouse cursor at all times, with a visible muzzle flash when firing. Fires at one shot every 18 frames (~3.3 shots per second). Bullets travel fast in a straight line (14 px/frame) and stop on contact with cars or enemies. Toggle firing on and off with the **F key** — a red "FIRING" or grey "FIRE OFF" label in the HUD shows the current state. The aim direction shows as a faint dotted line from the gun barrel.

### Ammo
You start each wave with 500 ammo. The HUD shows current ammo count at all times. Running out of ammo means you can't fire.

### Health
You start each wave with 100 HP shown as a color-coded health bar (green → yellow → red as it depletes). Damage sources include zombie contact, burn stacks from dumpster fires, and shock stacks from electric zombies and the boss's shockwave ring. Health carries over between waves — you don't reset to 100 on each new wave.

### Every-2-Wave Crates (Supply Drops)
A green medkit crate drops somewhere on the map at the end of waves 2, 4, 6, and 8. Walking over it grants **+30 HP** (capped at 100) and **+200 ammo**. It shows a pulsing green cross symbol with the label "+30HP+200AMMO". These are the main way to recover health and keep your ammo topped up between waves.

### Wave 10 Boss Fight Ammo Crates
During the boss fight, a **+80 ammo** crate drops near the player every 60 seconds. These are yellow crates labeled "+80 AMMO" and are the only pickups available during the boss fight.

### The Shotgun (Win Condition)
When the boss dies, a shotgun pickup spawns near its body. Walking over it immediately triggers the WIN screen — it's purely a win condition item, not a playable weapon.

---

## 5. EXTRA DETAILS

**Wave Panel (Password Locked)** — The left sidebar shows a password input by default. The password is `0l1v3r`. Enter it correctly and the 10 wave buttons appear, letting you jump to any wave. Enter it wrong and "incorrect" flashes and the input clears. The panel re-locks every single time you die or win. The death screen has a hint reminding you to "enter password to skip to a wave."

**Wave Structure** — 10 waves total. Waves 1–4 are normal zombies only, scaling from 20 to 35. Wave 5 is an exact 20/20 split of normal and fungi. Wave 6 is a normal/fungi mix. Waves 7–9 introduce electric zombies into the mix. Wave 10 is the boss fight exclusively — no regular zombies spawn.

**Screen Shake** — Every impactful event has calibrated screen shake: firing the pistol (light), zombie contact (medium), boss attacks (heavy), boss ground slam (very heavy at magnitude 20), boss death (magnitude 22).

**Particle System** — Blood splatter, muzzle flash sparks, electric zap arcs, purple spore bursts, fire embers, smoke puffs, and explosion particles are all part of the same particle pool. They fade out over time and are culled off-screen for performance.

**Enemy Y-Sorting** — All zombies and the boss are drawn in Y-order so enemies further down the screen appear in front of enemies higher up, giving the illusion of depth on the flat map.

**Status Effects on Player** — Two visible status effects: the cyan shock ring (from electric zombie or boss shockwave) and the orange burn ring (from dumpster fires). Both show as pulsing aura rings around the player character and are listed in the HUD with stack counts and damage-per-second numbers.

**Player Character** — A tactical soldier with a military cap, hexagonal armor plates, an animated walking stride with leg animation tied to movement speed, a visible face with one visible eye, and a pistol that rotates independently toward the mouse cursor.

**Score System** — Each enemy kill awards points equal to the enemy's base value multiplied by the current wave number. Normal = 10×wave, electric = 25×wave, fungi = 30×wave. Final score is shown on the win and death screens.

**Boss Intro Camera Pan** — When wave 10 starts, the camera detaches from the player and slowly pans to the center of the map at 0.03 lerp speed (much slower than the normal 0.1 follow speed), building tension before the boss erupts.

**Wave Banner** — At the start of each wave, a centered banner fades in showing the wave number and enemy composition (e.g. "WAVE 7 | 50 ZOMBIES | ELECTRIC") then fades out over about 2.3 seconds.
