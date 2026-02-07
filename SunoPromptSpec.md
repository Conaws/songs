# Suno Prompt Specification

A complete reference for formatting instructions into maximally expressive Suno AI prompts.

---

## Two-Field System

Suno uses two separate input fields. Understanding their distinct purposes is critical.

| Field | Purpose | Contains |
|-------|---------|----------|
| **Style of Music** | Global blueprint for the song | Genre, mood, instruments, vocal style, high-level structure |
| **Lyrics/Custom Lyrics** | Section-by-section control | `[Structure Tags]`, lyrics, inline vocal/energy cues |

### Style of Music Field

This is a **short creative brief**. It defines *what the song is*.

**Include:**
- Genre or genre fusion
- Overall mood/emotional direction
- Main instruments (2-4 max)
- Vocal style (type, tone, delivery)
- High-level structure cues (build, drop, cinematic chorus)

**Exclude:**
- Lyrics or verses
- Song titles or artist names
- Narrative storytelling
- Vague filler ("cool," "fire," "radio hit")

**Example:**
```
Uplifting gospel trap with 808s, female layered vocals, and a big cinematic chorus
```

### Lyrics Field

This is where **structure tags** and **section-local cues** live.

**Rule of Thumb:**
- Writing lyrics → use `[Verse]`, `[Chorus]`, `[Bridge]` in the Lyrics field
- No custom lyrics → describe structure in the Style of Music field

---

## Placement Rules That Change Outcomes

| Rule | What To Do | Why It Helps |
|------|------------|--------------|
| **Top-load the palette** | Before first lyric: 1 mood + 1 energy + 1-2 instruments | Prevents "random first 10 seconds" |
| **Localize the hard turn** | Place `[Energy: High]` immediately before chorus | Prevents verses from running hot |
| **One job per tag** | Avoid conflicts like `[Mood: sad, happy, angry]` | Conflicts get averaged out |
| **Fewer instruments = cleaner output** | Pick 2-3 anchor timbres | Less clutter, cleaner arrangement |
| **Write for performance** | Keep lines tight and short | Improves intelligibility |
| **Front-load importance** | Most important descriptors in first 20-30 words | Strongest influence on generation |

---

## Core Structure Tags

### Primary Section Tags

| Tag | Purpose | Common Fix When It Fails |
|-----|---------|-------------------------|
| `[Intro]` | Establish palette; keep short | If too loud, add calm mood cue before it |
| `[Verse]` | Story lane; lower density than chorus | If repeating, write Verse 2 with angle shift |
| `[Pre-Chorus]` | Build tension before chorus | If weak, shorten phrasing and add `[Build-Up]` |
| `[Chorus]` | Hook lane; strongest energy | If doesn't lift, add `[Energy: High]` before it |
| `[Bridge]` | Contrast lane; change harmony/rhythm/space | If feels like Verse 3, strip drums or half-time |
| `[Outro]` | Resolve lane; plan the landing | If cuts hard, keep last line short, plan fade |
| `[Hook]` | Short catchy phrase | Use for memorable one-liners |
| `[Final Chorus]` | Biggest version of chorus | Add `[Energy: High]` for maximum lift |

### Dynamic/Energy Tags

Use only when you need a clear dynamic move:

| Tag | Purpose |
|-----|---------|
| `[Build]` / `[Build-Up]` | Gradual lift into chorus/drop |
| `[Drop]` | Impact lane (beat-forward hook moment) |
| `[Breakdown]` | Strip-back contrast (space + tension) |
| `[Interlude]` | Transitional instrumental passage |
| `[Solo]` | Instrumental spotlight |
| `[Fade Out]` | Gradual ending |
| `[End]` | Abrupt stop |

### Palette Tags (Place at Top)

```
[Mood: Focused]
[Energy: Medium]
[Instrument: Keys, Drums]
```

---

## Music Structure Tags

These advanced tags guide harmonic, melodic, and arrangement behavior:

### Tension & Release

| Tag | Effect |
|-----|--------|
| `[Ascending progression]` | Chord sequence that rises to create forward momentum |
| `[Descending melody]` | Melodic line stepping down for release/calm |
| `[Build-up dynamics]` | Gradual increase in volume/density toward peak |
| `[Falling tension]` | Release phase with simpler harmony, softer dynamics |
| `[Gradual swell]` | Slow intensity increase that blooms into next section |
| `[Musical tension]` | Harmonic/rhythmic pressure demanding resolution |
| `[Unresolved tension]` | Deliberately unfinished feeling |

### Transitions & Modulation

| Tag | Effect |
|-----|--------|
| `[Bridge modulation]` | Key change in/because of bridge |
| `[Chromatic transition]` | Move using notes outside key for sleek motion |
| `[Diatonic pivot]` | Smooth shift using chord common to both keys |
| `[Half-step change]` | Semitone modulation for dramatic lift |
| `[Relative switch]` | Move between relative major/minor |
| `[Sudden shift]` | Abrupt change in key/groove/texture |
| `[Knockout transition]` | Hard-hitting change with force |

### Emotional Direction

| Tag | Effect |
|-----|--------|
| `[Emotional climax]` | Feeling peaks with strongest lyric + biggest lift |
| `[Climactic theme]` | Central idea at maximum impact |
| `[Heightened emotion]` | Deliberate escalation of intensity |
| `[Introspective moment]` | Quieter, inward section |
| `[Yearning climax]` | Peak driven by longing rather than triumph |
| `[Uplifting message]` | Lyrical turn toward hope/resilience |
| `[Wistful hopeful]` | Bittersweet mix of longing and optimism |

### Harmonic Color

| Tag | Effect |
|-----|--------|
| `[Brightening harmonies]` | More open/hopeful harmony choices |
| `[Flattened tone]` | Bluesy, moody darker tint (♭3/♭6/♭7) |
| `[Circle of fifths]` | Movement through keys by perfect fifths |
| `[Harmonic surprise]` | Unexpected chord that still feels intentional |
| `[Jazz turn]` | Extensions, altered dominants, ii-V gestures |
| `[Neapolitan chord]` | bII major for bold dramatic color |

### Arrangement & Texture

| Tag | Effect |
|-----|--------|
| `[Atmospheric shift]` | Change in mood/space/sonic environment |
| `[Quiet arrangement]` | Sparse production for intimacy |
| `[Lush layers]` | Stacked harmonies/pads/counter-melodies |
| `[Textural contrast]` | Change in sonic density or timbre |
| `[Orchestral swell]` | Cinematic rise using strings/brass/pads |
| `[Outward expansion]` | Section opens up the soundstage |
| `[Zenith intensity]` | Highest energy point in track |

### Narrative & Lyric Direction

| Tag | Effect |
|-----|--------|
| `[Anticipatory lyrics]` | Lines that hint at what's coming |
| `[Lyrical foreshadowing]` | Early details that later pay off |
| `[Progressive storytelling]` | Each section advances the situation |
| `[Rising lyrics]` | Lines escalating in intensity/urgency |
| `[Guided imagery]` | Vivid sensory details like a camera moving |
| `[Dramatic twist]` | Surprising turn that reframes the moment |

---

## Voice & Vocal Tags

### Gender/Character
```
[Male Vocal]    [Female Vocal]    [Duet]
[Choir]         [Boy]             [Girl]
[Man]           [Woman]           [Children]
```

### Vocal Tone
```
[Airy]          [Breathy]         [Crisp]
[Deep]          [Gritty]          [Smooth]
[Raspy]         [Silky]           [Warm]
```

### Vocal Style
```
[Whisper]       [Spoken Word]     [Rap]
[Harmonies]     [Falsetto]        [Belting]
[Growl]         [Crooning]        [Operatic]
[Scat]          [Humming]         [Chanting]
```

### Vocal Effects
```
[Auto-tuned]    [Distorted]       [Reverbed]
[Vocoder]       [Telephone Effect] [Filtered]
```

### Vocal Emotion
```
[Vulnerable]    [Powerful]        [Soft]
[Aggressive]    [Melancholic]     [Joyful]
[Sultry]        [Defiant]         [Tender]
[Desperate]     [Triumphant]      [Intimate]
```

### Pitch & Range
```
[Low-pitched]   [High-pitched]    [Mid-range]
[Vocal expansion]  [Falsetto]     [Belting]
```

---

## Instrument Tags

### Limit to 2-4 per generation

**Keyboards:**
```
Piano, Electric Piano, Rhodes, Wurlitzer
Synth, Analog Synth, Moog Synth, Synth Pad
Organ, Harpsichord, Celesta
```

**Strings:**
```
Acoustic Guitar, Electric Guitar, Distorted Guitar
Nylon Guitar, 12-String Guitar, Bass Guitar
Violin, Cello, Harp, Ukulele, Banjo
```

**Drums/Percussion:**
```
Drums, 808s, TR-909, Drum Machine
Live Drums, Brushed Drums, Breakbeat
Congas, Tambourine, Handclaps, Timpani
```

**Wind/Brass:**
```
Saxophone, Trumpet, Trombone, Flute
Harmonica, Accordion, French Horn
```

**Electronic:**
```
Synth Bass, Acid Bass, Lead Synth
Arpeggiator, Glitch, Sidechain
```

---

## Genre Reference

**Electronic:** EDM, House, Techno, Trance, Dubstep, Drum and Bass, Synthwave, Chillwave, Future Bass, Trap, Ambient

**Hip-Hop/R&B:** Hip Hop, Boom Bap, Lo-fi Hip Hop, Trap Rap, R&B, Neo-Soul, Funk

**Rock:** Indie Rock, Alt Rock, Hard Rock, Punk, Grunge, Metal, Shoegaze, Post-Rock

**Pop:** Synth Pop, Electropop, Indie Pop, Dream Pop, Bedroom Pop, Dance Pop, K-Pop

**Folk/Country:** Folk, Indie Folk, Americana, Country, Bluegrass, Singer-Songwriter

**Jazz/Blues:** Jazz, Smooth Jazz, Bebop, Bossa Nova, Blues, Swing

**Classical:** Orchestral, Cinematic, Film Score, Chamber Music, Neoclassical

---

## Templates

### Template A: Full Song Structure

```
[Mood: Focused]
[Energy: Medium]
[Instrument: Keys, Drums]

[Intro]
(quiet movement; establish palette)

[Verse 1]
(tight lines; story lane)
Your verse lyrics here
Keep lines short and clear

[Pre-Chorus]
[Build-Up]
(shorter phrasing; raise anticipation)

[Chorus]
[Energy: High]
(simple hook; biggest lift)
Your hook lyrics here
Most memorable part

[Verse 2]
(new angle; same pocket)
Second verse lyrics
Advance the story

[Chorus]
[Energy: High]
(keep hook consistent)

[Bridge]
[Breakdown]
(space + contrast)
Bridge lyrics here

[Final Chorus]
[Energy: High]
(biggest version; same hook)

[Outro]
[Fade Out]
(leave room for fade)
```

### Template B: EDM/Electronic (Build-Drop)

```
[Mood: Euphoric]
[Energy: Building]
[Instrument: Synth, 808s, Lead]

[Intro]
[Atmospheric]
(kick-less atmosphere + arp motif, filtered percussion)

[Build]
[Build-up dynamics]
(risers + snare roll, add bass movement)

[Drop]
[Energy: High]
[Zenith intensity]
(full kick + bass, hook synth, strong groove)

[Breakdown]
(remove kick, keep pad + vocal chop motif)

[Build]
[Gradual swell]
(tension returns, bigger risers, wider harmony)

[Drop]
[Energy: High]
(second drop variation - new top line or bass rhythm)

[Outro]
[Fade Out]
(simplify elements, fade with motif)
```

### Template C: Intimate Ballad

```
[Mood: Vulnerable]
[Energy: Low]
[Instrument: Piano, Soft Strings]

[Intro]
[Quiet arrangement]
(space; single instrument)

[Verse 1]
[Soft] [Breathy] [Intimate]
Close, personal lyrics
Short phrases, room to breathe

[Chorus]
[Vulnerable] [Tender]
[Ascending progression]
Emotional hook here
Let the melody lift gently

[Verse 2]
[Introspective moment]
Deeper into the story
New details, same intimacy

[Bridge]
[Whisper]
[Emotional climax]
The confession or realization

[Final Chorus]
[Building] [Heightened emotion]
Same hook, more intensity

[Outro]
[Fade Out]
[Yielding resolution]
```

### Template D: Loop for Shorts/Reels (20-35 sec)

```
[Hook Loop]
[Mood: Confident]
[Energy: Medium→High]
[Instrument: Bass, Drums, Simple Lead]

(loop-friendly; minimal variation; clean downbeat)
Hook lyric line one
Hook lyric line two
(repeat hook; keep cadence identical)
```

---

## Advanced Techniques

### Technique A: Structure + Constraint

Add one constraint that prevents chaos:
- "Keep verses minimal; save full instrumentation for chorus."
- "No key change. No tempo change."
- "Keep the hook melody consistent across all choruses."

### Technique B: Build Variation Intentionally

Direct variation explicitly:
- "Verse 2 adds a counter melody."
- "Final chorus adds harmonies and extra drums."
- "Second drop switches bass rhythm, same hook lead."

### Technique C: Prevent Section Blur

Add clear boundaries:
- "Hard stop into chorus."
- "Drums drop for one bar before bridge."
- "Short break before final chorus."

### Technique D: Vocal Transitions

```
[Verse 1]
[Male Vocal] [Smooth]
His part of the verse

[Verse 1 continued]
[Female Vocal] [Airy]
Her response

[Chorus]
[Duet] [Harmonies]
Together now
```

---

## Anti-Patterns to Avoid

| Don't | Do Instead |
|-------|------------|
| `happy upbeat song` | `Upbeat synth-pop, 120 BPM, major key, joyful, bright synths` |
| `sad slow song` | `Melancholic ballad, 68 BPM, sparse piano, vulnerable female vocal` |
| `like Coldplay` | `2000s alt-rock, atmospheric, falsetto male vocal, piano-driven, anthemic` |
| `[Mood: sad, happy, angry]` | Pick ONE mood per tag |
| `[Fast] [Slow]` | Pick one tempo/energy |
| `[Heavy Metal] [Smooth Jazz]` | Commit to a coherent genre |
| 10+ instrument tags | Limit to 2-4 key instruments |
| Empty structure tags | Add lyrics or `[Instrumental]` under each |
| Vague words ("cool", "fire") | Specific descriptors with clear meaning |
| Lyrics in Style field | Lyrics belong in Lyrics field only |

---

## Quick Reference

### Style Prompt Formula
```
[Era] [Genre], [BPM], [2-4 Instruments], [Mood], [Texture], [Vocal Style]
```

### Lyrics Field Formula
```
[Palette tags at top]
[Section Tag]
[Inline voice/energy cues]
Actual lyrics here
```

### Essential Flow
```
[Intro] → [Verse] → [Pre-Chorus] → [Chorus] →
[Verse 2] → [Chorus] → [Bridge] → [Final Chorus] → [Outro]
```

### Voice Direction Formula
```
[Gender] [Texture] [Emotion]
Example: [Female Vocal] [Breathy] [Vulnerable]
```

### Iteration Strategy
1. Start broad, get genre/feel right
2. Refine instruments and texture
3. Adjust vocal style and emotion
4. Fine-tune structure and dynamics
5. Generate 6+ versions
6. Use Replace to fix single sections rather than regenerating everything

---

## Sources

- [Suno Wiki - List of Metatags](https://sunoaiwiki.com/resources/2024-05-13-list-of-metatags/)
- [Musci.io - Suno Tags Complete Guide](https://musci.io/blog/suno-tags)
- [How To Prompt Suno - Voice Tags Guide](https://howtopromptsuno.com/making-music/voice-tags)
- [Jack Righteous - Meta Tags & Structure Command Guide](https://jackrighteous.com/en-us/pages/suno-ai-meta-tags-guide)
- [Travis Nicholson - How To Write Suno AI Prompts](https://travisnicholson.medium.com/how-to-write-suno-ai-prompts-with-examples-46700d2c3003)
