# Suno Prompt Specification

A comprehensive guide for crafting maximally expressive prompts for Suno AI music generation.

---

## Overview

Suno uses two input fields:
1. **Style Prompt** — Describes the overall sound, genre, mood, and instrumentation
2. **Lyrics Field** — Contains lyrics with embedded `[metatags]` for structure and vocal direction

This spec covers both fields and how to use them together effectively.

---

## The Golden Rules

| Rule | Rationale |
|------|-----------|
| **4-7 descriptors** in style prompt | Too few = generic; too many = confused output |
| **Front-load importance** | First 20-30 words have strongest influence |
| **2-4 instruments max** | More causes muddiness and conflicts |
| **Iterate 6+ times** | Rarely perfect on first generation |
| **No artist names** | Copyright restrictions; use style descriptors instead |
| **Era + Genre** | "80s synth-pop" beats "synth-pop" alone |

---

## Style Prompt Structure

### Formula
```
[Era] [Genre/Subgenre], [BPM], [Key Instruments], [Mood], [Texture/Production], [Vocal Style]
```

### Examples

**Synthwave:**
```
1980s synthwave, 118 BPM, analog synth arpeggios, gated reverb drums,
neon-soaked atmosphere, dreamy male falsetto, lush pads, punchy bass
```

**Indie Folk:**
```
2010s indie folk, 92 BPM, fingerpicked acoustic guitar, warm upright piano,
intimate vulnerable female vocal, lo-fi tape warmth, wistful nostalgic
```

**Trap:**
```
Modern trap, 140 BPM half-time, heavy 808 sub bass, sparse hi-hats,
dark atmospheric pads, aggressive male rap, autotuned ad-libs
```

**Orchestral Cinematic:**
```
Epic cinematic orchestral, sweeping strings, powerful brass swells,
thundering timpani, triumphant heroic mood, building crescendo
```

---

## Metatag Reference

### Structure Tags
Place these in the **lyrics field** to define song sections:

| Tag | Purpose |
|-----|---------|
| `[Intro]` | Opening instrumental or vocal |
| `[Verse]` / `[Verse 1]` | Main narrative sections |
| `[Pre-Chorus]` | Tension building before chorus |
| `[Chorus]` | Hook, most memorable part |
| `[Post-Chorus]` | Extension after chorus |
| `[Bridge]` | Contrasting section, often before final chorus |
| `[Hook]` | Short catchy phrase |
| `[Break]` | Stripped-down moment |
| `[Drop]` | EDM-style climax after buildup |
| `[Buildup]` | Rising tension toward drop |
| `[Interlude]` | Transitional instrumental |
| `[Solo]` | Instrumental spotlight |
| `[Outro]` | Closing section |
| `[Fade Out]` | Gradual ending |
| `[End]` | Abrupt stop |

### Voice Tags

**Gender/Character:**
```
[Male Vocal]    [Female Vocal]    [Duet]
[Choir]         [Boy]             [Girl]
[Man]           [Woman]           [Children]
```

**Vocal Style:**
```
[Whisper]       [Spoken Word]     [Rap]
[Harmonies]     [Falsetto]        [Belting]
[Growl]         [Crooning]        [Operatic]
[Scat]          [Humming]         [Chanting]
[Yelling]       [Screaming]       [Call and Response]
```

**Vocal Texture:**
```
[Breathy]       [Airy]            [Crisp]
[Deep]          [Gritty]          [Smooth]
[Raspy]         [Silky]           [Nasally]
```

**Vocal Effects:**
```
[Reverb]        [Delay]           [AutoTune]
[No AutoTune]   [Distorted Vocals] [Filtered Vocals]
[Vocoder]       [Telephone Effect] [Radio Effect]
```

**Vocal Emotion:**
```
[Vulnerable]    [Powerful]        [Soft]
[Aggressive]    [Melancholic]     [Joyful]
[Sultry]        [Defiant]         [Tender]
[Desperate]     [Triumphant]      [Haunting]
```

### Instrument Tags

**Keyboards:**
```
[Piano]             [Electric Piano]      [Rhodes]
[Synth]             [Analog Synth]        [Moog Synth]
[Organ]             [Synth Pad]           [Wurlitzer]
[Harpsichord]       [Celesta]
```

**Strings:**
```
[Acoustic Guitar]   [Electric Guitar]     [Distorted Guitar]
[Clean Guitar]      [12-String Guitar]    [Nylon Guitar]
[Bass Guitar]       [Slap Bass]           [Fretless Bass]
[Violin]            [Viola]               [Cello]
[Double Bass]       [Harp]                [Ukulele]
[Banjo]             [Mandolin]
```

**Drums/Percussion:**
```
[Drums]             [808s]                [Drum Machine]
[TR-909]            [TR-808]              [Breakbeat]
[Live Drums]        [Brushed Drums]       [Electronic Drums]
[Congas]            [Bongos]              [Tambourine]
[Handclaps]         [Shaker]              [Timpani]
```

**Wind/Brass:**
```
[Saxophone]         [Alto Sax]            [Tenor Sax]
[Trumpet]           [Muted Trumpet]       [Trombone]
[Flute]             [Pan Flute]           [Clarinet]
[Harmonica]         [Accordion]           [Oboe]
[French Horn]       [Tuba]
```

**Electronic:**
```
[Synth Bass]        [Acid Bass]           [Wobbly Bass]
[Lead Synth]        [Arpeggiator]         [Glitch]
[Bitcrushed]        [Granular]            [Sidechain]
```

### Mood/Energy Tags

**Mood:**
```
[Uplifting]     [Melancholic]   [Haunting]      [Dark]
[Joyful]        [Nostalgic]     [Romantic]      [Intense]
[Dreamy]        [Peaceful]      [Euphoric]      [Epic]
[Intimate]      [Bittersweet]   [Triumphant]    [Ominous]
[Whimsical]     [Mysterious]    [Aggressive]    [Hopeful]
```

**Energy:**
```
[High Energy]   [Medium Energy]  [Low Energy]    [Chill]
[Driving]       [Explosive]      [Building]      [Steady]
[Frantic]       [Hypnotic]       [Pulsing]       [Relaxed]
```

**Texture/Production:**
```
[Lo-fi]         [Hi-fi]         [Gritty]        [Clean]
[Raw]           [Lush]          [Sparse]        [Dense]
[Tape-Saturated] [Vinyl Hiss]   [Atmospheric]   [Punchy]
[Warm]          [Bright]        [Polished]      [Muddy]
[Distorted]     [Compressed]    [Reverb-Drenched]
```

### Genre Tags (Curated Selection)

**Electronic/Dance:**
```
EDM, House, Deep House, Tech House, Techno, Trance,
Dubstep, Drum and Bass, Jungle, Synthwave, Retrowave,
Chillwave, Future Bass, Trap, Industrial, EBM,
Ambient, Downtempo, Trip-Hop, Breakbeat, UK Garage
```

**Hip-Hop/R&B:**
```
Hip Hop, Rap, Boom Bap, Lo-fi Hip Hop, Trap Rap,
Old School Hip Hop, Conscious Rap, Gangsta Rap,
R&B, Neo-Soul, Soul, Funk, Contemporary R&B
```

**Rock/Metal:**
```
Rock, Indie Rock, Alt Rock, Pop Rock, Hard Rock,
Punk Rock, Post-Punk, Grunge, Metal, Heavy Metal,
Thrash Metal, Death Metal, Progressive Rock,
Psychedelic Rock, Shoegaze, Post-Rock, Emo
```

**Pop:**
```
Pop, Synth Pop, Electropop, Indie Pop, Dream Pop,
Bedroom Pop, Dance Pop, Art Pop, Chamber Pop,
Bubblegum Pop, Teen Pop, K-Pop, J-Pop
```

**Folk/Country/Acoustic:**
```
Folk, Indie Folk, Folk Rock, Americana, Country,
Bluegrass, Singer-Songwriter, Acoustic, Celtic
```

**Jazz/Blues:**
```
Jazz, Smooth Jazz, Bebop, Cool Jazz, Fusion,
Bossa Nova, Blues, Delta Blues, Chicago Blues,
Soul Jazz, Swing, Big Band
```

**World:**
```
Latin, Salsa, Reggaeton, Reggae, Dancehall,
Afrobeat, Afropop, Flamenco, Bossa Nova,
World Music, Arabic, Indian Classical
```

**Classical/Orchestral:**
```
Classical, Orchestral, Chamber Music, Baroque,
Romantic Era, Neoclassical, Cinematic, Film Score,
Epic Orchestral, Opera, Choral, Minimalist
```

### Sound Effect Tags

**Environmental:**
```
[Birds Chirping]    [Rain]              [Thunder]
[Wind]              [Ocean Waves]       [City Ambience]
[Forest]            [Fire Crackling]    [Crickets]
```

**Human:**
```
[Applause]          [Cheering]          [Clapping]
[Whistling]         [Audience Laughing] [Crowd Chanting]
[Screams]           [Gasps]
```

**Technical:**
```
[Phone Ringing]     [Beeping]           [Static]
[Record Scratch]    [Tape Stop]         [Silence]
```

---

## Lyrics Field Format

### Basic Structure
```
[Intro]

[Verse 1]
First verse lyrics here
More lyrics on next line

[Pre-Chorus]
Building tension lyrics

[Chorus]
Catchy hook lyrics
Most memorable part

[Verse 2]
Second verse lyrics

[Bridge]
[Emotional] [Vulnerable]
Contrasting lyrics here

[Final Chorus]
[Powerful] [Belting]
Catchy hook with intensity

[Outro]
[Fade Out]
```

### Inline Voice Direction
```
[Verse 1]
[Soft] [Breathy]
Walking through the morning light
Shadows fading from the night

[Chorus]
[Powerful] [Belting]
We're alive, we're alive tonight!
```

### Vocal Transitions
```
[Verse 1]
[Male Vocal] [Smooth]
His part of the verse here

[Verse 1 continued]
[Female Vocal] [Airy]
Her response lyrics here

[Chorus]
[Duet] [Harmonies]
Together now we sing as one
```

---

## Complete Prompt Examples

### Example 1: Nostalgic Synthwave Ballad

**Style Prompt:**
```
1985 synthwave ballad, 98 BPM, dreamy analog synth pads,
gated reverb snare, neon-lit atmosphere, warm male vocal
with subtle chorus effect, nostalgic melancholic,
lush string synths, driving arpeggios
```

**Lyrics:**
```
[Intro]
[Instrumental]

[Verse 1]
[Soft] [Reverb]
Neon signs reflect on rain-soaked streets
Another night alone with fading beats
The radio plays songs we used to know
Before you had to go

[Pre-Chorus]
[Building]
And I'm still here waiting

[Chorus]
[Powerful] [Falsetto]
Driving through the endless night
Chasing after fading light
Every mile brings me closer to goodbye
Under purple skies we fly

[Verse 2]
[Vulnerable]
Photographs are scattered on the floor
Memories of what we were before
The tape deck plays our song on endless loop
While I'm stuck inside this room

[Bridge]
[Whisper] [Intimate]
Maybe in another life
Maybe in another time

[Final Chorus]
[Belting] [Euphoric]
Driving through the endless night...

[Outro]
[Fade Out]
```

### Example 2: Hard-Hitting Trap Anthem

**Style Prompt:**
```
Modern trap, 145 BPM half-time feel, heavy 808 sub bass,
crisp hi-hats with rolls, dark minor key, aggressive male rap,
sparse piano stabs, distorted ad-libs, hard-hitting punchy mix
```

**Lyrics:**
```
[Intro]
[808s] [Dark]

[Verse 1]
[Aggressive] [Rap]
Coming through with the pressure, yeah
Stack it up, getting better, yeah
Never fold under weather, yeah
We forever, put together, yeah

[Hook]
[AutoTune] [Melodic]
Run it up, run it up, to the top
Never stop, never stop, what we got

[Verse 2]
[Aggressive] [Rap]
Started low, now we elevated
Every move calculated
Success anticipated
Legacy we created

[Drop]
[High Energy]

[Hook]
[AutoTune] [Harmonies]
Run it up, run it up, to the top...

[Outro]
[Fade Out]
```

### Example 3: Intimate Indie Folk

**Style Prompt:**
```
2010s indie folk, 88 BPM, fingerpicked acoustic guitar,
warm upright piano accents, soft brushed drums, intimate vulnerable
female vocal, lo-fi tape warmth, wistful nostalgic autumn feeling,
sparse delicate arrangement
```

**Lyrics:**
```
[Intro]
[Acoustic Guitar]

[Verse 1]
[Soft] [Breathy] [Intimate]
Cardboard boxes line the hall
Pictures coming off the wall
Seven years inside these rooms
Now it's May and I leave June

[Chorus]
[Vulnerable] [Tender]
And I don't know where I'm going
But I know I can't stay here
Where the ghosts of who we were
Still whisper in my ear

[Verse 2]
[Soft]
Coffee cups still in the sink
Gives me too much time to think
Your sweater's hanging by the door
You won't be needing it anymore

[Bridge]
[Whisper]
Maybe someday I'll come back
When the missing doesn't hurt

[Final Chorus]
[Building] [Emotional]
And I don't know where I'm going...

[Outro]
[Humming] [Fade Out]
```

### Example 4: Epic Orchestral Cinematic

**Style Prompt:**
```
Epic cinematic orchestral, sweeping string section, powerful brass fanfares,
thundering timpani and bass drums, soaring choir, triumphant heroic mood,
building crescendos, John Williams style, major key, 120 BPM
```

**Lyrics:**
```
[Intro]
[Instrumental] [Building]

[Verse 1]
[Choir] [Soft] [Mysterious]
From the ashes we will rise
Reaching for the distant skies
Through the darkness, see the light
Warriors prepare to fight

[Chorus]
[Choir] [Powerful] [Triumphant]
Stand together, stand as one
The battle's lost but war's not done
With fire burning in our hearts
A brand new day is gonna start

[Instrumental Break]
[Solo] [Brass Fanfare]

[Bridge]
[Soft] [Strings]
Remember those who came before
Who gave their all and gave us more

[Final Chorus]
[Explosive] [Full Orchestra]
Stand together, stand as one!

[Outro]
[Fade Out] [Peaceful]
```

---

## Anti-Patterns to Avoid

| Don't | Do Instead |
|-------|------------|
| `happy upbeat song` | `Upbeat synth-pop, 120 BPM, major key, joyful, bright synths` |
| `sad slow song` | `Melancholic ballad, 68 BPM, sparse piano, vulnerable female vocal, intimate` |
| `like Coldplay` | `2000s alt-rock, atmospheric, falsetto male vocal, piano-driven, anthemic chorus` |
| `[Fast] [Slow]` | Pick one tempo/energy |
| `[Heavy Metal] [Smooth Jazz]` | Commit to a coherent genre |
| 10+ instrument tags | Limit to 2-4 key instruments |
| Empty structure tags | Add lyrics or `[Instrumental]` under each tag |

---

## Quick Reference Card

### Style Prompt Template
```
[Decade] [Genre], [BPM], [2-4 Instruments], [Mood], [Texture], [Vocal Style]
```

### Essential Structure Flow
```
[Intro] → [Verse 1] → [Pre-Chorus] → [Chorus] →
[Verse 2] → [Chorus] → [Bridge] → [Final Chorus] → [Outro]
```

### Voice Direction Formula
```
[Gender] [Texture] [Emotion]
Example: [Female Vocal] [Breathy] [Vulnerable]
```

### Iteration Strategy
1. Start broad, get the genre/feel right
2. Refine instruments and texture
3. Adjust vocal style and emotion
4. Fine-tune structure and dynamics
5. Generate 6+ versions, cherry-pick best sections

---

## Sources

- [Suno Wiki - List of Metatags](https://sunoaiwiki.com/resources/2024-05-13-list-of-metatags/)
- [Musci.io - Suno Tags Complete Guide](https://musci.io/blog/suno-tags)
- [How To Prompt Suno - Voice Tags Guide](https://howtopromptsuno.com/making-music/voice-tags)
- [Travis Nicholson - How To Write Suno AI Prompts](https://travisnicholson.medium.com/how-to-write-suno-ai-prompts-with-examples-46700d2c3003)
- [LitMedia - Suno Prompts Guide](https://www.litmedia.ai/resource-music-tips/suno-prompts/)
