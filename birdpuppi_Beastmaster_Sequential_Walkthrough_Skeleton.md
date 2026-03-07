# Way of the Beastmaster — Sequential Walkthrough & Expansion Skeleton

## Status Key
```
[DONE]     = Fully implemented in the current build
[TBC]      = Hinted at, set up, or partially stubbed — needs completion
[EXPAND]   = New content faithful to established lore, themes, and patterns
[SYSTEM]   = Mechanical system that needs building
```

## Established Lore Bible (Canon Reference)
```
WORLD:     Orbath (oval island). Two continents: Reliquim (West), Adplagam (East).
           Vast ocean in the center — Council of Wizards resides there.
CAPITAL:   Holstein, home of the Silver Spire (Iron Empire HQ).
KING:      Adalrico Dominus, rules from atop the Spire.
RELIGION:  Pan, the Great Forest God (a Satyr). Blesses Magisters via ritual.
MAGIC:     Magisters = animal controllers. Green mist from fingertips.
           Blessing = control over animals. Curse = pheromones that make animals want you.
           Magister's Dirk = amplifier dagger, "all Magisters are given one."
           Magic addiction exists — can corrode the mind (Rogue Warlock precedent).
VILLAIN:   The Strange Man — another Magister using powers for evil.
           Seen in the forest with a massive wolf (red eyes). Green glowing eyes.
           Frederick is tracking him. Kami says "it could spell doom for all of Orbath."
           Could control Dragons, spark wars.
COUNCIL:   "Should the Council hear about it, they might seek us out" — Kami.
           They track Magisters by magical "signature."
COMPANION: Kami — wolf, served Pan for years, granted speech at your Awakening.
           Had a wife (Aleida) and 4 children (Vesper, Berion, Saige, Eike).
           Eike rescued during SQ2 (Wrenville wolves quest).
PLAYER:    Amnesiac. Woke naked in the Forest of Madness after a botched Awakening.
           "There must have been a problem with the Awakening" — Kami.
           Missing their Dirk ("I do not know why you did not have one" — Kami).
           Birthright Magister — this is inherited, not learned.
TOWNS:     Holstein (capital), Scarhaven (farming village), Streamdale (dragon mountains),
           Wrenville (northern trade route), Seahome (bypass to The Bridge).
FACTIONS:  Iron Empire (military, the Spire), Bandits/Mercenaries (Killian's group),
           Adplagam spies (infiltrating the Spire), The Council of Wizards.
FINN:      White-furred boy in Scarhaven Inn. Knows your name before you tell him.
           Gives you a Birdpup Feather. "You can hear a child giggling in the back
           of your mind." Fourth-wall break: "Stay tuned for more exciting things."
           Likely an avatar of Pan, or the developer's self-insert/guide character.
```

---

# PROLOGUE: AWAKENING

## P-1. Title Screen
- **[DONE]** New Game / Load Game

## P-2. The Forest of Madness — Waking Up
- **[DONE]** Intro1: Wake up cold, naked, amnesiac, surrounded by broken glass (mirror?)
- **[DONE]** Species selection: Canine / Feline / Vulpine / Avian / Reptile / Dragon
- **[DONE]** Full character creation chain: Age → Body → Height → Hair → HairC → Eye → Cock → DickL
- **[DONE]** CharacterFinish: Review yourself one last time

## P-3. Meeting Kami
- **[DONE]** Intro2: Wander the cold forest, need shelter
- **[DONE]** Intro3: A talking Wolf appears — Kami introduces himself
- **[DONE]** Dialogue options (explore all before continuing):
  - Intro3c1: "What is a Magister?" — dominion over animals, blessing & curse, pheromones
  - Intro3c2: "Why can you talk?" — Pan blessed him, served Pan for years
  - Intro3c3: "Where am I?" — Forest of Madness, 3 miles south of Holstein
- **[DONE]** Intro3c4: Decide to get moving, Kami leads

## P-4. The Bandits
- **[DONE]** Intro4: Walking for hours, exhausted
- **[DONE]** Intro5: Ambushed by Killian's group (mercenaries, not bandits)
- **[DONE]** Intro6: Killian gives you clothes. Optional Kami dialogue:
  - Kami1c1: "Should we trust Killian?" — Kami is wary
  - Kami1c2: "Can you really talk?" — Kami explains why he was silent
  - Kami1c3: "Tell me about my powers" — Kami says you need to explore them
- **[DONE]** Intro7: Sleep under the stars. Something touched you in the night.
- **[DONE]** Intro8: Killian explains Holstein, the Spire, the Iron Empire
- **[DONE]** Intro9: Travel together to the capital
- **[DONE]** Intro10: Killian says goodbye at the gates. "This is where we part ways."
- **[DONE]** TheBeginning: "Your journey begins. Here, and now." → Hub

---

# ACT 1: HOLSTEIN — THE CAPITAL

## Chapter 1: Getting Your Bearings

### 1.1 The Hub (Holstein Square)
- **[DONE]** Hub: Central square with marble fountain, Silver Spire visible overhead
- **[DONE]** Day/night descriptions, 7 exits
- **[DONE]** Persistent footer: Character sheet / Inventory / Talk to Kami (KamiMenu)
- **[DONE]** KamiMenu: Dynamic dialogue that unlocks based on flags:
  - Powers explanation (evolves with $pk)
  - "Will I end up like that Rogue Warlock?" (after DinusI)
  - "Are you mad I have sex with strangers?" (after MisfitF)
  - "What is the Magister's Dirk?" (after acquiring it)

### 1.2 The Inn — Dinus the Bear
- **[DONE]** HubInn: Arrive at the inn, see the bounty board and counter
- **[DONE]** InnStay: Meet Dinus — 8-foot bear innkeeper, kind, fatherly
- **[DONE]** InnStayPay: Rent a room (10 gold) → InnStayRoom
- **[DONE]** InnStayRoom: Your room. Three options:
  - KamiSS1: Sex with Kami (top or bottom, branching)
  - HolsteinKEquip: Equip Kami's gear (Helm/Collar/Paws/Back slots)
  - InnStaySleep: Sleep → next day → HubInn
- **[DONE]** DinusI → DinusI2: Dinus's backstory — tells of a Rogue Warlock in the Forest of Madness. "His eyes were glowing green." Dinus beheaded him but lost his squad. Retired, opened the inn.
- **[DONE]** DinusSS1-5: Dinus sexual encounter chain (under the counter)

### 1.3 The Fountain Square
- **[DONE]** HubFount: The great fountain, mercenaries sparring
- **[DONE]** FountD1 → Wyatt1: Meet Wyatt (daytime). Muscular canine, blue-grey fur, green eyes. Experienced fighter. Becomes your mentor/friend.
- **[DONE]** Wyatt2: Return visits — 4 dialogue topics:
  - Wyatt2c1: The Silver Spire — "King Adalrico Dominus resides at the top"
  - Wyatt2c2: Wyatt's past — grew up rough, self-made
  - Wyatt2c3: Making money — errands, mercenary work
  - Wyatt2c4: Places to avoid — alleys, and the Spire (Adplagam spies, violent guards)
- **[DONE]** FountD2: Sit and relax, take in the sights
- **[DONE]** FountN1: Night — a hooded Rat figure at the fountain
  - FountN11: Agree to his demands (sexual encounter with potion)
  - Decline → Hub
  - Returns on subsequent nights (Misfit or Rat revisit variants)

### 1.4 The Market
- **[DONE]** HubMarket: Three stalls
- **[DONE]** MarkMagic: Magic items stall (Reptilian woman)
  - Buy: Silver Orb (20g), Dog Collar (30g), Ruby Necklace (50g)
  - MarkMagicF1: Sell Magic Flower for 100g
- **[DONE]** MarkHerb: Herb stall
  - Buy: Pain Leaves, Health Potion, Endowment Potion
  - EPFuck → EPFuck2: Drink the Endowment Potion (blackout, size change)
- **[DONE]** MarkPed: Peddler in the back (Raccoon)
  - MarkPed2: Discover the Magister's Dirk (10g)
  - MarkPed22: Buy it — vision of power, Kami excited, explains what it is
  - MarkPed23: Decline — Kami whines

### 1.5 The Silver Spire
- **[DONE]** HubSpire: Walk toward the Spire, guards everywhere, guard threatens you
- **[TBC]** Currently a dead end — guard says "Get the fuck out of here"
  - _The Spire is referenced constantly: King Adalrico, Iron Empire HQ, Adplagam spies, military command. This is the most important locked location in the game._

### 1.6 The Alley — Daytime
- **[DONE]** Alley1D: Wander the back streets
- **[DONE]** MisfitI: Meet Misfit the Ratman — alchemist, brews potions underground, trades beer with Dinus
- **[DONE]** MisfitSS1: Sexual encounter with Misfit

### 1.7 The Alley — Nighttime
- **[DONE]** Alley1N: Dangerous at night, two paths:
  - Alley1N1: Peek in illuminated window → WyattSS1-SSE: Discover Wyatt lives here (his brother works night shift at the Spire as a guard). Share a meal, optional sexual escalation chain.
  - Alley1N2 → Alley1N21: Approach dark figure at end of alley. Feral animal attacks, use Dirk to calm it with powers, escape.

---

## Chapter 2: The Quests

### 2.1 The Bounty Board (Holstein Inn)
- **[DONE]** InnQuests: Three postings on the board

### 2.2 Main Quest — King's Decree: The Forest Hunt
- **[DONE]** MQ1: Royal decree from King Adalrico — hunt wild animals near Scarhaven (500g reward)
- **[DONE]** MQ2: Ask Dinus about transport. Carriage or walk.
- **[DONE]** MQ3: Travel to Scarhaven
- **[DONE]** MQ4: Arrive at Scarhaven, see the village and forest
- **[DONE]** MQ5: Enter command tent — soldiers draw weapons on Kami, you explain
- **[DONE]** MQ52: Briefing — hunt animals in the forest, bring back a head
- **[DONE]** Maze (4x4 grid, 16 nodes): Navigate the Forest of Madness
  - Items: Strange Mushroom (Maze12 area), Speedband (Wyatt's headband)
  - Dead mercenaries, bodies, escalating tension
  - Maze11: Find the Strange Man with his massive wolf (red eyes, green-eyed figure)
- **[DONE]** MQ6: Approach the figure — something evil, crackling with power
- **[DONE]** MQ7: Run. The massive wolf chases you. Trip on a root.
- **[DONE]** MQ8: Tap into your power — first real use of Beastmaster magic
- **[DONE]** MQ9: Command wolves to retreat — green mist bombs
- **[DONE]** MQ10: Wolves calm. Alpha howls, bows to you, leaves.
- **[DONE]** MQ11: Collapse. Wake in tent. Meet Frederick (feline captain, king's insignia). He gives you 500g. "We'll make a soldier of you yet."
- **[DONE]** MQ12: Carriage ride back. Kami warns: "A Magister using magic for evil... doom for all of Orbath." Council might seek you out. Sets $MQ1D=1, $pk=1.

### 2.3 Side Quest 1 — Streamdale: Evict the Dragon (100g)
- **[DONE]** SQ1 → SQ11: Accept quest, travel to Streamdale
- **[DONE]** SQ12: Carriage or walk. Discuss strategy with Kami.
- **[DONE]** SQ13: Arrive — dragon damage, smoke, burned crops
- **[DONE]** SQ14: Carriage up the mountain, enter cave above the clouds
- **[DONE]** SQ15: Mercenary enters first — killed instantly
- **[DONE]** SQ16: Dragon recognizes you as a Magister
- **[DONE]** SQ17: 1 adult dragon + 3 whelps. He's protecting his children. Branch:
  - SQ1SS1 → SQ1SS2-4 → SQ1SSE: Sexual compromise with whelps → dragon agrees
  - SQ18: Negotiate diplomatically (multiple outcomes at SQ19/SQ1E depending on approach)
- **[DONE]** SQ1E: Return to Streamdale mayor. Multiple endings based on approach:
  - Dragon leaves peacefully (scale as proof)
  - Dragon stays but promises peace (mayor may or may not accept)
  - Failure (mayor disappointed but thanks you)

### 2.4 Side Quest 2 — Wrenville: Wolves on the Trade Route
- **[DONE]** SQ2 → SQ21: Accept quest, ask Dinus about Wrenville
- **[DONE]** SQ22: Travel. Find wrecked carriage on the trade route.
- **[DONE]** SQ23: Mercenaries tell you to stand back
- **[DONE]** SQ24: Kami recognizes the wolves — Aleida (his wife) and their children. Eike (youngest) captured by mercenaries.
- **[DONE]** SQ25: Convince mercenaries to let you stay, or sneak
- **[DONE]** SQ2E: Rescue Eike from the cage at night. Kami's family reunites and leaves for the forest. Quest complete.

---

# ACT 2: SCARHAVEN — THE VILLAGE

## Chapter 3: A Second Home

### 3.1 Travel & Arrival
- **[DONE]** Carriages: Holstein ↔ Scarhaven travel system
- **[DONE]** ScarHub: Arrive at the small farming village. Day/night descriptions.

### 3.2 The Blacksmith — Hans the Corgi
- **[DONE]** ScarBS: Visit the blacksmith's shop
- **[DONE]** SBSK: Browse Kami gear — purchase Battle Helm, Spiked Collar, Claw Guards, Pack Saddle
- **[DONE]** SBSC: Browse player gear — "Nothing in your size, come back another time"
- **[DONE]** SBSH: Talk to Hans (daytime) — 4 dialogue topics + Frederick reference:
  - SBSHc1: His job — generations of family blacksmiths, supplies the Empire militia
  - SBSHc2: Personal life — awkward, deflects, asks about you
  - SBSHc3: Sex life — leads to SBSHSS chain (3 size variants: small/medium/large)
  - SBSHc4: The war — sour expression, then recovers
  - SBSHf: About Frederick — knows him, directs you
- **[DONE]** SBSHn: Visit Hans at night — knock on his door
  - SBSHn2: Stay the night, cuddle
  - SBSHn3: Wake up together → ScarHub

### 3.3 The Inn — Wes, Finn, and the Stables
- **[DONE]** ScarInn: Quieter than Holstein. Multiple options:
- **[DONE]** SIIK → SIIK2: Talk to Wes (Shark innkeeper). Rent room (10g).
  - SIIKR: Room — Kami SS / equip gear / sleep
  - SIIKRS: Sleep → ScarInn
- **[DONE]** SIB: Scarhaven bounty board — "words magically fade from vision"
- **[DONE]** Finn: Mysterious white-furred boy. Gives you the Birdpup Feather. Knows your name. "Stay tuned for more exciting things."
- **[DONE]** SISt: Visit the stables (day/night variants)
  - HorseSS1-3: Tame a horse using Beastmaster powers → sexual encounter

### 3.4 The Barracks — Frederick & Pren
- **[DONE]** ScarBarracks: Busy military outpost
- **[DONE]** SBaF: Visit Frederick's office (after meeting him in MQ11)
  - SBaF2: First meeting — describe him properly (feline, captain, king's insignia cape)
  - SBaF3: Tell Frederick about your powers — TRUST CHECK:
    - SBaF3c1: Tell the truth → Frederick believes you, Pren confirms your Magister scent. Frederick asks for help tracking the Strange Man. (SUCCESS)
    - SBaF3c2: Lie → Pren partially exposes you. Frederick frowns but offers limited trust. (PARTIAL)
    - SBaF3c3: Lie badly → Pren calls you out completely. Trust lost. (FAIL)
  - Frc1: Ask about Scarhaven — "simple country town, supply food to the capital. Not like Seahome — poor bastards are the bypass to The Bridge."
  - Frc2: Ask about Frederick — personal life, uncomfortable but opens up
  - Frc3: Ask about Pren — sword summons the Imp, who appears on the desk
  - Frc4: Ask about leads on the Strange Man — "Nothing yet. Once I hear something, I'll let you know."
- **[DONE]** PrenSS-4: Accept Pren's sexual offer (Imp encounter chain)
- **[DONE]** SBaB → SBaBSS: Bathroom encounter (Reptile, age-gated)

### 3.5 The Outskirts
- **[DONE]** ScarOther (day): Find Dillan — cream/black Fox boy urinating behind a house
  - FBM1 → FBM2: Approach → escalation, branch:
    - FMBc1 → FMBc12: Take him yourself
    - FMBc2 → FMBc22: Involve Kami
  - Revisit variant: Dillan recognizes you
- **[DONE]** ScarOther (night): "Nothing here. Go to bed." (STUB)

---

# ACT 2.5: COMPLETING THE EXISTING WORLD

_Everything below this line is [TBC] or [EXPAND]. These are the gaps within the already-established framework that need filling before new content is added._

## Chapter 4: The Silver Spire Opens

### 4.1 Gaining Access
- **[TBC]** The Spire is the most referenced location in the game. Access should gate behind reputation/quest progress.
- **[EXPAND]** Trigger: After completing the Main Quest (MQ12) AND either Side Quest, return to the Spire. Frederick's recommendation + your demonstrated powers convince a guard to let you approach.
- **[EXPAND]** Alternative: Wyatt's brother works the night shift at the Spire as a guard (established in WyattSS1 dialogue). Night visit → Wyatt's brother lets you in through a side entrance.

### 4.2 The Spire — Interior (New Sub-Location, ~18 passages)
- **[EXPAND]** SpireEntry: Pass the drawbridge. Grand military interior. Guards everywhere.
- **[EXPAND]** SpireHall: Main hall — soldiers, officials, war table with map of Orbath
  - Social NPC: A sympathetic officer or aide who takes interest in you
  - Dialogue tree (4 topics): The war effort, Adplagam's spies, the King, the Strange Man
- **[EXPAND]** SpireAudience: Audience with someone of authority (not the King yet — a general or advisor)
  - They've heard of the forest incident. They want to recruit you.
  - "A Magister could be invaluable to the Empire."
  - Choice: Accept a role (gain access, lose independence) or decline (maintain freedom, limited access)
- **[EXPAND]** SpireBarracks: Military quarters
  - Service: Military-grade equipment shop (player gear — the system SBSC was holding space for)
  - SS encounter: Guard or officer (fits the pattern of 1 SS per sub-location)
- **[TBC]** The Silver Orb: Finally has a purpose here — possibly a key, a pass, or resonates with Spire magic
- **[TBC]** The Ruby Necklace: "Your Magister powers allow you to feel the energy pulsing within it" — possibly an Adplagam artifact, recognized by someone in the Spire

### 4.3 The Spire — Plot Advancement
- **[EXPAND]** Learn that the Strange Man has been seen near Seahome
- **[EXPAND]** Frederick's investigation (Frc4) finally gets a lead: "There have been sightings near The Bridge. Go to Seahome."
- **[EXPAND]** The Council of Wizards has sent an envoy — they're aware of the rogue Magister
- **[EXPAND]** Kami's reaction: worried. "Should the Council hear about it, they might seek us out."

---

## Chapter 5: Scarhaven Completed

### 5.1 Scarhaven Bounty Board Unlocked
- **[TBC]** SIB currently blocks with "words magically fade." This should unlock after the Main Quest.
- **[EXPAND]** Justification: Your Magister powers have grown ($pk=1). The magical ward on the board was meant to keep non-Magisters from reading certain quests. Now you can see through it.

### 5.2 Scarhaven Side Quest A — Seahome Delivery (~15 passages)
- **[EXPAND]** A merchant needs goods delivered to Seahome. Simple fetch quest, but introduces Seahome as a visitable location.
- **[EXPAND]** Theme: INTRODUCTION / WORLDBUILDING for Hub 3
- **[EXPAND]** Encounter a suspicious traveler on the road — Adplagam spy? Ordinary merchant? Trust theme.
- **[EXPAND]** Reward: Gold + reputation in Seahome

### 5.3 Scarhaven Side Quest B — The Beast in the Caves (~20 passages)
- **[EXPAND]** A farmer's livestock is being taken by something in the caves north of town.
- **[EXPAND]** Theme: BEAST TAMING ADVANCEMENT — this is where you learn a new spell
- **[EXPAND]** The creature is a large feral cat/bear hybrid — not evil, just hungry
- **[EXPAND]** Use Beastmaster powers to calm and redirect it. $pk advances to 2.
- **[EXPAND]** New power: Animal Communication (passive — you can now "hear" animal emotions more clearly)
- **[EXPAND]** Optional: Tame the beast as a temporary second companion (Dog Collar finally usable?)

### 5.4 Scarhaven Night Expansion (~12 passages)
- **[TBC]** ScarOther night is a stub. Fill with content matching the Holstein night pattern:
- **[EXPAND]** Outskirts at night: Encounter a wounded traveler from Seahome who tells of strange animal attacks on The Bridge
- **[EXPAND]** Barracks at night: Frederick is working late — exclusive night dialogue about the investigation. More personal, less guarded.
- **[EXPAND]** Inn at night: Different patrons. A traveling merchant from Adplagam (introduces eastern continent culture).

### 5.5 Player Equipment at the Blacksmith
- **[TBC]** SBSC is a stub. Hans says "come back another time."
- **[SYSTEM]** Requires at minimum a basic stat system or narrative equipment effects
- **[EXPAND]** After completing a Scarhaven quest, Hans has "something in your size" — a light leather armor set.
- **[EXPAND]** Equipment gives narrative bonuses (e.g., "your armor absorbs the blow" during encounters) rather than numerical stats, staying consistent with the Twine format.

---

# ACT 3: SEAHOME — THE CROSSROADS

_This is the first major new hub. Everything is [EXPAND] but built from established lore._

## Chapter 6: The Bridge Town

### 6.1 Travel to Seahome
- **[EXPAND]** Carriages updated: Holstein ↔ Scarhaven ↔ Seahome
- **[EXPAND]** Frederick told you: "Seahome is just northeast of here, the bypass up to The Bridge. They get a lot of traffic."
- **[EXPAND]** Carriage ride introduces the landscape shift — from farmland to coastal/bridge territory

### 6.2 Seahome Hub (~8 passages)
- **[EXPAND]** A bustling crossroads town. Larger than Scarhaven, smaller than Holstein. Built around The Bridge — a massive ancient structure connecting Reliquim to... something (another region? Adplagam access point?).
- **[EXPAND]** Theme: CROSSROADS / TRADE / ESPIONAGE — everyone passes through, nobody stays long
- **[EXPAND]** Tone: Paranoid. Lots of strangers. Hard to know who to trust.
- **[EXPAND]** Day/night cycle with distinct moods
- **[EXPAND]** Sub-locations (5, matching density):

### 6.3 Seahome Sub-Location A: The Tavern (~13 passages)
- **[EXPAND]** Service NPC: Tavern keeper (new species not yet used — maybe an Equine or Ursine type)
- **[EXPAND]** Social NPC: A traveling scholar or bard who knows about Magisters
  - Dialogue: Magister history, the Awakening ritual, what happened to past Magisters
  - Reveals: There have been MULTIPLE Magisters over the centuries. Most vanished.
- **[EXPAND]** Room rental, Kami SS (reuse existing system)
- **[EXPAND]** Bounty board: 2 quests (one leading to The Bridge, one local)

### 6.4 Seahome Sub-Location B: The Docks/Market (~13 passages)
- **[EXPAND]** Trade hub — goods from everywhere. Exotic items.
- **[EXPAND]** Service: Shop with new items (Kami gear upgrades, player gear, new consumables)
- **[EXPAND]** Social NPC: A merchant from Adplagam — first direct contact with the eastern continent
  - Dialogue: Life in Adplagam, what they know about Magisters, rumors of war
  - Possible spy? Trust theme continues from Frederick's arc.
- **[EXPAND]** SS encounter: Dock worker or merchant (fits 1-per-sublocation pattern)
- **[TBC]** Strange Mushroom: An alchemist here might identify it — "This is a Mindshroom. It enhances magical perception temporarily."

### 6.5 Seahome Sub-Location C: The Bridge (~13 passages)
- **[EXPAND]** A massive ancient stone bridge spanning a chasm or strait. Heavily guarded.
- **[EXPAND]** Theme: BOUNDARY / THRESHOLD — crossing means leaving Reliquim
- **[EXPAND]** The Bridge is where the Strange Man was last sighted (Frederick's lead)
- **[EXPAND]** Investigation: Talk to guards, find claw marks, sense residual magic
- **[EXPAND]** Social NPC: Bridge guard captain — dialogue about security, recent incidents
- **[EXPAND]** Discovery: The Strange Man crossed The Bridge heading east. Toward Adplagam.
- **[EXPAND]** Gate: You can't cross yet. Need authorization from the Spire or another means.

### 6.6 Seahome Sub-Location D: The Shrine (~10 passages)
- **[EXPAND]** A small, overgrown shrine to Pan hidden behind the town
- **[EXPAND]** Theme: SPIRITUAL / POWER GROWTH
- **[EXPAND]** Your Dirk resonates here. Birdpup Feather glows.
- **[EXPAND]** Meditation/ritual: Advance $pk to 2 or 3
- **[EXPAND]** New power: Beast Sight (see through an animal's eyes temporarily)
- **[EXPAND]** Finn appears here if you have the feather. He's more forthcoming:
  - Hints at his nature (avatar of Pan? A Birdpup spirit?)
  - "You'll need to be stronger for what's coming."
  - Gives a cryptic clue about the Strange Man's identity

### 6.7 Seahome Sub-Location E: Back Alleys (~10 passages)
- **[EXPAND]** Pattern match: Every hub has a dangerous/seedy area
- **[EXPAND]** Night content: Encounter with an Adplagam spy who mistakes you for an ally
- **[EXPAND]** Day content: Street urchins, information broker, underground market
- **[EXPAND]** SS encounter: Spy or urchin (fits pattern)
- **[EXPAND]** Plot: Learn that Adplagam is actively seeking Magisters — they want to weaponize the power

---

## Chapter 7: Seahome Quests

### 7.1 Seahome Quest A — The Bridge Incident (~18 passages)
- **[EXPAND]** Animals are attacking travelers on The Bridge at night
- **[EXPAND]** Theme: BEAST TAMING LEVEL 2 — larger, more dangerous creatures
- **[EXPAND]** Dungeon: The Bridge at night (linear, 6-8 nodes, like the maze but simpler)
- **[EXPAND]** Boss: A massive beast (bear? griffin?) being controlled by residual magic left by the Strange Man
- **[EXPAND]** Resolution: Calm the beast, discover a magical anchor (an item left by the Strange Man to keep the beast aggressive). Take it to Frederick or the Spire.
- **[EXPAND]** Reward: Gold + Bridge access unlocked

### 7.2 Seahome Quest B — The Missing Merchant (~12 passages)
- **[EXPAND]** An Adplagam merchant has gone missing near town
- **[EXPAND]** Theme: TRUST / ESPIONAGE — is the merchant a victim or a spy?
- **[EXPAND]** Investigation: Track them using Beast Sight (new power)
- **[EXPAND]** Discovery: The merchant was kidnapped by Iron Empire soldiers who suspected espionage
- **[EXPAND]** Choice: Help the merchant escape (gain Adplagam contacts) or turn them in (gain Empire reputation)
- **[EXPAND]** Consequence: Affects how Adplagam and the Spire treat you going forward

---

# ACT 4: THE PURSUIT

_The main plot advances. The Strange Man is identified and pursued._

## Chapter 8: The Investigation Converges

### 8.1 Return to the Spire (~8 passages)
- **[EXPAND]** Present evidence from Seahome (magical anchor, witness accounts)
- **[EXPAND]** The Spire takes the threat seriously. The Strange Man is identified:
  - He is **a former Magister** who went rogue — the same type of person Dinus's warlock story warned about
  - He crossed into Adplagam and is building an army of controlled beasts
  - The Council of Wizards has formally requested Reliquim's cooperation
- **[EXPAND]** You are given a mission: Cross The Bridge, track the rogue Magister, report back
- **[TBC]** King Adalrico: Brief audience. He acknowledges you. "We need you, Magister."

### 8.2 Return to Frederick (~6 passages)
- **[TBC]** Frc4 finally resolves: "I have a lead."
- **[EXPAND]** Frederick provides tactical support — soldiers, supplies, a contact in Adplagam
- **[EXPAND]** Frederick's personal stake: The Strange Man killed some of his soldiers in the forest. This is personal.
- **[EXPAND]** Optional: Deeper relationship with Frederick (dialogue + SS, matching Hans's depth)

### 8.3 Kami's Conflict (~6 passages)
- **[EXPAND]** Kami is torn. His family is safe (SQ2), but crossing into Adplagam means leaving Reliquim.
- **[EXPAND]** Emotional dialogue: "I have followed you faithfully, Master. But I fear what lies ahead."
- **[EXPAND]** Player choice: Reassure Kami / Acknowledge the danger / Release him from service
  - Releasing Kami: He refuses. "I will not leave you. You are my Master, and my friend."
- **[EXPAND]** Kami reveals: Pan warned him this might happen. "He said you would face another of your kind."

---

## Chapter 9: Crossing The Bridge

### 9.1 The Bridge — Crossing (~6 passages)
- **[EXPAND]** Authorized crossing. The Bridge is ancient, covered in carvings.
- **[EXPAND]** Kami identifies the carvings as old Magister symbols. "This bridge was built by Magisters."
- **[EXPAND]** Midway across: Sense the Strange Man's magic strongly. He's been here recently.
- **[EXPAND]** Birdpup Feather reacts — giggling sound, warmth. Finn's presence?

### 9.2 The Eastern Shore (~4 passages)
- **[EXPAND]** Transition: Adplagam is visually different — darker forests, different architecture
- **[EXPAND]** Kami is on edge. Animals here don't respond the same way to your magic.
- **[EXPAND]** A sign: A small outpost marks the border. "You are now entering Adplagam territory."

---

# ACT 5: ADPLAGAM — THE EASTERN CONTINENT

_Late-game content. Highest level of projection, but anchored in established lore._

## Chapter 10: Enemy Territory

### 10.1 Adplagam Hub — Border Town (~50-60 passages)
- **[EXPAND]** A new hub matching Holstein/Scarhaven density (5 sub-locations)
- **[EXPAND]** Theme: ENEMY TERRITORY / FISH OUT OF WATER
- **[EXPAND]** The people here distrust Reliquim citizens. Kami draws suspicion.
- **[EXPAND]** Sub-locations: Inn, Market, Shrine/Temple, Underground, Outskirts
- **[EXPAND]** New NPCs: 4-5 characters with full dialogue trees + SS chains
- **[EXPAND]** The Strange Man has been here. He's left a trail of controlled beasts.

### 10.2 Tracking the Rogue Magister (~20 passages)
- **[EXPAND]** Follow the trail through Adplagam
- **[EXPAND]** 2-3 dungeons/encounters of escalating difficulty
- **[EXPAND]** Power advancement: $pk reaches maximum. New abilities unlock.
- **[EXPAND]** Learn the Rogue Magister's identity and motivation:
  - He was a Magister who lost control. Magic addiction (Dinus's foreshadowing).
  - He believes Pan abandoned him. He wants to destroy the Magister system.
  - He's building a beast army to attack Holstein and the Spire.

### 10.3 The Council of Wizards (~15 passages)
- **[EXPAND]** Reachable from Adplagam's coast or via a magical means
- **[EXPAND]** The Council exists on an island in the central ocean
- **[EXPAND]** They are ancient, powerful, and morally ambiguous
- **[EXPAND]** They want the Rogue Magister stopped — but they also want to control YOU
- **[EXPAND]** Choice: Accept the Council's help (power boost but strings attached) or refuse (harder path, freedom)

---

# ACT 6: THE RECKONING

## Chapter 11: Confrontation

### 11.1 The Rogue Magister's Lair (~20 passages)
- **[EXPAND]** A corrupted forest/cave where the Rogue Magister has made his base
- **[EXPAND]** His beast army: the massive wolf from MQ6 (now fully under his control) + others
- **[EXPAND]** Dungeon: Larger maze (6x6?) or multi-stage encounter
- **[EXPAND]** Final use of all accumulated powers and items

### 11.2 The Final Choice
- **[EXPAND]** Confront the Rogue Magister. He's not a monster — he's broken.
- **[EXPAND]** Theme matches SQ1 (Dragon diplomacy): Violence vs. compassion vs. compromise
- **[EXPAND]** Choices:
  - Destroy him (use full power, risk magic addiction yourself)
  - Redeem him (use empathy, Beastmaster bond — hardest path)
  - Imprison him (Council's preferred option — morally grey)
- **[EXPAND]** The Strange Man's beast (massive wolf) recognizes your authority regardless — callback to MQ10 when the alpha bowed to you

### 11.3 Resolution
- **[EXPAND]** Return to Holstein. Report to the Spire.
- **[EXPAND]** Frederick's reaction (depends on trust level from SBaF3)
- **[EXPAND]** Kami's reflection: "You have grown, Master."
- **[EXPAND]** Finn appears one final time — reveals his true nature
- **[EXPAND]** The Birdpup Feather's purpose: It was Pan's gift. A token of the god's faith in you.
- **[EXPAND]** Epilogue: Your place in the world — Magister of Reliquim, wandering adventurer, or something else entirely

---

# SYSTEMS TO BUILD

## S-1. Combat System
- **[SYSTEM]** Not stat-heavy — narrative combat fits the Twine format
- **[SYSTEM]** Choices during encounters: Fight / Calm (Beastmaster) / Flee / Use Item
- **[SYSTEM]** Health Potion and Pain Leaves become functional
- **[SYSTEM]** Kami equipment provides narrative advantages ("Kami's helm deflects the blow")
- **[SYSTEM]** Player equipment (once SBSC is filled) provides similar bonuses

## S-2. Power Progression ($pk levels)
- **[DONE]** $pk=0: No powers
- **[DONE]** $pk=1: Calming Spell (green mist, pacifies animals) — learned in MQ8
- **[EXPAND]** $pk=2: Animal Communication (sense emotions, basic intent) — learned in Scarhaven Quest B
- **[EXPAND]** $pk=3: Beast Sight (see through animal eyes) — learned at Seahome Shrine
- **[EXPAND]** $pk=4: Beast Bond (temporarily control a single animal) — learned in Adplagam
- **[EXPAND]** $pk=5: Full Dominion (mass control, the power the Rogue Magister abuses) — endgame

## S-3. Reputation System
- **[SYSTEM]** Track trust/reputation with:
  - Frederick (SBaF3 trust check already exists — expand)
  - The Iron Empire / Spire (quest completion, Spire access)
  - Adplagam contacts (merchant quest choice in Seahome)
  - The Council of Wizards (endgame)
- **[SYSTEM]** Affects dialogue options, access to locations, ending options

## S-4. Item Resolution
- **[TBC]** Silver Orb → Spire key or magical focus item
- **[TBC]** Ruby Necklace → Adplagam artifact, recognized by eastern NPCs
- **[TBC]** Dog Collar → Second beast companion (tamed creature) or Kami power-up
- **[TBC]** Strange Mushroom → Alchemical ingredient (Seahome alchemist identifies it)
- **[TBC]** Birdpup Feather → Pan's token, resonates at shrines, reveals Finn's nature
- **[TBC]** Magic Flower → Alchemy system ingredient (if system built), or unique quest item

## S-5. Day/Night Completion
- **[SYSTEM]** Every sub-location should have meaningful day AND night content
- **[SYSTEM]** Night content pattern: More intimate/dangerous encounters, different NPCs available
- **[SYSTEM]** Time advances: Sleep (full cycle), certain actions (partial advance), quest travel (auto-set)

---

# EXPANSION PRIORITY ORDER

_Recommended build sequence, filling closest-to-done content first:_

```
PHASE 1 — Complete Existing Hubs
  1. Scarhaven night content (Outskirts, Barracks, Inn)     ~12 passages
  2. Scarhaven bounty board + 2 quests                      ~35 passages
  3. Player equipment at Hans's shop                        ~6 passages
  4. Item resolution (Silver Orb, Dog Collar, Mushroom)     ~8 passages
  Subtotal: ~61 passages

PHASE 2 — The Silver Spire
  5. Spire access trigger (post-MQ reputation gate)          ~4 passages
  6. Spire interior (hall, audience, barracks, shop)         ~18 passages
  7. Spire plot advancement (Strange Man lead → Seahome)     ~6 passages
  Subtotal: ~28 passages

PHASE 3 — Seahome (Hub 3)
  8. Hub + 5 sub-locations                                   ~60 passages
  9. 2 quests (Bridge Incident, Missing Merchant)            ~30 passages
  10. Finn's expanded role at the Shrine                     ~6 passages
  Subtotal: ~96 passages

PHASE 4 — Main Plot Resolution
  11. Frederick's investigation chain resolves               ~10 passages
  12. Crossing The Bridge                                    ~10 passages
  13. Adplagam border town (Hub 4)                           ~55 passages
  14. Rogue Magister pursuit + dungeons                      ~30 passages
  15. Council of Wizards                                     ~15 passages
  16. Final confrontation + epilogue                         ~25 passages
  Subtotal: ~145 passages

TOTAL NEW CONTENT: ~330 passages
CURRENT BUILD:      232 passages
PROJECTED FINAL:   ~562 passages
```

---

# KILLIAN — RETURN ARC (Optional)

- **[EXPAND]** Killian is an Avian mercenary who helped you in the Prologue. He said "This is where we part ways" but clearly had more to his character.
- **[EXPAND]** Killian could reappear in Seahome or Adplagam as a mercenary-for-hire.
- **[EXPAND]** He recognizes you, is impressed by your growth.
- **[EXPAND]** Optional companion for dangerous quests. Dialogue tree + SS chain (matching pattern).
- **[EXPAND]** His "men aren't comfortable with a kid" line could evolve — they now respect you.
- **[EXPAND]** He may have information about the Strange Man (mercenaries hear things).
