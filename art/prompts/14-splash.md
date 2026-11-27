# 14 Splash lanterns

- Masters: `art/source/lantern-lit.svg`, `art/source/lantern-unlit.svg`,
  `art/source/lantern-lit.png`, `art/source/lantern-unlit.png`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Star lanterns for the login splash: five light up one by one as Plasma
starts. Lit and unlit share the star shape (the unlit was re-rendered from
the lit pick so the light-up transition does not pop). The splash output
images are renamed `lantern-lit/unlit.png` (were `pumpkin-*`), with the QML
and comments updated.

| Model | Settings |
|---|---|
| `recraftv4_1_utility_vector` (SVG) | 1:1, count 2, ×2 rounds |

The PNG masters are rasterized from the SVG masters (`rsvg-convert -w 1024`) with the white backdrop flood-filled to transparent: the splash build only reads raster masters (as in halloween-openSUSE), so without them it silently fell back to placeholder pumpkins.
