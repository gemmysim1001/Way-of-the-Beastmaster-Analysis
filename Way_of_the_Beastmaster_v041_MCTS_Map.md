# Way of the Beastmaster v0.41 - Complete MCTS Game Tree

## Legend
```
[ROOT]     = Root/entry node
[BRANCH]   = Decision point (player choice)
[LINEAR]   = Single path forward (no choice)
[LEAF]     = Terminal/return node (loops back)
[CHAR]     = Character interaction
[SS]       = Sexual scene
[ITEM]     = Item acquisition
[QUEST]    = Quest node
[BATTLE]   = Combat encounter (RPG battle system)
[SPELL]    = Spell acquisition
-->        = Leads to
|          = Branch option
W/L/D      = Win / Lose / Draw (MCTS outcome style)
```

---

## GAME METADATA

```
Title:            Way of the Beastmaster
Version:          0.41
Engine:           Twine 2.2.1 / Harlowe 2.1.0
IFID:             D7B85E84-57FD-45F8-BA87-C06377DDB39A
Start Node:       PID 37 (Title)
Total Passages:   465 (PIDs 1-465)
```

---

## CHARACTERS ENCOUNTERED

| Character | Species | Location | Role | Interactions |
|-----------|---------|----------|------|-------------|
| **Kami** | Wolf (white fur, blue eyes) | Companion (everywhere) | Guide/familiar/servant | Dialogue, SS (Inn room, any location with bed), combat partner |
| **Killian** | Avian (dirty feathers) | Forest (Intro) | Mercenary leader | Dialogue only |
| **Dinus** | Bear (white fur, 8ft) | Holstein Inn | Innkeeper | Dialogue, SS |
| **Wyatt** | Canine (blue-grey fur, green eyes) | Holstein Fountain | Mercenary/adventurer | Dialogue, SS (night alley), Relationship |
| **Misfit** | Ratman (grey/blue fur) | Holstein Alley (day) | Alchemist, sewer dweller | Dialogue, SS, Relationship (fully fleshed out) |
| **Night Rat** | Rat | Holstein Fountain (night) | Stranger | Dialogue, SS (coerced) |
| **Night Figure** | Unknown | Holstein Alley (night) | Dangerous stranger | Encounter |
| **Hans** | Corgi (white/cream fur, 4ft) | Scarhaven Blacksmith | Blacksmith, Frederick's friend | Dialogue, SS (day & night), Relationship |
| **Frederick** | Feline (grey/blue, white-dyed head fur) | Scarhaven Barracks | Guard Captain | Dialogue, trust check |
| **Pren/Penn** | Imp (2ft, bluish-red, dark eyes) | Scarhaven Barracks | Frederick's assistant | Dialogue, SS |
| **Finn** | Canine pup (white fur, red eyes) | Scarhaven Inn | Traveler / disguised god | Gives feather; SS (with Divine Potion) |
| **Wes** | Shark (muscular, no neck) | Scarhaven Inn | Innkeeper | Room rental, quest info |
| **Horse** | Horse | Scarhaven Stables | Feral animal | Beast taming, SS |
| **FBM Boy** | Unknown | Scarhaven Outskirts | Unnamed boy | SS |
| **Dragon + 3 Whelps** | Dragon | Streamdale Mountain | Quest boss (SQ1) | Negotiation, SS |
| **Fiend** | Ratman (black fur, red eyes, muscular) | Holstein Sewers | Misfit's brother | Dialogue, SS (within relationship & post-breakup) |
| **Soir** | Feline (black fur, grey streaks, white hair, ~12yo) | Holstein Tailor Shop | Tailor's assistant | SS |
| **Gnoll Teen** | Gnoll (tawny cream/brown fur) | Hixborough Mountains | Mountain enemy | Battle, SS (win or lose) |
| **Pigorc** | Pigorc (pig-orc hybrid) | Hixborough Mountains | Mountain enemy | Battle, SS (lose/flee only) |
| **Akos** | Reptile (black/brown scales, ~50yo) | Hixborough Mountains | Senior of Arcplage Academy, mage | Dialogue, SS (paw/sex, Reptile/Dragon species only or general) |
| **Zexir** | Dragon (turquoise/teal scales, massive ~10m) | Isle of Dragons - Council Chamber | Isle leader, head of Magic/Education | Dialogue, lore, teaches spells, SS (night visits) |
| **Erel** | Avian (red/white feathers, parrot-like beak) | Isle of Dragons - Animal Doctor | Veterinarian | Dialogue (interested in animals, not people) |
| **Hran** | Dragon (wingless, stocky, muscular, jagged horns) | Isle of Dragons - Caves/Night training | Young recruit (~45 dragon years / ~15 equivalent) | Dialogue, SS |
| **Raln** | Dragon (large) | Isle of Dragons - Arena | Military head, combat trainer | Dialogue (rude but kind-hearted) |
| **Hooded Mage** | Unknown (Magister) | Hixborough Mountains summit | Antagonist | Summons Dark Dragon; triggers IoD intro |
| **Dark Dragon** | Dragon | Hixborough Mountains summit | Boss (unbeatable) | Knocks Kami off mountain; player rescued by IoD patrol |

---

## MONTE CARLO TREE SEARCH - FULL EXPANSION

```
[ROOT] Title (pid 37)
  |
  +--> [LINEAR] Intro1 (pid 1) - "It's cold..." (wake up with amnesia)
         |
         +--> [BRANCH] Species (pid 5) - "You stare at your reflection..."
                |
                |-- CC (pid 6, Canine) -------> Age
                |-- CF (pid 7, Feline) -------> Age
                |-- CV (pid 194, Vulpine) ----> Age
                |-- CA (pid 8, Avian) --------> Age
                |-- CR (pid 9, Reptile) ------> Age
                |-- CD (pid 10, Dragon) ------> Age
                |
                +--> [LINEAR] Age (pid 11) - "How old are you?" (10-16)
                       |
                       +--> [LINEAR] Body (pid 12) - "Body frame selection"
                              |
                              +--> [LINEAR] Height (pid 13) - "Height selection"
                                     |
                                     +--> [BRANCH] Hair (pid 16)
                                            |-- (has hair) --> HairC (pid 17) --> Eye
                                            |-- (bald/feathered) -----------> Eye
                                            |
                                            +--> [LINEAR] Eye (pid 87) - "Eye color"
                                                   |
                                                   +--> [LINEAR] Cock (pid 14) - "Genitalia"
                                                          |
                                                          +--> [LINEAR] DickL (pid 15) - "Size"
                                                                 |
                                                                 +--> [LINEAR] CharacterFinish (pid 18)
                                                                        |
                                                                        V
```

---

## ACT 1: THE INTRO SEQUENCE (Linear)

```
CharacterFinish (pid 18)
  |
  +--> [LINEAR] Intro2 (pid 19) - Forest, cold, meet Kami
         |
         +--> [BRANCH] Intro3 (pid 20) - Meet Kami (talking Wolf)
                |
                |-- Intro3c1 (pid 21): "Magister?" ---------+
                |-- Intro3c2 (pid 22): "You're my Servant?" +-- (explore all, then...)
                |-- Intro3c3 (pid 23): "Where am I?" -------+
                |                                            |
                +--> Intro3c4 (pid 24): "Let's get moving" <-+
                       |
                       +--> [LINEAR] Intro4 (pid 25) - Walking for hours
                              |
                              +--> [LINEAR] Intro5 (pid 26) - Meet Killian & bandits
                                     |
                                     +--> [BRANCH] Intro6 (pid 27) - Killian gives clothes
                                            |
                                            |-- [OPTIONAL] Kami1 (pid 28): Talk to Kami
                                            |     |
                                            |     +-- Kami1c1 (pid 30): "Trust Killian?"
                                            |     +-- Kami1c2 (pid 31): "Can others hear you?"
                                            |     +-- Kami1c3 (pid 32): "My perks?"
                                            |     +-- Intro7: "Time to sleep"
                                            |
                                            +--> [LINEAR] Intro7 (pid 29) - Sleep under stars
                                                   |
                                                   +--> [LINEAR] Intro8 (pid 33) - Travel to Holstein
                                                          |
                                                          +--> [LINEAR] Intro9 (pid 34) - Arrive
                                                                 |
                                                                 +--> [LINEAR] Intro10 (pid 35) - Killian goodbye
                                                                        |
                                                                        +--> TheBeginning (pid 230) --> Hub
```

---

## ACT 2: THE HUB (Holstein - Open World)

```
[ROOT] Hub (pid 36) (Holstein Capital) - CENTRAL NODE
  |
  |   [PERSISTENT FOOTER on every Hub page:]
  |   +--> Character (pid 3) (view stats / save-load)
  |   +--> inventory (pid 4) (view items)
  |   +--> Spells (pid 421) (view spell book)
  |   +--> KamiMenu (pid 41) (talk to Kami)
  |
  +========================================+
  |                                        |
  |  EIGHT BRANCHES FROM HUB:             |
  |                                        |
  |  1. HubInn -------> The Inn           |
  |  2. HubFount -----> The Fountain      |
  |  3. HubMarket ----> The Market        |
  |  4. HolsteinTailor-> The Tailor [NEW] |
  |  5. HubSpire -----> The Silver Spire  |
  |  6. Alley1D/1N ---> Alley (Day/Night) |
  |  7. Carriages ----> Travel            |
  |  8. FiendSingle --> Fiend (post-BU)   |
  |                                        |
  +========================================+
```

---

### BRANCH 1: THE INN (HubInn, pid 38)

```
HubInn
  |
  +-- [BRANCH] InnStay (pid 44) - Talk to Innkeeper (Dinus the Bear)
  |     |
  |     +-- InnStayPay (pid 46): "Rent a room" (10 gold)
  |     |     |
  |     |     +-- (no gold) --> back to HubInn
  |     |     +-- (has gold) --> InnStayRoom (pid 48)
  |     |           |
  |     |           +-- [BRANCH] Room options:
  |     |                 |
  |     |                 +-- KamiSS1 (pid 49) [SS]: Sex with Kami
  |     |                 |     |
  |     |                 |     +-- KamiSS1c1 (pid 51): "Top Kami"
  |     |                 |     |     +--> KamiSS1c12 (pid 53)
  |     |                 |     |           +--> InnStaySleep
  |     |                 |     |
  |     |                 |     +-- KamiSS1c2 (pid 52): "Bottom for Kami"
  |     |                 |           +--> KamiSS1c22 (pid 54)
  |     |                 |                 +--> InnStaySleep
  |     |                 |
  |     |                 +-- HolsteinKEquip (pid 156): Equip Kami's gear
  |     |                 |     |
  |     |                 |     +-- KEquipHelm (pid 158)
  |     |                 |     +-- KEquipCollar (pid 159)
  |     |                 |     +-- KEquipPaws (pid 160)
  |     |                 |     +-- KEquipBack (pid 161)
  |     |                 |     +--> back to InnStayRoom
  |     |                 |
  |     |                 +-- (rest) InnStaySleep (pid 50): "Go to sleep"
  |     |                 |     +--> HubInn (next day/night)
  |     |                 |
  |     |                 +-- (if has Zexir's Amulet) OrbathAmulet (pid 393)
  |     |                       +--> IoDHub (teleport to Isle of Dragons)
  |     |
  |     +-- [CHAR] DinusI (pid 47): "Tell me about yourself"
  |     |     +--> DinusI2 (pid 55) (rogue warlock backstory)
  |     |           +--> HubInn
  |     |
  |     +-- [SS] DinusSS1 (pid 88): "Hang out with Dinus" (visit >=11)
  |           +--> DinusSS2 (pid 89) --> DinusSS3 (pid 90)
  |                 --> DinusSS4 (pid 91) --> DinusSS5 (pid 92) --> HubInn
  |
  +-- [QUEST] InnQuests (pid 45) - The Bounty Board
  |     |
  |     +-- MQ1: "King's Decree: Slay the Wild Animals" (500 Gold)
  |     +-- SQ1: "Village of Streamdale: Evict the Dragon" (100 Gold)
  |     +-- SQ2: "Merchant Axedull: Evict the Wolf Pack" (200 Gold)
  |     +-- (back) --> HubInn
  |
  +--> Hub (return to square)
```

---

### BRANCH 2: THE FOUNTAIN (HubFount, pid 43)

```
HubFount (The Fountain Square)
  |
  +-- [DAYTIME BRANCHES:]
  |     |
  |     +-- FountD1 (pid 56): "Try and make some friends"
  |     |     |
  |     |     +-- [CHAR] Wyatt1 (pid 59): Meet Wyatt (first time)
  |     |     |     +--> Hub
  |     |     +-- (nobody found) --> HubFount
  |     |
  |     +-- FountD2 (pid 57): "Take a seat"
  |     |     +--> HubFount
  |     |
  |     +-- [CHAR] Wyatt2 (pid 60): "Talk to Wyatt" (after meeting)
  |     |     |
  |     |     +-- Wyatt2c1 (pid 62): "Silver Spire?"
  |     |     +-- Wyatt2c2 (pid 63): "Where from?"
  |     |     +-- Wyatt2c3 (pid 64): "Make money?"
  |     |     +-- Wyatt2c4 (pid 65): "Places to avoid?"
  |     |     +--> HubFount
  |     |
  |     +-- [CHAR] WyattR (pid 239): Confess feelings to Wyatt
  |           +--> WyattR2 (pid 240) --> WyattRHub (pid 238)
  |
  +-- [NIGHTTIME BRANCH:]
  |     |
  |     +-- FountN1 (pid 58): "Approach the figure"
  |           |
  |           +-- FountN11 (pid 66) [SS]: Rat's demands
  |           |     +--> HubFount
  |           +-- (refuse) --> Hub
  |
  +--> Hub (return)
```

---

### BRANCH 3: THE MARKET (HubMarket, pid 39)

```
HubMarket (daytime only; closed at night)
  |
  +-- MarkMagic (pid 67): "Magic Items Stall"
  |     |
  |     +-- MarkMagicF1 (pid 70): Show the Magic Flower
  |     +--> HubMarket
  |
  |     [ITEMS AVAILABLE:]
  |     Silver Orb (pid 71) [ITEM] - "Glows dimly, unknown purpose"
  |     Dog Collar (pid 72) [ITEM] - "Cursed collar, Kami refuses"
  |     Ruby Necklace (pid 73) [ITEM] - "Gold-plated, cabochon ruby"
  |
  +-- MarkHerb (pid 68): "Herb & Potion Stall"
  |     |
  |     +--> HubMarket
  |
  |     [ITEMS AVAILABLE:]
  |     Pain Leaves (pid 74) [ITEM] - "Dulls pain" (heals Kami 10 HP)
  |     Health Potion (pid 75) [ITEM] - "Heals wounds"
  |     Endowment Potion (pid 76) [ITEM] - "Sexual enhancement"
  |       +--> EPFuck (pid 77): Drink the potion
  |             +--> EPFuck2 (pid 82): Pass out, wake up changed
  |                   +--> Hub
  |
  +-- MarkPed (pid 69): "Peddler in the back"
  |     |
  |     +-- MarkPed2 (pid 78): "What's this weapon?"
  |           |
  |           +-- MarkPed22 (pid 79): Buy the Magister's Dirk [ITEM]
  |           |     +--> Hub (Kami is excited)
  |           |
  |           +-- MarkPed23 (pid 80): Decline purchase
  |                 +--> HubMarket
  |
  +--> Hub (return)
```

---

### BRANCH 4: THE TAILOR (HolsteinTailor, pid 458) [NEW IN v0.41]

```
HolsteinTailor
  |
  +-- [First visit:] HolsteinTailor2 (pid 459) - Meet Soir the feline assistant
  |     |
  |     +--> HolsteinTailor3 (pid 460) - Getting measured
  |           |
  |           +--> [SS] HolsteinTailor4 (pid 461) - Soir's advances
  |                 |
  |                 +--> HolsteinTailor5 (pid 462) - Escalation
  |                       |
  |                       +--> HolsteinTailor6 (pid 463) - Scene
  |                             |
  |                             +--> HolsteinTailor7 (pid 464) - Aftermath, buy clothes (30g)
  |                                   +--> Hub
  |
  +-- [Return visits:] Repeat SS with Soir
        +--> Hub
```

---

### BRANCH 5: THE SILVER SPIRE (HubSpire, pid 40)

```
HubSpire
  |
  +--> Hub (guard turns you away - placeholder for future content)
```

---

### BRANCH 6: ALLEY - DAYTIME (Alley1D, pid 83)

```
Alley1D (Daytime Alley)
  |
  +-- [CHAR] MisfitI (pid 85): Talk to Misfit (Ratman)
  |     |
  |     +-- MisfitSS1 (pid 86) [SS]: Accept advances
  |     |     +--> Hub
  |     +--> Hub
  |
  +-- [SS] MisfitSS1 (pid 86): Direct sexual encounter
  |     +--> Hub
  |
  +-- [CHAR] MisfitR (pid 236): Confess feelings to Misfit
  |     +--> MisfitR2 (pid 237) --> MisfitRHub (pid 235)
  |
  +--> Hub (return)
```

---

### BRANCH 7: ALLEY - NIGHTTIME (Alley1N, pid 84)

```
Alley1N (Nighttime Alley - dangerous)
  |
  +-- Alley1N1 (pid 93): "Peek in the illuminated window"
  |     |
  |     +-- [CHAR] WyattSS1 (pid 95): Find Wyatt inside
  |     |     +--> WyattSS2 (pid 96): He offers you food
  |     |           |
  |     |           +-- (eat and leave) --> Hub
  |     |           +-- WyattSS3 (pid 97) [SS]: Offer sexual favors
  |     |                 |
  |     |                 +-- (stop here) --> Hub
  |     |                 +-- WyattSS4 (pid 98): Go further
  |     |                       |
  |     |                       +-- WyattSS5 (pid 99): Scene
  |     |                       |     +--> WyattSSE (pid 100)
  |     |                       |           +--> WyattSSE2 (pid 241) (if in relationship)
  |     |                       |                 +--> Hub
  |     |                       +-- WyattSSE (pid 100): Aftermath
  |     |                             +--> Hub
  |     |
  |     +--> Alley1N (go back)
  |
  +-- Alley1N2 (pid 94): "Approach the figure at the end"
  |     +--> Alley1N21 (pid 101): Dangerous encounter, Kami protects
  |           +--> Hub
  |
  +--> Hub (return)
```

---

### BRANCH 8: FIEND SINGLE (FiendSingle, pid 287) [NEW - Post-Misfit breakup]

```
FiendSingle (appears on Hub if $MisfitBU is true and $FiendF is true)
  |
  +--> FiendSingle2 (pid 288): Meet Fiend in the sewers
        |
        +--> [SS] FiendSingle3 (pid 289): Make your move
              |
              +--> FiendSingle4 (pid 290): Escalation
                    |
                    +--> FiendSingle5 (pid 292): Scene
                          |
                          +--> FiendSingle6 (pid 293): Aftermath
                                +--> Hub
```

---

### CARRIAGES (Carriages, pid 166) - Travel System

```
Carriages
  |
  +-- HolC (pid 231): "Go to Holstein"
  |     +--> Hub
  |
  +-- ScarC (pid 167): "Go to Scarhaven"
        +--> ScarHub
```

---

## RELATIONSHIP SYSTEM [NEW IN v0.41]

```
RELATIONSHIP HUB STRUCTURE:
  |
  |  Available Partners: Wyatt, Hans, Misfit
  |  (Only one at a time; $Single must be true to start new)
  |  LoveMeter: 0-1000+ scale
  |  Heart Ring (pid 465): Shows current $Relationship and $LoveMeter
  |
  +-- WYATT (WyattRHub, pid 238)
  |     Status tiers: 0-250 / 251-500 / 501-750 / 751-1000 / 1001+
  |     Activities: NONE currently (placeholder - "too busy adventuring")
  |     Break Up: WyattRBU (pid 243) - can undo
  |
  +-- HANS (HansRHub, pid 234)
  |     Status tiers: same as above
  |     Activities: NONE currently (placeholder - "too busy smithing")
  |     Break Up: HansRBU (pid 244) - can undo (high LM = crying)
  |
  +-- MISFIT (MisfitRHub, pid 235) [FULLY FLESHED OUT]
        Status tiers: same as above
        Activities:
          +-- MisfitRI (pid 245): Ask about himself
          |     +-- MisfitRI1 (pid 246): Childhood
          |     +-- MisfitRI2 (pid 247): Work (alchemy)
          |     +-- MisfitRI3 (pid 248): Sexual interests
          |     +-- MisfitRI4 (pid 249): Hobbies
          |     +-- MisfitRI5 (pid 250): His people
          |     +-- MisfitRISS (pid 251) [SS]: Scene
          |           +--> MisfitRISS2 (pid 263)
          |
          +-- MisfitHouse (pid 252): Visit his sewer home
          |     +--> MisfitHouse2 (pid 253): Inside the house
          |           +-- MisfitHSS (pid 254) [SS]: "Something kinky"
          |           |     +-- MisfitHSSc1 (pid 264): Kami joins
          |           |     |     +--> MisfitHSSc12-14 (pids 266-268)
          |           |     +-- MisfitHSSc2 (pid 265): Misfit only
          |           |           +--> MisfitHSSc21-22 (pids 269-270)
          |           |
          |           +-- MisfitLabGame (pid 255): Alchemy minigame
          |           |     (random ingredient matching, 4 rounds)
          |           |     +--> MisfitLabGame2-6 (pids 256-260)
          |           |           +--> MisfitRHub (reward: Divine Potion or gold)
          |           |
          |           +-- MisfitFiend1 (pid 280): Hang with Fiend (if met)
          |                 +--> MisfitFiend2 (pid 281) [SS]
          |                       +-- MisfitFiendLow (pid 282): Threesome
          |                       |     +--> Low2-4 (pids 284-286)
          |                       +-- MisfitFiendHigh (pid 283): Just Fiend
          |
          +-- MisfitFam (pid 273): Meet family (LoveMeter >= 250)
          |     +--> MisfitFiend (pid 279): Meet Fiend
          |           +-- MisfitFiendc1-5 (pids 274-278): Dialogue options
          |
          +-- MisfitPicnic (pid 298): Special outing (LoveMeter >= 500)
          |     +--> MisfitPicnic2 (pid 303): Forest clearing picnic
          |           +--> MisfitPicnic3 (pid 304): Wholesome ending (+50 LM)
          |
          +-- MisfitTrueEnd (pid 271): True ending (LoveMeter > 1000)
          |     Misfit gives Glass Ornament [ITEM] + "I love you"
          |
          +-- Break Up: MisfitRBU (pid 242) - can undo
                (sets $MisfitBU = true, enables FiendSingle on Hub)
```

---

## MAIN QUEST 1: THE FOREST OF MADNESS (MQ, Holstein Bounty Board)

```
MQ1 (pid 102): Accept the Royal Decree (500 Gold)
  |
  +--> MQ2 (pid 105) --> MQ3 (pid 106) --> MQ4 (pid 107)
        --> MQ5 (pid 108) --> MQ52 (pid 109) --> Maze9
              |
              +--> [THE MAZE - 4x4 GRID FOREST]

================================
  THE MAZE (Navigable Forest)
================================

Grid Layout:
  Maze1(112) -- Maze2(120)  -- Maze3(121)  -- Maze4(122)
    |            |              |              |
  Maze5(113) -- Maze6(117)  -- Maze7(118)  -- Maze8(119)
    |            |              |              |
  Maze9(110) -- Maze10(114) -- Maze11(115) -- Maze12(116)
    |            |              |              |
  Maze13(111)-- Maze14(123) -- Maze15(124) -- Maze16(125)

Entry: Maze9 (pid 110)

Items in Maze:
  Strange Mushroom (pid 126) [ITEM] - found in maze
  Speedband (pid 311) [ITEM] - Wyatt's headband

GOAL --> Maze11 --> MQ6 (pid 127) --> MQ7-12
  MQ7 (pid 128) --> MQ8 (pid 129) --> MQ9 (pid 130)
  --> MQ10 (pid 131) --> MQ11 (pid 132) --> MQ12 (pid 133)
  --> Hub (QUEST COMPLETE)
```

---

## SIDE QUEST 1: THE DRAGON OF STREAMDALE (SQ1, Holstein Bounty Board)

```
SQ1 (pid 103): Accept "Evict the Dragon" (100 Gold)
  |
  +--> SQ11 (pid 134) --> SQ12 (pid 135) --> SQ13 (pid 136)
        --> SQ14 (pid 137) --> SQ15 (pid 138) --> SQ16 (pid 139)
              --> SQ17 (pid 140)
                    |
                    +-- [BRANCH] Two approaches:
                    |
                    +-- SQ1SS1 (pid 141) [SS]: Sexual favor
                    |     +--> SQ1SS2 (pid 144) --> SQ1SS3 (pid 145)
                    |           --> SQ1SS4 (pid 146) --> SQ1SSE (pid 147)
                    |                 --> SQ19 (pid 143) --> SQ1E (pid 148) --> Hub
                    |
                    +-- SQ18 (pid 142): Negotiate diplomatically
                          +--> SQ19 (pid 143) --> SQ1E (pid 148) --> Hub
```

---

## SIDE QUEST 2: THE WRENVILLE JOB (SQ2, Holstein Bounty Board)

```
SQ2 (pid 104): Accept "Evict the Wolf Pack" (200 Gold)
  |
  +--> SQ21 (pid 149) --> SQ22 (pid 150) --> SQ23 (pid 151)
        --> SQ24 (pid 152) --> SQ25 (pid 153) --> SQ2E (pid 154) --> Hub
```

---

## SCARHAVEN HUB (Second Town)

```
[ROOT] ScarHub (pid 168) (Scarhaven Town)
  |
  +=========================================+
  |  FIVE BRANCHES FROM SCARHAVEN:          |
  |                                         |
  |  1. ScarBS -------> Blacksmith (Hans)   |
  |  2. ScarInn ------> Inn                 |
  |  3. ScarBarracks -> Barracks            |
  |  4. ScarOther ----> Outskirts           |
  |  5. Carriages ----> Travel              |
  +=========================================+
```

---

### SCARHAVEN BRANCH 1: BLACKSMITH (ScarBS, pid 169)

```
ScarBS (Hans the Corgi's Blacksmith)
  |
  +-- SBSK (pid 173): "Browse Kami's gear"
  +-- SBSC (pid 174): "Browse your gear" ("nothing in your size")
  |
  +-- [CHAR] SBSH (pid 175): "Talk to Hans" (daytime)
  |     |
  |     +-- SBSHc1 (pid 176): "Your job"
  |     +-- SBSHc2 (pid 177): "Personal life"
  |     +-- SBSHc3 (pid 178): "Sex life"
  |     |     |
  |     |     +-- [SS] SBSHSS (pid 180): Accept Hans' advances
  |     |           +--> SBSHSS2 (pid 181)
  |     |                 +-- SBSHSS2s (pid 182): small frame
  |     |                 |     +--> SBSHSS2s2 (pid 185) --> SBSHSS2s3 (pid 186) --> ScarHub
  |     |                 +-- SBSHSS2m (pid 183): medium frame
  |     |                 |     +--> SBSHSS2m2 (pid 187) --> SBSHSSm3 (pid 188) --> ScarHub
  |     |                 +-- SBSHSS2l (pid 184): large frame
  |     |                       +--> SBSHSS2l2 (pid 189) --> SBSHSS2l3 (pid 190) --> ScarHub
  |     |
  |     +-- SBSHc4 (pid 179): "The war"
  |     +-- SBSHf (pid 191): "Tell me about Frederick"
  |     +--> ScarHub
  |
  +-- [CHAR] SBSHn (pid 196): "Visit Hans at night"
  |     +-- SBSHn2 (pid 197): Stay the night (cuddle)
  |     |     +--> SBSHn3 (pid 198): Wake up together
  |     |           +--> ScarHub
  |     +-- (leave) --> ScarHub
  |
  +-- [CHAR] HansR (pid 232): Confess feelings to Hans
  |     +--> HansR2 (pid 233) --> HansRHub (pid 234)
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 2: INN (ScarInn, pid 170)

```
ScarInn (Scarhaven Inn)
  |
  +-- [CHAR] SIIK (pid 214): Talk to Wes (Innkeeper)
  |     +-- SIIK2 (pid 217): "Rent a room" (10 gold)
  |           +-- (no gold) --> ScarInn
  |           +-- (has gold) --> SIIKR (pid 218) (your room)
  |                 +-- KamiSS1 [SS]: Sex with Kami (same tree)
  |                 +-- SHKEquip (pid 219): Equip Kami's gear
  |                 +-- SIIKRS (pid 220): "Go to sleep"
  |                 +-- (if has amulet) OrbathAmulet --> IoDHub
  |
  +-- SIB (pid 213): "Bounty Board" [EXPANDED IN v0.41]
  |     |
  |     +-- MQu2: "King's Decree: Investigate the Rumblings" (500 Gold) [MAIN QUEST 2]
  |     +-- SQ3: "Capture the Bandit Leader" (200 Gold) [STUB]
  |     +-- SQ4: "Von Aldersant: A Request" (300 Gold) [STUB]
  |     +-- (back) --> ScarInn
  |
  +-- [CHAR] Finn (pid 212): Talk to Finn
  |     +--> ScarInn (gives Birdpup Feather [ITEM])
  |     +-- [SS] FinnSS1 (pid 261): Give Divine Potion to Finn
  |           (Finn revealed as disguised god)
  |           +--> FinnSS2 (pid 294) --> FinnSS3 (pid 295)
  |                 --> FinnSS4 (pid 296) --> FinnSS5 (pid 297)
  |                       +--> ScarHub (+100 gold)
  |
  +-- SISt (pid 215): "Visit the Stables"
  |     +-- [SS] HorseSS1 (pid 227): Tame the Horse
  |     |     +--> HorseSS2 (pid 228) --> HorseSS3 (pid 229) --> ScarInn
  |     +--> ScarInn
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 3: BARRACKS (ScarBarracks, pid 171)

```
ScarBarracks
  |
  +-- [CHAR] SBaF (pid 192): "Visit Frederick's Office"
  |     |
  |     +-- [First visit:] SBaF2 (pid 199) --> SBaF3 (pid 200)
  |     |     |
  |     |     +-- SBaF3c1 (pid 202): Frederick believes (SUCCESS)
  |     |     +-- SBaF3c2 (pid 203): Pren exposes lie (PARTIAL)
  |     |     +-- SBaF3c3 (pid 201): Pren calls out (FAIL)
  |     |
  |     +-- [Return visits:] Frederick dialogue
  |     |     +-- Frc1 (pid 204): "About Scarhaven"
  |     |     +-- Frc2 (pid 205): "About yourself"
  |     |     +-- Frc3 (pid 206): "About Pren" (sword drawn!)
  |     |     +-- Frc4 (pid 207): "Forest stranger leads?"
  |     |
  |     +-- [SS] PrenSS (pid 208): Accept Pren's offer
  |           +--> PrenSS2 (pid 209) --> PrenSS3 (pid 210)
  |                 --> PrenSS4 (pid 211) --> ScarBarracks
  |
  +-- SBaB (pid 193): "Go to the Bathroom"
  |     +-- [SS] SBaBSS (pid 195): Encounter with Reptile
  |     +--> ScarBarracks
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 4: OUTSKIRTS (ScarOther, pid 172)

```
ScarOther
  |
  +-- [SS] FBM1 (pid 221): "Approach the boy"
  |     +--> FBM2 (pid 222)
  |           +-- FMBc1 (pid 223): "Take him yourself"
  |           |     +--> FMBc12 (pid 225) --> ScarHub
  |           +-- FMBc2 (pid 224): "Involve Kami"
  |                 +--> FMBc22 (pid 226) --> ScarHub
  |
  +--> ScarHub
```

---

## MAIN QUEST 2: THE HIXBOROUGH MOUNTAINS [NEW IN v0.41]

This is the major new quest chain found on the Scarhaven Bounty Board.

```
MQu2 (pid 301): Accept "Investigate the Rumblings" (500 Gold)
  |
  +--> MQu21 (pid 302): Wes gives info (mage + dragon rumored)
        |
        +-- MQu2Gear (pid 312): Check Kami's Equipment
        |     +--> MQu22 or SIB (return)
        |
        +--> MQu22 (pid 313): Carriage to Extola village, begin ascent
              |  (sets $KH to $KMH - Kami starts at full health)
              |
              +--> [BATTLE] Gnoll (pid 314): Gnoll teen ambush
                    |
                    +-- Fight (pid 315) --> FightScreen (pid 317)
                    |     [SEE BATTLE SYSTEM BELOW]
                    |     |
                    |     +-- [WIN] GnollWin (pid 321)
                    |     |     +-- "Have your way" --> GnollWin2-4 (pids 327-329) [SS]
                    |     |     |     +--> MountainPassage
                    |     |     +-- "Leave him" --> MountainPassage
                    |     |
                    |     +-- [LOSE] GnollLose (pid 322)
                    |           +--> GnollLose2 (pid 325) [SS - gnoll rapes player]
                    |                 +--> GnollLose3 (pid 326) (steals 30 gold, return to ScarHub)
                    |
                    +-- Try to Flee (1/3 chance)
                          +-- [PASS] FleePass (pid 316) --> ScarHub (retreat)
                          +-- [FAIL] FleeFailGnoll (pid 323) (gnoll steals 30 gold)
                                +--> MountainPassage (continue anyway)

MountainPassage (pid 324): Linear path upward
  |
  +-- MountainPassage2 (pid 330): Examine backpack [OPTIONAL]
  |     (Heals Kami +4 HP, gains 5 coins)
  |
  +--> CliffFace (pid 331): Cliff with insects blocking a cave
        |
        +-- [BRANCH] Three approaches to insects:
        |
        +-- (if has Magister's Dirk) Use Dirk to command insects
        |     +-- CFBDirkWin (pid 333): Success - insects disperse
        |     |     +--> Meet Akos
        |     +-- CFBDirkLose (pid 332): Fail - insects attack,
        |           Akos saves you with fire
        |           +--> Meet Akos
        |
        +-- [BATTLE] Fight insects (Monster=2, "Swarm of Insects")
              +-- CBugsWin (pid 335): Win - Akos burns remains
              |     +--> Meet Akos
              +-- CBugsLose (pid 334): Lose - Akos saves you
                    +--> Meet Akos

Akos (pid 336): Meet the reptilian mage
  |
  +--> Akos2 (pid 337): Introduction
        |
        +-- (if Reptile/Dragon species) [SS OPTION]
        |     +-- AkosPaw1 (pid 338): Paw worship scene
        |     |     +--> AkosPaw2 (pid 341) --> AkosPaw3 (pid 342)
        |     |           +--> AkosFinish
        |     +-- AkosSex1 (pid 340): Full sex scene
        |     |     +--> AkosSex2 (pid 344) --> AkosSex3 (pid 345)
        |     |           +--> AkosFinish
        |     +-- AkosReject (pid 339): Decline
        |           +--> AkosFinish (Akos lifts you up cliff)
        |
        +-- (other species) AkosReject path only
        |
        +--> AkosFinish (pid 343): Get Magically Treated Meats [ITEM]
              Akos lifts party up cliff with forcefield magic
              |
              +--> [BATTLE] Pigorc (pid 347): Ambush in rock crevice
                    |
                    +-- Fight (Monster=3, "Horc", 25HP/5ATK/0SPD/0ARM)
                    |     |
                    |     +-- [WIN] PigorcFWin (pid 349)
                    |     |     +--> Plateau (continue)
                    |     |
                    |     +-- [LOSE] PigorcFLose (pid 348)
                    |           +--> PigorcFLose2 (pid 355) [SS - pigorc rapes player]
                    |                 +--> PigorcFLose3 (pid 356)
                    |                       +--> PigorcFLose4 (pid 357)
                    |                             +--> ScarHub (retreat)
                    |
                    +-- Try to Flee
                          +-- [PASS] FleePassPigorc (pid 351) --> Plateau
                          +-- [FAIL] FleeFailPigorc (pid 350)
                                +--> FleeFailPigorc2 (pid 353) [SS]
                                      +--> FleeFailPigorc3 (pid 354)
                                            +--> ScarHub (retreat)

Plateau (pid 352): Rest area near summit
  |
  +-- (if has Pain Leaves) Feed to Kami (+10 HP)
  +-- (if has Magically Treated Meats) Feed to Kami (+8 HP)
  |
  +--> Plateau2 (pid 358): Wake up, spoon Kami, continue
        |
        +--> MQu2Finish (pid 359): Summit arena - meet Hooded Mage
              |
              | "A fellow Magister...how cumbersome."
              | Mage summons Dark Dragon (Monster=4, 150HP/15ATK/5SPD/10ARM)
              |
              +--> MQu2Finish2 (pid 360): UNWINNABLE FIGHT
                    Dragon is too powerful. Kami sacrifices himself,
                    pushes player out of Dragon's claw, gets flung
                    off mountain. Player blacks out. IoD patrol rescues.
                    |
                    +--> IoDIntro (pid 361) [ISLE OF DRAGONS]
```

---

## THE BATTLE SYSTEM [NEW IN v0.41]

```
COMBAT MECHANICS (FightScreen, pid 317):

  FLOW:
    Fight (pid 315) sets monster stats by $Monster value
    --> FightScreen: displays HP, allows "Attack" or "Try to Flee"

  KAMI'S STATS (base):
    Max Health: 20 + equipment bonuses
    Attack: 5 + equipment bonuses
    Speed: 8 + equipment bonuses
    Armour: 0 + equipment bonuses

  MONSTER ROSTER:
    $Monster=1: Gnoll      (20 HP, 3 ATK, 4 SPD, 1 ARM)
    $Monster=2: Swarm      (15 HP, 5 ATK, 5 SPD, 0 ARM)
    $Monster=3: Horc       (25 HP, 5 ATK, 0 SPD, 0 ARM)
    $Monster=4: Dark Dragon (150 HP, 15 ATK, 5 SPD, 10 ARM)

  TURN ORDER: Determined by comparing $KS (Kami Speed) vs $MonS (Monster Speed)
    Higher speed attacks first.

  HIT/MISS: Random roll 1-100 compared against miss chance
    $KMissC = $MonS * 5  (chance Kami misses)
    $EMissC = $KS * 5    (chance enemy misses)

  DAMAGE: Attacker's ATK - Defender's ARM

  FLEE: 1/3 chance of success (random 0,1,2; success on 0)
    Flee always succeeds vs Insects ($Monster=2)
    Flee vs Dark Dragon ($Monster=4) always goes to MQu2Finish2

  OUTCOMES BY MONSTER:
    Win  --> VictoryScreen (pid 320) routes to GnollWin/CBugsWin/PigorcFWin
    Lose --> GameOverScreen (pid 319) routes to GnollLose/CBugsLose/PigorcFLose
    Dark Dragon: ALL outcomes (win/lose/flee) --> MQu2Finish2 (unwinnable)

  EQUIPMENT STAT TABLE (EquipmentCheck, pid 310, header tag):
    HELM SLOT:
      No Helm:        +0 HP, +0 ATK, +0 SPD, +0 ARM
      Battle Helm:    +3 HP, -1 ATK, -2 SPD, +5 ARM
      Speedband:      +0 HP, +1 ATK, +4 SPD, +1 ARM
      Padded Helmet:  +2 HP, +0 ATK, -1 SPD, +3 ARM

    COLLAR SLOT:
      No Collar:      +0 all
      Spiked Collar:  +0 HP, +2 ATK, +2 SPD, +1 ARM
      Magic Collar:   +15 HP, +0 ATK, +0 SPD, +0 ARM
      Wolf's Rebuke:  +7 HP, +5 ATK, +5 SPD, +1 ARM  [BEST]

    PAWS SLOT:
      No Guards:      +0 HP, +0 ATK, +1 SPD, +0 ARM
      Claw Guards:    +0 HP, +2 ATK, +0 SPD, +2 ARM
      Obsidian Guards:+1 HP, +0 ATK, -4 SPD, +10 ARM

    BACK SLOT:
      No Armour:      +0 HP, +0 ATK, +1 SPD, +0 ARM
      Small Pack Saddle: +5 HP, -1 ATK, -1 SPD, +0 ARM
      Padded Armour:  +5 HP, +0 ATK, -2 SPD, +3 ARM
```

---

## ISLE OF DRAGONS (Third Hub, New in v0.41)

Accessed by: Completing MQu2 (forced entry after mountain defeat), or using Zexir's Amulet from any Inn room.

```
IoDIntro (pid 361): Wake up in unknown room, 2 weeks unconscious
  |
  +--> IoDIntro2 (pid 362): Explore room, find clothes
        |
        +--> IoDIntro3 (pid 363): Dragon at window tells you to go to council
              |
              +--> IoDIntro4 (pid 364): Walk down hall to council chamber
                    |
                    +--> IoDIntro5 (pid 365): Meet Zexir
                          |
                          +-- IoDIntro5c1 (pid 366): "Where am I?" (Isle of Dragons)
                          +-- IoDIntro5c2 (pid 367): "Who are you?" (Zexir, isle leader)
                          +-- IoDIntro5c3 (pid 368): "Where is Kami?" (safe at village)
                          +-- IoDIntro5c4 (pid 369): "How did you know I'm a Magister?"
                          |
                          +--> IoDIntro6 (pid 370): Go find Kami
                                |
                                +--> IoDIntro7 (pid 371): Meet Erel the animal doctor
                                      |
                                      +--> IoDIntro8 (pid 372): Reunite with Kami
                                            |
                                            +--> IoDHub (pid 373)
```

### ISLE OF DRAGONS HUB (IoDHub, pid 373)

```
[ROOT] IoDHub (Icaria Town Plaza)
  |
  +==========================================+
  |  BRANCHES FROM ISLE HUB:                 |
  |                                          |
  |  1. ErelHub -------> Animal Doctor       |
  |  2. CouncilChamber -> Council / Zexir    |
  |  3. IODArena ------> Arena (Raln)        |
  |  4. IODShop -------> Market              |
  |  5. IODInn --------> Inn (bounty board)  |
  |  6. IoDHouses -----> Dragon Homes/Caves  |
  +==========================================+
```

### IOD BRANCH 1: EREL (ErelHub, pid 374)

```
ErelHub (daytime only)
  |
  +-- [CHAR] ErelC (pid 381): Get to know Erel
        |
        +-- Erelc1 (pid 382): How he came to the island
        +-- Erelc2 (pid 383): Is he single? (interested in animals, not people)
        +-- Erelc3 (pid 384): His medical knowledge (studied in Adplagam)
        +-- Erelc4 (pid 385): Spells he knows (basic healing, light)
        +--> IoDHub
```

### IOD BRANCH 2: COUNCIL CHAMBER (CouncilChamber, pid 375)

```
CouncilChamber
  |
  +-- IoDRoom (pid 386): Rest in assigned room
  |     |
  |     +-- IoDKEquip (pid 388): Change Kami's equipment
  |     +-- KamiSS1 [SS]: Sex with Kami (same tree)
  |     +-- (rest) IoDStaySleep (pid 389): Sleep (3 dream variants)
  |     +-- (if has amulet) IoDAmulet (pid 392): Teleport to Holstein/Scarhaven
  |
  +-- TeleporterC (pid 387): Use teleporter (if no amulet)
  |     Travel to Holstein or Scarhaven (50 gold fee)
  |
  +-- [CHAR] Zexir1D (pid 390): Visit Zexir (daytime)
  |     |
  |     +-- Zexir1DWorld (pid 412): "Teach me about the world"
  |     |     +--> Zexir1DWorld2 (pid 416): Dragon-Nomad war history
  |     |           +--> Zexir1DWorld3 (pid 417): Map of Orbath
  |     |                 +--> Zexir1DWorld4 (pid 418): Advice ("trust no-one")
  |     |
  |     +-- Zexir1DMagic (pid 414): "Teach me magic"
  |     |     +--> Zexir1DMagic2 (pid 422): Learn Volition Light [SPELL]
  |     |           +--> Zexir1DMagic3 (pid 424): "Teach me more"
  |     |                 +--> Zexir1DMagic4 (pid 425): Learn Volition Fireball [SPELL]
  |     |
  |     +-- Zexir1DIsle (pid 415): "Tell me about the Isle"
  |     |     +--> Zexir1DIsle2 (pid 419): 3 heads of leadership
  |     |           (Zexir=Magic, Raln=Military, Valia=unspecified)
  |     |
  |     +-- Zexir1DFight (pid 413): "Teach me to fight" (redirects to Raln)
  |
  +-- [SS] Zexir1N (pid 391): Visit Zexir (nighttime)
        |
        +-- (50% chance) ZexirAltSS1 (pid 431): Catch Zexir with student
        |     +--> ZexirAltSS2 (pid 435): Watch the scene
        |           +--> CouncilChamber
        |
        +-- (50% chance) Zexir1N: Sneak into his room
              |
              +-- (if knows Fireball) Zexir1N2 (pid 427): "Hang out"
              |     |
              |     +-- [SS] ZexirSS1 (pid 429): Touch his slit
              |     |     +--> ZexirSS2 (pid 432) --> ZexirSS3 (pid 433)
              |     |           --> ZexirSS4 (pid 434) --> CouncilChamber
              |     |
              |     +-- Zexir1N21 (pid 430): "Too much, leave"
              |           +--> CouncilChamber
              |
              +-- (no Fireball) Zexir1N1 (pid 428): Zexir sends you away
                    +--> CouncilChamber
```

### IOD BRANCH 3: ARENA (IODArena, pid 376)

```
IODArena (daytime only)
  |
  +-- [First visit:] IODArenaD2 (pid 403): Meet Raln
  |     (Raln berates you; arena not yet available for training)
  |
  +-- [Return visits:] "Not ready to spar yet" (placeholder)
  |
  +--> IoDHub
```

### IOD BRANCH 4: MARKET (IODShop, pid 377)

```
IODShop (daytime only)
  |
  +-- IoDMStall (pid 394): Magic Vendor (wizened raccoon)
  |     +-- (if has Dog Collar) Dispel curse for 50g --> Wolf's Rebuke [ITEM]
  |     +-- (if has Strange Mushroom) Sell for 40g
  |
  +-- IoDVStall (pid 395): Herbal Vendor (mouse woman)
  |     +-- (if has Strange Mushroom) Sell for 40g
  |     +-- Purchase Empty Bottle (pid 402) [ITEM] (10g)
  |
  +-- IoDBStall (pid 396): Equipment Vendor (bear)
  |     +-- Padded Helmet (pid 400) [ITEM] (20g) - +2HP, -1SPD, +3ARM
  |     +-- Obsidian Guards (pid 398) [ITEM] (40g) - +1HP, -4SPD, +10ARM
  |     +-- Padded Armour (pid 397) [ITEM] (30g) - +5HP, -2SPD, +3ARM
  |     +-- Magic Collar (pid 399) [ITEM] (25g) - +15HP
  |
  +--> IoDHub
```

### IOD BRANCH 5: INN (IODInn, pid 378)

```
IODInn
  |
  +-- Bounty Board: "Nothing available right now" (placeholder)
  |
  +--> IoDHub
```

### IOD BRANCH 6: DRAGON HOUSES / CAVES (IoDHouses, pid 379)

```
IoDHouses (daytime only; dangerous at night)
  |
  +-- (if met Hran via SS) Cave203 (pid 436): Visit Hran at home
  |     |
  |     +-- (1/3 chance he's home)
  |     |     +-- Cave2032 (pid 440): Read grandfather's journal
  |     |     |     +-- Hran2SS1 (pid 441) [SS]: Have sex with Hran
  |     |     |     |     +-- Hran2SSc1 (pid 443): Hran tops
  |     |     |     |     |     +--> Hran2SSc12-15 (pids 445-448)
  |     |     |     |     +-- Hran2SSc2 (pid 444): Player tops
  |     |     |     |           +-- Hran2SSc2c1 (pid 449): One variant
  |     |     |     |           |     +--> Hran2SSc2c12-13 (pids 451-452)
  |     |     |     |           +-- Hran2SSc2c2 (pid 450): Another variant
  |     |     |     |                 +--> Hran2SSc2c22-23 (pids 453-454)
  |     |     |     +-- Cave2033 (pid 442): Just friends
  |     |     |
  |     |     +--> IoDHouses
  |     |
  |     +-- (2/3 chance not home) --> IoDHouses
  |
  +-- IoDCaves (pid 437): Pick a random cave (3 random encounters)
  |     |
  |     +-- (1/3) Den of sleeping hatchlings - kicked out by mother
  |     +-- (1/3) Cave102 (pid 438): Mother Dragon + cute hatchling (observe only)
  |     +-- (1/3) Cave124 (pid 439): Two Dragons having sex
  |           +-- Cave124Pass (pid 455): Stay quiet - watch [SS voyeur]
  |           +-- Cave124Fail (pid 456): Get caught - kicked out
  |
  +--> IoDHub

NIGHTTIME at IoDHouses:
  |
  +-- Hran (pid 404): Find Hran training at night
        |
        +-- Hran1 (pid 405): Introduction (first time)
        |     +--> Hran2 (pid 406): Learns you're a Magister
        |           +--> Hran3 (pid 407): Mating curse discussion
        |                 +-- [SS] HranSS1 (pid 408): Accept
        |                 |     +--> HranSS2 (pid 410) --> HranSS3 (pid 411)
        |                 |           +--> IoDHub
        |                 +-- Hran4 (pid 409): Decline --> IoDHub
        |
        +-- (return visit) Direct to SS or leave
```

---

## INVENTORY ITEMS (Complete List - v0.41)

```
ITEMS (inventory passage, pid 4)
  |
  +-- Coin Pouch (pid 42)          - Currency (start: 500 gold in Variables)
  +-- Magic Flower (pid 61)        - Rare alchemy reagent (given by girl in intro)
  +-- Silver Orb (pid 71)          - Unknown purpose, glows dimly (Market)
  +-- Dog Collar (pid 72)          - Cursed collar; dispellable at IoD --> Wolf's Rebuke
  +-- Ruby Necklace (pid 73)       - Gold-plated jewelry (Market)
  +-- Pain Leaves (pid 74)         - Heals Kami +10 HP (Market)
  +-- Health Potion (pid 75)       - Heals wounds (Market)
  +-- Endowment Potion (pid 76)    - Sexual enhancement, causes blackout (Market)
  +-- Magister's Dirk (pid 81)     - Royal Magister blade (Peddler); used vs insects
  +-- Strange Mushroom (pid 126)   - Sellable for 40g at IoD (Forest Maze)
  +-- Speedband (pid 311)          - Wyatt's headband; +1ATK, +4SPD, +1ARM (Forest Maze)
  +-- Birdpup Feather (pid 216)    - White feather, black tip (Finn, Scarhaven)
  +-- Divine Potion (pid 262)      - Golden god-potion; give to Finn for SS [NEW]
  +-- Glass Ornament (pid 272)     - Misfit's love token (Misfit TrueEnd) [NEW]
  +-- Magically Treated Meats (pid 346) - Never-rotting jerky from Akos; heals Kami +8 HP [NEW]
  +-- Zexir's Amulet (pid 380)     - Teleport to/from Isle of Dragons [NEW]
  +-- Mysterious Gem (pid 457)      - Red gem, whispers obscenities (Isle caves) [NEW]
  +-- Empty Bottle (pid 402)        - Standard empty bottle (IoD market, 10g) [NEW]
  +-- Heart Ring (pid 465)          - Shows relationship status + LoveMeter [NEW]

KAMI EQUIPMENT (Helm / Collar / Paws / Back)
  HELM:
  +-- No Helm (pid 306)            - Default
  +-- Battle Helm (pid 162)        - +3HP, -1ATK, -2SPD, +5ARM (Holstein/Scarhaven smiths)
  +-- Speedband (pid 311)          - +0HP, +1ATK, +4SPD, +1ARM (Forest Maze)
  +-- Padded Helmet (pid 400)      - +2HP, +0ATK, -1SPD, +3ARM (IoD market, 20g) [NEW]

  COLLAR:
  +-- No Collar (pid 307)          - Default
  +-- Spiked Collar (pid 163)      - +0HP, +2ATK, +2SPD, +1ARM (Holstein/Scarhaven smiths)
  +-- Magic Collar (pid 399)       - +15HP (IoD market, 25g) [NEW]
  +-- Wolf's Rebuke (pid 401)      - +7HP, +5ATK, +5SPD, +1ARM (dispel Dog Collar at IoD) [NEW/BEST]

  PAWS:
  +-- No Guards (pid 308)          - +0HP, +0ATK, +1SPD, +0ARM (default)
  +-- Claw Guards (pid 164)        - +0HP, +2ATK, +0SPD, +2ARM (Holstein/Scarhaven smiths)
  +-- Obsidian Guards (pid 398)    - +1HP, +0ATK, -4SPD, +10ARM (IoD market, 40g) [NEW]

  BACK:
  +-- No Armour (pid 309)          - +0HP, +0ATK, +1SPD, +0ARM (default)
  +-- Small Pack Saddle (pid 165)  - +5HP, -1ATK, -1SPD, +0ARM (Holstein/Scarhaven smiths)
  +-- Padded Armour (pid 397)      - +5HP, +0ATK, -2SPD, +3ARM (IoD market, 30g) [NEW]
```

---

## SPELLS (Spell Book, pid 421) [NEW IN v0.41]

```
SPELLS
  |
  +-- Calm (pid 420)
  |     Basic Magister spell. Calms a creature into docile state.
  |     Side effect: makes them horny for you.
  |     (Pre-learned; set in Variables)
  |
  +-- Volition Light (pid 423)
  |     Orb of bright white light. Illuminates dark places.
  |     Learned from: Zexir (Zexir1DMagic --> Zexir1DMagic2)
  |
  +-- Volition Fireball (pid 426)
        Condensed fire ball to throw at enemies.
        "The flames keep talking to you."
        Learned from: Zexir (Zexir1DMagic3 --> Zexir1DMagic4)
        Required for: Night visit SS with Zexir
```

---

## BOUNTY BOARDS - COMPLETE LISTING

```
HOLSTEIN BOUNTY BOARD (InnQuests, pid 45):
  1. [MAIN] King's Decree: Slay the Wild Animals (500 Gold) --> MQ1
  2. Village of Streamdale: Evict the Dragon (100 Gold) --> SQ1
  3. Merchant Axedull: Evict the Wolf Pack (200 Gold) --> SQ2

SCARHAVEN BOUNTY BOARD (SIB, pid 213):
  1. [MAIN] King's Decree: Investigate the Rumblings (500 Gold) --> MQu2
  2. Scarhaven Royal Guard: Capture the Bandit Leader (200 Gold) --> SQ3 [STUB]
  3. Von Aldersant: A Request (300 Gold) --> SQ4 [STUB]

ISLE OF DRAGONS BOUNTY BOARD (IODInn, pid 378):
  "Nothing available right now." [PLACEHOLDER]
```

---

## STUBS / INCOMPLETE CONTENT

```
PASSAGES THAT ARE PLACEHOLDERS OR UNFINISHED:

1. SQu41 (pid 305): "Double-click this passage to edit it."
   -- Completely empty placeholder. Likely intended for SQ4 content.

2. SQ3 (pid 299): "Capture the Bandit Leader" (200 Gold)
   -- Displays quest text but ends with "try this at another time"
   -- Returns to SIB. No quest chain exists.

3. SQ4 (pid 300): "Von Aldersant: A Request" (300 Gold)
   -- "A rather delicate request...seeking children"
   -- Displays quest text but ends with "leave it for now"
   -- Returns to SIB. SQu41 is the empty stub for this.

4. HubSpire (pid 40): Silver Spire
   -- Guard turns you away. No content beyond description.

5. WyattRHub (pid 238): Wyatt Relationship Hub
   -- "Too much adventuring to do" -- no activities available.

6. HansRHub (pid 234): Hans Relationship Hub
   -- "Too busy working" -- no activities available.

7. IODArena / IODArenaD2 (pids 376, 403): Arena
   -- Meet Raln but "not ready to spar yet." No combat training.

8. IODInn (pid 378): Isle of Dragons Inn Bounty Board
   -- "Nothing available right now." Empty board.

9. Variables (pid 157): Debug/init passage
   -- Pre-sets inventory with Strange Mushroom and Zexir's Amulet
   -- Sets starting coin to 500 (debug values, not production)

10. Basic Copy Paste Shit (pid 291): Developer template passage
    -- Internal development reference.

11. Useful Links and Shit (pid 155): Developer notes passage.
```

---

## THEMES AND STORY ARCS

### Major Narrative Threads

1. **The Magister's Burden**: The player is a Magister -- gifted with power over animals, but cursed with pheromones that make animals desire them sexually. The rogue warlock from Dinus's story (InnStay/DinusI2) shows the dark path a Magister can take.

2. **The Hooded Mage / Dark Magister**: The antagonist encountered at the summit of the Hixborough Mountains (MQu2Finish, pid 359). Commands a Dark Dragon. Recognizes the player as "a fellow Magister." Identity unknown. This is the central mystery/villain thread.

3. **The Forest God Pan**: Mentioned in intro lore. Pan blessed the player as Magister, gifted Kami speech. The "Awakening" involved ritual coitus with Pan. Pan is also responsible for the rogue warlock Dinus killed. Dream sequences reference a Satyr figure (InnStaySleep, dream 3).

4. **Dragon-Nomad Relations**: Explored extensively on the Isle of Dragons. 500-year-old war between Dragons and "Nomads" (non-dragons). Magisters served as mediators/peacekeepers. Zexir teaches this history (Zexir1DWorld). The Streamdale quest (SQ1) is a microcosm of this tension.

5. **Misfit's Redemption Arc**: The only fully-realized relationship. Misfit goes from shady alley rat to loving partner. His True Ending (LoveMeter >1000) features genuine emotional confession and a handcrafted glass ornament. His brother Fiend provides comic relief and additional SS content.

6. **Finn the Disguised God**: The white-furred pup at Scarhaven Inn is actually a deity. Giving him the Divine Potion triggers a teleportation to a private realm and a sexual encounter where he reveals his divine nature (FinnSS1-5). He rewards the player with 100 gold and implants the desire to bring more Divine Potions.

### Lore/World-Building

- **Orbath**: Ring-shaped continent. Reliquim (west, lush) and Adplagam (east, desert). Central ocean houses the Council of Wizards.
- **Holstein**: Capital of Reliquim. Home to the Silver Spire (military HQ, guarded).
- **Scarhaven**: Frontier town. Guard Captain Frederick, Blacksmith Hans.
- **Isle of Dragons**: Hidden island, 800 servants + 500+ dragons. Led by Zexir (magic), Raln (military), Valia (unnamed role). Town called Icaria.
- **Hixborough Mountains**: North of Holstein. Village of Extola at base. Heaven's Reach outpost at summit. Infested with gnolls and pigorcs.
- **Arcplage Academy**: Akos is a Senior there. An educational institution for mages.

### How Kami Can Get Injured
- **Battle system**: Kami takes damage when enemies land hits (ATK - ARM = damage). If $KH reaches 0, Kami is "defeated" and the battle is lost, triggering the Lose outcome for that monster.
- **Gnoll encounter**: Gnoll kicks Kami during flee attempt (FleeFailGnoll). Gnoll knocks Kami down in combat loss (GnollLose).
- **Pigorc encounter**: Pigorc slams Kami aside (PigorcFLose, FleeFailPigorc).
- **Dark Dragon**: Kami is flung off the mountain by the Dragon's claw strike (MQu2Finish2) -- the most dramatic injury. He survives but requires 2 weeks of recovery on the Isle.
- **Insect swarm**: Can wound Kami during CliffFace battle (CBugsLose).
- **Night alley figure**: Kami protects player from dangerous stranger (Alley1N21).

---

## DAY/NIGHT CYCLE SYSTEM

```
TIME SYSTEM:
  $DN     = current time ("day" or "night")
  $DNO    = next time
  $DNO2   = time after next

  Cycle advances when player sleeps or rests:
    (set:$DN to $DNO)(set:$DNO to $DNO2)(set:$DNO2 to $DN)
    Effect: day -> night -> day -> night...

  Time-gated content:
    DAY ONLY:  HubMarket shops, Alley1D (Misfit), FountD1/D2 (Wyatt),
               ScarBS (Hans daytime), ErelHub, IODShop, IODArena,
               IoDHouses exploration, Zexir1D
    NIGHT ONLY: Alley1N (Wyatt SS, Night Figure), FountN1 (Night Rat),
                SBSHn (Hans night), Zexir1N, Hran night training
```

---

## CURRENCY SYSTEM

```
GOLD ($coin):
  Starting amount: varies (Killian gives "some coins" in intro)
  Debug/Variables passage sets to 500

  INCOME SOURCES:
    Quest rewards: MQ1 (500g), SQ1 (100g), SQ2 (200g), MQu2 (500g)
    FinnSS5: +100g after divine encounter
    MountainPassage2: +5g from dead adventurer's pack
    Selling Strange Mushroom at IoD: +40g

  EXPENSES:
    Inn room (Holstein/Scarhaven): 10g per night
    Tailor clothes: 30g
    IoD Equipment: Padded Helmet 20g, Magic Collar 25g, Padded Armour 30g, Obsidian Guards 40g
    Dispel Dog Collar curse at IoD: 50g
    Empty Bottle at IoD: 10g
    Teleporter at IoD (if no amulet): 50g

  LOSSES:
    Gnoll steals 30g on flee fail or combat loss
```

---

## MCTS DECISION TREE SUMMARY (Probability-Weighted Paths)

```
TOTAL NODES: 465 passages
TOTAL CHARACTERS: 25+ interactable (including monsters)
TOTAL ITEMS: 28 (12 inventory + 8 Kami equipment + 8 new)
TOTAL SPELLS: 3 (Calm, Volition Light, Volition Fireball)
TOTAL QUESTS: 6 (2 main + 2 completed side + 2 stub side)
TOTAL LOCATIONS: 3 towns + 1 maze + forest intro + mountain path
TOTAL BATTLES: 4 monster types (Gnoll, Swarm, Horc, Dark Dragon)

CRITICAL PATH (shortest to current "endgame"):
  Title -> Intro1 -> Species -> [6 creation steps] -> Intro2-10
  -> TheBeginning -> Hub -> Carriages -> ScarHub -> SIB
  -> MQu2 -> MQu21-22 -> Gnoll -> Mountain -> Akos -> Pigorc
  -> Plateau -> MQu2Finish -> MQu2Finish2 -> IoDIntro -> IoDHub
  -> [open world continues]

DECISION DEPTH BY BRANCH:
========================================================
  Character Creation:      6 species x appearance combos
  Intro Dialogue:          3 optional topics (Kami1, Intro3)
  Holstein Inn:            3 paths (room/talk/SS) depth 2-5
  Holstein Fountain:       5 paths (day/night/Wyatt) depth 1-4
  Holstein Market:         3 stalls, depth 2-3
  Holstein Tailor [NEW]:   1 path, depth 5 (SS chain)
  Holstein Alley Day:      2 paths (talk/SS) depth 1-2
  Holstein Alley Night:    2 paths (window/figure) depth 2-5
  Fiend Single [NEW]:     1 path, depth 5 (SS chain)
  Main Quest 1 (Forest):  16-node maze + 7-node boss sequence
  Side Quest 1 (Dragon):  9 nodes, branch at SQ17 (sex/diplomacy)
  Side Quest 2 (Wrenville): 5 nodes, linear
  Main Quest 2 (Mtns)[NEW]: 30+ nodes, 3 battles, 1 boss (unwinnable)
  Scarhaven Blacksmith:    3 shop + 4 dialogue + 3 SS variants + relationship
  Scarhaven Inn:           5 paths (room/board/finn/stables/bounties)
  Scarhaven Barracks:      3 paths (Frederick/Pren/bathroom)
  Scarhaven Outskirts:     1 path, branch into 2 SS variants
  Misfit Relationship[NEW]: 15+ activities, alchemy minigame, family, picnic, true end
  Isle of Dragons [NEW]:   6 sub-hubs, 40+ passages
    Erel:                  4 dialogue topics
    Zexir Day:             4 topics (world/magic/isle/fight) + 2 spell acquisitions
    Zexir Night:           2 SS paths (50% voyeur, 50% direct)
    Arena:                 Meet Raln (placeholder)
    Market:                3 vendors, new equipment + curse removal
    Dragon Caves:          3 random encounters + Hran relationship
========================================================

MCTS EXPANSION FACTOR PER NODE:
  Hub (Holstein):    8 children  <-- highest branching
  ScarHub:           5 children
  IoDHub:            6 children  <-- new hub
  InnQuests:         4 children (3 quests + back)
  SIB:               4 children (3 quests + back)
  Species:           6 children (race selection)
  MisfitRHub:        6 children (highest relationship branching)
  Maze nodes:        2-5 children each (navigation)
  FightScreen:       2-3 children (attack/flee)
  CliffFace:         3 children (dirk/fight/climb)

LEAF NODES (terminals that return to hubs): ~65
DEAD END / DYNAMIC NODES (item descriptions): ~25
LINEAR CHAINS (no player choice): ~55%
BRANCHING NODES (real decisions): ~45%

ROLLOUT OUTCOMES:
  - Every path eventually loops back to Hub, ScarHub, or IoDHub
  - No permanent death / game over states exist
  - MQu2 boss fight is UNWINNABLE by design (all outcomes -> IoDIntro)
  - Quest completion flags unlock new dialogue and areas
  - Time-of-day (day/night) gates certain content
  - Gold gates room rentals and shop purchases
  - Trust mechanics gate Frederick's friendship (SBaF3)
  - LoveMeter gates relationship activities (250/500/1000 thresholds)
  - Species gates Akos SS content (Reptile/Dragon only for paw/sex)
  - Spell knowledge gates Zexir night SS (requires Volition Fireball)
  - Item possession gates several paths:
      Magister's Dirk -> insect bypass
      Divine Potion -> Finn SS
      Zexir's Amulet -> IoD fast travel
      Dog Collar + 50g -> Wolf's Rebuke
```

---

## FULL GRAPH ADJACENCY (for computational MCTS)

```
Title --> Intro1
Intro1 --> Species
Species --> CC, CF, CV, CA, CR, CD
CC/CF/CV/CA/CR/CD --> Age
Age --> Body --> Height --> Hair
Hair --> HairC, Eye
HairC --> Eye
Eye --> Cock --> DickL --> CharacterFinish
CharacterFinish --> Intro2 --> Intro3
Intro3 --> Intro3c1, Intro3c2, Intro3c3
Intro3c1 --> Intro3c2, Intro3c3, Intro3c4
Intro3c2 --> Intro3c1, Intro3c3, Intro3c4
Intro3c3 --> Intro3c1, Intro3c2, Intro3c4
Intro3c4 --> Intro4 --> Intro5 --> Intro6
Intro6 --> Kami1, Intro7
Kami1 --> Kami1c1, Kami1c2, Kami1c3, Intro7
Intro7 --> Intro8 --> Intro9 --> Intro10 --> TheBeginning --> Hub

Hub --> HubInn, HubFount, HubMarket, HolsteinTailor, HubSpire, Alley1D, Alley1N, Carriages, FiendSingle
HubInn --> InnStay, InnQuests, Hub
InnStay --> InnStayPay, DinusI, DinusSS1
InnStayPay --> HubInn, InnStayRoom
InnStayRoom --> KamiSS1, HolsteinKEquip, InnStaySleep, OrbathAmulet
KamiSS1 --> KamiSS1c1, KamiSS1c2
KamiSS1c1 --> KamiSS1c12 --> InnStaySleep, SIIKRS, IoDStaySleep
KamiSS1c2 --> KamiSS1c22 --> InnStaySleep, SIIKRS, IoDStaySleep
InnStaySleep --> HubInn
DinusI --> DinusI2 --> HubInn
DinusSS1 --> DinusSS2 --> HubInn, DinusSS3
DinusSS3 --> DinusSS4 --> DinusSS5 --> HubInn
InnQuests --> MQ1, SQ1, SQ2, HubInn

HubFount --> FountD1, FountD2, Hub, Wyatt2, FountN1, WyattR
FountD1 --> Wyatt1, HubFount
Wyatt1 --> Hub
Wyatt2 --> Wyatt2c1, Wyatt2c2, Wyatt2c3, Wyatt2c4, HubFount
FountN1 --> FountN11, Hub
FountN11 --> HubFount
WyattR --> WyattR2 --> WyattRHub
WyattRHub --> WyattRBU, Hub

HubMarket --> MarkMagic, MarkHerb, MarkPed, Hub
MarkMagic --> MarkMagicF1, HubMarket
MarkHerb --> HubMarket, EPFuck
EPFuck --> EPFuck2 --> Hub
MarkPed --> MarkPed2, HubMarket
MarkPed2 --> MarkPed22, MarkPed23
MarkPed22 --> Hub
MarkPed23 --> HubMarket

HolsteinTailor --> HolsteinTailor2 --> HolsteinTailor3 --> HolsteinTailor4
HolsteinTailor4 --> HolsteinTailor5 --> HolsteinTailor6 --> HolsteinTailor7 --> Hub

HubSpire --> Hub

Alley1D --> Hub, MisfitSS1, MisfitI, MisfitR
MisfitI --> MisfitSS1, Hub
MisfitSS1 --> Hub
MisfitR --> MisfitR2 --> MisfitRHub
MisfitRHub --> MisfitRI, MisfitHouse, MisfitFam, MisfitPicnic, MisfitTrueEnd, MisfitRBU, Hub
MisfitRI --> MisfitRI1-5, MisfitRISS, MisfitRHub
MisfitHouse --> MisfitHouse2
MisfitHouse2 --> MisfitHSS, MisfitLabGame, MisfitFiend1, MisfitRHub
MisfitHSS --> MisfitHSSc1, MisfitHSSc2
MisfitHSSc1 --> MisfitHSSc12 --> MisfitHSSc13 --> MisfitHSSc14 --> MisfitRHub
MisfitHSSc2 --> MisfitHSSc21 --> MisfitHSSc22 --> MisfitRHub
MisfitLabGame --> MisfitLabGame2-6 --> MisfitRHub
MisfitFam --> MisfitFiend --> MisfitFiendc1-5 --> MisfitRHub
MisfitFiend1 --> MisfitFiend2 --> MisfitFiendLow, MisfitFiendHigh
MisfitFiendLow --> MisfitFiendLow2-4 --> MisfitRHub
MisfitPicnic --> MisfitPicnic2 --> MisfitPicnic3 --> Hub
MisfitTrueEnd --> MisfitRHub
MisfitRBU --> Hub, MisfitRHub

FiendSingle --> FiendSingle2 --> FiendSingle3 --> FiendSingle4
FiendSingle4 --> FiendSingle5 --> FiendSingle6 --> Hub

Alley1N --> Alley1N1, Alley1N2, Hub
Alley1N1 --> WyattSS1, Alley1N
WyattSS1 --> WyattSS2 --> Hub, WyattSS3
WyattSS3 --> Hub, WyattSS4
WyattSS4 --> WyattSS5, WyattSSE
WyattSS5 --> WyattSSE
WyattSSE --> Hub, WyattSSE2
WyattSSE2 --> Hub
Alley1N2 --> Alley1N21 --> Hub

Carriages --> HolC, ScarC
HolC --> Hub
ScarC --> ScarHub

MQ1 --> MQ2 --> MQ3 --> MQ4 --> MQ5 --> MQ52 --> Maze9
[Maze grid: see above]
Maze11 --> MQ6 --> MQ7 --> MQ8 --> MQ9 --> MQ10 --> MQ11 --> MQ12 --> Hub

SQ1 --> SQ11 --> SQ12 --> SQ13 --> SQ14 --> SQ15 --> SQ16 --> SQ17
SQ17 --> SQ1SS1, SQ18
SQ1SS1 --> SQ1SS2 --> SQ1SS3 --> SQ1SS4 --> SQ1SSE --> SQ19
SQ18 --> SQ19 --> SQ1E --> Hub

SQ2 --> SQ21 --> SQ22 --> SQ23 --> SQ24 --> SQ25 --> SQ2E --> Hub

SQ3 --> SIB
SQ4 --> SIB
SQu41 --> (empty)

ScarHub --> ScarBS, ScarInn, ScarBarracks, ScarOther, Carriages
ScarBS --> SBSK, SBSC, SBSH, ScarHub, SBSHn, HansR
SBSH --> SBSHc1-4, SBSHf, SBSHSS, ScarHub
SBSHSS --> SBSHSS2 --> SBSHSS2s, SBSHSS2m, SBSHSS2l
SBSHSS2s --> SBSHSS2s2 --> SBSHSS2s3 --> ScarHub
SBSHSS2m --> SBSHSS2m2 --> SBSHSSm3 --> ScarHub
SBSHSS2l --> SBSHSS2l2 --> SBSHSS2l3 --> ScarHub
SBSHn --> SBSHn2 --> SBSHn3 --> ScarHub
HansR --> HansR2 --> HansRHub
HansRHub --> HansRBU, ScarHub

ScarInn --> SIIK, SIB, SISt, Finn, ScarHub
SIIK --> SIIK2 --> ScarInn, SIIKR
SIIKR --> KamiSS1, SHKEquip, SIIKRS, OrbathAmulet
SIIKRS --> ScarInn
SIB --> MQu2, SQ3, SQ4, ScarInn
Finn --> ScarInn, FinnSS1
FinnSS1 --> FinnSS2 --> FinnSS3 --> FinnSS4 --> FinnSS5 --> ScarHub
SISt --> ScarInn, HorseSS1
HorseSS1 --> HorseSS2 --> HorseSS3 --> ScarInn

ScarBarracks --> SBaF, SBaB, ScarHub
SBaF --> Frc1-4, ScarBarracks, SBaF2, PrenSS
SBaF2 --> SBaF3 --> SBaF3c1, SBaF3c2, SBaF3c3
PrenSS --> PrenSS2 --> PrenSS3 --> PrenSS4 --> ScarBarracks
SBaB --> SBaBSS, ScarBarracks

ScarOther --> FBM1, ScarHub
FBM1 --> FBM2 --> FMBc1, FMBc2
FMBc1 --> FMBc12 --> ScarHub
FMBc2 --> FMBc22 --> ScarHub

MQu2 --> MQu21 --> MQu2Gear, MQu22
MQu2Gear --> MQu22, SIB
MQu22 --> Gnoll
Gnoll --> Fight, FleePass, FleeFail
Fight --> FightScreen
FightScreen --> VictoryScreen, GameOverScreen, FleePass, FleeFail
VictoryScreen --> GnollWin, CBugsWin, PigorcFWin, MQu2Finish2
GameOverScreen --> GnollLose, CBugsLose, PigorcFLose, MQu2Finish2
GnollWin --> GnollWin2 --> GnollWin3 --> GnollWin4 --> MountainPassage
GnollWin --> MountainPassage
GnollLose --> GnollLose2 --> GnollLose3 --> ScarHub
FleePass --> ScarHub (or Plateau for pigorc)
FleeFailGnoll --> MountainPassage
MountainPassage --> MountainPassage2, CliffFace
MountainPassage2 --> CliffFace
CliffFace --> CFBDirkWin, CFBDirkLose, Fight(insects)
CFBDirkWin --> Akos
CFBDirkLose --> Akos
CBugsWin --> Akos
CBugsLose --> Akos
Akos --> Akos2
Akos2 --> AkosPaw1, AkosSex1, AkosReject
AkosPaw1 --> AkosPaw2 --> AkosPaw3 --> AkosFinish
AkosSex1 --> AkosSex2 --> AkosSex3 --> AkosFinish
AkosReject --> AkosFinish
AkosFinish --> Pigorc
Pigorc --> Fight, FleePass, FleeFail
PigorcFWin --> Plateau
PigorcFLose --> PigorcFLose2 --> PigorcFLose3 --> PigorcFLose4 --> ScarHub
FleePassPigorc --> Plateau
FleeFailPigorc --> FleeFailPigorc2 --> FleeFailPigorc3 --> ScarHub
Plateau --> Plateau2 --> MQu2Finish
MQu2Finish --> MQu2Finish2 --> IoDIntro

IoDIntro --> IoDIntro2 --> IoDIntro3 --> IoDIntro4 --> IoDIntro5
IoDIntro5 --> IoDIntro5c1-4
IoDIntro5c1-4 --> IoDIntro6 --> IoDIntro7 --> IoDIntro8 --> IoDHub

IoDHub --> ErelHub, CouncilChamber, IODArena, IODShop, IODInn, IoDHouses
ErelHub --> ErelC --> Erelc1-4 --> IoDHub
CouncilChamber --> IoDRoom, TeleporterC, Zexir1D, Zexir1N
IoDRoom --> IoDKEquip, KamiSS1, IoDStaySleep, IoDAmulet
IoDStaySleep --> IoDRoom (next day)
IoDAmulet --> Hub, ScarHub
OrbathAmulet --> IoDHub
TeleporterC --> Hub, ScarHub (50g)
Zexir1D --> Zexir1DWorld, Zexir1DMagic, Zexir1DIsle, Zexir1DFight, IoDHub
Zexir1DWorld --> Zexir1DWorld2 --> Zexir1DWorld3 --> Zexir1DWorld4
Zexir1DMagic --> Zexir1DMagic2 (learn Light) --> Zexir1DMagic3 --> Zexir1DMagic4 (learn Fireball)
Zexir1DIsle --> Zexir1DIsle2
Zexir1DFight --> (advises see Raln)
Zexir1N --> ZexirAltSS1 (50%), Zexir1N (50%)
ZexirAltSS1 --> ZexirAltSS2 --> CouncilChamber
Zexir1N --> Zexir1N2, Zexir1N1
Zexir1N2 --> ZexirSS1, Zexir1N21
ZexirSS1 --> ZexirSS2 --> ZexirSS3 --> ZexirSS4 --> CouncilChamber
Zexir1N1 --> CouncilChamber
Zexir1N21 --> CouncilChamber

IODArena --> IODArenaD2 --> IoDHub
IODShop --> IoDMStall, IoDVStall, IoDBStall, IoDHub
IODInn --> IoDHub
IoDHouses --> Cave203, IoDCaves, IoDHub, Hran
Cave203 --> Cave2032, Cave2033, Hran2SS1, IoDHouses
Hran2SS1 --> Hran2SSc1, Hran2SSc2
Hran2SSc1 --> Hran2SSc12-15
Hran2SSc2 --> Hran2SSc2c1, Hran2SSc2c2
IoDCaves --> Cave102, Cave124, IoDHouses
Cave124 --> Cave124Pass, Cave124Fail
Hran --> Hran1 --> Hran2 --> Hran3 --> HranSS1, Hran4
HranSS1 --> HranSS2 --> HranSS3 --> IoDHub
Hran4 --> IoDHub
```
