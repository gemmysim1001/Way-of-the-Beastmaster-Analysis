# Way of the Beastmaster v0.41 — Full Expansion Skeleton

## Status Key
```
[DONE]     = Fully implemented and playable in v0.41 (465 passages)
[TBC]      = Hinted at, stubbed, or set up in-game — needs completion
[EXPAND]   = New content faithful to established lore, themes, and patterns
[SYSTEM]   = Mechanical system that needs building or extending
```

## Established Lore Bible (Canon Reference)
```
WORLD:     Orbath (oval island). Two continents: Reliquim (West), Adplagam (East).
           Vast ocean in center — Council of Wizards resides there.
CAPITAL:   Holstein, home of the Silver Spire (Iron Empire HQ).
KING:      Adalrico Dominus, rules from atop the Spire.
RELIGION:  Pan, the Great Forest God (a Satyr). Blesses Magisters via ritual.
MAGIC:     Magisters = animal controllers. Green mist from fingertips.
           Blessing = control over animals. Curse = pheromones that attract animals sexually.
           Magister's Dirk = amplifier dagger, "all Magisters are given one."
           Magic addiction exists — can corrode the mind (Rogue Warlock precedent).
           Volition Spells: Light (basic illumination), Fireball (combat, learned from Zexir).
VILLAIN:   The Hooded Mage / Strange Man — another Magister using powers for evil.
           Seen in the forest with a massive wolf (red eyes, green-eyed figure).
           Later: commands the Dark Dragon at the mountain summit. Recognizes player
           as "a fellow Magister." Full identity never revealed.
           Frederick is tracking him. Kami says "it could spell doom for all of Orbath."
COUNCIL:   "Should the Council hear about it, they might seek us out" — Kami.
           They track Magisters by magical "signature."
COMPANION: Kami — wolf, served Pan for years, granted speech at your Awakening.
           Had a wife (Aleida) and 4 children (Vesper, Berion, Saige, Eike).
           Eike rescued during SQ2 (Wrenville wolves quest).
PLAYER:    Amnesiac. Woke naked in the Forest of Madness after a botched Awakening.
           "There must have been a problem with the Awakening" — Kami.
           Missing their Dirk ("I do not know why you did not have one" — Kami).
           Birthright Magister — this is inherited, not learned.
TOWNS:     Holstein (capital), Scarhaven (frontier village), Streamdale (dragon mountains),
           Wrenville (northern trade route), Seahome (bypass to The Bridge).
           Isle of Dragons / Icaria — hidden dragon island, 800 servants + 500+ dragons.
FACTIONS:  Iron Empire (military, the Spire), Bandits/Mercenaries (Killian's group),
           Adplagam spies (infiltrating the Spire), The Council of Wizards,
           Isle of Dragons (dragon civilization led by triumvirate).
IoD LEADERS: Zexir (Magic/Education), Raln (Military/Defense), Valia (role unspecified).
FINN:      White-furred boy in Scarhaven Inn. Knows your name before you tell him.
           Gives you a Birdpup Feather. "You can hear a child giggling in the back
           of your mind." Fourth-wall break: "Stay tuned for more exciting things."
           Likely an avatar of Pan, or the developer's self-insert/guide character.
           If given Divine Potion: revealed as a disguised god, powerful SS encounter.
DARK DRAGON: Massive dragon commanded by the Hooded Mage at the mountain summit.
           Unwinnable boss fight — player is flung off the mountain.
           Isle of Dragons patrol rescues the player. IoD has interest in this dragon.
ZEXIR:     Turquoise dragon, ~10m. Head of magic/education on IoD.
           Teaches Volition Light and Volition Fireball.
           Night visits: 50% catch him with a student, 50% private encounter.
           Must know Fireball for his SS to unlock.
           Lore: explains the Dragon-Nomad war, gives a map of Orbath,
           advice "trust no-one."
EREL:      Avian (parrot-like), red/white feathers. Veterinarian on IoD.
           Studied in Adplagam. Interested in animals, not people.
           Dialogue only — no SS (unusual for this game's pattern).
HRAN:      Young dragon (~45 dragon years / ~15 equivalent). Wingless, stocky.
           Night training encounters, SS (tops/bottoms branching).
           Grandfather's journal in his cave. No relationship system.
RALN:      Wingless dragon, stocky, jagged horns. Head of military.
           Rude but kind-hearted. Arena = "not ready to spar yet."
VALIA:     Third IoD leader. Named once. Never appears. Role "unspecified."
```

---

# PROLOGUE: AWAKENING (pids 37, 1-35, 230)

## P-1. Title Screen
- **[DONE]** Title (pid 37): New Game / Load Game

## P-2. The Forest of Madness — Waking Up
- **[DONE]** Intro1 (pid 1): Wake up cold, naked, amnesiac, surrounded by broken glass
- **[DONE]** Species selection (pid 5): Canine / Feline / Vulpine / Avian / Reptile / Dragon
- **[DONE]** Full character creation chain: Age → Body → Height → Hair → HairC → Eye → Cock → DickL
- **[DONE]** CharacterFinish (pid 18): Review yourself

## P-3. Meeting Kami
- **[DONE]** Intro2 (pid 19): Wander the cold forest, need shelter
- **[DONE]** Intro3 (pid 20): A talking Wolf appears — Kami introduces himself
- **[DONE]** Dialogue options (explore all):
  - Intro3c1: "What is a Magister?" — dominion over animals, blessing & curse, pheromones
  - Intro3c2: "Why can you talk?" — Pan blessed him, served Pan for years
  - Intro3c3: "Where am I?" — Forest of Madness, 3 miles south of Holstein
- **[DONE]** Intro3c4: Decide to get moving, Kami leads

## P-4. The Bandits
- **[DONE]** Intro4-5: Ambushed by Killian's group (mercenaries, not bandits)
- **[DONE]** Intro6: Killian gives you clothes. Optional Kami dialogue (trust, speech, powers)
- **[DONE]** Intro7: Sleep under the stars. Something touched you in the night.
- **[DONE]** Intro8-9: Killian explains Holstein, the Spire, the Iron Empire. Travel together.
- **[DONE]** Intro10: Killian says goodbye at the gates.
- **[DONE]** TheBeginning (pid 230): "Your journey begins." → Hub

---

# ACT 1: HOLSTEIN — THE CAPITAL (~120 passages)

## Chapter 1: Getting Your Bearings

### 1.1 The Hub (pid 36)
- **[DONE]** Central square with marble fountain, Silver Spire visible overhead
- **[DONE]** Day/night descriptions, 8 exits (7 original + Tailor added in v0.41)
- **[DONE]** Persistent footer: Character (pid 3) / Inventory (pid 4) / Spells (pid 421) / KamiMenu (pid 41)
- **[DONE]** KamiMenu: Dynamic dialogue unlocked by flags ($pk, DinusI, MisfitF, Dirk)

### 1.2 The Inn — Dinus the Bear (HubInn, pid 38)
- **[DONE]** InnStay (pid 44): Meet Dinus — 8-foot bear innkeeper
- **[DONE]** InnStayPay (pid 46): Rent a room (10g) → InnStayRoom (pid 48)
- **[DONE]** InnStayRoom: Three options:
  - KamiSS1 (pid 49): Sex with Kami (top/bottom branching)
  - HolsteinKEquip (pid 156): Equip Kami gear (Helm/Collar/Paws/Back)
  - InnStaySleep (pid 50): Sleep → next day
  - OrbathAmulet (pid 393): Teleport to IoD (if has Zexir's Amulet)
- **[DONE]** DinusI → DinusI2 (pid 55): Dinus's backstory — Rogue Warlock, green glowing eyes, beheaded him, lost squad
- **[DONE]** DinusSS1-5 (pids 88-92): Dinus SS chain (requires visit >= 11)

### 1.3 The Bounty Board (InnQuests, pid 45)
- **[DONE]** Three postings: MQ1 (500g), SQ1 (100g), SQ2 (200g)

### 1.4 The Fountain Square (HubFount, pid 43)
- **[DONE]** DAYTIME:
  - FountD1 (pid 56): Look for allies → Wyatt1 (pid 59): Meet Wyatt (first time)
  - FountD2 (pid 57): Sit and relax
  - Wyatt2 (pid 60): Return visits — 4 dialogue topics (Spire, past, money, danger)
  - WyattR (pid 239): Confess feelings → WyattR2 → WyattRHub (pid 238)
- **[DONE]** NIGHTTIME:
  - FountN1 (pid 58): Hooded Rat figure → FountN11 (pid 66): SS encounter

### 1.5 The Market (HubMarket, pid 39) — Day only
- **[DONE]** MarkMagic (pid 67): Silver Orb (20g), Dog Collar (30g), Ruby Necklace (50g), sell Magic Flower (100g)
- **[DONE]** MarkHerb (pid 68): Pain Leaves, Health Potion, Endowment Potion (+ EPFuck SS chain)
- **[DONE]** MarkPed (pid 69): Peddler → Magister's Dirk (10g, vision of power, Kami excited)

### 1.6 The Tailor (HolsteinTailor, pid 458) — v0.41 addition
- **[DONE]** HolsteinTailor2-7 (pids 459-464): Meet Soir (black feline), get measured, SS chain, buy clothes (30g)

### 1.7 The Silver Spire (HubSpire, pid 40)
- **[DONE]** Guard turns you away. Single link back to Hub.
- **[TBC]** Currently a dead end — the most referenced locked location in the game.
  - _Referenced by: Wyatt (warns about guards + Adplagam spies), Killian (explains Empire HQ), Intro lore (King Adalrico resides here), Frederick (king's insignia). Every major NPC acknowledges the Spire's importance._

### 1.8 The Alley — Daytime (Alley1D, pid 83)
- **[DONE]** MisfitI (pid 85): Meet Misfit the Ratman — alchemist, sewer dweller
- **[DONE]** MisfitSS1 (pid 86): SS encounter
- **[DONE]** MisfitR (pid 236): Confess feelings → MisfitR2 → MisfitRHub (pid 235)

### 1.9 The Alley — Nighttime (Alley1N, pid 84)
- **[DONE]** Alley1N1 (pid 93): Peek in illuminated window → WyattSS1-SSE: Wyatt's place, meal, optional SS chain. His brother works night shift at the Spire as a guard.
- **[DONE]** Alley1N2 (pid 94) → Alley1N21 (pid 101): Dark figure, feral animal attack, Kami protects, escape.

### 1.10 Carriages (pid 166)
- **[DONE]** HolC (pid 231): Go to Holstein
- **[DONE]** ScarC (pid 167): Go to Scarhaven

---

## Chapter 2: Relationships

### 2.1 Misfit — FULLY COMPLETE
- **[DONE]** MisfitRHub (pid 235): Full relationship hub with activities, status tiers (0-1000+)
- **[DONE]** MisfitRI (pid 245): Ask about himself — 5 topics (childhood, work, sex, hobbies, his people)
- **[DONE]** MisfitHouse (pid 252): Visit his sewer home
  - MisfitHSS (pid 254): "Something kinky" — Kami joins or Misfit only (branching)
  - MisfitLabGame (pid 255): Alchemy minigame (4 rounds, ingredient matching) → Divine Potion or gold
  - MisfitFiend1 (pid 280): Hang with Fiend (if met) → threesome or solo
- **[DONE]** MisfitFam (pid 273): Meet family (LM >= 250) → MisfitFiend (pid 279): Meet Fiend
- **[DONE]** MisfitPicnic (pid 298): Special outing (LM >= 500) → wholesome ending (+50 LM)
- **[DONE]** MisfitTrueEnd (pid 271): True ending (LM > 1000) → Glass Ornament + "I love you"
- **[DONE]** MisfitRBU (pid 242): Break Up → enables FiendSingle on Hub

### 2.2 Fiend — POST-BREAKUP CONTENT
- **[DONE]** FiendSingle (pid 287): Appears on Hub if $MisfitBU + $FiendF
- **[DONE]** FiendSingle2-6 (pids 288-293): Fiend SS chain

### 2.3 Wyatt — SHELL ONLY
- **[DONE]** WyattR (pid 239): Confess feelings
- **[DONE]** WyattR2 (pid 240): Wyatt accepts
- **[DONE]** WyattRHub (pid 238): Relationship hub EXISTS
- **[TBC]** Activities: NONE — "Too much adventuring to do"
  - _Has tier structure (0-250 / 251-500 / 501-750 / 751-1000 / 1001+) and breakup (WyattRBU, pid 243), but zero dates, dialogue, or scenes._

### 2.4 Hans — SHELL ONLY
- **[DONE]** HansR (pid 232): Confess feelings
- **[DONE]** HansR2 (pid 233): Hans accepts
- **[DONE]** HansRHub (pid 234): Relationship hub EXISTS
- **[TBC]** Activities: NONE — "Too busy working"
  - _Same skeleton as Wyatt. Breakup (HansRBU, pid 244) includes crying if LoveMeter high. Nothing to build LoveMeter with._

---

## Chapter 3: The Quests

### 3.1 Main Quest 1 — King's Decree: The Forest Hunt (500g)
- **[DONE]** MQ1 → MQ2: Accept quest, ask Dinus about transport
- **[DONE]** MQ3-MQ5: Travel to Scarhaven, command tent, briefing
- **[DONE]** MQ52: Enter the forest
- **[DONE]** Maze (4x4 grid, 16 nodes, pids 110-125): Navigate the Forest of Madness
  - Items found: Strange Mushroom (Maze1 area), Speedband (Maze8, from Wyatt)
  - Maze11: Exit to boss encounter
- **[DONE]** MQ6-MQ7: Find the Strange Man with massive wolf. Run. Trip.
- **[DONE]** MQ8-MQ9: Tap into power — first real Beastmaster magic. Green mist. Command wolves.
- **[DONE]** MQ10: Alpha wolf bows to you, leaves.
- **[DONE]** MQ11: Collapse, wake in tent, meet Frederick. 500g reward.
- **[DONE]** MQ12: Carriage back. Kami warns about the rogue Magister. Sets $MQ1D=1, $pk=1.

### 3.2 Side Quest 1 — Streamdale: Evict the Dragon (100g)
- **[DONE]** SQ1-SQ15: Accept, travel, arrive (dragon damage), enter cave, mercenary killed
- **[DONE]** SQ16: Dragon recognizes you as Magister
- **[DONE]** SQ17: 1 adult + 3 whelps, protecting children. Branch:
  - SQ1SS1-SSE: Sexual compromise → dragon agrees
  - SQ18: Negotiate diplomatically
- **[DONE]** SQ1E: Return to mayor. Multiple endings by approach.

### 3.3 Side Quest 2 — Wrenville: Wolves on the Trade Route (200g)
- **[DONE]** SQ2-SQ23: Accept, travel, find wrecked carriage, mercenaries stand guard
- **[DONE]** SQ24: Kami recognizes Aleida (his wife) and children. Eike captured.
- **[DONE]** SQ25-SQ2E: Rescue Eike, family reunites, quest complete.

---

# ACT 2: SCARHAVEN — THE FRONTIER (~60 passages)

## Chapter 4: The Border Town

### 4.1 The Hub (ScarHub, pid 168)
- **[DONE]** Frontier village, 5 exits. Day/night descriptions.

### 4.2 The Blacksmith — Hans (ScarBS, pid 169)
- **[DONE]** SBSK (pid 173): Browse Kami gear (functional shop)
- **[DONE]** SBSC (pid 174): Browse player gear — "nothing in your size" **(STUB)**
- **[DONE]** SBSH (pid 175): Talk to Hans (day) — 5 topics (job, personal, sex, war, Frederick)
  - SBSHSS (pid 180): Hans SS — 3 body-frame variants (small/medium/large)
- **[DONE]** SBSHn (pid 196): Visit Hans at night — stay the night, cuddle, wake together
- **[DONE]** HansR (pid 232): Relationship entry (see Ch. 2.4 — shell only)

### 4.3 The Inn (ScarInn, pid 170)
- **[DONE]** SIIK (pid 214): Talk to Wes (Shark innkeeper). Room rental (10g).
  - SIIKR (pid 218): Room — Kami SS / equip / sleep / amulet teleport
- **[DONE]** SIB (pid 213): Scarhaven bounty board — v0.41 EXPANDED:
  - MQu2: Main Quest 2 — playable (see Ch. 5)
  - SQ3 (pid 299): "Capture the Bandit Leader" (200g) — **[TBC]** STUB ("try at another time")
  - SQ4 (pid 300): "Von Aldersant: A Request" (300g) — **[TBC]** STUB ("leave it for now"). SQu41 (pid 305) empty.
- **[DONE]** Finn (pid 212): Gives Birdpup Feather. "Stay tuned for more exciting things."
  - FinnSS1-5 (pids 261, 294-297): Give Divine Potion → Finn revealed as disguised god. SS. +100g.
- **[DONE]** SISt (pid 215): Stables → HorseSS1-3: Horse taming + SS

### 4.4 The Barracks (ScarBarracks, pid 171)
- **[DONE]** SBaF (pid 192): Visit Frederick's office
  - First visit: SBaF2-3 → Trust check (3 outcomes: success/partial/fail)
  - Return visits: Frc1-4 (Scarhaven, himself, Pren, Strange Man leads)
- **[DONE]** PrenSS (pid 208): Pren SS chain
- **[DONE]** SBaB (pid 193) → SBaBSS (pid 195): Bathroom encounter (Reptile)

### 4.5 The Outskirts (ScarOther, pid 172)
- **[DONE]** FBM1 (pid 221): Approach boy → FBM2: 2 variants (solo / Kami)
- **[DONE]** Night: "Nothing here. Go to bed." **(STUB)**
  - **[TBC]** Night outskirts content is empty.

---

## Chapter 5: Main Quest 2 — The Mountain (v0.41)

### 5.1 MQu2 — King's Decree: Investigate the Rumblings (500g)
- **[DONE]** MQu2 (from SIB): Accept quest. Travel to Hixborough Mountains.
- **[DONE]** Multi-passage mountain climb with 3 battle encounters:
  - Battle 1: Gnoll
  - Battle 2: Insect Swarm
  - Battle 3: Pigorc
- **[DONE]** MQu2Finish (pid 359): Summit — The Hooded Mage appears.
  - Recognizes player as "a fellow Magister."
  - Commands the Dark Dragon.
  - Unwinnable boss fight.
- **[DONE]** MQu2Finish2 (pid 360): Kami is flung off the mountain. Player blacks out.
  - Rescued by Isle of Dragons patrol.
  - → IoDIntro (forced transition to Act 3)

---

# ACT 3: ISLE OF DRAGONS — THE SANCTUARY (~80 passages)

## Chapter 6: Icaria

### 6.1 Arrival (Linear intro, pids 361-372)
- **[DONE]** IoDIntro (pid 361): Wake in unknown room, 2 weeks unconscious
- **[DONE]** IoDIntro2-3: Explore room, dragon at window directs you to council
- **[DONE]** IoDIntro4-5: Walk to council chamber. Meet Zexir. 4 dialogue options:
  - "Where am I?" — Isle of Dragons
  - "Who are you?" — Zexir, head of magic/education
  - "Where is Kami?" — safe at village
  - "How did you know I'm a Magister?" — sensed it
- **[DONE]** IoDIntro6-7: Go find Kami, meet Erel the vet
- **[DONE]** IoDIntro8 (pid 372): Reunite with Kami → IoDHub

### 6.2 The Hub (IoDHub, pid 373)
- **[DONE]** Icaria Town Plaza. 6 exits. Day/night gating on several branches.

### 6.3 Animal Doctor — Erel (ErelHub, pid 374) — Day only
- **[DONE]** ErelC (pid 381): Get to know Erel — 4 topics (arrival, single?, medical knowledge, spells)
- **[TBC]** Erel has NO SS content — unusual for this game's pattern (every other named NPC has one)
  - _Erel's "interested in animals, not people" line may be intentional character trait or placeholder excuse._

### 6.4 Council Chamber (pid 375) — Zexir's Domain
- **[DONE]** IoDRoom (pid 386): Player's assigned room — Kami equip, Kami SS, sleep (3 dream variants), amulet teleport
- **[DONE]** TeleporterC (pid 387): Travel to Holstein/Scarhaven (50g fee, if no amulet)
- **[DONE]** IoDAmulet (pid 392): Travel FROM IoD (free with amulet)
- **[DONE]** Zexir1D (pid 390): Visit Zexir (day) — 4 topics:
  - Zexir1DWorld (pid 412): World history → Dragon-Nomad war → Map of Orbath → "trust no-one"
  - Zexir1DMagic (pid 414): Learn Volition Light → Learn Volition Fireball
  - Zexir1DIsle (pid 415): 3 heads of leadership (Zexir/Raln/Valia)
  - Zexir1DFight (pid 413): "Teach me to fight" → redirects to Raln **(DEAD END — Raln has no content)**
- **[DONE]** Zexir1N (pid 391): Visit Zexir (night) — 50/50 random:
  - ZexirAltSS1 (pid 431): Catch Zexir with student → watch
  - Zexir's room: If knows Fireball → ZexirSS1-4 (pids 429-434): Full SS. If not → sent away.

### 6.5 Arena — Raln (IODArena, pid 376) — Day only
- **[DONE]** IODArenaD2 (pid 403): First visit — meet Raln. "Not yet available for training."
- **[TBC]** Return visits: "Not ready to spar yet" **(PLACEHOLDER)**
  - _Raln is described in detail (wingless, stocky, muscular, jagged horns, rude but kind-hearted) and has a full character concept. The arena was clearly meant to be a combat training system._
  - _Zexir1DFight sends you to Raln, creating a circular dead end — two NPCs pointing at each other with no content._

### 6.6 Market (IODShop, pid 377) — Day only
- **[DONE]** IoDMStall (pid 394): Magic vendor — dispel Dog Collar curse (50g → Wolf's Rebuke), sell Strange Mushroom (40g)
- **[DONE]** IoDVStall (pid 395): Herbal vendor — sell Strange Mushroom (40g), buy Empty Bottle (10g)
- **[DONE]** IoDBStall (pid 396): Equipment vendor — Padded Helmet (20g), Obsidian Guards (40g), Padded Armour (30g), Magic Collar (25g)

### 6.7 Inn (IODInn, pid 378)
- **[DONE]** The inn exists.
- **[TBC]** Bounty Board: "Nothing available right now." **(EMPTY PLACEHOLDER)**
  - _Following the pattern: Holstein board has 3 quests, Scarhaven has 3 (1 playable), IoD has 0._

### 6.8 Dragon Houses / Caves (IoDHouses, pid 379)
- **[DONE]** DAYTIME — Cave exploration:
  - IoDCaves (pid 437): Pick a random cave (3 random encounters):
    - Den of sleeping hatchlings — kicked out by mother
    - Cave102 (pid 438): Mother Dragon + cute hatchling (observe)
    - Cave124 (pid 439): Two Dragons having sex → watch quietly (voyeur SS) or get caught
  - Cave203 (pid 436): Visit Hran at home (conditional: met him, 1/3 chance home)
    - Cave2032 (pid 440): Read grandfather's journal
    - Hran2SS1 (pid 441): Hran SS — tops/bottoms branching (6 passage tree)
    - Cave2033 (pid 442): Just friends option
- **[DONE]** NIGHTTIME — Hran training:
  - Hran (pid 404): Find Hran training
  - Hran1-3 (pids 405-407): Introduction, Magister reveal, mating curse discussion
    - HranSS1-3 (pids 408-411): SS chain → IoDHub
    - Hran4 (pid 409): Decline → IoDHub

---

# STUB & TBC INVENTORY — What Exists But Needs Finishing

## Stub Locations (In-Game Dead Ends)

| # | Location | PID | In-Game Message | Hub |
|---|----------|-----|-----------------|-----|
| 1 | Silver Spire | 40 | Guard: "Get the fuck out of here" | Holstein |
| 2 | Player Gear Shop | 174 | Hans: "Nothing in your size" | Scarhaven |
| 3 | Scarhaven Night Outskirts | 172 | "Nothing here. Go to bed." | Scarhaven |
| 4 | SQ3: Capture Bandit Leader | 299 | "Try this at another time" | Scarhaven |
| 5 | SQ4: Von Aldersant Request | 300, 305 | "Leave it for now" / empty passage | Scarhaven |
| 6 | Arena (Raln) | 376, 403 | "Not ready to spar yet" | IoD |
| 7 | IoD Bounty Board | 378 | "Nothing available right now" | IoD |

## Stub Systems (Mechanics Hinted But Not Built)

| # | System | Current State | Evidence |
|---|--------|--------------|----------|
| 1 | Wyatt Relationship | Hub exists, 0 activities | Tier structure + breakup implemented |
| 2 | Hans Relationship | Hub exists, 0 activities | Tier structure + breakup implemented |
| 3 | Combat/Training | No system | Arena placeholder, 3 MQu2 battles exist but ad-hoc |
| 4 | Player Equipment | No system | SBSC stub, IoD sells gear, no stat application |
| 5 | Item Usage | 8 items with no purpose | Items have descriptions hinting at function |
| 6 | Erel SS | Dialogue only | Only named NPC without SS content |
| 7 | Hran Relationship | SS exists, no relationship hub | Hran has depth (journal, training, multiple SS) but no formal system |

## Unused Items (Purchased/Found, Never Referenced Again)

| # | Item | Acquired At | Description Hint | Likely Purpose |
|---|------|------------|-----------------|----------------|
| 1 | Silver Orb | Holstein Market (20g) | "Glows dimly, unknown purpose" | Spire key? Magical focus? |
| 2 | Dog Collar | Holstein Market (30g) | "Kami refuses to put it on" / IoD can dispel curse → Wolf's Rebuke | Beast companion enabler |
| 3 | Ruby Necklace | Holstein Market (50g) | "Magister powers feel energy pulsing" | Adplagam artifact? Spire recognition? |
| 4 | Birdpup Feather | Finn (Scarhaven) | "Not sure what it's for... giggling child" | Pan's token, shrine resonance |
| 5 | Strange Mushroom | Forest Maze | "Magical property, sparkling" | Can sell (40g) at IoD, but intended use unclear |
| 6 | Speedband | Wyatt (Maze) | "Makes you run faster" | Never mechanically checked |
| 7 | Pain Leaves | Holstein Market | "Dulls pain you receive" | Combat consumable (no combat system) |
| 8 | Health Potion | Holstein Market | "Heals wounds, speeds regeneration" | Combat consumable (no combat system) |
| 9 | Empty Bottle | IoD Market (10g) | Standard empty bottle | Alchemy/crafting (no system) |
| 10 | Glass Ornament | Misfit (LM>1000) | Sentimental reward | Narrative only |
| 11 | Mysterious Gem | IoD Caves | "Red gem, whispers obscenities" | Unknown — most cryptic item |

## Dangling Plot Threads

| # | Thread | Setup Location | What's Known | Resolution |
|---|--------|---------------|-------------|------------|
| 1 | Hooded Mage identity | MQu2Finish (pid 359) | Fellow Magister, commands Dark Dragon | **NONE** |
| 2 | Strange Man in forest | MQ6, Frederick (Frc4) | Green-eyed, massive wolf, killing soldiers | **NONE** — may be same as #1 |
| 3 | Dark Dragon's origin | MQu2 mountain summit | Controlled by the Hooded Mage | **NONE** — IoD should care deeply |
| 4 | Valia (3rd IoD leader) | Zexir1DIsle2 (pid 419) | Named, role "unspecified" | **NONE** — never appears |
| 5 | Forest God Pan | Intro lore, dreams, Satyr | Blessed Magisters, Kami served him | **NONE** — Finn is likely his avatar |
| 6 | Alley night creature | Alley1N21 (pid 101) | Feral animal, Dirk senses aura | **NONE** — never identified |
| 7 | Council of Wizards | Kami dialogue | Track Magisters by signature, fear rogue | **NONE** — never contacted |
| 8 | Adplagam spies | Wyatt (Spire warnings) | Infiltrating the Spire | **NONE** — mentioned only |
| 9 | Kami's family (post-SQ2) | SQ2E | Aleida + children leave for forest | **NONE** — no follow-up |
| 10 | Seahome / The Bridge | Frederick (Frc1) | "Not like Seahome — poor bastards, bypass to The Bridge" | **NONE** — location never accessible |

---

# EXPANSION PLAN — FAITHFUL TO ORIGINAL INTENT

_Priority order: fill closest-to-done content first, then build outward._

---

## PHASE 1: Complete Existing Hubs (~85 new passages)

### 1A. Wyatt Relationship — Fill the Shell (~15 passages)
- **[EXPAND]** WyattRHub activities (matching Misfit's pattern):
  - Ask about himself: 4-5 dialogue topics (mercenary life, his brother at the Spire, past loves, fighting philosophy, what he wants from life)
  - Visit his place: His alley apartment (already established in Alley1N1). Cook together, spar, or relax.
  - SS activity: Dedicated relationship SS (distinct from the existing casual Alley1N SS)
  - Special outing (LM >= 500): He takes you to the rooftops at night — view of the city, the Spire lit up. Wholesome + intimate.
  - True ending (LM > 1000): Wyatt offers to travel with you permanently. Gift item: his mercenary badge.
- **[EXPAND]** Wyatt's brother at the Spire becomes a plot resource (see Phase 2)

### 1B. Hans Relationship — Fill the Shell (~15 passages)
- **[EXPAND]** HansRHub activities (matching Misfit's pattern):
  - Ask about himself: 4-5 dialogue topics (family trade, why he stayed in Scarhaven, Frederick's friendship, the war's toll, loneliness)
  - Visit his workshop: After hours. Help him forge something. Learn about smithing.
  - SS activity: Dedicated relationship SS (distinct from existing casual SBSHSS)
  - Special outing (LM >= 500): Picnic outside town, he shows you where he and Frederick used to play as kids. Vulnerable moment.
  - True ending (LM > 1000): Hans makes you a custom weapon/armor piece. Gift item: Master-forged Dirk Sheath (enhances your Dirk).
- **[EXPAND]** Player gear shop unlocks through relationship progress — Hans has "something in your size" after LM >= 250.

### 1C. Scarhaven Quests — Fill SQ3 and SQ4 (~30 passages)

#### SQ3 — Capture the Bandit Leader (200g, ~15 passages)
- **[TBC]** Quest is listed on the board. Stub says "try at another time."
- **[EXPAND]** Theme: TRACKING / COMBAT — military quest matching Scarhaven's martial tone
- **[EXPAND]** Frederick provides intel: bandits raiding supply caravans between Scarhaven and Seahome
- **[EXPAND]** Travel to bandit camp (forest/road setting). Use Beastmaster powers to scout (send Kami ahead, or use animal communication).
- **[EXPAND]** Encounter: The bandit leader is a desperate veteran, not purely evil. Driven to banditry by the war.
- **[EXPAND]** Branch: Capture by force (combat) / Negotiate surrender (persuasion) / Trick them (Kami diversion)
- **[EXPAND]** Return to Frederick. Reward + reputation. Frederick comments on your growing abilities.
- **[EXPAND]** Connection to Killian? The bandit leader may know Killian's group ("We worked with a man named Killian once").

#### SQ4 — Von Aldersant: A Request (300g, ~15 passages)
- **[TBC]** Quest is listed: "A rather delicate request... seeking children." SQu41 (pid 305) is the empty continuation.
- **[EXPAND]** Theme: INVESTIGATION / MORAL COMPLEXITY — matches the darker undertone
- **[EXPAND]** A noble family (Von Aldersant) lost children during the war. They want them found.
- **[EXPAND]** Investigation: Travel to locations, use animal allies to search. Question villagers.
- **[EXPAND]** Discovery: The children were taken by a Beastmaster-like figure (controlled animals carried them away). Early hint at the Hooded Mage's broader activities.
- **[EXPAND]** Branch: Find the children (alive, with animals in the wild, they've adapted) / Find evidence they're gone (darker resolution)
- **[EXPAND]** Moral choice: Return them to the noble family (reward) or realize they're safer in the wild (less reward, but compassion)
- **[EXPAND]** Plot hook: The animal behavior connects to the Strange Man investigation.

### 1D. Scarhaven Night Content (~8 passages)
- **[TBC]** ScarOther night is a stub. Barracks/Inn have no distinct night content.
- **[EXPAND]** Outskirts at night: A wounded traveler from the road. News of attacks near Seahome. Possible SS.
- **[EXPAND]** Barracks at night: Frederick working late. More personal, less guarded. Exclusive night dialogue about the investigation and his past. Possible SS path.
- **[EXPAND]** Inn at night: Different atmosphere. A traveling merchant from Adplagam. Introduces eastern continent culture. Wes is more talkative at night.

### 1E. IoD Arena — Raln Content (~12 passages)
- **[TBC]** Arena is a placeholder. Raln is fully described but has no content.
- **[EXPAND]** Raln training system (narrative combat, not stat-based):
  - First session: Raln tests you. "You're scrawny, but let's see what you've got." Teach basic defense.
  - Progression: 3 training tiers matching the relationship tier pattern.
  - Tier 1: Basic sparring — learn to dodge, Kami assists. Raln grudgingly impressed.
  - Tier 2: Weapons training — Raln gives you a practice sword. Teaches discipline.
  - Tier 3: Beast+Warrior combo — integrate Beastmaster powers with combat. Kami and player fight as a unit.
- **[EXPAND]** Raln dialogue (4 topics matching other NPCs):
  - His role on IoD, why he's wingless, his fighting philosophy, what he thinks of Zexir
- **[EXPAND]** Raln SS: After training trust is established. Raln is gruff but tender.
- **[EXPAND]** Connect to Zexir1DFight: Link now leads to actual content instead of circular redirect.
- **[EXPAND]** Combat training unlocks narrative advantages in future encounters.

### 1F. IoD Bounty Board — 2 Quests (~20 passages)

#### IoD Quest 1 — The Dark Dragon's Trail (~12 passages)
- **[TBC]** Board is empty. The Dark Dragon is the reason you're on IoD.
- **[EXPAND]** Theme: INVESTIGATION — the IoD leaders want answers about the controlled dragon
- **[EXPAND]** Zexir asks you to investigate: "A dragon controlled by a Magister. This is unprecedented."
- **[EXPAND]** Search for traces: Caves where the Dark Dragon rested, claw marks, residual magic
- **[EXPAND]** Use Volition spells to detect magical signatures. Fireball reveals hidden traces.
- **[EXPAND]** Discovery: The Dark Dragon was a young IoD dragon that went missing years ago. Valia's records confirm.
- **[EXPAND]** Introduces Valia as a character (resolves her "unspecified" role — she keeps records/history)
- **[EXPAND]** Reward: Zexir's Amulet (if not already obtained — formalizes IoD trust in you)

#### IoD Quest 2 — The Hatchling Problem (~8 passages)
- **[EXPAND]** Theme: BEAST TAMING — using your powers to help dragons
- **[EXPAND]** A clutch of hatchlings has gone feral — won't respond to dragon parents
- **[EXPAND]** Erel asks for your help: "Your powers work on all animals. Dragons are animals too."
- **[EXPAND]** Navigate to the hatchling den (established cave system). Calm them with Beastmaster magic.
- **[EXPAND]** Erel's expanded role: Works alongside you, his veterinary knowledge + your powers
- **[EXPAND]** Opens Erel SS path (if desired): The collaboration creates intimacy.
- **[EXPAND]** Reward: Dragon parents grateful. Standing on IoD increases.

### 1G. Valia — Third Leader (~5 passages)
- **[TBC]** Named in Zexir1DIsle2 (pid 419). Never appears.
- **[EXPAND]** Role: Historian / Archivist / Records Keeper (completes the triumvirate: Zexir=Magic, Raln=Military, Valia=History)
- **[EXPAND]** Location: Library or archive room off the Council Chamber
- **[EXPAND]** Dialogue (4 topics): IoD history, dragon lineages, the Dark Dragon's identity, Magister legends
- **[EXPAND]** She knows more about Magisters than Zexir — has ancient texts
- **[EXPAND]** Plot critical: Her records reveal that the Hooded Mage was once known to the Council

---

## PHASE 2: The Silver Spire Opens (~25 new passages)

### 2A. Gaining Access
- **[TBC]** HubSpire is a dead end. Access must gate behind progress.
- **[EXPAND]** Trigger: After MQu2 completion (you've fought the Hooded Mage, proven yourself)
- **[EXPAND]** Method A: Frederick writes a letter of recommendation. Guard reluctantly admits you.
- **[EXPAND]** Method B: Wyatt's brother (established in Alley1N) lets you in through a side entrance at night.
- **[EXPAND]** Method C: If Wyatt relationship is active, he arranges a meeting through his brother.

### 2B. Spire Interior (~18 passages)
- **[EXPAND]** SpireEntry: Grand military interior. Imposing scale. Guards, banners, war table.
- **[EXPAND]** SpireHall: Main corridor — soldiers, officials. Map of Orbath on the wall (matches Zexir's map lore).
- **[EXPAND]** Social NPC: An aide or junior officer who's sympathetic to you. Dialogue tree (4 topics): the war effort, Adplagam threats, the King, rumors of the Strange Man.
- **[EXPAND]** SpireAudience: Meet a general or advisor (not the King yet).
  - They've heard of your abilities. "A Magister working with the Empire could turn the tide."
  - Choice: Accept a formal role (gain access + resources, lose freedom) / Decline (maintain independence, limited Spire access)
- **[EXPAND]** SpireBarracks: Military quarters.
  - Service: Military-grade equipment shop — player gear (resolves SBSC intent)
  - SS encounter: Guard or officer (1-per-sublocation pattern)
- **[EXPAND]** Silver Orb purpose: Resonates with Spire magic. Acts as a pass or focus item.
- **[EXPAND]** Ruby Necklace: An officer recognizes it as Adplagam-made. "Where did you get this?" Opens espionage subplot.

### 2C. Spire Plot Advancement (~7 passages)
- **[EXPAND]** The Spire has intelligence: The Hooded Mage has been tracked toward Seahome / The Bridge.
- **[EXPAND]** Frederick's lead (Frc4) finally resolves: "We have a sighting near The Bridge."
- **[EXPAND]** The Council of Wizards has sent a formal request — they know about the rogue Magister.
- **[EXPAND]** Kami's reaction: "Should the Council hear about it, they might seek us out." — his own words come true.
- **[EXPAND]** Mission: You're asked to investigate Seahome. The Spire provides a carriage pass.

---

## PHASE 3: Seahome — The Bridge Town (New Hub, ~90 new passages)

### 3A. Travel & Arrival
- **[EXPAND]** Carriages updated: Holstein ↔ Scarhaven ↔ Seahome
- **[EXPAND]** Frederick's lore (Frc1): "Seahome is the bypass to The Bridge. Lots of traffic."
- **[EXPAND]** Carriage ride: Landscape shifts from farmland to coastal. Kami is tense.

### 3B. Seahome Hub (~8 passages)
- **[EXPAND]** Theme: CROSSROADS / TRADE / PARANOIA — everyone passes through, nobody stays
- **[EXPAND]** Bustling but anxious. Larger than Scarhaven, smaller than Holstein. Built around The Bridge.
- **[EXPAND]** Day/night cycle. 5 sub-locations (matching hub density pattern).

### 3C. The Tavern (~15 passages)
- **[EXPAND]** Service NPC: Tavern keeper (new species — Equine or Ursine)
- **[EXPAND]** Social NPC: Traveling scholar who knows Magister history
  - Reveals: Multiple Magisters have existed over the centuries. Most vanished or went mad.
  - "The Awakening is meant to be guided by a senior Magister. Yours... wasn't."
- **[EXPAND]** Room rental, Kami SS (reuse existing system)
- **[EXPAND]** Bounty board: 2 quests
- **[EXPAND]** SS encounter: Tavern patron or worker

### 3D. The Docks/Market (~13 passages)
- **[EXPAND]** Trade hub — goods from both continents. Exotic items and Kami gear upgrades.
- **[EXPAND]** Social NPC: Adplagam merchant — first direct eastern continent contact
  - Dialogue: Life in Adplagam, what they know about Magisters, rumors of war
  - Possible spy? Trust theme continues from Scarhaven.
- **[EXPAND]** Strange Mushroom identification: An alchemist here identifies it as a "Mindshroom" — enhances magical perception.
- **[EXPAND]** Empty Bottle purpose: Alchemist can brew a potion with the Mindshroom if you bring both.

### 3E. The Bridge (~15 passages)
- **[EXPAND]** A massive ancient stone structure. Heavily guarded. Covered in old carvings.
- **[EXPAND]** Investigation: Talk to guards, find claw marks, sense residual magic
- **[EXPAND]** Kami identifies carvings as old Magister symbols. "This bridge was built by Magisters."
- **[EXPAND]** Discovery: The Hooded Mage crossed here heading east. Toward Adplagam.
- **[EXPAND]** Gate: Can't cross yet. Need Spire authorization or another means.
- **[EXPAND]** Social NPC: Bridge guard captain — war stories, security concerns, recent incidents
- **[EXPAND]** Birdpup Feather reacts here — warmth, giggling, Finn's presence?

### 3F. A Shrine to Pan (~10 passages)
- **[EXPAND]** Small, overgrown shrine hidden behind the town
- **[EXPAND]** Your Dirk resonates. Birdpup Feather glows.
- **[EXPAND]** Meditation: Advance $pk. New power: Beast Sight (see through animal eyes)
- **[EXPAND]** Finn appears if you have the feather. More forthcoming:
  - Hints at his nature (avatar of Pan? Birdpup spirit?)
  - "You'll need to be stronger for what's coming."
  - Cryptic clue about the Hooded Mage's identity

### 3G. Back Alleys (~10 passages)
- **[EXPAND]** Pattern match: Every hub has a dangerous/seedy underbelly
- **[EXPAND]** Night: Encounter Adplagam spy who mistakes you for an ally
- **[EXPAND]** Day: Street urchins, information broker, underground market
- **[EXPAND]** SS encounter: Spy or local
- **[EXPAND]** Plot: Learn Adplagam is actively seeking Magisters — they want to weaponize the power

### 3H. Seahome Quests (~30 passages)

#### Seahome Quest A — The Bridge Incident (~18 passages)
- **[EXPAND]** Animals attacking travelers on The Bridge at night
- **[EXPAND]** Theme: BEAST TAMING LEVEL 2 — larger, more dangerous creatures
- **[EXPAND]** Dungeon: The Bridge at night (linear, 6-8 nodes)
- **[EXPAND]** Boss: Massive beast controlled by residual magic left by the Hooded Mage
- **[EXPAND]** Resolution: Calm the beast, find a magical anchor (item left to keep the beast aggressive)
- **[EXPAND]** Take evidence to Frederick or the Spire. Bridge access unlocked.

#### Seahome Quest B — The Missing Merchant (~12 passages)
- **[EXPAND]** Adplagam merchant gone missing near town
- **[EXPAND]** Theme: TRUST / ESPIONAGE
- **[EXPAND]** Use Beast Sight to track them
- **[EXPAND]** Discovery: Kidnapped by Empire soldiers who suspected espionage
- **[EXPAND]** Choice: Help escape (gain Adplagam contacts) or turn in (gain Empire reputation)
- **[EXPAND]** Consequence: Affects how Adplagam and the Spire treat you

---

## PHASE 4: Main Plot Resolution (~145 new passages)

### 4A. The Investigation Converges (~8 passages)
- **[EXPAND]** Present evidence from Seahome to the Spire
- **[EXPAND]** The Hooded Mage is identified: a former Magister gone rogue — same pattern as Dinus's warlock story
- **[EXPAND]** He crossed into Adplagam, building an army of controlled beasts
- **[EXPAND]** Council of Wizards formally requests Reliquim's cooperation
- **[EXPAND]** Mission: Cross The Bridge, track the rogue Magister, report back
- **[TBC]** King Adalrico: Brief audience. Acknowledges you. "We need you, Magister."

### 4B. Frederick's Resolution (~6 passages)
- **[TBC]** Frc4 resolves: "I have a lead."
- **[EXPAND]** Frederick provides soldiers, supplies, a contact in Adplagam
- **[EXPAND]** Personal stake: The Strange Man killed his soldiers. This is personal.
- **[EXPAND]** Optional deeper relationship with Frederick (dialogue + SS)

### 4C. Kami's Conflict (~6 passages)
- **[EXPAND]** Kami is torn. Family safe (SQ2), but crossing into Adplagam means leaving Reliquim.
- **[EXPAND]** Emotional dialogue: "I have followed you faithfully, Master. But I fear what lies ahead."
- **[EXPAND]** Choice: Reassure Kami / Acknowledge danger / Offer to release him
  - Releasing: He refuses. "I will not leave you. You are my Master, and my friend."
- **[EXPAND]** Kami reveals: Pan warned him. "He said you would face another of your kind."

### 4D. Crossing The Bridge (~10 passages)
- **[EXPAND]** Authorized crossing. Ancient carvings = old Magister symbols.
- **[EXPAND]** Midway: Sense the Hooded Mage's magic strongly. Recent presence.
- **[EXPAND]** Birdpup Feather reacts — warmth, giggling.
- **[EXPAND]** Eastern shore: Adplagam is visually different — darker forests, different architecture.
- **[EXPAND]** Kami on edge. Animals respond differently to your magic here.

### 4E. Adplagam Border Town (New Hub, ~55 passages)
- **[EXPAND]** Theme: ENEMY TERRITORY / FISH OUT OF WATER
- **[EXPAND]** People distrust Reliquim citizens. Kami draws suspicion.
- **[EXPAND]** 5 sub-locations: Inn, Market, Shrine/Temple, Underground, Outskirts
- **[EXPAND]** 4-5 new NPCs with dialogue trees + SS chains
- **[EXPAND]** The Hooded Mage has been here. Trail of controlled beasts.
- **[EXPAND]** 2 local quests matching hub density

### 4F. The Pursuit (~20 passages)
- **[EXPAND]** Follow the trail through Adplagam
- **[EXPAND]** 2-3 encounters of escalating difficulty
- **[EXPAND]** $pk reaches maximum. New abilities unlock.
- **[EXPAND]** Learn the Hooded Mage's identity and motivation:
  - A Magister who lost control. Magic addiction (Dinus's foreshadowing).
  - Believes Pan abandoned him. Wants to destroy the Magister system.
  - Building a beast army to attack Holstein and the Spire.

### 4G. The Council of Wizards (~15 passages)
- **[EXPAND]** Reachable from Adplagam coast or by magical means
- **[EXPAND]** Island in the central ocean. Ancient, powerful, morally ambiguous.
- **[EXPAND]** They want the Hooded Mage stopped — but they also want to control YOU
- **[EXPAND]** Choice: Accept Council help (power boost, strings attached) / Refuse (harder path, freedom)

### 4H. Confrontation (~20 passages)
- **[EXPAND]** The Hooded Mage's lair: corrupted forest/cave
- **[EXPAND]** His beast army: the massive wolf from MQ6 (fully under control) + others
- **[EXPAND]** Dungeon: Multi-stage encounter using accumulated powers and items
- **[EXPAND]** The Hooded Mage is not a monster — he's broken.
  - Theme matches SQ1 (Dragon diplomacy): Violence vs. compassion vs. compromise
- **[EXPAND]** Choices:
  - Destroy him (use full power, risk magic addiction yourself)
  - Redeem him (empathy, Beastmaster bond — hardest path)
  - Imprison him (Council's preference — morally grey)
- **[EXPAND]** The massive wolf recognizes your authority — callback to MQ10 alpha bowing

### 4I. Resolution & Epilogue (~10 passages)
- **[EXPAND]** Return to Holstein. Report to the Spire.
- **[EXPAND]** Frederick's reaction (depends on trust level from SBaF3)
- **[EXPAND]** Kami: "You have grown, Master."
- **[EXPAND]** Finn appears one final time — reveals his true nature
- **[EXPAND]** Birdpup Feather's purpose: Pan's gift. A token of the god's faith in you.
- **[EXPAND]** Epilogue: Your place in the world (choices reflecting relationship, faction, and moral decisions)

---

# SYSTEMS TO BUILD

## S-1. Narrative Combat
- **[SYSTEM]** Not stat-heavy — narrative choices during encounters
- **[SYSTEM]** Options: Fight / Calm (Beastmaster) / Flee / Use Item
- **[SYSTEM]** Health Potion and Pain Leaves become functional
- **[SYSTEM]** Kami equipment provides narrative advantages ("Kami's helm deflects the blow")
- **[SYSTEM]** Player equipment provides similar bonuses
- **[SYSTEM]** Raln's training (Arena) unlocks advanced combat options
- **[DONE]** Precedent: MQu2 has 3 ad-hoc battle encounters (Gnoll, Insect Swarm, Pigorc)

## S-2. Power Progression ($pk levels)
- **[DONE]** $pk=0: No powers (pre-MQ1)
- **[DONE]** $pk=1: Calming Spell — green mist, pacifies animals (learned MQ8)
- **[DONE]** Volition Light — basic illumination (learned from Zexir)
- **[DONE]** Volition Fireball — combat spell (learned from Zexir)
- **[EXPAND]** $pk=2: Animal Communication — sense emotions, basic intent
- **[EXPAND]** $pk=3: Beast Sight — see through animal eyes temporarily
- **[EXPAND]** $pk=4: Beast Bond — temporarily control a single animal
- **[EXPAND]** $pk=5: Full Dominion — mass control (the power the Hooded Mage abuses)

## S-3. Reputation Tracking
- **[DONE]** Frederick trust check (SBaF3 — success/partial/fail)
- **[DONE]** Misfit LoveMeter (0-1000+, fully functional)
- **[TBC]** Wyatt LoveMeter (tier structure exists, nothing feeds into it)
- **[TBC]** Hans LoveMeter (tier structure exists, nothing feeds into it)
- **[EXPAND]** Iron Empire / Spire reputation (quest completions, Spire access choices)
- **[EXPAND]** Adplagam reputation (merchant quest choice in Seahome)
- **[EXPAND]** Council of Wizards reputation (endgame)
- **[EXPAND]** IoD standing (quest completions, Zexir/Raln trust)

## S-4. Item Resolution
- **[TBC]** Silver Orb → Spire key, magical focus, or resonance item
- **[TBC]** Dog Collar → Beast companion enabler (Wolf's Rebuke version from IoD dispel)
- **[TBC]** Ruby Necklace → Adplagam artifact recognized by NPCs
- **[TBC]** Strange Mushroom → Mindshroom (Seahome alchemist identifies), enhances magical perception
- **[TBC]** Birdpup Feather → Pan's token, resonates at shrines, reveals Finn's nature
- **[TBC]** Empty Bottle → Alchemy ingredient (combine with Mindshroom for perception potion)
- **[TBC]** Mysterious Gem → "Whispers obscenities" — cursed item? IoD dragon artifact? Ties to Dark Dragon?
- **[EXPAND]** Pain Leaves → Combat consumable: "Kami chews the leaves and shrugs off the blow"
- **[EXPAND]** Health Potion → Combat consumable: Restores after encounters
- **[EXPAND]** Speedband → Flee bonus: "Wyatt's headband gives you a burst of speed"

## S-5. Day/Night Completion
- **[DONE]** Holstein: Full day/night split (Alley, Fountain, Market day-only)
- **[DONE]** Scarhaven: Partial (Hans day/night, Outskirts night = stub)
- **[DONE]** IoD: Partial (Erel/Arena/Market day-only, Hran/Zexir night content)
- **[SYSTEM]** Every sub-location should have meaningful day AND night content
- **[SYSTEM]** Night pattern: More intimate/dangerous encounters, different NPCs
- **[SYSTEM]** Time advances: Sleep (full cycle), travel (auto-set), certain actions (partial)

---

# EXPANSION SUMMARY

```
                                        PASSAGES    STATUS
PROLOGUE (Awakening)                      ~35       [DONE]
ACT 1: Holstein                          ~120       [DONE]
  - Silver Spire interior                 ~25       [EXPAND] (Phase 2)
ACT 2: Scarhaven                          ~60       [DONE]
  - SQ3 + SQ4 quests                      ~30       [EXPAND] (Phase 1C)
  - Night content                           ~8       [EXPAND] (Phase 1D)
  - Relationship completion                ~30       [EXPAND] (Phase 1A-B)
ACT 2.5: Main Quest 2 (Mountain)          ~30       [DONE]
ACT 3: Isle of Dragons                    ~80       [DONE]
  - Arena (Raln)                           ~12       [EXPAND] (Phase 1E)
  - IoD quests + Valia                     ~25       [EXPAND] (Phase 1F-G)
ACT 3.5: Seahome (new hub)               ~90       [EXPAND] (Phase 3)
ACT 4: Main Plot Resolution             ~145       [EXPAND] (Phase 4)

CURRENT BUILD:                           ~465 passages
PHASE 1 (Complete existing):              ~85 new passages  →  ~550
PHASE 2 (Silver Spire):                   ~25 new passages  →  ~575
PHASE 3 (Seahome):                        ~90 new passages  →  ~665
PHASE 4 (Resolution):                    ~145 new passages  →  ~810

PROJECTED FINAL BUILD:                   ~810 passages
```

---

# OPTIONAL: RETURNING CHARACTERS

## Killian — Return Arc
- **[EXPAND]** Killian (Avian mercenary from Prologue) reappears in Seahome or Adplagam
- **[EXPAND]** Recognizes you, impressed by growth. "You've changed since the forest, kid."
- **[EXPAND]** Optional companion for dangerous quests. Dialogue + SS chain.
- **[EXPAND]** His men may have intel on the Hooded Mage (mercenaries hear things).

## Kami's Family — Reunion
- **[EXPAND]** Post-SQ2, Kami's family (Aleida, Vesper, Berion, Saige, Eike) left for the forest
- **[EXPAND]** Possible reunion during forest travel. Kami's emotional arc deepens.
- **[EXPAND]** Eike remembers you. The children have grown.

## Hran — Relationship Path
- **[EXPAND]** Hran has SS content but no formal relationship system
- **[EXPAND]** If relationship system added: Activities (training together, reading grandfather's journal, exploring caves), true ending (Hran asks to leave IoD and travel with you).
