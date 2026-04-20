# Assets

Drop the following files here when you have them, then update the HTML references:

## Recommended assets

| File | Used on | Size |
|---|---|---|
| `logo.svg` | Cover (Slide 1) | Any — SVG scales |
| `lasha.jpg` | Team (Slide 6) | 400×400, square |
| `cofounder.jpg` | Team (Slide 6) | 400×400, square |
| `gogorishvili.jpg` | Team (Slide 6) | 400×400, square |
| `kobalava.jpg` | Team (Slide 6) | 400×400, square |

## Optional

| File | Used on |
|---|---|
| `favicon.ico` | Browser tab icon |
| `og-image.png` | Social preview when shared (1200×630) |

## How to swap avatar initials for real photos

In `MediMind-PitchDeck.html`, find a team-avatar block like:

```html
<div class="team-avatar">LK</div>
```

Replace with:

```html
<div class="team-avatar" style="background-image: url('assets/lasha.jpg'); background-size: cover; background-position: center; color: transparent;"></div>
```
