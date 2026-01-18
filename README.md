# ScaleBuddy - Music Theory Reference Tool

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue" alt="Version">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
  <img src="https://img.shields.io/badge/Status-Active-success" alt="Status">
</p>

<p align="center">
  <strong>A comprehensive, single-file web application for music theory reference</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#usage">Usage</a> •
  <a href="#scales">Scales</a> •
  <a href="#chords">Chords</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#license">License</a>
</p>

---

## 🎵 What is ScaleBuddy?

**ScaleBuddy** is a lightweight, single-file web application that serves as a comprehensive music theory reference tool. It helps musicians, composers, and students quickly explore scales, triads, and chords for any root note.

### Key Features

- **40+ Scales** across 8 categories (Diatonic, Pentatonic, Symmetric, Jazz, World, Exotic, and more)
- **30+ Chords** including triads, seventh chords, extended chords, and classical chords
- **Roman Numeral Analysis** for scale degree triads
- **Proper Enharmonic Spelling** based on scale degrees
- **Offline-Capable** - works without internet connection
- **Modern UI** with responsive design
- **Auto-Updating** - instant results as you select options

---

## 🚀 Quick Start

### Option 1: Local Usage (No Installation Required)

1. Download the `index.html` file
2. Open it directly in any modern web browser (Chrome, Firefox, Safari, Edge)
3. Select a root note and scale from the dropdown menus
4. View the results instantly!

### Option 2: Live Demo

Visit the live demo at:  
**https://ozakinci.github.io/ScaleBuddy/**

---

## 📖 Usage

### Basic Workflow

1. **Select Root Note** - Choose from 12 pitch classes (C, C#, D, D#, E, F, F#, G, G#, A, A#, B, Db, Eb, Gb, Ab, Bb)
2. **Select Scale Type** - Choose from 40+ scales organized by category
3. **View Results** - Three sections appear automatically:

#### Scale Notes Section
Shows all notes in the selected scale with technical names and scale degrees in a table format for perfect alignment.

**Example (C Major):**
```
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┐
│  C  │  D  │  E  │  F  │  G  │  A  │  B  │  ← Notes (purple)
├─────┼─────┼─────┼─────┼─────┼─────┼─────┤
│  I  │ ii  │ iii │  IV │  V  │ vi  │vii° │  ← Roman numerals (gray)
└─────┴─────┴─────┴─────┴─────┴─────┴─────┘

C Tonic
D Supertonic
E Mediant
F Subdominant
G Dominant
A Submediant
B Leading Tone
```

#### Scale Triads Section
Shows triads for each scale degree with Roman numeral analysis.

**Example (C Major):**
```
I C - E - G (C Major)
ii D - F - A (D Minor)
iii E - G - B (E Minor)
IV F - A - C (F Major)
V G - B - D (G Major)
vi A - C - E (A Minor)
vii° B - D - F (B Diminished)
```

#### Scale Chords Section
Lists all possible chords for the selected root note and scale.

**Example (C Major chords):**
```
Cadd2 C - D - E - G
Cadd4 C - E - F - G
Cadd9 C - E - G - D
Cadd11 C - E - G - F
Cadd13 C - E - G - A
Caug C - E - G#
Cdim C - Eb - Gb
Cmaj7 C - E - G - B
Cmin7 C - Eb - G - Bb
... (30+ chords total)
```

### Tips

- **Unselected Dropdowns** are highlighted with a yellow tint
- **Results auto-update** when both dropdowns are selected
- **No results** appear if only one dropdown is selected
- **Works offline** - no internet connection required
- **Mobile-friendly** - responsive design for all screen sizes

---

## 🎼 Scales Included

ScaleBuddy includes **40+ scales** organized into 8 categories:

### Diatonic Modes
- Major (Ionian)
- Natural Minor (Aeolian)
- Harmonic Minor
- Melodic Minor (Ascending)
- Dorian
- Phrygian
- Lydian
- Mixolydian
- Locrian

### Minor Variants
- Harmonic Minor
- Melodic Minor (Ascending)
- Neapolitan Minor
- Neapolitan Major

### Pentatonic & Blues
- Major Pentatonic
- Minor Pentatonic
- Blues Scale

### Symmetric Scales
- Whole Tone
- Diminished (Half-Whole)
- Diminished (Whole-Half)
- Augmented
- Tritone

### Jazz & Contemporary
- Major Bebop
- Minor Bebop
- Dominant Bebop
- Prometheus
- Enigmatic

### Gypsy & Eastern European
- Hungarian Minor
- Hungarian Gypsy
- Double Harmonic (Gypsy)
- Phrygian Dominant

### World & Exotic
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
- Oriental

### Chromatic
- Chromatic

---

## 🎸 Chords Included

ScaleBuddy includes **30+ chords** organized into 7 categories:

### Basic Triads
- Major
- Minor
- Diminished
- Augmented
- Suspended 2nd
- Suspended 4th
- Power (5th)

### Sixth Chords
- Major 6th
- Minor 6th
- 6/9

### Seventh Chords
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

### Extended Chords
- 9th
- Major 9th
- Minor 9th
- 11th
- Minor 11th
- 13th
- Minor 13th

### Added Tone Chords
- add2
- add4
- add9
- add11
- add13

### Suspended Chords
- sus2
- sus4
- 7sus2
- 7sus4

### Altered Chords
- Altered (7alt)

### Special/Classical Chords
- Neapolitan (N6)
- Italian 6th
- French 6th
- German 6th
- Augmented Major 7

---

## 🛠️ Technical Details

### Technology Stack
- **HTML5** - Semantic structure
- **CSS3** - Modern styling with gradients, animations, and responsive design
- **Vanilla JavaScript** - No frameworks or build tools required

### Architecture
Single-file application (`index.html`) containing:
- HTML structure
- CSS styles (in `<style>` tag)
- JavaScript logic (in `<script>` tag)

### Data Structure
All music theory data is hard-coded for offline capability:

```javascript
// Scale definitions (semitones from root)
const SCALES = {
  major: [0, 2, 4, 5, 7, 9, 11],
  minor: [0, 2, 3, 5, 7, 8, 10],
  // ... 40+ scales
};

// Chord definitions (semitones from root)
const CHORDS = {
  'Major': [0, 4, 7],
  'Minor': [0, 3, 7],
  // ... 30+ chords
};
```

### Core Functions
- `getScaleNotes()` - Calculates scale notes with proper enharmonic spelling
- `getScaleTriads()` - Generates triads for each scale degree with Roman numeral analysis
- `getAllChordsForScale()` - Lists all possible chords for a given scale
- `applyEnharmonicSpelling()` - Applies proper enharmonic spelling based on parent scale

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Adding New Scales

1. Research the scale interval pattern (semitones from root)
2. Add to `SCALES` object in `index.html`
3. Add to `SCALE_NAMES` object for display name
4. Add to the appropriate `<optgroup>` in the HTML dropdown
5. Test the scale with various root notes

**Example:**
```javascript
// In SCALES object
myNewScale: [0, 2, 3, 5, 7, 8, 10],

// In SCALE_NAMES object
myNewScale: 'My New Scale Name',

// In HTML dropdown
<option value="myNewScale">My New Scale Name</option>
```

### Adding New Chords

1. Research the chord interval pattern (semitones from root)
2. Add to `CHORDS` object in `index.html`
3. Test the chord with various root notes

**Example:**
```javascript
// In CHORDS object
'My New Chord': [0, 4, 7, 10, 14],
```

### Code Style

- Use camelCase for JavaScript variables and functions
- Use kebab-case for HTML IDs and classes
- Keep functions focused and well-commented
- Follow the existing code organization pattern

### Testing

1. Open `index.html` in a browser
2. Test all scale categories
3. Test edge cases (chromatic scale, diminished scales)
4. Verify enharmonic spelling is correct
5. Check responsive design on mobile

---

## 📚 Music Theory Sources

Scale and chord interval patterns are based on authoritative music theory references:

### Scales
- [Wikipedia: List of musical scales and modes](https://en.wikipedia.org/wiki/List_of_musical_scales_and_modes)
- "The Jazz Theory Book" by Mark Levine
- "The Complete Musician" by Steven Laitz

### Chords
- [Wikipedia: List of chord names](https://en.wikipedia.org/wiki/List_of_chord_names)
- "The Chord Scale Theory & Jazz Harmony" by Bert Ligon
- "Harmony and Voice Leading" by Aldwell & Schachter

### Validation
All interval patterns have been cross-referenced with multiple sources to ensure accuracy.

---

## 🔧 Troubleshooting

### Issue: Dropdowns not updating
**Solution:** Make sure both root note and scale type are selected. If only one is selected, no results will appear.

### Issue: Wrong enharmonic spelling
**Solution:** This is intentional! The tool uses proper enharmonic spelling based on scale degrees. For example, in C Major, the 6th degree is A (not Bb), even though they sound the same.

### Issue: Scale not found
**Solution:** Check the spelling of the scale name in the dropdown. All scales are listed in the HTML `<optgroup>` tags.

### Issue: Browser compatibility
**Solution:** The app works in all modern browsers (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+). For older browsers, some CSS features may not work.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 ScaleBuddy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- Built with ❤️ for musicians and music students everywhere
- Inspired by the need for a quick, offline music theory reference
- Thanks to the music theory community for authoritative sources

---

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Troubleshooting](#troubleshooting) section
2. Review the [Contributing](#contributing) guidelines
3. Open an issue on GitHub

---

## 🎯 Roadmap

Future features may include:

- [ ] Audio playback of scales and chords
- [ ] Chord progression generator
- [ ] Staff notation display
- [ ] Keyboard diagram visualization
- [ ] Mobile app version
- [ ] Advanced search/filtering
- [ ] User presets/saved combinations
- [ ] Export functionality (PDF, MIDI)

---

**Made with 🎵 for musicians by musicians**

*ScaleBuddy - Your comprehensive music theory companion*
