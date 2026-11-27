# 12 Settings base: bauble, people, sparkle, sprig, clock

- Masters: `art/source/vectors/settings-bauble.svg`, `art/source/vectors/glyph-people.svg`,
  `art/source/vectors/glyph-sparkle.svg`, `art/source/vectors/sprig.svg`,
  `art/source/vectors/clock.svg`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Retires the last Halloween-named machinery: `settings-pumpkin` is now
`settings-bauble` (same flatten mechanics, gold bauble with cap instead of
pumpkin with stem), `glyph-ghosts` is `glyph-people`, `emblem-lantern` is
`glyph-sparkle`. A gold bauble base with cap, solid two-bust people, a
single-path sparkle, a solid fir sprig and a handless clock face (Breeze
hands overlay at build; the first clock shipped static hands that would
have ghosted).

| Model | Settings |
|---|---|
| `recraftv4_1_utility_pro_vector` (SVG) | settings-bauble, 1:1, count 2 |
| `recraftv4_1_utility_vector` (SVG) | glyphs + ornaments, 1:1, count 2, ×2 rounds |

Adversarial review (all four angles, twice): fixed the bauble flatten
missing the cap (three golds → one: cap shapes now flatten with the body),
the ornament white-strip eating the clock face (cream instead), ghost
hands (handless re-render), grey-crumb sparkle and needle-mush sprig
(re-renders), stale pumpkin wording across docs and code, and the clock
fallback comment. Filed as next phase, not solved here: star-lantern
splash masters plus the `pumpkin-lit.png` QML rename (the splash still
runs placeholder pumpkins).
