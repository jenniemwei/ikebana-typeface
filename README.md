# Ikebana font tester

A minimal, standalone preview for the Ikebana typeface.

- Type text and preview it using the included font. Uppercase input displays as lowercase.
- Adjust text size and color.
- Click between letters to select a pair, then adjust its kerning with the slider.
- Positive kerning extends the bottom pot with a matching rectangle.
- Use the left and right arrow keys while the preview is focused to select pairs, or Reset to clear the selected pair's spacing.

## Local preview

From the repository directory, run:

```sh
python3 -m http.server 4173
```

Open http://localhost:4173 in your browser. No build step or package installation is needed.

## Files

- `index.html` contains the interface, styles, and interaction logic.
- `assets/` contains the current OpenType font.

The pot-extension bounds in `index.html` are measured from the included font. If the font outlines change, update `potBounds`, the units-per-em value, and the ascender used by `positionPotExtensions` to match.

The site can be hosted by any static web server. Text and spacing edits stay in the current browser session and are not saved after a reload.
