# 🧠 Behavior Design Review

A Figma plugin for analyzing UI designs using behavioral design principles and adding **individual suggestion notes** directly linked to specific elements.

## Features

### 🔍 Frame Analysis
- Extracts text, buttons, and hierarchy from selected frames
- Analyzes design patterns against behavioral heuristics
- Generates **element-specific** recommendations

### 📊 Behavioral Heuristics Evaluation
- **Fogg's Ability**: Minimize physical/cognitive effort (checks text length, font sizes)
- **Spark Triggers**: Clear calls to action (detects buttons, CTAs)
- **Scarcity/Urgency**: Use of loss aversion
- **Social Proof**: Influence through community validation
- **Goal Gradient**: Progress indicators to increase completion

### 📝 Individual Element Notes
The plugin creates **individual notes for each element** that needs attention:
- Notes positioned to the right of the frame
- **Connector lines** linking each note to the specific element
- **Color-coded dots** to identify the observation source
- Clear separation between issues (⚠️) and suggestions (💡)

### What Gets Created

When you click "Add Notes", the plugin generates:

| Element | Description |
|---------|-------------|
| **Summary Card** | Overall behavioral score at the top |
| **Individual Notes** | One note per element observation |
| **Connector Lines** | Dashed lines linking notes to elements |
| **Source Dots** | Colored dots indicating which element is being referenced |

### 🌐 Multilingual Support
- English (EN)
- Español (ES)

### 🎨 Theme Support
- Light mode
- Dark mode

## Installation

1. Open Figma Desktop
2. Go to Plugins > Development > Import plugin from manifest...
3. Select the `manifest.json` file from this directory

## Usage

1. **Select a Frame**: Choose a frame in Figma to analyze
2. **Choose Criteria**: Select which behavioral heuristics to evaluate
3. **Add Context** (optional): Provide additional context for the analysis
4. **Review Observations**: See element-specific issues and suggestions
5. **Add Notes**: Creates individual notes with connectors on the canvas
6. **View Notes**: Each note is linked to the specific element it references

## Project Structure

```
├── manifest.json    # Figma plugin manifest (v3)
├── code.js         # Main plugin logic (Figma API)
├── ui.html         # Plugin UI (HTML/CSS/JS)
├── package.json    # Project dependencies
└── README.md       # This file
```

## Technical Details

- **Manifest Version**: 1.0.0 (Manifest V3)
- **Language**: Pure JavaScript (no TypeScript dependencies)
- **UI Framework**: Vanilla HTML/CSS/JavaScript
- **Communication**: postMessage API between UI and Figma sandbox

## Note Types

### Issue Notes (⚠️)
- Text too long (cognitive load)
- Font size too small (readability)
- Deep hierarchy (navigation complexity)

### Suggestion Notes (💡)
- Add CTA buttons
- Add urgency indicators
- Add social proof elements
- Add progress indicators

## Behavioral Design Principles

This plugin is based on established behavioral design frameworks:

1. **BJ Fogg's Behavior Model**: B = MAT (Behavior = Motivation + Ability + Trigger)
2. **Robert Cialdini's Principles of Persuasion**: Scarcity, Social Proof, etc.
3. **Goal Gradient Effect**: Hull's hypothesis on increased effort near goal completion

## Development

No build step required! The plugin uses plain JavaScript and runs directly in Figma.

### Linting

```bash
npm install
npm run lint
```

## License

MIT
