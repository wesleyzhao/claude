# Claude Code Quickstart

Self-serve quickstart guide for setting up Claude Code, plus presentation slides.

**Live URL:** https://wesleyzhao.github.io/claude/

## Slide Structure

### Quickstart (2 slides)
1. **Entry** - Two paths: "Quickstart" or "Book time with me"
2. **Steps** - Single terminal that builds up:
   - Click 1: Install output appears
   - Click 2: Login prompt appears
   - Click 3: Build prompt appears

### Presentation (10 slides)
3-12. Original presentation slides (Rudy quote through CTA)

## URL Parameters
- `?presentation` - Skip quickstart, go to presentation
- `?slide=N` - Jump to slide N (1-indexed)
- `?debug=1` - Show layout outlines

## Navigation
- **Next:** Right arrow, Space, Enter, Click
- **Previous:** Left arrow, Backspace
- **Fullscreen:** F key
- **Blackout:** B key

## Merging Updates from Main Presentation

This repo can pull updates from the original presentation:

```bash
# Add the original repo as a remote (one time)
git remote add presentation https://github.com/wesleyzhao/class-presentation.git

# Fetch and merge updates
git fetch presentation main
git merge presentation/main

# Resolve any conflicts in index.html, then commit
```

The quickstart slides are at the beginning of index.html, presentation slides follow.

## Files
- `index.html` - Everything (slides, CSS, JS)
- `CLAUDE.md` - This file
- `*.jpg/*.jpeg` - Image assets

## External Links
- Calendly: https://calendly.com/weszhao-stanford/30min
- Docs: https://code.claude.com/docs

## Deployment
Push to `main` branch. GitHub Pages auto-deploys.

```bash
git push origin main
```
