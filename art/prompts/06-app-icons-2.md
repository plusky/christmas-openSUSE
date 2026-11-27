# 06 More app icons: mail to disk usage

- Masters: `art/source/vectors/app-mail.svg`, `art/source/vectors/app-music.svg`,
  `art/source/vectors/app-videos.svg`, `art/source/vectors/app-maps.svg`,
  `art/source/vectors/app-calculator.svg`, `art/source/vectors/app-clocks.svg`,
  `art/source/vectors/app-contacts.svg`, `art/source/vectors/app-camera.svg`,
  `art/source/vectors/app-notes.svg`, `art/source/vectors/app-diskusage.svg`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Second app batch: envelope + letter + sparkle (mail), headphones (music),
rounded TV + play (videos), folded map + pin (maps), calculator (calculator),
gold ring clock (clocks), bust card (contacts), webcam bar (camera),
sticky note (notes), pie chart (diskusage).

| Model | Settings |
|---|---|
| `recraftv4_1_utility_pro_vector` (SVG) | 1:1, 2048x2048, count 2, ×3 rounds |

Round 1 picked readable drafts; round 2 (adversarial review) demanded
bigger shapes, fewer details, navy instead of red bodies and one 4-point
sparkle accent; round 3 fixed the remainder (cream outlines on red bodies,
flattened folds, single bust, webcam distinct from the spectacle DSLR,
outlined sticky note, flat pie, new contacts without Santa hat).

Adversarial review (4 reviewers × 3 rounds): fixed red-on-ember melts
(outlines, navy bodies), cream-on-light washouts (navy page edges), missing
seasonal cues, metaphor misses (gift box, star lantern, fir photo),
bauble-as-negative-dot, webcam/spectacle split (`camera-photo` now maps to
`app-camera`; `DEVICES` dead entry removed). Declined with reasons:
16px variants (Halloween has none; two icons logged as icon-polish
follow-ups), status-hue adjacency (shape and context carry meaning),
master-format globals (the build emits clean viewBox-only SVGs; verified).
