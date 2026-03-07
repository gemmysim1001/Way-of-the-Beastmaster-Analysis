# Way of the Beastmaster - Complete MCTS Game Tree

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
-->        = Leads to
|          = Branch option
W/L/D      = Win / Lose / Draw (MCTS outcome style)
```

---

## CHARACTERS ENCOUNTERED

| Character | Species | Location | Role | Interactions |
|-----------|---------|----------|------|-------------|
| **Kami** | Wolf | Companion (everywhere) | Guide/familiar | Dialogue, SS (Inn room) |
| **Killian** | Unknown | Forest (Intro) | Bandit leader | Dialogue only |
| **Dinus** | Bear | Holstein Inn | Innkeeper | Dialogue, SS |
| **Wyatt** | Unknown (muscular) | Holstein Fountain | Mercenary/friend | Dialogue, SS (night alley) |
| **Misfit** | Ratman | Holstein Alley (day) | Shady figure | Dialogue, SS |
| **Night Rat** | Rat | Holstein Fountain (night) | Stranger | Dialogue, SS (coerced) |
| **Night Figure** | Unknown | Holstein Alley (night) | Dangerous stranger | Encounter |
| **Hans** | Corgi | Scarhaven Blacksmith | Blacksmith | Dialogue, SS (day & night) |
| **Frederick** | Feline | Scarhaven Barracks | Guard Captain | Dialogue, trust check |
| **Pren** | Imp | Scarhaven Barracks | Frederick's assistant | Dialogue, SS |
| **Finn** | Unknown (boy) | Scarhaven Inn | Traveler | Dialogue, gives feather |
| **Wes** | Unknown (tall) | Scarhaven Inn | Innkeeper | Room rental |
| **Horse** | Horse | Scarhaven Stables | Feral animal | Beast taming, SS |
| **Dragon + 3 Whelps** | Dragon | Streamdale Mountain | Quest boss | Negotiation, SS |
| **FBM Boy** | Unknown | Scarhaven Outskirts | Unnamed boy | SS |

---

## MONTE CARLO TREE SEARCH - FULL EXPANSION

```
[ROOT] Title
  |
  +--> [LINEAR] Intro1 - "It's cold..." (wake up with amnesia)
         |
         +--> [BRANCH] Species - "You stare at your reflection..."
                |
                |-- CC (Canine) ---------> Age
                |-- CF (Feline) ---------> Age
                |-- CV (Vulpine/Fox) ----> Age
                |-- CA (Avian) ----------> Age
                |-- CR (Reptile) --------> Age
                |-- CD (Dragon) ---------> Age
                |
                +--> [LINEAR] Age - "How old are you?"
                       |
                       +--> [LINEAR] Body - "Body frame selection"
                              |
                              +--> [LINEAR] Height - "Height selection"
                                     |
                                     +--> [BRANCH] Hair
                                            |-- (has hair) --> HairC --> Eye
                                            |-- (bald/feathered) -------> Eye
                                            |
                                            +--> [LINEAR] Eye - "Eye color"
                                                   |
                                                   +--> [LINEAR] Cock - "Genitalia"
                                                          |
                                                          +--> [LINEAR] DickL - "Size"
                                                                 |
                                                                 +--> [LINEAR] CharacterFinish
                                                                        |
                                                                        V
```

---

## ACT 1: THE INTRO SEQUENCE (Linear)

```
CharacterFinish
  |
  +--> [LINEAR] Intro2 - Forest, cold, need shelter
         |
         +--> [BRANCH] Intro3 - Meet Kami (talking Wolf)
                |
                |-- Intro3c1: "What is a Magister?" ----+
                |-- Intro3c2: "Why can you talk?" ------+-- (explore all, then...)
                |-- Intro3c3: "Where are we?" ----------+
                |                                       |
                +--> Intro3c4: "Let's get moving" <-----+
                       |
                       +--> [LINEAR] Intro4 - Walking for hours
                              |
                              +--> [LINEAR] Intro5 - Meet Killian & bandits
                                     |
                                     +--> [BRANCH] Intro6 - Killian gives you clothes
                                            |
                                            |-- [OPTIONAL] Kami1: Talk to Kami
                                            |     |
                                            |     +-- Kami1c1: "What about Killian?"
                                            |     +-- Kami1c2: "Can you really talk?"
                                            |     +-- Kami1c3: "Tell me about my powers"
                                            |     +-- Intro7: "Time to sleep"
                                            |
                                            +--> [LINEAR] Intro7 - Sleep under stars
                                                   |
                                                   +--> [LINEAR] Intro8 - Travel to Holstein
                                                          |
                                                          +--> [LINEAR] Intro9 - Arrive
                                                                 |
                                                                 +--> [LINEAR] Intro10 - Killian says goodbye
                                                                        |
                                                                        +--> TheBeginning --> HUB
```

---

## ACT 2: THE HUB (Holstein - Open World)

```
[ROOT] Hub (Holstein Capital) - CENTRAL NODE
  |
  |   [PERSISTENT FOOTER on every Hub page:]
  |   +--> Character (view stats)
  |   +--> inventory (view items)
  |   +--> KamiMenu (talk to Kami)
  |
  +========================================+
  |                                        |
  |  SEVEN BRANCHES FROM HUB:             |
  |                                        |
  |  1. HubInn -----> The Inn             |
  |  2. HubFount ---> The Fountain/Square |
  |  3. HubMarket --> The Market          |
  |  4. HubSpire ---> The Silver Spire   |
  |  5. Alley1D ----> Alley (Daytime)    |
  |  6. Alley1N ----> Alley (Nighttime)  |
  |  7. Carriages --> Travel to other     |
  |                   locations           |
  +========================================+
```

---

### BRANCH 1: THE INN (HubInn)

```
HubInn
  |
  +-- [BRANCH] InnStay - Talk to Innkeeper (Dinus the Bear)
  |     |
  |     +-- InnStayPay: "Rent a room"
  |     |     |
  |     |     +-- (no gold) --> back to HubInn
  |     |     +-- (has gold) --> InnStayRoom
  |     |           |
  |     |           +-- [BRANCH] Room options:
  |     |                 |
  |     |                 +-- KamiSS1 [SS]: Sex with Kami
  |     |                 |     |
  |     |                 |     +-- KamiSS1c1: "Top Kami"
  |     |                 |     |     +--> KamiSS1c12 (scene)
  |     |                 |     |           +--> InnStaySleep OR SIIKRS
  |     |                 |     |
  |     |                 |     +-- KamiSS1c2: "Bottom for Kami"
  |     |                 |           +--> KamiSS1c22 (scene)
  |     |                 |                 +--> InnStaySleep OR SIIKRS
  |     |                 |
  |     |                 +-- HolsteinKEquip: Equip Kami's gear
  |     |                 |     |
  |     |                 |     +-- KEquipHelm --> Battle Helm [ITEM]
  |     |                 |     +-- KEquipCollar --> Spiked Collar [ITEM]
  |     |                 |     +-- KEquipPaws --> Claw Guards [ITEM]
  |     |                 |     +-- KEquipBack --> Small Pack Saddle [ITEM]
  |     |                 |     +--> back to InnStayRoom
  |     |                 |
  |     |                 +-- InnStaySleep: "Go to sleep"
  |     |                       +--> HubInn (next day)
  |     |
  |     +-- [CHAR] DinusI: "Tell me about yourself, Dinus"
  |     |     +--> DinusI2 (backstory about assault victim)
  |     |           +--> HubInn
  |     |
  |     +-- [SS] DinusSS1: "Hang out with Dinus"
  |           +--> DinusSS2: Touch him
  |                 |
  |                 +-- (decline) --> HubInn
  |                 +-- DinusSS3: Go further
  |                       +--> DinusSS4: Rimming scene
  |                             +--> DinusSS5: Aftermath
  |                                   +--> HubInn
  |
  +-- [QUEST] InnQuests - The Bounty Board
  |     |
  |     +-- MQ1: Main Quest - "Royal Decree" ---------> [SEE MAIN QUEST TREE]
  |     +-- SQ1: Side Quest 1 - "Dragon Problem" -----> [SEE SIDE QUEST 1 TREE]
  |     +-- SQ2: Side Quest 2 - "Fancy Parchment" ----> [SEE SIDE QUEST 2 TREE]
  |     +-- (back) --> HubInn
  |
  +--> Hub (return to square)
```

---

### BRANCH 2: THE FOUNTAIN (HubFount)

```
HubFount (The Fountain Square)
  |
  +-- [DAYTIME BRANCHES:]
  |     |
  |     +-- FountD1: "Look for allies"
  |     |     |
  |     |     +-- [CHAR] Wyatt1: Meet Wyatt (first time)
  |     |     |     +--> Hub (he introduces himself)
  |     |     +-- (nobody found) --> HubFount
  |     |
  |     +-- FountD2: "Sit and relax"
  |     |     +--> HubFount
  |     |
  |     +-- [CHAR] Wyatt2: "Talk to Wyatt" (after meeting him)
  |           |
  |           +-- Wyatt2c1: "What's the Silver Spire?"
  |           +-- Wyatt2c2: "Where are you from?"
  |           +-- Wyatt2c3: "How do I make money?"
  |           +-- Wyatt2c4: "Places to avoid?"
  |           +--> HubFount (all are info-only, loop back)
  |
  +-- [NIGHTTIME BRANCH:]
  |     |
  |     +-- FountN1: "Approach the stranger" (night)
  |           |
  |           +-- FountN11: [SS] Agree to Rat's demands
  |           |     +--> HubFount
  |           +-- (refuse) --> Hub
  |
  +--> Hub (return)
```

---

### BRANCH 3: THE MARKET (HubMarket)

```
HubMarket
  |
  +-- MarkMagic: "Magic Items Stall"
  |     |
  |     +-- MarkMagicF1: Show the Magic Flower
  |     |     +--> HubMarket (info about the flower)
  |     +--> HubMarket
  |
  |     [ITEMS AVAILABLE:]
  |     Silver Orb [ITEM] - "Glows dimly, unknown purpose"
  |     Dog Collar [ITEM] - "Black collar, magical, Kami refuses it"
  |     Ruby Necklace [ITEM] - "Gold-plated, cabochon ruby"
  |
  +-- MarkHerb: "Herb & Potion Stall"
  |     |
  |     +--> HubMarket
  |
  |     [ITEMS AVAILABLE:]
  |     Pain Leaves [ITEM] - "Dulls pain"
  |     Health Potion [ITEM] - "Heals wounds"
  |     Endowment Potion [ITEM] - "Sexual enhancement"
  |       +--> EPFuck: Drink the potion
  |             +--> EPFuck2: Pass out, wake up changed
  |                   +--> Hub
  |
  +-- MarkPed: "Peddler in the back"
  |     |
  |     +-- MarkPed2: "What's this weapon?"
  |           |
  |           +-- MarkPed22: Buy the Magister's Dirk [ITEM]
  |           |     +--> Hub (Kami is excited)
  |           |
  |           +-- MarkPed23: Decline purchase
  |                 +--> HubMarket (Kami whines)
  |
  +--> Hub (return)
```

---

### BRANCH 4: THE SILVER SPIRE (HubSpire)

```
HubSpire
  |
  +--> Hub (currently locked / just description)
  |    "Despite Wyatt's warnings..." - placeholder for future content
```

---

### BRANCH 5: ALLEY - DAYTIME (Alley1D)

```
Alley1D (Daytime Alley)
  |
  +-- [CHAR] MisfitI: Talk to Misfit (Ratman)
  |     |
  |     +-- MisfitSS1 [SS]: Accept Misfit's advances
  |     |     +--> Hub
  |     +--> Hub
  |
  +-- [SS] MisfitSS1: Direct sexual encounter
  |     +--> Hub
  |
  +--> Hub (return safely)
```

---

### BRANCH 6: ALLEY - NIGHTTIME (Alley1N)

```
Alley1N (Nighttime Alley - dangerous)
  |
  +-- Alley1N1: "Peek in the illuminated window"
  |     |
  |     +-- [CHAR] WyattSS1: Find Wyatt inside
  |     |     +--> WyattSS2: He offers you food
  |     |           |
  |     |           +-- (eat and leave) --> Hub
  |     |           +-- WyattSS3 [SS]: Offer sexual favors
  |     |                 |
  |     |                 +-- (stop here) --> Hub
  |     |                 +-- WyattSS4: Go further
  |     |                       |
  |     |                       +-- WyattSS5: Handjob scene
  |     |                       |     +--> WyattSSE --> Hub
  |     |                       +-- WyattSSE: Aftermath/cuddle
  |     |                             +--> Hub
  |     |
  |     +--> Alley1N (go back)
  |
  +-- Alley1N2: "Approach the figure at the end"
  |     +--> Alley1N21: Dangerous encounter, Kami protects you
  |           +--> Hub (escape)
  |
  +--> Hub (return)
```

---

### BRANCH 7: CARRIAGES (Travel System)

```
Carriages
  |
  +-- HolC: "Go to Holstein (capital)"
  |     +--> Hub
  |
  +-- ScarC: "Go to Scarhaven"
        +--> ScarHub [SEE SCARHAVEN TREE]
```

---

## MAIN QUEST: THE FOREST OF MADNESS (MQ)

```
MQ1: Accept the Royal Decree
  |
  +--> MQ2: Decide to travel to Scarhaven
        |
        +--> MQ3: Take carriage to Scarhaven
              |
              +--> MQ4: Arrive at Scarhaven, enter camp
                    |
                    +--> MQ5: Enter the command tent (soldiers draw weapons)
                          |
                          +--> MQ52: Briefing - "Hunt animals in the forest"
                                |
                                +--> [THE MAZE - 4x4 GRID FOREST]

================================
  THE MAZE (Navigable Forest)
================================

Grid Layout (approximate):
  Maze1  -- Maze2  -- Maze3  -- Maze4
    |        |         |         |
  Maze5  -- Maze6  -- Maze7  -- Maze8
    |        |         |         |
  Maze9  -- Maze10 -- Maze11 -- Maze12
    |        |         |         |
  Maze13 -- Maze14 -- Maze15 -- Maze16

Entry: Maze9 (entrance)

Navigation connections:
  Maze1  <-> Maze2, Maze5
  Maze2  <-> Maze1, Maze3, Maze6
  Maze3  <-> Maze2, Maze4, Maze7
  Maze4  <-> Maze3, Maze8
  Maze5  <-> Maze1, Maze6, Maze9
  Maze6  <-> Maze2, Maze5, Maze7, Maze10
  Maze7  <-> Maze3, Maze6, Maze8, Maze11 (+ self-loop)
  Maze8  <-> Maze4, Maze7, Maze12
  Maze9  <-> Maze5, Maze10, Maze13  [ENTRANCE]
  Maze10 <-> Maze6, Maze9, Maze11, Maze14
  Maze11 <-> Maze7, Maze10, Maze12, Maze15  [GOAL: MQ6 exit here]
  Maze12 <-> Maze8, Maze11, Maze16
  Maze13 <-> Maze9, Maze14
  Maze14 <-> Maze10, Maze13, Maze15
  Maze15 <-> Maze11, Maze14, Maze16
  Maze16 <-> Maze12, Maze15

Items in Maze:
  Strange Mushroom [ITEM] - found in maze
  Speedband [ITEM] - Wyatt's headband

GOAL --> Maze11 --> MQ6: "Approach the powerful figure"
  |
  +--> MQ7: Run from the roar
        |
        +--> MQ8: Tap into Beastmaster powers
              |
              +--> MQ9: Command wolves to stand down
                    |
                    +--> MQ10: Wolves obey, you collapse
                          |
                          +--> MQ11: Wake up in tent
                                |
                                +--> MQ12: Carriage ride back
                                      +--> Hub (QUEST COMPLETE)
```

---

## SIDE QUEST 1: THE DRAGON OF STREAMDALE (SQ1)

```
SQ1: Accept "Dragon Problem" quest
  |
  +--> SQ11: Bound for Streamdale
        |
        +--> SQ12: Take carriage
              |
              +--> SQ13: Arrive - see dragon damage
                    |
                    +--> SQ14: Carriage up the mountain
                          |
                          +--> SQ15: Enter cave, mercenary goes first (dies)
                                |
                                +--> SQ16: Dragon recognizes you as Beastmaster
                                      |
                                      +--> SQ17: Discover 1 adult + 3 whelps
                                            |
                                            +-- [BRANCH] Two approaches:
                                            |
                                            +-- SQ1SS1 [SS]: Offer sexual favor
                                            |     |
                                            |     +--> SQ1SS2: Whelps join in
                                            |           |
                                            |           +--> SQ1SS3: Escalation
                                            |                 |
                                            |                 +--> SQ1SS4: Climax
                                            |                       |
                                            |                       +--> SQ1SSE: Aftermath
                                            |                             +--> SQ19 --> SQ1E
                                            |
                                            +-- SQ18: Negotiate diplomatically
                                                  |
                                                  +--> SQ19: Leave cave with Scale
                                                        |
                                                        +--> SQ1E: Return to mayor
                                                              +--> Hub (QUEST COMPLETE, reward)
```

---

## SIDE QUEST 2: THE WRENVILLE JOB (SQ2)

```
SQ2: Accept "Fancy Parchment" quest
  |
  +--> SQ21: Ask innkeeper about Wrenville
        |
        +--> SQ22: Take carriage to Wrenville
              |
              +--> SQ23: Mercenary tells you to stand back
                    |
                    +--> SQ24: Kami explains the danger
                          |
                          +--> SQ25: Convince mercenaries to let you stay
                                |
                                +--> SQ2E: Sneak around mercenaries
                                      +--> Hub (QUEST COMPLETE)
```

---

## SCARHAVEN HUB (Second Town)

```
[ROOT] ScarHub (Scarhaven Town)
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

### SCARHAVEN BRANCH 1: BLACKSMITH (ScarBS)

```
ScarBS (Hans the Corgi's Blacksmith)
  |
  +-- SBSK: "Browse Kami's gear"
  |     +--> ScarHub (shop items for Kami)
  |
  +-- SBSC: "Browse your gear"
  |     +--> ScarHub ("nothing in your size")
  |
  +-- [CHAR] SBSH: "Talk to Hans" (daytime)
  |     |
  |     +-- SBSHc1: "Tell me about your job"
  |     +-- SBSHc2: "Tell me about your personal life"
  |     +-- SBSHc3: "Tell me about your sex life"
  |     |     |
  |     |     +-- [SS] SBSHSS: Accept Hans' advances
  |     |           |
  |     |           +--> SBSHSS2: Make a move
  |     |                 |
  |     |                 +-- [BRANCH by player size:]
  |     |                 |
  |     |                 +-- SBSHSS2s (small frame):
  |     |                 |     +--> SBSHSS2s2 --> SBSHSS2s3 --> ScarHub
  |     |                 |
  |     |                 +-- SBSHSS2m (medium frame):
  |     |                 |     +--> SBSHSS2m2 --> SBSHSSm3 --> ScarHub
  |     |                 |
  |     |                 +-- SBSHSS2l (large frame):
  |     |                       +--> SBSHSS2l2 --> SBSHSS2l3 --> ScarHub
  |     |
  |     +-- SBSHc4: "Tell me about the war"
  |     +-- SBSHf: "Tell me about Frederick"
  |     +--> ScarHub
  |
  +-- [CHAR] SBSHn: "Visit Hans at night" (knock on door)
  |     |
  |     +-- SBSHn2: "Stay the night" (cuddle)
  |     |     +--> SBSHn3: Wake up together
  |     |           +--> ScarHub
  |     +-- (leave) --> ScarHub
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 2: INN (ScarInn)

```
ScarInn (Scarhaven Inn)
  |
  +-- [CHAR] SIIK: Talk to Wes (Innkeeper)
  |     |
  |     +-- SIIK2: "Rent a room"
  |     |     |
  |     |     +-- (no gold) --> ScarInn
  |     |     +-- (has gold) --> SIIKR (your room)
  |     |           |
  |     |           +-- KamiSS1 [SS]: Sex with Kami
  |     |           |     (same tree as Holstein room)
  |     |           |     +-- KamiSS1c1 (top) --> KamiSS1c12
  |     |           |     +-- KamiSS1c2 (bottom) --> KamiSS1c22
  |     |           |
  |     |           +-- SHKEquip: Equip Kami's gear
  |     |           |     +-- KEquipHelm / KEquipCollar / KEquipPaws / KEquipBack
  |     |           |     +--> SIIKR
  |     |           |
  |     |           +-- SIIKRS: "Go to sleep"
  |     |                 +--> ScarInn
  |     |
  |     +--> ScarInn
  |
  +-- SIB: "Bounty Board"
  |     +--> ScarInn (text is magically unreadable)
  |
  +-- [CHAR] Finn: Talk to Finn
  |     +--> ScarInn (gives Birdpup Feather [ITEM])
  |
  +-- SISt: "Visit the Stables"
  |     |
  |     +-- [SS] HorseSS1: Attempt to tame the Horse
  |     |     |
  |     |     +-- HorseSS2: Pleasure the horse
  |     |     |     +--> HorseSS3: Completion
  |     |     |           +--> ScarInn
  |     |     +-- (fail/leave) --> ScarInn
  |     |
  |     +--> ScarInn
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 3: BARRACKS (ScarBarracks)

```
ScarBarracks
  |
  +-- [CHAR] SBaF: "Visit Frederick's Office"
  |     |
  |     +-- [First visit:] SBaF2 --> SBaF3: Explain your powers
  |     |     |
  |     |     +-- [BRANCH - TRUST CHECK:]
  |     |     |
  |     |     +-- SBaF3c1: Frederick believes you (SUCCESS)
  |     |     |     +--> ScarBarracks (friendship gained)
  |     |     |
  |     |     +-- SBaF3c2: Pren exposes your lie (PARTIAL FAIL)
  |     |     |     +--> ScarBarracks (Frederick frowns)
  |     |     |
  |     |     +-- SBaF3c3: Pren calls you out (FAIL)
  |     |           +--> ScarBarracks (trust lost)
  |     |
  |     +-- [Return visits:] Talk to Frederick
  |     |     +-- Frc1: "Tell me about Scarhaven"
  |     |     +-- Frc2: "Tell me about yourself"
  |     |     +-- Frc3: "Tell me about Pren" (sword drawn!)
  |     |     +-- Frc4: "Any leads on the forest stranger?"
  |     |     +--> ScarBarracks
  |     |
  |     +-- [SS] PrenSS: "Accept Pren's offer" (if available)
  |           |
  |           +--> PrenSS2: Oral scene
  |                 |
  |                 +--> PrenSS3: Penetration
  |                       |
  |                       +--> PrenSS4: Climax
  |                             +--> ScarBarracks
  |
  +-- SBaB: "Go to the Bathroom"
  |     |
  |     +-- [SS] SBaBSS: Encounter with Reptile
  |     |     +--> ScarBarracks
  |     +-- (just leave) --> ScarBarracks
  |
  +--> ScarHub
```

---

### SCARHAVEN BRANCH 4: OUTSKIRTS (ScarOther)

```
ScarOther (Explore the outskirts)
  |
  +-- [SS] FBM1: "Approach the boy"
  |     |
  |     +--> FBM2: Escalation
  |           |
  |           +-- FMBc1: "Take him yourself"
  |           |     +--> FMBc12: Scene
  |           |           +--> ScarHub
  |           |
  |           +-- FMBc2: "Involve Kami"
  |                 +--> FMBc22: Scene
  |                       +--> ScarHub
  |
  +--> ScarHub
```

---

## INVENTORY ITEMS (Complete List)

```
ITEMS
  |
  +-- Coin Pouch        - Currency container
  +-- Magic Flower      - Rare alchemy reagent (given by girl in intro)
  +-- Silver Orb        - Unknown purpose, glows dimly (Market)
  +-- Dog Collar        - Magical collar, Kami refuses (Market)
  +-- Ruby Necklace     - Gold-plated jewelry (Market)
  +-- Pain Leaves       - Dulls pain when chewed (Market)
  +-- Health Potion     - Heals wounds (Market)
  +-- Endowment Potion  - Sexual enhancement, causes blackout (Market)
  +-- Magister's Dirk   - Royal Magister blade (Peddler)
  +-- Strange Mushroom  - Magical mushroom (Forest Maze)
  +-- Speedband         - Wyatt's headband, increases speed
  +-- Birdpup Feather   - White feather, black tip (Finn, Scarhaven)

KAMI EQUIPMENT
  +-- Battle Helm       - Steel wolf helm (head slot)
  +-- Spiked Collar     - Leather + spikes (neck slot)
  +-- Claw Guards       - Iron claw covers (paw slot)
  +-- Small Pack Saddle - Carrying saddle (back slot)
```

---

## MCTS DECISION TREE SUMMARY (Probability-Weighted Paths)

```
TOTAL NODES: 232 passages
TOTAL CHARACTERS: 15 interactable
TOTAL ITEMS: 16
TOTAL QUESTS: 3 (1 main + 2 side)
TOTAL LOCATIONS: 2 towns + 1 maze + forest intro

CRITICAL PATH (shortest to "endgame"):
  Title -> Intro1 -> Species -> [6 creation steps] -> Intro2-10
  -> TheBeginning -> Hub -> [open world]

DECISION DEPTH BY BRANCH:
========================================================
  Character Creation:     6 species x appearance combos
  Intro Dialogue:         3 optional topics (Kami1, Intro3)
  Holstein Inn:           3 paths (room/talk/SS) depth 2-5
  Holstein Fountain:      5 paths (day/night) depth 1-4
  Holstein Market:        3 stalls, depth 2-3
  Holstein Alley Day:     2 paths (talk/SS) depth 1-2
  Holstein Alley Night:   2 paths (window/figure) depth 2-5
  Main Quest (Forest):    16-node maze + 7-node boss sequence
  Side Quest 1 (Dragon):  9 nodes, branch at SQ17 (sex/diplomacy)
  Side Quest 2 (Wrenville): 5 nodes, linear
  Scarhaven Blacksmith:   3 shop + 4 dialogue + 3 SS variants
  Scarhaven Inn:          4 paths (room/board/finn/stables)
  Scarhaven Barracks:     3 paths (Frederick/Pren/bathroom)
  Scarhaven Outskirts:    1 path, branch into 2 SS variants
========================================================

MCTS EXPANSION FACTOR PER NODE:
  Hub (Holstein):    7 children  <-- highest branching
  ScarHub:           5 children
  InnQuests:         4 children (3 quests + back)
  Species:           6 children (race selection)
  Wyatt2:            5 children (dialogue options)
  SBaF:              7 children (Frederick's office)
  Maze nodes:        2-5 children each (navigation)

LEAF NODES (terminals that return to hubs): ~45
DEAD END / DYNAMIC NODES (item descriptions): ~15
LINEAR CHAINS (no player choice): ~60%
BRANCHING NODES (real decisions): ~40%

ROLLOUT OUTCOMES:
  - Every path eventually loops back to Hub or ScarHub
  - No permanent death / game over states exist
  - No true ending implemented (open-ended sandbox)
  - Quest completion flags unlock new dialogue options
  - Time-of-day (day/night) gates certain content
  - Gold gates room rentals
  - Trust mechanics gate Frederick's friendship (SBaF3)
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
Kami1c1 --> Kami1c2, Kami1c3, Intro7
Kami1c2 --> Kami1c1, Kami1c3, Intro7
Kami1c3 --> Kami1c1, Kami1c2, Intro7
Intro7 --> Intro8 --> Intro9 --> Intro10 --> TheBeginning --> Hub
Hub --> HubInn, HubFount, HubMarket, HubSpire, Alley1D, Alley1N, Carriages
HubInn --> InnStay, InnQuests, Hub
InnStay --> InnStayPay, DinusI, DinusSS1
InnStayPay --> HubInn, InnStayRoom
InnStayRoom --> KamiSS1, HolsteinKEquip, InnStaySleep
KamiSS1 --> KamiSS1c1, KamiSS1c2
KamiSS1c1 --> KamiSS1c12 --> InnStaySleep, SIIKRS
KamiSS1c2 --> KamiSS1c22 --> InnStaySleep, SIIKRS
InnStaySleep --> HubInn
DinusI --> DinusI2 --> HubInn
DinusSS1 --> DinusSS2 --> HubInn, DinusSS3
DinusSS3 --> DinusSS4 --> DinusSS5 --> HubInn
InnQuests --> MQ1, SQ1, SQ2, HubInn
HubFount --> FountD1, FountD2, Hub, Wyatt2, FountN1
FountD1 --> Wyatt1, HubFount
Wyatt1 --> Hub
Wyatt2 --> Wyatt2c1, Wyatt2c2, Wyatt2c3, Wyatt2c4, HubFount
FountD2 --> HubFount
FountN1 --> FountN11, Hub
FountN11 --> HubFount
HubMarket --> MarkMagic, MarkHerb, MarkPed, Hub
MarkMagic --> MarkMagicF1, HubMarket
MarkMagicF1 --> HubMarket
MarkHerb --> HubMarket
MarkPed --> MarkPed2, HubMarket
MarkPed2 --> MarkPed22, MarkPed23
MarkPed22 --> Hub
MarkPed23 --> HubMarket
HubSpire --> Hub
Alley1D --> Hub, MisfitSS1, MisfitI
MisfitI --> MisfitSS1, Hub
MisfitSS1 --> Hub
Alley1N --> Alley1N2, Alley1N1, Hub
Alley1N1 --> WyattSS1, Alley1N
WyattSS1 --> WyattSS2 --> Hub, WyattSS3
WyattSS3 --> Hub, WyattSS4
WyattSS4 --> WyattSS5, WyattSSE
WyattSS5 --> WyattSSE --> Hub
Alley1N2 --> Alley1N21 --> Hub
Carriages --> HolC, ScarC
HolC --> Hub
ScarC --> ScarHub
MQ1 --> MQ2, InnQuests
MQ2 --> MQ3 --> MQ4 --> MQ5 --> MQ52 --> Maze9
[Maze grid: see above]
Maze11 --> MQ6 --> MQ7 --> MQ8 --> MQ9 --> MQ10 --> MQ11 --> MQ12 --> Hub
SQ1 --> SQ11, InnQuests
SQ11 --> SQ12 --> SQ13 --> SQ14 --> SQ15 --> SQ16 --> SQ17
SQ17 --> SQ1SS1, SQ18
SQ1SS1 --> SQ1SS2 --> SQ1SS3 --> SQ1SS4 --> SQ1SSE --> SQ19
SQ18 --> SQ19 --> SQ1E --> Hub
SQ2 --> SQ21, InnQuests
SQ21 --> SQ22 --> SQ23 --> SQ24 --> SQ25 --> SQ2E --> Hub
ScarHub --> ScarBS, ScarInn, ScarBarracks, ScarOther, Carriages
ScarBS --> SBSK, SBSC, SBSH, ScarHub, SBSHn
SBSH --> SBSHc1, SBSHc2, SBSHc3, SBSHc4, ScarHub
SBSHc3 --> SBSHSS --> SBSHSS2
SBSHSS2 --> SBSHSS2s, SBSHSS2m, SBSHSS2l
SBSHSS2s --> SBSHSS2s2 --> SBSHSS2s3 --> ScarHub
SBSHSS2m --> SBSHSS2m2 --> SBSHSSm3 --> ScarHub
SBSHSS2l --> SBSHSS2l2 --> SBSHSS2l3 --> ScarHub
SBSHn --> SBSHn2 --> SBSHn3 --> ScarHub
ScarInn --> SIIK, SIB, SISt, Finn, ScarHub
SIIK --> SIIK2 --> ScarInn, SIIKR
SIIKR --> KamiSS1, SHKEquip, SIIKRS
SIIKRS --> ScarInn
SISt --> ScarInn, HorseSS1
HorseSS1 --> HorseSS2, ScarInn
HorseSS2 --> HorseSS3 --> ScarInn
ScarBarracks --> SBaF, SBaB, ScarHub
SBaF --> Frc1-4, ScarBarracks, SBaF2, PrenSS
SBaF2 --> SBaF3 --> SBaF3c1, SBaF3c2, SBaF3c3
PrenSS --> PrenSS2 --> PrenSS3 --> PrenSS4 --> ScarBarracks
SBaB --> SBaBSS, ScarBarracks
SBaBSS --> ScarBarracks
ScarOther --> FBM1, ScarHub
FBM1 --> FBM2 --> FMBc1, FMBc2
FMBc1 --> FMBc12 --> ScarHub
FMBc2 --> FMBc22 --> ScarHub
```
