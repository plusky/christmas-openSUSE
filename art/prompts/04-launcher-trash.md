# 04 Launcher and trash

- Masters: `art/source/vectors/launcher.svg`, `art/source/vectors/trash.svg`,
  `art/source/vectors/snow.svg`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

The launcher shows the hero (Santa hat and striped scarf, as in
`art/source/hero.png`); the trash is a red wooden winter bin, snow-capped,
with snow-plus-star contents for the full state.

| Model | Settings |
|---|---|
| `recraftv4_1_utility_pro_vector` (SVG) | 1:1, 2048x2048, count 4 (launcher), count 2 (trash, snow) |

Launcher prompt: flat vector application-launcher icon, head and shoulders
of the hero chameleon (leaf-green, Santa hat, striped scarf) in three-quarter
view inside a round deep-night-blue badge with a thin star-gold ring; bold,
readable at 22 px; plain white outside. Chosen #3 of 4: full hat, eye,
scarf, shoulders. Post-processing: none by hand. `to_chameleon_green()` moves
its greens to the openSUSE chameleon green; its band was widened 70–185° to
60–190° so no yellow-green residue sits near olive and the teals unify.

Trash prompt: sturdy wooden bucket, deep red staves, dark metal bands,
golden rim, snow cap, three feet, front view. Chosen #2 of 2.

Full contents (`snow.svg`), third attempt: TALL white snow mound with a navy
outline, one gold star, nothing else. Round 1 (mound + bauble + star) read
decorated, not full, and the red bauble read as an error dot at 16px; round 2
(mound + star, no outline) lost its edge on light backgrounds; round 3 kept
mound + star and added the outline. The warm-colour selector it replaced
missed the gold star (R=193 < 200, confirmed absent from the built icon);
`snow_markup()` now takes every non-backdrop shape, which the outline
needs. `tools/vectors.py` also learned to flatten Recraft's occasional
`url(#gradient)` fills to their mean stop colour (the launcher ring) and to
fail closed with `SystemExit` on malformed masters (missing d/fill/viewBox,
unknown gradients).

Adversarial review (4 reviewers, twice where re-rendered): fixed red-on-ember
bucket melt readings (gold rim 3.22:1 and snow 5.1:1 carry the silhouette;
any red body melts on ember-red selection, as Breeze folders do on blue),
snow boundary on light (navy outline), olive-lookalike greens (band
widening), star dropped from built full (selector fix). Declined with
reasons in the pull request: hat+scarf on the launcher (the established
hero; Halloween's launcher also carried both), waste-bag/planter metaphors
(un-Christmasly), dedicated 16px launcher/trash glyphs (no 16px variants in
Halloween either; follow-up), ring re-saturation (watch only).
