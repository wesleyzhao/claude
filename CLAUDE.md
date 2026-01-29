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
- **Go to slide:** G key (prompts for slide number)
- **First slide:** Home key
- **Last slide:** End key
- **Touch:** Swipe left/right

## Testing & Debug Features
- **Jump to slide:** Add `?slide=N` to URL (e.g., `index.html?slide=6`)
- **Debug mode:** Add `?debug=1` to URL to show layout outlines
- **Combined:** `index.html?slide=3&debug=1`

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

## CSS Architecture

### Layout Tokens (CSS Variables)
All sizing is controlled via CSS variables in `:root`:
- **Content:** `--content-max-width`, `--content-min-width`
- **Photos:** `--photo-large-w`, `--photo-large-h`, `--photo-small`
- **Terminal:** `--terminal-min-width`, `--terminal-row-height`, `--terminal-font-size`
- **Spacing:** `--space-xs` through `--space-2xl`

### Slide Type Classes
Reusable base classes for common patterns:
- `.slide-type-quote` - Centered quote with attribution
- `.slide-type-photos` - Title at top, photo grid below
- `.slide-type-comparison` - Two boxes side by side
- `.slide-type-terminal` - Left steps + right terminal
- `.slide-type-text` - Centered text, flexible

## Common Modifications

### Adding/changing a slide
Edit the HTML in `index.html`. Each slide is a `<div class="slide">` with corresponding CSS. Consider using a slide type class for common patterns.

### Changing MBA students
Update slide 3's `.evidence-grid` HTML. Each person is an `.evidence-person` div with photo, name, role, and project.

### Adjusting fonts/colors
Modify the CSS custom properties in `:root` at the top of the `<style>` block.

### Adjusting sizes
Modify the layout tokens in `:root` (e.g., `--photo-large-w: 380px`).

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

### Quick testing tips
- **Test specific slide:** `index.html?slide=6` jumps directly to slide 6
- **Debug layout:** `index.html?debug=1` shows layout outlines
- **Mobile preview:** Resize browser to 480px wide or use Chrome DevTools mobile emulation
- **Keyboard shortcut:** Press G to jump to any slide by number
