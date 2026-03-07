# Way of the Beastmaster v0.41 — Creative Style Guide

_Reference document for writing expansion content faithful to the original._

---

## 1. NARRATION VOICE

### POV & Tense
- **Second person, present tense** is the baseline
- Past tense **drifts in naturally** for ongoing states and retrospective beats — this is a feature, not a bug
- The voice reads like a storyteller narrating to you, not a strict grammar exercise

```
PRESENT (immediate action):
"You and Kami stand in one of the busiest establishments you've ever seen."

PAST DRIFT (ongoing state):
"It's high time you finally got moving. The cold was beginning to set
in too much, and your teeth were starting to chatter."

MIXED (the game's natural rhythm):
"You're not quite sure what this 'journey' is that he's speaking of,
but you can vaguely understand why someone would give you a guide,
after chucking you in the middle of nowhere."
```

### Paragraph Length
- **2-5 sentences** typical, rarely exceeding 100 words per paragraph
- Location descriptions run longer (4-5 sentences)
- Dialogue-adjacent prose is shorter (1-3 sentences)
- Action sequences use shorter, punchier paragraphs

### Descriptive Density
- **Moderate** — more than bare gamebook prose, less than literary fiction
- **Functional description** with concrete measurements: heights in feet, distances in metres
- Physical descriptions are front-loaded on first encounter, never repeated
- Sensory focus: **visual > tactile > sound > smell** (smell only in SS or magic scenes)

```
TYPICAL LOCATION:
"The Marketplace appears to be one long lap, primarily. There is a
sizeable walkway that goes around in a complete square until you
eventually end up back where you came from. Stalls line the path
left and right, with an island of them in the middle."

TYPICAL CHARACTER INTRO:
"He was about 4 foot high and no taller, with small stubby legs
and arms, but an unnaturally long body. He looked canine in posture
and nature, with a mixture of white and cream fur."

HEIGHTENED (magic/emotional):
"Every sense is heightened. You can smell the air, smell the fear in
your companion's very body language. Each snarl and pant falls on
your ears as if they were right up against them. You can practically
taste the palpable tension in the air, as well as the nectar of
something sweet: magic."
```

### Character Introduction Pattern
Every new character follows: **species → build/size → distinguishing features → clothing → personality impression**

```
Dinus:  Bear → 8 foot, well-built → beautiful white coat → [clothing] → kind, fatherly
Hans:   Corgi → 4 foot, stubby → white/cream fur, auburn flecks → dirty apron → gruff, cocky
Soir:   Feline → black fur, grey streaks → striking white hair → linen shirt → trying to look professional
Erel:   Avian → red/white feathers → rounded beak like a parrot → [clothing] → gentle, professional
Raln:   Dragon → wingless, stocky → jagged horns → [no clothing] → rude, intimidating
```

---

## 2. TONE

### Three Registers
The game operates in three tonal modes and shifts between them fluidly:

**1. Casual/Humorous** (dominant — exploration, hub navigation, character banter)
```
"His voice was gruff, and his expression was cocky, but his height
made it hard to take him seriously."

"'The fuck do you think you're doing?' You're startled by a guard
glaring down at you, spear in hand."
```

**2. Dramatic/Earnest** (main quest events, emotional beats, Kami moments)
```
"You don't care that he's heavy, and you don't care that the weight
of him makes you fell over. You're filled with an overwhelming
happiness that knows no bounds."

"Your heart is pounding. An ear-splitting roar erupts through the
forest and you press your hands to your ears as you run."
```

**3. Explicit/Matter-of-fact** (SS content — presented without euphemism or shock value)
```
[SS content is written plainly, with anatomical directness.
Not clinical, not purple prose. Just... what happens.]
```

### Humor Style
- **Dry, situational comedy** — the narration acknowledges absurdity casually
- Never outright jokes or punchlines
- The player character's inner voice is mildly bewildered and self-deprecating
- "Somehow, you don't feel any better." (after learning about the Awakening)
- "Your inner self couldn't help but make some remark about a sword that polishes itself."

### Fourth Wall
- **Almost never broken.** The game stays in-world.
- **One exception:** Finn. He is the ONLY character who breaks the fourth wall.
  - "Enjoying yourself? I hope so! A lot of work was put into this."
  - "Stay tuned for more exciting things in the future."
- No other character or narration passage references the game as a game.

### Profanity
- **Allocated by character, not by the narrator.**
- The narration itself rarely swears.
- Guard NPCs, Pren, Misfit, and rough characters use "fuck," "shit," "cunts" freely.
- Kami NEVER swears. Frederick rarely. Zexir and Erel never.
- Profanity signals class/roughness, not narrative emphasis.

---

## 3. PUNCTUATION & PROSE TECHNIQUES

### Ellipses (signature technique)
The game's most distinctive punctuation habit. Used for:
- Trailing speech: "I just, uh...y'know."
- Narrative pauses: "He was...well, short."
- Hesitation: "Maybe he needs a break..."
- Unfinished thoughts: "I was only a young adult when I saw my family burned and torn to shreds."

### Italics (`//text//` in Harlowe)
Used for:
- Single-word emphasis: "it's so damn //loud//"
- Internal stress: "What is it you //want?//"
- Character speech emphasis: "'Sorry that your dog doesn't love my //dick//'"

### Exclamation marks
- **Rare in narration** — reserved for genuine surprise
- **Common in dialogue** — especially from energetic characters (Hans, Soir, Hran)
- "'Good afternoon!'" / "'Aww! Cute doggy.'" / "'Oh! You're that Magister!'"

### Internal Monologue
- **Blended seamlessly** into second-person narration — no italics, no special formatting
- The character's thoughts ARE the narration
- "You're not sure what this 'council chamber' was all about, but if you wanted answers, then you'd have to go there."
- "So many questions were swimming through your mind. You don't even know where to begin."

---

## 4. DIALOGUE

### Format
- **NPC dialogue:** Plain double quotes inline with narration. No special markup.
- **Kami dialogue:** Uses Harlowe hook syntax: `|Kami>["text"]` or `["text"]<Kami|` with outline enchantment
- **Player dialogue:** Almost never directly quoted (see below)

### Dialogue-to-Narration Ratio
- Passages are **60-80% narration** with dialogue woven in as brief punctuating lines
- Most passages have 1-3 lines of spoken dialogue
- Long dialogue stretches (Zexir lectures, Dinus backstory) are broken up with narration

### Dialogue Line Length
- **Short to medium** — usually 1-2 sentences
- Characters rarely speak more than 3 sentences in a single quoted block
- Attribution is informal and varied: before, after, or absent

### The Player's Voice
- **Near-silent protagonist.** The player almost never speaks in quotes.
- ~80% of "speech" is **narrated**: "You tell him that you met him after the animal attacks."
- ~15% is **link text** (dialogue as choice): `[["Who are you?"->passage]]`
- ~5% is **rare direct quotes** embedded in narration
- This creates a **blank slate** — personality defined by choices, not words

---

## 5. CHARACTER VOICE REFERENCE

### Formality Spectrum (most → least formal)

| Character | Address for Player | Contractions | Swears | Key Trait |
|-----------|-------------------|-------------|--------|-----------|
| **Kami** | "Master," "Sire" | Never | Never | Archaic servant. Full sentences. "I cannot," "I shall." |
| **Zexir** | "Child," "Magister" | Rarely | Never | Professorial. "Shant." Long flowing clauses. Ancient wisdom. |
| **Frederick** | "$name" | Sometimes | Never | Military precision. Calm, measured, diplomatic. |
| **Erel** | "$name" | Sometimes | Never | Shy, educated. Hedging: "I, well..." Uses "shall we?" |
| **Raln** | "Boy," "little one" | Often | Mild ("blasted") | Drill sergeant bark. Short commands. Insults with grudging respect. |
| **Killian** | "kid" | Often | Mild ("arseholes") | Gruff warmth. British spelling. Brief, practical. |
| **Dinus** | "kid," "$name" | Heavy | Mild ("damn") | Folksy paternal. "What can I do you for?" Self-censors for the child. |
| **Wyatt** | "kid," "Wolf kid," "babe" | Heavy | Never | Bro-ish. "Yo," "dude." Protective. Modern-sounding slang. |
| **Hans** | "kid," "babe," "hun" | Heavy | Once | Nervous trailing off. "S'just, y'know..." Uses "Daddy" not "father." |
| **Hran** | "$name" | Heavy | Never | Stutters: "N-Non," "O-Okay." "Kinda," "gotta." Self-deprecating. |
| **Wes** | "kid" | Heavy | Never | Terse. Minimal. Transactional. No small talk. |
| **Misfit** | "kid" | Heaviest | Heavy | Constant fillers: "uh," "y'know." Crude + vulnerable contrast. |
| **Pren** | "babe," "slut," "kid" | Heavy | Heaviest | Zero filter. Mockingly formal "sire." Degrading. |
| **Finn** | "$name" | Sometimes | Never | "Howdy." Fourth-wall breaking. Mysteriously cheerful. |

### Voice Samples

**Kami** — always deferential, never casual:
> "I can't pertain to know much about people, Master $name, but Bandits and Marauders have never been kind folk."

**Dinus** — folksy, self-censoring:
> "He was rambling about how he'd been sexually assaulted by someone. Some god. Oh, uh-- I mean, you know. The god had touched his no-no place."

**Wyatt** — modern, bro-ish, protective:
> "There are a few people around here who would more than happily ask you to do some unspeakable things for coin, kid. Make sure you tell them no."

**Misfit** — crude, hedging, vulnerable underneath:
> "It's fucking incredible how a couple of different reagents in the right order can make a potion that can grow back a fucking limb."

**Hans** — nervous, trailing off:
> "Well, s'just, y'know. I've had my fair share, but not...had my fair share?"

**Frederick** — measured, military:
> "Now's the time to tell the truth, $name. I understand you might have been scared for your wellbeing, but trust me, whatever secrets you hide are safe here."

**Zexir** — ancient, professorial:
> "I shant overload you with information, child, so I will go on to explain the world around you for now."

**Raln** — barking, abrupt:
> "So you're that blasted Magister that Zexir speaks so highly of? I didn't expect you to be just a child."

**Hran** — stuttering, adolescent:
> "Kinda freaky... But also kinda good, right? ...Oh, right, you Nomads aren't really into all that, uh...'interspecies' stuff."

**Pren** — maximum crude:
> "Sorry pumpkin, I'm busy having a wank. Maybe come back another time if you're after that pompous cat."

---

## 6. CHOICE ARCHITECTURE

### Choice Types (by frequency)
```
38% Navigation     — "Go to the Inn." / "Leave." / "Head back outside."
24% Dialogue       — "Ask about X" / quoted speech as links
 9% Character      — Species, body, age selections
 5% Lore inquiry   — Multi-topic menus (explore all before continuing)
 4% Sexual         — Position/partner choices, consent opt-in/out
 4% Action/Combat  — "Fight" / "Flee" / "Use the Dirk"
 3% Accept/Decline — Quest acceptance, NPC offers
 3% Purchase       — "Purchase X (Ng)" format
 2% Relationship   — "Confess feelings" / "Break Up"
 2% System         — Save/Load, equipment, return buttons
 6% Other          — Contextual
```

### Choice Formatting Rules
1. **Navigation** ends with a period: `[[Go to the Inn.->HubInn]]`
2. **Dialogue** uses quotes: `[["Who are you?"->passage]]`
3. **Actions** are imperative: `[[Ask Kami for sex.->KamiSS1]]`
4. **Purchases** show cost: `Purchase a Silver Orb. (20 gold)`
5. **Simple continue** uses exactly: `[[Continue.->passage]]`
6. **Leave/Return** standardized per hub: `[[Leave.->Hub]]`, `[[Leave.->ScarHub]]`, `[[Leave.->IoDHub]]`
7. **System menus** use dynamic return: `(link-goto: "Return", (history:)'s last)`

### The "Explore and Converge" Dialogue Pattern
Multi-topic dialogues show all options, hide visited ones, converge to the same exit:
```
Visit Wyatt → 4 topics (Spire, past, money, danger)
Each topic: show info → return to remaining topics + exit
All topics optional. Player reads what they want, then moves on.
```

### The "Progressive Unlock" Pattern
Repeated visits gate increasingly intimate content:
```
Visit 1:    Stranger introduction
Visit 2:    Learns your name
Visit 3-5:  Familiar greeting
Visit 6-10: New dialogue unlocked
Visit 11+:  SS content unlocked
```

### The "Branch by Flag" Pattern
Hub passages render entirely different content based on state:
```
(if:$WyattMet is false)[first meeting scene]
(elseif:$WyattMet is true)[return visit with dialogue options]
```

### False Choices
- The game **does not disguise false choices as real ones.**
- When there's only one path: `[[Continue.->passage]]` — no pretense.
- 129 passages use exactly the text "Continue." as a solo link.

---

## 7. GATING PATTERNS

### Gate Types (by frequency)
```
MOST COMMON:
  Boolean flags    — $WyattMet, $MisfitF, $HansF, $MQ1D
  Gold checks      — (if:$coin is >=N) / (elseif:$coin is <N)
  Time of day      — (if:$DN is "day") / (elseif:$DN is "night")
  Visit history    — (if:(history:) contains "PassageName")

MODERATE:
  Visit counters   — $innsc thresholds (0, 1, 2-5, 6-10, 11+)
  Inventory        — (if:$inv contains "Item Name")
  Relationship     — (if:$Relationship is "Hans")
  LoveMeter        — (if:$LoveMeter is >=250)

RARE:
  Spells           — (if:$Spells contains "Calm")
  Location         — (if:$location is "Holstein")
  Body frame       — $body gates Hans SS variants
```

### Purchase Pattern (exact template)
```harlowe
|Tag>[Purchase Item. (N gold)]
(link:"Purchase Item. (N gold)")[(if:$coin is <N)[(clickreplace:?Tag)[
  You cannot afford this. The stall owner grimaces at you.]]
(elseif:$coin is >=N)[(clickreplace:?Tag)[
  You purchased the Item! (set:$inv to $inv + (a:"Item"))
  (set:$coin to $coin - N)
  Description of the item.]]
```

### Locked Content Display
```harlowe
(if:$LoveMeter is >=250)[[[Ask to meet Misfit's family.->MisfitFam]]]
(elseif:$LoveMeter is <250)[|Locked>[You don't know Misfit well enough yet.]]
```
The `|Locked>` hook renders in red. Only used in relationship hubs.

---

## 8. STRUCTURAL PATTERNS

### Spoke-and-Hub Architecture
- Every sub-location, NPC, quest return, and scene conclusion routes back to a hub
- Sub-locations are rarely more than 2-3 passages deep before returning
- The three hubs (Hub, ScarHub, IoDHub) are gravitational centers

### Exit Text Standards
```
Sub-location → hub:       [[Leave.->Hub]]
                           [[Head back outside.->Hub]]
Sub-sub → parent:          [[Leave.->HubMarket]]
                           [[Return.->HubInn]]
After NPC chat:            [[Say goodbye and leave.->ScarBarracks]]
After SS scene:            [[Get dressed and leave.->ScarHub]]
                           [[Return.->HubInn]]
Declining an offer:        [[Decline and leave.->Hub]]
                           [[Refuse and leave.->ScarBarracks]]
```

### Day/Night Cycle
```harlowe
Time advance: (set:$DN to $DNO)(set:$DNO to $DNO2)(set:$DNO2 to $DN)
```
- Sleep = full cycle advance
- SS scenes = time advance (sex takes time)
- Travel = auto-set to appropriate time
- Night closes shops, changes NPC availability, opens different encounters

### Tags for Scene Formatting
```
tags="dnsc dnsi"  — hides the persistent footer (Character/Inventory/Spells/KamiMenu)
                    Used on SS scenes and linear narrative sequences
```

---

## 9. SS CONTENT PATTERNS

### Entry Pattern
1. Normal exploration leads to suggestive setup
2. Narration describes attraction/arousal BEFORE the choice
3. Explicit opt-in choice alongside a decline option
4. **Always a way out.** No forced voluntary SS.

### Entry Choice Examples
```
[[Ask Kami for sex.->KamiSS1]]                    — direct, alongside rest/equip options
(link:"Grope Dinus' package.")                     — after buildup passage
[[Something kinky.->MisfitHSS]]                    — alongside lab/leave options
[[Offer some sort of deal.->SQ1SS1]]               — ambiguous (quest context)
[[Say that you have no problems with...->HranSS1]] — notably direct
[[Agree.->MisfitSS1]]                              — alongside [[Decline and leave.->Hub]]
```

### Scene Length
- **Shortest:** 1 passage (bathroom encounter, Misfit casual)
- **Typical:** 3-5 passages (setup → escalation → action → aftermath)
- **Longest:** 6-7 passages (Wyatt, Hran with all branches)

### Scene Structure
```
Passage 1: Setup/consent — context, initial contact, opt-in choice
Passage 2: Escalation — foreplay, undressing, initial contact
Passage 3-4: Action — main act, often with mid-scene choices
Passage 4-5: Climax — described for both parties
Final: Aftermath — emotional beat, variable setting, return link
```

### Mid-Scene Choices (common feature)
- Kami: top or bottom
- Dinus: 4 sequential choice points
- Wyatt: 4 graduated choices
- Hans: body-frame variant
- Hran: top/bottom, then slit/ass
- Some scenes are linear once entered (Pren, Horse, Finn)

### Kami During Other SS Scenes
- **Leaves or turns away.** Text specifically notes his exit.
- "Kami gives you a look...steps out, giving you some privacy."
- "Kami snorts and trots off to the entrance of the Alley."
- Can optionally participate in Misfit threesome (MisfitHSSc1)
- Whelps scene: "Kami looks decidedly resigned"
- Zexir scene: "your canine companion bolts to the other side of the room"

### Casual vs. Relationship SS

| Aspect | Casual | Relationship |
|--------|--------|-------------|
| Entry | Direct proposition or physical impulse | Embedded in conversation/domestic scene |
| Dialogue during | Minimal or crude | Names used, tenderness expressed |
| Physical description | Anatomy and mechanics | Emotional reactions, eye contact, kissing |
| Aftermath | "Thanks, kid" / "Leave." | Cuddling, kissing, affectionate dialogue |
| Variables set | Flags only | $LoveMeter incremented |
| Return to | Hub | Relationship hub or conversation menu |

### Aftermath Variables
```
$FuckedKami = true          — changes repeat Kami SS dialogue
$MisfitF = true             — unlocks Kami jealousy dialogue
$HansF = true               — unlocks relationship track
$LoveMeter += 10/20/50      — relationship depth (varies by scene intimacy)
$coin += N or -= N          — Finn pays 100g, GnollLose steals coins
Day/night advances          — SS scenes consume time
```

---

## 10. CONTENT PROPORTIONS

### Passage Breakdown
```
~19%  SS/Adult content (90 passages)
~18%  Isle of Dragons (mix of plot, dialogue, SS)
~11%  Holstein core (inn, fountain, market)
~9%   Scarhaven (blacksmith, barracks, inn)
~6%   Quest content (maze, mountains, villages)
~6%   Combat system
~9%   Items/Equipment/System passages
~4%   Intro/Tutorial
~3%   Character Creation
~3%   Hub/Navigation
~12%  Dialogue, relationships, events
```

### SS Per Hub
```
Holstein:   6 scenes (Kami, Dinus, Wyatt, Misfit casual x2, EPFuck)
Scarhaven:  6 scenes (Kami reuse, Hans, Pren, Horse, Finn, SBaBSS)
IoD:        4 scenes (Hran x2, Zexir + voyeur alt, cave voyeur)
Quests:     4 scenes (Dragon Whelps, Akos, GnollLose, FleeFailPigorc)
```

### SS Location Pattern
- **Private rooms:** Inn room (Kami), Misfit's house, Wyatt's place, barracks office, council chamber
- **Semi-public/secluded:** Behind counter, alley, stables at night, smithy
- **Night-gated:** Wyatt, Misfit casual, Horse, Hran first, Zexir alt
- **Quest-gated:** Dragon Whelps, Akos
- **Combat consequence:** Gnoll, Pigorc

---

## 11. WRITING DNA — SUMMARY

### What the game IS:
- A storyteller voice narrating your adventure in second person
- Functional prose that frontloads concrete detail (species, height, fur color)
- Character voices that clearly signal class and personality through speech patterns
- A blank-slate protagonist defined entirely by choices
- Explore-at-your-own-pace hub design with progressive unlock via repeat visits
- SS content that is opt-in, signaled by buildup, and varies in emotional weight by context
- Humor that comes from character absurdity and situational comedy, never from jokes
- Drama that earns its weight through Kami's loyalty, NPC vulnerability, and the player's isolation

### What the game IS NOT:
- Literary or poetic prose (it's workmanlike in the best sense)
- Fourth-wall breaking (except Finn)
- Stat-heavy or mechanically complex (narrative gating over numerical stats)
- Grimdark or cynical (even the darkest moments have warmth)
- Verbose (paragraphs are short, dialogue is shorter, choices are shortest)

### Rules for Expansion Writing:
1. **Keep paragraphs to 2-5 sentences.** If you're writing more, split.
2. **Use concrete measurements.** Heights in feet, distances in metres.
3. **Introduce characters with the species-build-features-clothing-personality pattern.**
4. **Let past tense drift in** for ongoing states. Don't fight it.
5. **Use ellipses** for pauses, hesitation, and trailing speech.
6. **Match each character's formality level.** Don't make Kami casual or Misfit formal.
7. **Narrate the player's actions** rather than quoting them. The player is a blank slate.
8. **Always provide an exit.** Every SS scene has a decline. Every conversation has a "Leave."
9. **Don't break the fourth wall** unless writing Finn.
10. **Profanity belongs to characters, not the narrator.**
11. **Hub return links use standard text:** "Leave." / "Return." / "Head back outside."
12. **SS scenes need setup → opt-in → escalation → action → aftermath.** Don't skip the buildup.
13. **Relationship SS has emotional weight.** Casual SS does not. The gap is intentional.
14. **Use `(history:)` for one-time events, `$flags` for persistent state, `$counters` for progression.**
15. **Night = intimate/dangerous. Day = social/commercial.** Maintain the pattern.
