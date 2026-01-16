# ScaleBuddy - AI Coding Instructions

## Project Overview
**ScaleBuddy** is a lightweight, single-file web application serving as a comprehensive music theory reference tool. Users select a root note and scale from dropdown menus to instantly view:
- **Scale Notes** - All notes in the selected scale
- **Scale Triads** - Triads for each scale degree with Roman numeral analysis
- **Scale Chords** - All possible chords for the selected root note and scale

**Tech Stack:** Vanilla HTML, CSS, JavaScript (no frameworks, no build tools)  
**Architecture:** Single `index.html` file containing all structure, styles, and logic  
**Deployment:** GitHub Pages (free hosting from GitHub repository)

---

## Core Requirements

### 1. Input Interface
Two dropdown menus that auto-update the display when both are selected:

**Root Note Dropdown:**
- All 12 pitch classes listed separately (no enharmonic merging)
- C, C#, D, D#, E, F, F#, G, G#, A, A#, B
- Db, Eb, Gb, Ab, Bb listed as separate options (even though they sound the same as sharps)

**Scale Dropdown:**
- Scales organized into logical groups using `<optgroup>` tags
- Groups: Diatonic Modes, Minor Variants, Pentatonic & Blues, Symmetric Scales, Jazz & Contemporary, Gypsy & Eastern European, World & Exotic, Chromatic
- Must include all scales known to man (comprehensive list)
- Scales should be researched and sourced from authoritative music theory references

### 2. Display Sections
Three sections appear below the dropdowns when both are selected:

**Scale Notes Section:**
- Displays all notes in the selected scale with technical names
- Uses proper enharmonic spelling based on scale degrees
- Format: Note names with scale degrees separated by arrows (e.g., "C (1) → D (2) → E (3) → F (4) → G (5) → A (6) → B (7)")
- Includes chord function names for each scale degree (e.g., "C Tonic", "D Supertonic", etc.)
- Formatting: Bold purple for note names, gray monospace for functions

**Scale Triads Section:**
- Shows triads for each scale degree with Roman numeral analysis
- Format: Roman numeral followed by triad notes and chord name (e.g., "I C - E - G (C Major)", "ii D - F - A (D Minor)")
- Uses proper notation: uppercase for major, lowercase for minor, ° for diminished, + for augmented
- Includes root note and quality in parentheses
- Compact format with empty lines between entries
- Formatting: Bold purple for Roman numerals, gray monospace for notes and chord names

**Scale Chords Section:**
- Lists all possible chords for the selected root note and scale
- Chords listed alphabetically by chord name within logical groups
- Includes essential blues & jazz chords (not exhaustive)
- Each chord shows: chord name and its notes
- Compact format with empty lines between entries
- Chord groups: Basic Triads, Sixth Chords, Seventh Chords, Extended Chords, Added Tone Chords, Suspended Chords, Altered Chords, Special/Classical Chords

### 3. UI/UX Requirements
- **Modern, clean design** with soft colors (purple/blue gradient)
- **Easy navigation** - intuitive layout with grouped dropdowns
- **Auto-updating** - display updates immediately when both dropdowns are selected
- **Subtle highlighting** - unselected dropdowns have yellow tint
- **No display** - if only one dropdown is selected, show nothing below
- **Offline-capable** - works without internet connection
- **Compact display** - triads and chords shown in compact format with bold purple names and gray notes

---

## Music Theory Data

### Notes (Pitch Classes)
All 12 notes must be listed separately in the root dropdown:
- Natural notes: C, D, E, F, G, A, B
- Sharps: C#, D#, F#, G#, A#
- Flats: Db, Eb, Gb, Ab, Bb

**Important:** C# and Db are separate options (they sound the same but are different pitch classes)

### Scales (Comprehensive List)
Research and include all scales known to man. Start with these categories:

**Diatonic Scales:**
- Major (Ionian)
- Natural Minor (Aeolian)
- Harmonic Minor
- Melodic Minor (Ascending)
- Dorian
- Phrygian
- Lydian
- Mixolydian
- Locrian

**Pentatonic Scales:**
- Major Pentatonic
- Minor Pentatonic
- Blues Scale (Minor Pentatonic with added blue note)
- Major Pentatonic with added notes

**Whole Tone & Diminished:**
- Whole Tone
- Diminished (Half-Whole)
- Diminished (Whole-Half)

**Exotic/World Scales:**
- Hungarian Minor
- Harmonic Minor (already listed)
- Double Harmonic (Gypsy)
- Phrygian Dominant
- Neapolitan Minor
- Neapolitan Major
- Enigmatic
- Augmented
- Prometheus
- Tritone
- Balinese
- Japanese (In Sen)
- Hirajoshi
- Iwato
- Yo
- Chinese
- Mongolian
- Persian
- Arabian
- Byzantine
- Hungarian Gypsy
- Oriental
- Major Bebop
- Minor Bebop
- Dominant Bebop
- Blues (multiple variants)
- Chromatic

**Research Required:** Use authoritative sources (Wikipedia, music theory textbooks, academic papers) to ensure accuracy.

### Chords (Essential List)
Organized by category for easier navigation. Includes essential blues & jazz chords:

**Basic Triads:**
- Major
- Minor
- Diminished
- Augmented
- Suspended 2nd
- Suspended 4th
- Power (5th)

**Sixth Chords:**
- Major 6th
- Minor 6th
- 6/9

**Seventh Chords:**
- Major 7th
- Dominant 7th
- Minor 7th
- Minor Major 7th
- Half-Diminished (m7b5)
- Fully Diminished 7th
- 7(b5)
- 7(#5)
- 7(b9)
- 7(#9)
- 7sus4

**Extended Chords:**
- 9th
- Major 9th
- Minor 9th
- 11th
- Minor 11th
- 13th
- Minor 13th

**Added Tone Chords:**
- add2
- add4
- add9
- add11
- add13

**Suspended Chords:**
- sus2
- sus4
- 7sus2
- 7sus4

**Altered Chords:**
- Altered (7alt)

**Special/Classical Chords:**
- Neapolitan (N6)
- Italian 6th
- French 6th
- German 6th
- Augmented Major 7

**Research Required:** Use authoritative sources (Wikipedia, jazz theory books, classical harmony texts) to ensure accuracy.

---

## Implementation Strategy

### Phase 1: Data Collection & Research
1. **Research all scales** - Create comprehensive list with interval patterns
2. **Research all chords** - Create comprehensive list with interval patterns
3. **Validate accuracy** - Cross-reference multiple authoritative sources

### Phase 2: Data Structure
```javascript
// All data hard-coded in JavaScript for offline capability
const NOTES = ['C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B', 'Db', 'Eb', 'Gb', 'Ab', 'Bb'];

const SCALES = {
  // Format: scaleName: [semitone intervals from root]
  major: [0, 2, 4, 5, 7, 9, 11],
  minor: [0, 2, 3, 5, 7, 8, 10],
  // ... all scales
};

const CHORDS = {
  // Format: chordName: [semitone intervals from root]
  'Major': [0, 4, 7],
  'Minor': [0, 3, 7],
  // ... all chords
};
```

### Phase 3: Core Logic
```javascript
// Calculate scale notes with proper enharmonic spelling
function getScaleNotes(rootNote, scaleIntervals) { ... }

// Calculate triads for each scale degree with Roman numeral analysis
function getScaleTriads(rootNote, scaleIntervals) { ... }

// Calculate all chords for a given scale
function getAllChordsForScale(rootNote, scaleIntervals) { ... }

// Apply enharmonic spelling based on scale degrees
function applyEnharmonicSpelling(notes, parentScale) { ... }
```

### Phase 4: UI Implementation
- Modern, clean design with soft colors (purple/blue gradient)
- Responsive layout
- Auto-update on dropdown changes
- Subtle highlighting for unselected dropdowns (yellow tint)
- Compact display format with bold purple names and gray notes

---

## Code Organization Pattern

```javascript
// 1. MUSIC DATA - Comprehensive scale and chord definitions
const NOTES = [...];
const SCALES = {...};
const CHORDS = {...};

// 2. MUSIC LOGIC - Calculation functions
function getScaleNotes(rootNote, scaleIntervals) { ... }
function getScaleTriads(rootNote, scaleIntervals) { ... }
function getScaleChords(rootNote, scaleIntervals) { ... }
function applyEnharmonicSpelling(notes, parentScale) { ... }

// 3. UI LOGIC - Display functions
function renderScaleNotes(notes) { ... }
function renderScaleTriads(triads) { ... }
function renderScaleChords(chords) { ... }
function updateDisplay() { ... }

// 4. EVENT HANDLERS - Dropdown interactions
document.addEventListener('DOMContentLoaded', () => { ... });
```

---

## Developer Workflow

### Local Testing
- Open `index.html` directly in browser (no server needed)
- Test dropdown selections
- Check browser console for errors
- Use DevTools to verify calculations

### Research Workflow
1. **Identify scale/chord** - What needs to be added?
2. **Find authoritative source** - Wikipedia, music theory textbooks, academic papers
3. **Extract interval pattern** - Convert to semitone intervals from root
4. **Validate** - Cross-reference with at least 2 sources
5. **Add to data structure** - Update JavaScript with new entry
6. **Test** - Verify display is correct

### Git & GitHub Workflow
Since you're new to GitHub, here's the learning path:

**Step 1: Install Git**
- Download and install Git from git-scm.com
- Configure with your name and email

**Step 2: Create GitHub Account**
- Sign up at github.com
- Create a new repository named "ScaleBuddy"

**Step 3: Local Repository**
```bash
# Navigate to project folder
cd c:\Users\tayoz\Downloads\ScaleBuddy

# Initialize git repository
git init

# Add files
git add index.html
git add copilot-instructions.md

# Commit changes
git commit -m "Initial commit: ScaleBuddy MVP"

# Connect to GitHub
git remote add origin https://github.com/YOUR_USERNAME/ScaleBuddy.git
git branch -M main
git push -u origin main
```

**Step 4: Future Updates (Pull, Update, Push)**
```bash
# Before making changes, pull latest from GitHub
git pull origin main

# Make your changes to the files

# After making changes, add and commit
git add .
git commit -m "Description of changes"

# Push to GitHub
git push
```

**Step 5: GitHub Pages Deployment**
- Go to repository on GitHub
- Settings → Pages → Source: Deploy from branch → main
- Your app will be at: https://YOUR_USERNAME.github.io/ScaleBuddy/

---

## Conventions

### Naming
- JavaScript variables: camelCase (`getScaleNotes`, `currentScale`)
- HTML IDs/classes: kebab-case (`root-note`, `scale-notes-display`)
- Scale names: Title Case with mode in parentheses (e.g., "Major (Ionian)")
- Chord names: Standard notation (e.g., "Major", "Minor", "Major 7th")

### Data Format
- **Intervals:** Always semitones from root (0 = root)
- **Notes:** Uppercase with optional # or b (C#, Db)
- **Scale/Chord names:** Human-readable, alphabetically sorted

### Validation
- Gracefully handle missing data
- Show user-friendly messages
- Don't crash on bad input

### Accessibility
- Semantic HTML
- Keyboard navigation
- Clear labels
- Good color contrast

---

## Research Sources

### Scales
- Wikipedia: "List of musical scales and modes"
- Music theory textbooks (e.g., "The Jazz Theory Book" by Mark Levine)
- Academic papers on world music scales

### Chords
- Wikipedia: "List of chord names"
- Jazz theory books (e.g., "The Chord Scale Theory & Jazz Harmony")
- Classical harmony texts (e.g., "Harmony and Voice Leading" by Aldwell & Schachter)

### Validation
- Cross-reference at least 2 sources for each scale/chord
- Verify interval patterns are correct
- Test with known examples (e.g., C Major scale should be C D E F G A B)

---

## Future Roadmap (TBD)
- Audio playback
- Chord progressions
- Staff notation display
- Keyboard diagram
- Mobile app version
- Advanced search/filtering
- User presets/saved combinations
