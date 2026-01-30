# Claude Code Quickstart Guide

## Project Purpose
A self-serve quickstart guide for setting up Claude Code, plus the original GSB presentation slides. Lives at `wesleyzhao.com/claude`. Designed for users to follow along on their own devices.

## Branch Strategy
This is the `quickstart` branch, maintained in a separate git worktree:
- **Main branch (`main`)**: Original presentation slides only
- **Quickstart branch (`quickstart`)**: Quickstart flow + presentation slides
- To pull in presentation updates: `git merge origin/main`

## Tech Stack
- Single `index.html` file (no build tools, no frameworks)
- Google Fonts (Inter)
- Inline CSS + JavaScript
- Deployable to GitHub Pages

## Slide Structure (15 slides total)

### Quickstart Slides (1-5)
1. **Entry Point** - "Start making something with Claude Code" + two paths (Quickstart / Book time)
2. **Step 1: Install** - Terminal with `curl` install command + copy button
3. **Step 2: Verify** - Type `claude` + PATH troubleshooting callout
4. **Step 3: Login** - Authentication prompt visualization
5. **Step 4: Build** - "Enter planning mode..." prompt + project ideas

### Presentation Slides (6-15)
6. **Rudy Quote** - "It was like a coming to Jesus moment."
7. **Punchline** - "Who needs a God, when you can download Claude."
8. **Emerson** - Photos + "So easy, an Emerson can do it."
9. **MBA Students** - Grid of 6 GSB classmates with projects
10. **Andreessen Quote** - "Biggest technological revolution of my life."
11. **Camus Quote** - "I rebel—therefore we exist."
12. **GSB Motto** - "Change lives. Change organizations. Change the world."
13. **How to Start** - Terminal demo with 3 steps
14. **The Couplet** - "Leave the CS kids alone..."
15. **CTA** - "Make something with Claude Code." + QR code

## URL Parameters
- `?presentation` - Jump directly to presentation (skips quickstart)
- `?slide=N` - Jump to slide N (1-indexed)
- `?debug=1` - Show layout outlines
- Combined: `?presentation&debug=1`

## Navigation Controls
- **Next:** Right arrow, Down arrow, Space, Enter, PageDown
- **Previous:** Left arrow, Up arrow, Backspace, PageUp
- **Blackout:** B key or period (.)
- **Fullscreen:** F key
- **Go to slide:** G key (prompts for slide number)
- **First slide:** Home key
- **Last slide:** End key
- **Touch:** Swipe left/right
- **Entry cards:** Click to navigate

## Key Features

### Copy-to-Clipboard Buttons
Commands can be copied with one click:
- Install command: `curl -fsSL https://claude.ai/install.sh | bash`
- PATH fix: `export PATH="$HOME/.local/bin:$PATH"`

### Callout Boxes
- **Warning (yellow)**: For troubleshooting tips (e.g., PATH issues)
- **Idea (purple)**: For suggestions and examples

### Entry Point Cards
Two clickable cards on the first slide:
1. **Quickstart** - Advances to Step 1
2. **Book time with me** - Opens Calendly in new tab

## Design System
- **Background:** #FAFAF8 (warm off-white)
- **Text:** #1B1B1B (dark charcoal)
- **Accent:** #D4725C (coral, Anthropic-inspired)
- **Warning:** #FEF9E7 bg, #F4D03F border
- **Idea:** #EDE7F6 bg, #7E57C2 border
- **Font:** Inter (Google Fonts)

## Adding New Steps

To add a new step (e.g., Step 5), use this template:

```html
<!-- QUICKSTART SLIDE N: STEP X - [TITLE] -->
<div class="slide" id="qs-stepX">
    <div class="slide-content slide-howto">
        <h2 class="howto-title">Step X: [Title]</h2>
        <div class="howto-container">
            <div class="howto-instructions">
                <p class="setup-instruction">[Main instruction]</p>
            </div>
            <div class="terminal terminal--compact">
                <!-- Terminal content -->
            </div>
        </div>
        <!-- Optional: callout-warning or callout-idea -->
        <p class="howto-footnote">
            <span class="nav-hint">[Navigation hint]</span>
        </p>
    </div>
</div>
```

Then update `QUICKSTART_SLIDES` constant in JavaScript.

## Files
- `index.html` - The entire presentation
- `CLAUDE.md` - This file
- `plan.md` - Implementation plan (in main repo)
- Image assets for presentation slides

## External Links
- **Calendly:** https://calendly.com/weszhao-stanford/30min?month=2026-01
- **Official docs:** https://code.claude.com/docs
- **Install script:** https://claude.ai/install.sh

## Testing
Open `index.html` directly in Chrome. No server needed.

### Quick testing tips
- **Test entry point:** `index.html` (default)
- **Test quickstart step 2:** `index.html?slide=3`
- **Test presentation only:** `index.html?presentation`
- **Debug layout:** `index.html?debug=1`
- **Mobile preview:** Resize browser or use DevTools

## Deployment
```bash
cd /Users/wesley/projects/claude-quickstart
git add . && git commit -m "message" && git push -u origin quickstart
```

## Merging Main Branch Updates
```bash
cd /Users/wesley/projects/claude-quickstart
git fetch origin main
git merge origin/main
# Resolve any conflicts in index.html
git commit
git push
```
