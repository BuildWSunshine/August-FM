# August FM

## Core Idea

**August FM** is a public, independent front-end learning project built as a fictional seasonal radio station for the feeling of August.

It is not meant to behave like a conventional streaming platform. The site itself is the experience: a scrollable, interactive broadcast world that combines a retro radio interface, cassette culture, summer photography, editorial layout, analogue textures, handwritten traces, music, and changing station moods.

The conceptual blend is:

- radio station
- mixtape
- summer magazine
- analogue scrapbook / signal archive
- interactive front-end experiment

The site begins bright, warm, cream/yellow, and sun-bleached, then gradually moves toward darkness. From the **Now Playing / listening section downward**, the design becomes fully dark, eventually reaching **true black**, with saturated yellow, red, blue, orange, and other signal colors doing the visual work.

The clean version of the site is the main direction. Collage influence is used selectively rather than becoming the entire layout.

---

## Why It Exists

August has strong emotional meaning for me, enough that I wanted a project tied to it rather than another random practice brief with no personal pull.

The earlier concept, **Things Left in August**, was beautiful but did not spark enough desire to actually build it. I kept returning mentally to LemonPod and music-related work, which made it obvious that the practice project needed to intersect with something I genuinely cared about.

August FM solves that.

It gives me a public learning build that I actually want to finish while still forcing me to practise employable front-end skills:

- semantic HTML
- custom CSS
- responsive layout
- Flexbox
- Grid
- JavaScript state
- event handling
- dragging
- audio controls
- animation
- Canvas
- browser APIs
- accessibility
- asset integration
- visual hierarchy

The learning philosophy is:

> I want this interaction to exist. What does the browser give me that can make it happen?

This is intentionally a project I build myself. AI can help teach, review, debug, explain, generate references, or help me think through structure, but the implementation is meant to remain my independent public learning work.

---

## Canon / Locked Decisions

### Project identity

- Project name: **August FM**
- Public learning project.
- Scrollable website.
- Fictional seasonal radio station.
- Strong summer identity without becoming generic Mediterranean travel branding.
- The project is music-driven, analogue, tactile, youthful, and a little rough around the edges.
- The clean site direction is preferred over the full collage-wall version.

### Overall visual progression

The page should move roughly through:

**sun cream / yellow → saturated summer color → darker hardware / cassette tones → deep night → true black**

The ending should be **black**, not charcoal or almost-black.

Once the design enters the dark listening section, bright saturated color should appear as controlled signals against the black rather than as full-page color floods.

### Hero

- Radio is centered in the hero.
- Oversized **AUGUST FM** text sits on the **left**.
- The title may overlap the radio slightly.
- The overlap should feel poster-like / graffiti-adjacent in placement, while keeping the same bold condensed type rather than becoming literal graffiti lettering.
- The hero remains clearer and calmer than the Signal Log / gallery.
- Cream / sun-faded background at the top.
- Small analogue / handwritten details are allowed around the hero, but not enough to bury the radio.
- The radio is the visual and interactive anchor.

### Main radio

Final form: believable fictional vintage-inspired radio hardware rather than a historically exact real radio.

The current final visual direction has:

- black / aged dark metal chassis
- amber/gold details
- large smoked-glass screen
- large round volume knob on the right
- three physical buttons vertically on the left
- analogue-style frequency rail across the bottom
- previous / next arrow controls at the two ends of the rail
- worn, tactile, believable materials
- no extra four buttons surrounding the volume knob
- no built-in cassette slot in the hero radio

The three left controls are locked as:

1. **PLAY**
2. **SOURCE**
3. **SAVE**

The right large dial controls **volume**.

The lower frequency line / station rail is draggable.

The left and right arrow buttons also move between stations or tracks, depending on current interaction context.

The screen changes dynamically to show the current station / song imagery and information.

For now...

### Stations

Core stations:

- **Citrus — 88.1 FM**
- **Drive — 92.3 FM**
- **Static — 96.7 FM**
- **Afterglow — 101.9 FM**

Station identity:

**Citrus**
- bright
- wet
- yellow
- fresh
- daytime
- buoyant

**Drive**
- roads
- cars
- open windows
- motion
- heat
- speed

**Static**
- cassette culture
- analogue noise
- street graphics
- rougher / stranger texture
- black / dirty cream / red / blue

**Afterglow**
- late-day into night
- slower
- reflective
- blue / black / orange / red
- eventually gives way to true black

### Music

The site should eventually contain **actual songs**.

Users should be able to:

- tune into a station
- hear music associated with that station
- switch between songs within a station
- move between stations
- pause / play
- change volume

The experience should still feel like a radio station rather than turning into a Spotify clone.

Each station can eventually own a small track rotation.

Commercial music licensing / public streaming rights must be considered before publishing copyrighted songs. Development can use placeholders, local test audio, original audio, licensed audio, or royalty-free tracks.

### Layout philosophy

Use both **CSS Grid and Flexbox**.

This is explicitly allowed and preferred.

Mental model:

> Grid handles the map.  
> Flexbox handles the furniture.

Examples:

- Grid for cassette + tracklist areas.
- Flexbox for track rows, nav groups, controls, card internals, etc.

No loyalty oath to one layout system. CSS is not a cult.

### Visual hierarchy

The site should remain readable and structured.

The **gallery / Signal Log** can carry much of the messier, physical, youth-culture energy, while the rest of the site carries smaller traces of the same world.

The clean version wins over the full collage-wall treatment.

Desired balance:

> clean radio interface + small traces of summer debris

rather than:

> entire website is a scrapbook

---

## Visual Language

### Root colors

Initial root palette:

```css
:root {
  --cream: #F3EBD7;
  --black: #000000;
  --radio-black: #10100F;

  --yellow: #F4C400;
  --signal-red: #E74425;

  --pool-blue: #72BFD0;
  --cassette-blue: #244A73;

  --afterglow-orange: #E86C24;

  --text-light: #F7F3EA;
  --text-dark: #111111;

  --citrus: #F4C400;
  --drive: #D89A2B;
  --static: #C9C3B8;
  --afterglow: #E86C24;

  --citrus-dark: #6E5A00;
  --drive-dark: #3B2A17;
  --static-dark: #1E1E1E;
  --afterglow-dark: #1A0E12;
}
```

These are starting variables, not locked direction. They can be tuned once actual assets and browser rendering are visible.

### Color behavior

Top:
- cream
- yellow
- black
- pool blue

Citrus:
- yellow
- cream
- water blue
- green

Drive:
- yellow
- asphalt
- black
- chrome / metal

Static:
- black
- dirty cream
- signal red
- cassette blue

Afterglow:
- navy / deep blue
- black
- orange
- red

End:
- **true black**
- small bright signal colors only

### Typography

Three voices maximum.

#### 1. Bold condensed display

For:

- AUGUST FM
- station names
- large section titles

Reference direction:
- Anton
- Bebas Neue
- Oswald
- similar condensed / poster-like sans serif

The title should sometimes act as a graphic object, not merely text.

#### 2. Technical / UI type

For:

- frequencies
- time
- track metadata
- controls
- NOW PLAYING
- station data

Possible direction:
- IBM Plex Mono
- Space Mono
- JetBrains Mono
- compact UI sans / mono

#### 3. Handwritten accent

Used sparingly for:

- notes
- annotations
- crew messages
- scraps
- slogans
- cassette labels

Not for long paragraphs.

### Materials / textures

Approved visual language:

- sun-faded cream paper
- paper grain
- cassette plastic
- smoked glass
- brushed / scratched metal
- chrome
- aged black plastic
- transparent plastic
- condensation
- photocopy noise
- film grain
- halftone
- print misregistration
- adhesive tape
- handwritten ink / marker
- worn labels
- stickers
- torn-paper edges
- small scuffs / scratches
- analogue signal markings

Texture should be controlled. The interface must not drown in decorative noise.

### Motifs

Primary recurring motifs:

- cassette tapes
- analogue frequency markings
- waveforms
- ON AIR / LIVE indicators
- lemons / citrus
- pool-water / wet summer texture
- cars
- wheels
- asphalt
- aluminum drink cans / tabs
- basketball / sport fragments
- bikes
- surf imagery
- graffiti
- handwritten notes
- stickers
- tape labels
- summer photography
- road / mirror / open-window imagery

### Red-on-black detail

The red-on-dark can-tab / Red Bull-adjacent visual language is liked as an inspiration for sharp high-contrast accents.

This is a visual reference only, not a requirement to reproduce Red Bull branding.

### Drawing / asset rules

Draw myself when the asset carries authorship / personality:

- handwritten labels
- cassette labels
- scribbles
- symbols
- notes
- small signature details

Generate / source support material when authorship matters less:

- paper textures
- atmospheric photo fragments
- generic background fragments
- lighting / material reference

Build with CSS / SVG when possible:

- arrows
- frequency ticks
- borders
- labels
- simple stickers
- UI shapes
- indicator dots
- tuning marker

Avoid turning the project into a folder full of unnecessary PNG fragments.

---

## Features

### Core hero radio

Intended interactions:

- PLAY button
- SOURCE button
- SAVE button
- draggable volume knob
- draggable station / frequency marker
- previous arrow
- next arrow
- dynamic screen content
- station artwork changes
- track artwork changes
- station / track information changes

### Volume knob

The large right dial should be independently rotatable.

Concept:

- drag around knob
- calculate angle from knob center
- clamp allowed angle
- convert angle to a normalized value
- update audio volume
- rotate visual knob using CSS

The knob should be a separate asset from the static radio chassis.

### Frequency rail

Static frequency scale can remain baked into the chassis image.

The active marker / needle should be separate.

The marker can be made in HTML/CSS instead of being another image.

Interaction:

- pointer drag left / right
- convert pointer location to rail position
- map position to station / track state
- snap to valid station points when appropriate
- arrows can also move through the same available options

### Radio screen

The radio screen should not be baked into the chassis content.

Use a real HTML region positioned inside the smoked-glass opening.

Possible dynamic contents:

- station image
- station name
- frequency
- current track
- artist
- status
- waveform / visualizer

The smoked-glass frame / reflection can remain part of the radio shell or sit as a visual overlay.

### Station cards

Four primary station cards:

- Citrus
- Drive
- Static
- Afterglow

Each should have:

- name
- frequency
- short mood description
- image / artwork
- tune / play action
- station-specific visual identity

### Now Playing

Dark section beginning the deeper nighttime portion of the site.

Likely layout:

- cassette area
- track list
- current track metadata
- playback controls
- waveform / progress
- volume
- possibly current station indicator

Use Grid for major composition and Flexbox inside smaller track rows.

### Cassette

Central motif for the Now Playing / mixtape area.

Potential committed-ish functionality:

- reels spin while audio plays
- reels stop on pause
- cassette label changes
- track / mix information

Possible Side A / Side B logic is interesting but not fully locked.

### Signal Log / gallery

This section carries most of the collage / real-world summer culture.

Possible content:

- photos
- painted cards
- bottle caps
- bikes
- cassette photos
- graffiti
- handwritten scraps
- sport fragments
- road imagery
- stickers
- fake broadcast slips
- timestamps
- little summer observations

Tiny interactions can include:

- note lift
- sticker peel
- photo tilt
- tape corner movement
- small object reaction

This section can be much messier than the main radio UI.

### Scroll progression

The site is scrollable and should feel like time is passing.

Possible progression:

```text
14:42
17:18
20:07
23:41
01:13
```

This is fictional site time, not necessarily real local time.

The visual atmosphere should move from sunlit cream into full black.

### Audio

Eventually:

- real audio playback
- station-specific track lists
- current time / duration
- previous / next track
- play / pause
- volume
- track-end behavior
- optional shuffle within a station
- station switching

### Canvas

Canvas is not required for the physical radio controls.

Best use:

- waveform
- spectrum
- signal visualization
- synthetic visualizer first
- real audio-reactive visualizer later

### Accessibility

Intended:

- semantic buttons
- keyboard-operable controls
- visible focus states
- accessible labels
- responsive layout
- reduced-motion consideration
- graceful fallback if JavaScript fails / is unavailable where practical

---

## Technical Direction

### Core stack

**HTML**
- semantic structure
- buttons
- navigation
- screen content
- audio elements
- sections
- track list

**CSS**
- custom properties
- Grid
- Flexbox
- responsive design
- positioning
- transforms
- transitions
- layering
- station themes
- dark progression
- knob rotation
- visual state classes
- texture overlays
- typography
- focus / hover / active states

**Vanilla JavaScript**
- DOM selection
- events
- station state
- track state
- audio state
- source state
- save state
- pointer dragging
- tuner calculations
- volume calculations
- dynamic screen updates
- responsive interaction behavior
- arrays / objects for station and track data
- conditional UI updates

### Browser APIs / native capabilities

**HTMLAudioElement / `<audio>`**
- play
- pause
- source switching
- duration
- currentTime
- volume
- ended event
- seeking

**Pointer Events**
- pointerdown
- pointermove
- pointerup

Used for:
- knob dragging
- station rail dragging
- mouse / touch / pen support through one event system

**Intersection Observer**
- scroll-triggered section state
- light-to-dark progression
- station section entrances
- animation activation

**Canvas API**
- signal / waveform visualization
- optional visual effects

**Web Audio API** — later
- `AudioContext`
- `AnalyserNode`
- real frequency / waveform data
- audio-reactive Canvas

### Frameworks / libraries

Current decision:

- **No Bootstrap**
- **No React**
- **No jQuery**
- **No GSAP**
- no framework required

Use browser-native tools unless a later problem genuinely justifies a library.

### Radio asset architecture

Recommended asset / DOM structure:

```text
radio
│
├── radio-shell.png
│
├── volume-knob.png
│
├── screen
│   ├── station artwork
│   ├── station name
│   ├── frequency
│   ├── track metadata
│   └── canvas waveform
│
├── PLAY button / hit area
├── SOURCE button / hit area
├── SAVE button / hit area
│
├── frequency rail
│   └── HTML/CSS tuning marker
│
├── previous button
└── next button
```

Rule:

> If it needs to visibly rotate independently, separate it.  
> If it only needs to be clicked, it can stay visually baked into the chassis with a real HTML control over it.  
> If its content changes, make that region real HTML.

Likely minimum radio image assets:

```text
assets/radio/
├── radio-shell.png
└── volume-knob.png
```

Potential additional overlay only if needed:

```text
└── knob-highlight.png
```

### Suggested project structure

```text
august-fm/
├── index.html
├── styles.css
├── script.js
├── assets/
│   ├── images/
│   ├── radio/
│   ├── stations/
│   ├── textures/
│   ├── audio/
│   ├── icons/
│   └── fonts/
└── README.md
```

This can change if the project grows enough to justify splitting JS / CSS into modules.

---

## My Original Notes

### 2026-09-15

> “Things Left in August is definitely the one. August alone holds so much emotional meaning to me enough to drown in.”

Initial direction was **Things Left in August**, a still-life interactive summer scene with objects such as a notebook, camera, headphones, letters, lemonade, fan, and Polaroids.

The scene became increasingly asset-heavy and eventually stopped generating enough excitement to justify the work.

### 2026-09-15

> “I need to scrap the Things Left in August idea because it doesn't spark enough interest to make. I keep going back to the LemonPod and that's what excites me.”

This triggered the move toward a music / cassette / radio project while keeping **August**.


### 2026-09-15

> “I would make this site scrollable. It feels like it deserves so much interactivity and effects.”

Scrollable format became canon.

### 2026-09-15

> “Almost black definitely black by the end and then the bright saturated colours do the heavy lifting or just splash of colour is more the idea against dark.”

True-black ending became canon.

### 2026-09-15

> “I'd eventually add actual songs to it too users can switch between if they are picking a radio station.”

Real music is an eventual goal.

### 2026-09-15

> “I'd keep the radio centered to middle in hero, and still the FM text to the left maybe even overlapping it slightly like graffiti would but keeping the same bold font.”

Hero composition clarified.

### 2026-09-15

Radio control idea:

- right big circle = volume
- lower station line = station / song changes
- screen = changing images / station-song information
- previous / next arrows = change stations or songs
- rail can also be dragged left / right

### 2026-09-15

Final left-side button decision:

- top = PLAY
- middle = SOURCE
- bottom = SAVE

### 2026-09-15

Real-radio references were gathered to make the fictional player more believable.

The final preference was the more realistic dark metal model with the extra four volume-surround buttons removed.

### 2026-09-15

Important CSS learning shift: layout tools can be mixed locally according to the problem.

### 2026-09-15

New August moodboard introduced:

- painted cards
- bottle caps
- transparent cassettes
- sticker-covered surfaces
- graffiti
- bikes / surf objects
- youth / street summer culture

Observation:

> “I think the gallery row is doing lots of heavy lifting there”

Conclusion: the gallery / Signal Log can carry most of the dense personality, but smaller traces should appear elsewhere.

### 2026-09-15

After comparing full collage and clean mockups:

> “I like the clean version far more so I think I'll stick to it in the end.”

Final site direction became:

**clean layout first, selective collage details second.**

### 2026-09-16

Asset-production reflection:

> “I can see why people hire people to do this. I absolutely dread making the assets for my sites even though I do love drawing.”

Working rule emerged:

- draw signature assets
- source / generate support assets
- build simple graphics in CSS / SVG
- do not spend creative energy manually producing everything

---

## Decision Log

### 2026-09-15 — Dropped Things Left in August

**Changed:** Interactive still-life concept → August FM.

**Why:** Things Left in August did not create enough excitement to sustain the build. Music, cassette culture, and LemonPod-adjacent ideas had much stronger pull.

### 2026-09-15 — Locked August FM as public learning build

**Changed:** Generic practice project → personally meaningful public front-end project.

**Why:** The project should teach employable skills while still being something I actually want to make.

### 2026-09-15 — Made the site scrollable

**Changed:** Single-scene experience → full scroll journey.

**Why:** August FM has enough visual and interaction range to deserve progression, effects, station sections, and a day-to-night arc.

### 2026-09-15 — Added light-to-black progression

**Changed:** One consistent palette → evolving page atmosphere.

**Why:** Scrolling can represent time passing and let the lower listening sections become more immersive.

### 2026-09-15 — Locked true black ending

**Changed:** Near-black / navy-only night → actual black.

**Why:** Saturated signal colors should carry the visual energy against darkness.

### 2026-09-15 — Decided on actual music later

**Changed:** Purely visual fake radio → eventual functioning audio player.

**Why:** Users should eventually be able to tune to stations and switch songs.

### 2026-09-15 — No Bootstrap

**Changed:** Possible framework-assisted layout → custom CSS.

**Why:** The project depends on custom editorial composition, radio hardware, scroll behavior, and layout learning. Bootstrap adds little value here.

### 2026-09-15 — Flexbox + Grid both allowed

**Changed:** One-layout-system-at-a-time mental model → choose based on local geometry.

**Why:** Grid is better for 2D page areas; Flexbox is better for one-dimensional internal alignment.

### 2026-09-15 — Radio controls clarified

**Locked:**
- PLAY
- SOURCE
- SAVE
- volume knob
- draggable frequency rail
- previous / next
- dynamic screen

**Why:** Avoid repetitive controls while preserving believable hardware behavior.

### 2026-09-15 — Radio became modular

**Changed:** One flat interactive image → layered hardware / DOM architecture.

**Why:** Independently moving parts need separate assets or HTML/CSS layers.

### 2026-09-15 — Realism pass on radio

**Changed:** polished concept-render look → more believable vintage-inspired hardware.

**Why:** Real radio references showed better material depth, smoked glass, analogue scale language, physical knob depth, and mechanical plausibility.

### 2026-09-15 — Final radio form chosen

**Changed:** realistic version with four secondary buttons around the volume knob → same version with those four buttons removed.

**Why:** Keep believable materials while restoring simplicity and interaction clarity.

### 2026-09-15 — Collage wall explored, then rejected as primary direction

**Changed:** heavy full-page collage → clean primary design with selective collage traces.

**Why:** The clean version is much more appealing and gives the interface room to breathe.

### 2026-09-15 — Signal Log retained as the high-density personality zone

**Changed:** collage everywhere → gallery / Signal Log carries most of the mess.

**Why:** Preserve visual hierarchy while still representing the youth / street / cassette / summer moodboard.

---

## Current State

### Concept

Strongly defined.

August FM has:

- a clear identity
- an assignment brief
- station structure
- visual palette
- scroll progression
- interaction philosophy
- technical stack
- radio control logic
- radio visual direction
- station identities
- clean-vs-collage decision

### Design

Several AI-generated visual references used for inspiration exist, including:

- clean August FM page concepts
- darker radio / cassette concepts
- collage-wall concepts
- clean + collage hybrid mockups
- hero background experiments
- multiple radio hardware versions
- final preferred radio version

Current preferred page reference is the **clean version** rather than the full collage version.

Current preferred radio is the believable dark-metal / amber model with:

- PLAY / SOURCE / SAVE on left
- blank smoked screen
- large volume dial on right
- analogue rail on bottom
- arrows left / right
- no extra four buttons around the volume knob

### Code

No finished August FM implementation exists yet.

Some first-draft CSS experimentation has started while reviewing:

- `:root` variables
- Flexbox
- Grid
- selectors
- classes vs IDs
- `nth-child`
- background-image plans

Laptop issues / repair have interrupted implementation, so planning and design work have continued while coding access is limited.

### Assets

Some generated references exist, but the final production asset set is not complete.

The radio shell will likely need proper preparation / separation before implementation.

---

## Next Steps

Immediate work only.

1. **Sketch / wireframe the clean final page**
   - hero
   - stations
   - Now Playing
   - Signal Log
   - footer

2. **Lock exact content order**
   - confirm whether an About block exists on the main page
   - confirm whether mixtape is its own section or part of Now Playing

3. **Prepare the final radio asset**
   - isolate / export static radio chassis
   - isolate volume knob
   - preserve blank screen region
   - determine exact rail bounds for draggable marker
   - note pixel coordinates / proportions for button overlays

4. **Prepare a minimal asset inventory**
   - one image per station
   - cassette asset
   - Signal Log images
   - paper / grain texture
   - handwritten marks / notes
   - only what V1 actually needs

5. **When laptop is available again**
   - create HTML skeleton first
   - create major CSS layout
   - place radio
   - build station cards
   - build Now Playing grid
   - make responsive structure work before advanced animation

6. **Then add radio interaction**
   - PLAY
   - SOURCE
   - SAVE
   - volume knob
   - draggable frequency marker
   - previous / next
   - dynamic screen

---

## Parking Lot

Interesting, not committed.

### Hidden station / secret frequency

A user might manually tune into an unlisted frequency and discover:

```text
UNKNOWN SIGNAL
```

Possible easter egg / secret transmission.

Not V1.

### Side A / Side B

Cassette could map:

- Side A → Citrus + Drive
- Side B → Static + Afterglow

Interesting but not locked.

### Cassette flipping

3D cassette flip animation.

Later polish.

### Cassette drag-to-deck

Drag a cassette physically into a deck and snap it into place.

Delightful, unnecessary, dangerous to schedule.

### Scroll timestamps

Fictional time progression such as:

```text
14:42
17:18
20:07
23:41
01:13
```

Strong idea, not yet required.

### Station-specific motion systems

Possible:

- Citrus → water / caustics / buoyant motion
- Drive → horizontal movement / road lines / odometer
- Static → jitter / scanlines / interference
- Afterglow → slower transitions / long fades

### Static between stations

When not locked to a valid frequency:

- visual interference
- noise
- unstable waveform
- reduced clarity
- audio static

Could make the tuning rail much more satisfying.

### Saved Signals

SAVE button could eventually create a small saved-tracks / saved-signals collection.

Exact behavior is not locked yet.

### Source modes

SOURCE button behavior is not fully defined.

Possible future modes:

- FM
- TAPE
- other source

I should not invent more until the core player needs it.

### Real audio visualizer

Move from synthetic Canvas waveform to real Web Audio `AnalyserNode` data.

Later.

### Micro-interactions

Possible Signal Log details:

- sticker peel
- note lift
- photo tilt
- tape edge lift
- bottle-cap wiggle
- can-tab movement
- tiny cursor response

Only after core functionality works.

### Physical / brand extensions

Not part of the current build:

- real radio hardware
- cassette merchandise
- physical broadcast system
- August FM operating system
- actual 24/7 station infrastructure

---

## External / AI References

### User-originated source material

The concept is grounded in:

- the emotional significance of August
- saved Pinterest moodboards
- cassette-tape fixation
- summer imagery
- radio / car-stereo references
- user preference for clean layouts with tactile detail
- user preference for black lower sections with saturated accent color
- user desire for actual music later
- user preference for personally meaningful practice work over arbitrary briefs

### Real-world visual references

Referenced / observed categories include:

- vintage home radios
- vintage car radios
- analogue frequency rails
- old tuning needles
- brushed metal knobs
- smoked glass panels
- cassette decks
- transparent cassette shells
- bottle caps
- sticker-covered surfaces
- graffiti walls / windows
- bikes with surfboards
- basketball imagery
- summer roads
- rear-view mirrors
- citrus photography
- analogue print / editorial design

These are inspiration references, not requirements to directly copy a specific real product.

### AI-generated references

AI was used to generate / explore:

- early Things Left in August scenes
- isolated still-life assets
- day / night assets
- August FM layout concepts
- station page concepts
- clean versions
- collage-wall versions
- clean + collage hybrid versions
- multiple radio designs
- realism passes on the radio
- hero-background collage concepts

AI-generated images are **reference material and/or provisional assets**, not proof of final authorship of the implementation.

### AI contribution boundaries

AI has contributed:

- brainstorming
- critique
- project framing
- visual direction suggestions
- technical explanations
- architecture guidance
- reference image generation

The intended public build remains an **independently implemented learning project**.

Sara aka me, own the project direction, choose what survives, and write the actual implementation.

---

# One-Line Project Definition

> **August FM is a scrollable fictional summer radio station built as an independent front-end learning project, moving from sun-bleached cream into true black through interactive stations, cassette culture, analogue hardware, music, and carefully controlled traces of summer debris.**

---