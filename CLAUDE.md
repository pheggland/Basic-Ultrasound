# CLAUDE.md - AI Assistant Guidelines for Basic-Ultrasound

## Project Overview

**Basic-Ultrasound** is a static HTML educational web application for teaching basic ultrasound fundamentals. It serves as Lecture 1 of an ultrasound course developed by SUSTAIN (Stavanger UltraSound Training And Innovation Network) at the University of Stavanger.

### Purpose
- Provide an interactive learning platform for medical students/professionals
- Teach fundamental concepts of ultrasound imaging
- Deliver educational content through video lectures, quizzes, and lecture notes

### Lecturer
- **Kristy E. Stohlmann**, University Lecturer in Ultrasound

## Codebase Structure

```
Basic-Ultrasound/
├── CLAUDE.md          # This file - AI assistant guidelines
├── README.md          # Minimal project documentation
└── index.html         # Main application (single-page HTML with embedded CSS)
```

### Key Files

| File | Purpose |
|------|---------|
| `index.html` | Main application - contains all HTML structure and embedded CSS (~550 lines) |
| `README.md` | Basic project description (minimal) |

## Technology Stack

- **Frontend**: Vanilla HTML5 with embedded CSS
- **Styling**: Inline `<style>` block (no external CSS files)
- **JavaScript**: None (static content only)
- **Build System**: None required
- **Dependencies**: None (no npm, pip, or other package managers)

### External Services Used
- **Panopto** (uis.cloud.panopto.eu): Video lecture hosting
- **Google Drive**: PDF lecture notes storage

## Development Workflow

### Getting Started
1. Clone the repository
2. Open `index.html` directly in a web browser
3. Make edits to HTML/CSS as needed
4. Refresh browser to see changes

### No Build Process Required
This is a static HTML project. There are no:
- Build tools or transpilers
- Package managers (npm, yarn, pip)
- Development servers
- Test frameworks

### Testing
- Manual browser testing only
- Test responsiveness at different viewport sizes (mobile breakpoint at 768px)

## Code Conventions

### HTML Structure
The `index.html` follows this section order:
1. `<head>` - Metadata and embedded CSS styles
2. `.header` - Page title/header
3. `.content` - Main content container containing:
   - `.welcome-section` - Course introduction
   - `.learning-objectives` - List of learning goals
   - `.video-wrapper` - Embedded Panopto video
   - `.quiz-section` - Quiz information and preview
   - `.pdf-section` - Lecture notes download
   - `.footer` - Organization info

### CSS Conventions
- All styles embedded in `<style>` block within `<head>`
- Uses CSS custom properties via gradient color schemes
- Mobile-first responsive design with `@media (max-width: 768px)` breakpoint
- BEM-like class naming (`.question-preview`, `.quiz-header`, etc.)
- Color scheme: Blues (#3498db), Greens (#27ae60), Purples (#667eea), Oranges (#e67e22)
- Font stack: `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`

### Component Classes
| Class | Purpose |
|-------|---------|
| `.container` | Main wrapper with max-width 900px |
| `.welcome-section` | Blue-bordered intro box |
| `.info-box` | Green-bordered information box |
| `.tips-box` | Yellow-bordered tips/hints box |
| `.cta-box` | Purple gradient call-to-action box |
| `.question-preview` | Quiz question display cards |
| `.btn`, `.btn-primary`, `.btn-success`, `.btn-warning` | Button styles |

## Known Issues / Incomplete Features

### Placeholder Content
The following placeholders exist in `index.html` and need real URLs:

```html
<!-- Line 451 and 515 - Quiz links contain placeholder text -->
<a href="[LEGG INN QUIZ-LENKE HER]" ...>
```

**Note**: The placeholder text is in Norwegian ("LEGG INN QUIZ-LENKE HER" = "INSERT QUIZ LINK HERE")

## AI Assistant Guidelines

### When Making Changes

1. **Preserve Structure**: Maintain the existing HTML section order and class naming conventions
2. **Embedded CSS Only**: Keep all styles in the `<style>` block - do not create external CSS files unless specifically requested
3. **No JavaScript**: This is a static HTML page - do not add JavaScript unless explicitly requested
4. **Responsive Design**: Test any layout changes at both desktop and mobile (768px) breakpoints
5. **Color Consistency**: Use the existing color palette when adding new elements
6. **Accessibility**: Maintain semantic HTML and proper heading hierarchy

### Common Tasks

#### Adding a New Section
1. Create a new `<div>` with appropriate class in `.content`
2. Use existing box styles (`.info-box`, `.tips-box`, `.cta-box`) for consistency
3. Add section header using existing header patterns (e.g., `.quiz-header`, `.pdf-header`)

#### Updating Quiz Link
Replace `[LEGG INN QUIZ-LENKE HER]` with actual URL in both locations (lines 451 and 515)

#### Adding New Lectures
Consider creating new HTML files (e.g., `lecture-2.html`) following the same structure as `index.html`

### Do Not

- Add external CSS/JS frameworks without explicit request
- Create complex build systems for this simple static site
- Remove existing educational content without confirmation
- Change the SUSTAIN branding or lecturer attribution
- Modify external service URLs (Panopto, Google Drive) without verification

### File Modification Tips

- The CSS block spans approximately lines 7-403
- The HTML body content starts at line 405
- Quiz links are at lines 451 and 515
- Video iframe is at lines 428-435
- PDF link is at line 536

## External Resources

- **Video Lecture**: `https://uis.cloud.panopto.eu/Panopto/Pages/Embed.aspx?id=fefaf567-073d-4e33-b6c6-aef60097cd27`
- **Lecture Notes PDF**: `https://drive.google.com/file/d/1TVOc4MYcAxwxcMfQF0x1BEjUd6FNOhBI/view?usp=sharing`

## Learning Objectives Covered

1. Define what ultrasound is
2. List ways ultrasound is used today
3. Discuss the advantages of ultrasound imaging
4. Describe how ultrasound images are created

---

*Last updated: January 2026*
