# Claude Code Presentation

## Project Purpose
A single-page HTML presentation for Wesley's GSB class talk convincing MBA students to spend one hour building something with Claude Code. Designed for fullscreen presentation mode with keyboard/clicker navigation.

## Tech Stack
- Single `index.html` file (no build tools, no frameworks)
- Google Fonts (Inter)
- Inline CSS + JavaScript
- Deployable to GitHub Pages

## Live URL
https://wesleyzhao.github.io/class-presentation/

## Presentation Structure (8 slides)

1. **Rudy Quote** (dark background) - "It was like a coming to Jesus moment." — Michael Rudy
2. **Emerson** - "It's so easy, an Emerson can do it." + two photos of Emerson (age 5)
3. **MBA Students** - "It's so easy, an MBA can do it." + 6 GSB classmates with photos showing what they built
4. **Andreessen Quote** - "This is the biggest technological revolution of my life." — Marc Andreessen
5. **Why Claude Code** - "Full access to your computer" + 3 feature icons
6. **How to Start** - Terminal simulation with 3 steps (download, ask, enter)
7. **The Couplet** - "Leave the CS kids alone. You can do it on your own."
8. **CTA** - "Make something with Claude Code." + QR placeholder

## Navigation Controls
- **Next:** Right arrow, Down arrow, Space, Enter, PageDown
- **Previous:** Left arrow, Up arrow, Backspace, PageUp
- **Blackout:** B key or period (.)
- **Fullscreen:** F key
- **First slide:** Home key
- **Last slide:** End key
- **Touch:** Swipe left/right

## Fragment Animations
Some slides have click-to-reveal fragments:
- Slide 3: Each MBA student reveals one at a time (6 fragments)
- Slide 6: Each terminal step reveals with corresponding left-side step label (3 fragments)

## Design System
- **Background:** #FAFAF8 (warm off-white)
- **Text:** #1B1B1B (dark charcoal)
- **Accent:** #D4725C (coral, Anthropic-inspired)
- **Font:** Inter (Google Fonts)
- **Dark slide variant:** #1B1B1B background for Rudy quote

## Key Files
- `index.html` - The entire presentation
- `backup-old-howto-slide.html` - Backup of pre-terminal "How to Start" slide design
- `CLAUDE.md` - This file

## Image Assets
- `emerson-dimsum.jpg` - Emerson photo (left)
- `emerson-gaming.jpg` - Emerson photo (right)
- `rahul.jpeg` - Rahul (Doctor, Nurse triage tool)
- `julien.jpeg` - Julien (Healthcare Strategy, Elder companion)
- `yash.jpeg` - Yash (PE/Consulting, Valentine's Day game)
- `rodrigo.jpeg` - Rodrigo (Consulting, Relationship coach)
- `kathy.jpg` - Kathy (Fulbright Scholar, Calendar color-coder)
- `tyler.jpeg` - Tyler (Investor, Meeting time finder)

## Common Modifications

### Adding/changing a slide
Edit the HTML in `index.html`. Each slide is a `<div class="slide">` with corresponding CSS.

### Changing MBA students
Update slide 3's `.evidence-grid` HTML. Each person is an `.evidence-person` div with photo, name, role, and project.

### Adjusting fonts/colors
Modify the CSS custom properties in `:root` at the top of the `<style>` block.

### Progress bar
Automatically calculated based on current slide / total slides. Coral colored at bottom of viewport.

## Git History Checkpoints
- `8929236` - Before terminal slide redesign (simple numbered steps)
- `4d71614` - Backup saved to backup-old-howto-slide.html

## Deployment
Push to `main` branch. GitHub Pages auto-deploys from root.

```bash
git add . && git commit -m "message" && git push
```

## Testing
Open `index.html` directly in Chrome. No server needed.
