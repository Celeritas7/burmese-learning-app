# Burmese Learning App

A comprehensive tool for learning Burmese language through Devanagari script transliteration and interactive conversation practice.

## 🎯 Project Overview

This application helps learners:
- Convert Burmese script to Devanagari script for pronunciation
- Practice conversations with word-by-word breakdowns
- Understand tone markers and vowel combinations

## 📁 Project Structure

```
burmese-learning-app/
├── README.md                          # This file
├── src/
│   ├── components/
│   │   ├── BurmeseConverter.jsx      # Main converter UI component
│   │   └── ConversationPractice.jsx  # Conversation practice interface
│   ├── logic/
│   │   └── converter.js              # Core conversion algorithm
│   └── data/
│       ├── consonants.js             # Burmese consonants mapping
│       ├── vowels.js                 # Burmese vowels mapping
│       └── characterDatabase.js      # Complete character mappings
├── docs/
│   ├── LEARNING_NOTES.md             # Your learning notes
│   └── ARCHITECTURE.md               # System architecture explanation
└── versions/
    └── snapshots/                    # Saved versions for comparison
```

## 🚀 Current Features

### ✅ Burmese to Devanagari Converter
- **Longest-match-first algorithm**: Accurately handles complex character sequences
- **Real-time conversion**: Type Burmese, see Devanagari instantly
- **Word-by-word breakdown**: Understand each component
- **Custom mappings**: Add missing characters on the fly

### ✅ Character Database
- 33+ consonants mapped
- 50+ vowel combinations
- Tone markers (१, २, ३)
- Special combination rules

### 🚧 In Progress
- Automatic consonant + vowel combination engine
- Conversation practice interface with chat-style UI
- Audio pronunciation support (planned)

## 🧠 How It Works

### The Longest-Match-First Algorithm

The converter uses a sophisticated matching algorithm:

1. **Sort all character mappings by length** (longest first)
2. **Process text left-to-right** naturally
3. **At each position, try longest matches first**
4. **When a match is found, add to output and move forward**

**Example:**
```
Input: မင်္ဂလာပါ
Processing:
  Position 0: Try "မင်္ဂလာပါ" → Match! → मिंग्गालाबा२
  Done!

Or if processing syllables:
  Position 0: Try "မင်္ဂ" → Match! → मिं
  Position 3: Try "လာ" → Match! → ग्गाला
  Position 5: Try "ပါ" → Match! → बा२
  Result: मिंग्गालाबा२
```

### Special Rules

#### Vowel ာ/ါ Rule
The vowel changes from `ာ` to `ါ` for these consonants:
- ခ, ဂ, ဃ, င, ချ, ဒ, ပ, ဝ

**Examples:**
- က + ာ = ကာ (का२) - uses ာ
- ခ + ါ = ခါ (खा२) - uses ါ

## 📝 Version History

### v1.0 - Basic Converter (Current)
- Initial converter with hardcoded character database
- Longest-match-first algorithm implemented
- Real-time conversion with breakdown
- Custom mapping feature

### v2.0 - Combination Engine (Planned)
- Automatic consonant + vowel combination
- All vowel rules implemented
- Medial support (ျ, ြ, ှ, ွ)

### v3.0 - Full Application (Planned)
- Conversation practice interface
- Progress tracking
- Multiple lesson support

## 🛠️ Technology Stack

- **Frontend**: React (functional components with hooks)
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **State Management**: React useState
- **Version Control**: Git + GitHub

## 📚 Learning Resources

### Key Concepts
1. **Burmese Script Structure**: Consonants + vowels + tone markers
2. **Devanagari Mapping**: Phonetic representation for pronunciation
3. **Tone System**: ១ (tone 1), २ (tone 2), ३ (tone 3)

### Useful Links
- [Burmese Script Wikipedia](https://en.wikipedia.org/wiki/Burmese_script)
- [Devanagari Script Wikipedia](https://en.wikipedia.org/wiki/Devanagari)

## 🤝 Contributing

This is a personal learning project. To track your progress:

```bash
# Save your changes
git add .

# Commit with descriptive message
git commit -m "Description of what you changed"

# Push to GitHub
git push origin main
```

### Commit Message Examples
- `"Added vowel combination rules for ာ/ါ"`
- `"Implemented medial character support"`
- `"Fixed tone marker positioning in complex words"`
- `"Added 20 new conversation examples"`

## 📊 Project Status

**Current Phase**: Building core converter logic
**Next Milestone**: Implement automatic consonant+vowel combination
**Long-term Goal**: Complete conversation practice platform

## 🎓 Learning Notes

See `docs/LEARNING_NOTES.md` for:
- Challenges encountered
- Solutions discovered
- Algorithm improvements
- Language rules learned

## 📞 Development Log

### Latest Updates
- ✅ Created basic converter UI
- ✅ Implemented longest-match algorithm
- ✅ Added custom mapping feature
- ✅ Discovered ာ/ါ vowel rule
- 🚧 Working on complete vowel combination system

## 🔮 Future Enhancements

1. **Performance Optimization**
   - Implement Trie data structure for faster matching
   - Benchmark different algorithm approaches

2. **UI Improvements**
   - Dark mode support
   - Keyboard shortcuts
   - Export/import custom mappings

3. **Educational Features**
   - Quiz mode
   - Spaced repetition for vocabulary
   - Pronunciation guides with audio

4. **Data Management**
   - CSV import for bulk character mappings
   - Database integration for persistence
   - Cloud sync for cross-device usage

---

**Last Updated**: January 2, 2026
**Version**: 1.0.0
**Status**: Active Development
