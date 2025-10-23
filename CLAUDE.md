# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Composer Client Checklist Form** - A single-page web application for music composers to gather comprehensive client information for audio-visual projects (films, documentaries, TV, video games, etc.). The entire application is self-contained in one HTML file with embedded CSS and JavaScript.

**Language:** French (UI text and form labels are all in French)

## How to Run

No build process required. Simply open the HTML file in a web browser:

```bash
# Open in default browser (Linux)
xdg-open composer-client-checklist.html

# Or use any web server
python3 -m http.server 8000
# Then navigate to http://localhost:8000/composer-client-checklist.html
```

## Architecture

### Single-File Application Structure

The `composer-client-checklist.html` file contains three embedded sections:
- **CSS** (`<style>` tag) - Responsive design with purple/blue gradient theme, print styles, mobile breakpoints
- **HTML** - Form structure with 8 main sections and 46 total input fields
- **JavaScript** (`<script>` tag) - Vanilla JS handling persistence, validation, and UI interactions

### Form Sections (in order)

1. **Informations sur le Projet** - Project type, duration, synopsis, target audience, distribution platforms
2. **Aspects Financiers** - Budget, payment modes, additional costs
3. **Spécifications Musicales** - Duration, themes, musical style, instrumentation, reference tracks
4. **Planning et Délais** - Timeline, milestones, composer availability
5. **Production Technique** - Sound engineer, delivery formats, synchronization requirements
6. **Aspects Juridiques et Droits** - SACEM registration, rights transfer, credits, portfolio usage
7. **Modalités de Collaboration** - Contact points, validation process, revision limits
8. **Éléments Complémentaires** - Temp tracks, constraints, future projects, billing details

### Data Persistence

**Storage:** Browser localStorage (key: `composerFormData`)
- Auto-saves on every input change (debounced)
- Manual save via "Sauvegarder" button (keyboard shortcut: Ctrl+S)
- Data persists across browser sessions

**Import/Export:**
- Export to JSON file (`donnees-formulaire.json`) - full structured data
- Export to TXT file (`fiche-client.txt`) - human-readable format
- Import from JSON (drag-and-drop or file picker)
- Keyboard shortcut: Ctrl+E for export

**Reset:** Clear all data with confirmation dialog

### Progress Tracking

The application tracks completion in real-time:
- **46 total fields** across all sections
- Visual progress indicator (bottom-right circle) shows percentage complete
- Filled fields get green border highlighting
- Progress calculation counts non-empty text inputs and textareas

Fields are identified by `data-field` attributes matching the stored data structure.

### Key JavaScript Functions

- `updateProgress()` - Calculates and displays completion percentage
- `saveData()` - Persists form data to localStorage with toast notification
- `loadData()` - Retrieves and populates form from localStorage
- `exportToJSON()` / `exportToTXT()` - Generate downloadable files
- `importFromJSON()` - Restore form state from JSON file
- `resetForm()` - Clear all data after confirmation

### Styling Notes

- **Responsive breakpoint:** `@media (max-width: 768px)` for mobile
- **Print styles:** `@media print` removes buttons and backgrounds for clean printouts
- **Theme colors:** Purple gradient header (#667eea to #764ba2), green accents (#4CAF50) for filled fields
- **Animations:** Smooth transitions on hover, auto-resizing textareas

## Making Changes

### Adding New Form Fields

1. Add HTML input/textarea with appropriate `data-field` attribute
2. Ensure field is within a `.question-item` container for styling
3. Field will automatically:
   - Save to localStorage on input
   - Count toward progress tracking
   - Export in JSON/TXT formats
   - Highlight when filled

### Modifying Export Formats

- **JSON export:** Modify `exportToJSON()` - uses direct localStorage data
- **TXT export:** Modify `exportToTXT()` - manually formatted string template with section headers

### Changing UI Theme

Colors are defined inline in CSS:
- Background gradient: `body { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }`
- Header gradient: `header { background: linear-gradient(135deg, #5f72bd 0%, #9b59b6 100%); }`
- Accent color: Green (#4CAF50) for filled states and buttons

### Translation/Localization

All UI text is hardcoded in French within the HTML. To translate:
1. Update all text content in HTML elements
2. Update labels, placeholders, and button text
3. Update `<html lang="fr">` attribute
4. Update toast notification messages in JavaScript
5. Update export filename strings in `exportToJSON()` and `exportToTXT()`

## Technical Constraints

- **No backend** - All data stored client-side only (no cloud sync)
- **No authentication** - Single-user per browser
- **Browser compatibility** - Requires modern browser with localStorage support
- **No dependencies** - Pure vanilla JavaScript (no libraries or frameworks)
- **Data portability** - Limited to JSON export/import (no database integration)
