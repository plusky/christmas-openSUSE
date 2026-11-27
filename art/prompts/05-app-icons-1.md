# 05 App icons, batch 1

- Masters: `art/source/vectors/app-browser.svg`, `art/source/vectors/app-konsole.svg`,
  `art/source/vectors/app-settings.svg`, `art/source/vectors/app-kate.svg`,
  `art/source/vectors/app-spectacle.svg`, `art/source/vectors/app-ark.svg`,
  `art/source/vectors/app-gwenview.svg`, `art/source/vectors/app-help.svg`,
  `art/source/vectors/app-sysmon.svg`, `art/source/vectors/app-discover.svg`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

The ten most visible apps, generated with the folder as style reference
(image weight 80): navy globe + star (browser), outlined terminal (konsole),
gear + chunky snowflake (settings), page + outlined pencil (kate), plain
navy camera (spectacle), flat tan archive box (ark), loupe + single fir
(gwenview), lifebuoy + ? (help), bar gauge (sysmon), navy bag + star
(discover).

| Model | Settings |
|---|---|
| `recraftv4_1_utility_pro_vector` (SVG) | 1:1, 2048x2048, count 2, ×2 rounds |

Round 1 failed review on detail density (micro continents, dot fields,
ribbon tails, sprig berries) and red bodies melting into the ember
selection. Round 2 was briefed from the reviewers' fixes: 2–4 large flat
shapes, no tiny details, navy instead of red bodies, exactly one seasonal
accent or none.

Adversarial review (4 reviewers × 2 rounds): fixed red-on-ember bodies
(discover/help re-rendered navy), cream-on-light analysis (rejected:
cream details sit on dark icon bodies, not on the tile), near-white
escape in `normalise()` (`#FFFFFE` shipped raw while `#FEFDFD` became
cream; fixed with a chroma gate, verified both ways), the `DEVICES`
camera-photo duplication (noted for the devices batch), short-name
breadth (noted, neutralised by kde/ links as designed).

Declined with reasons, all measured against the built preview or
Halloween precedent: 16px folder/app variants (Halloween has none;
two icons listed as icon-polish follow-ups), cream holds around every
red (Breeze-level precedent: identifiability, not zero melt), blue bodies
clamped to plum_icon (the folder back itself is unclamped by design),
candle/cranberry-adjacent decoration (shape and context carry meaning,
not hue alone; Christmas gold is candle-adjacent by design), platform
master-format globals (the build already strips C2PA/backdrops and emits
fresh viewBox-only SVGs — verified in the built files).
