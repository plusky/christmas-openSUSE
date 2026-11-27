# 02 Wallpapers

- Masters: `art/source/wallpaper-dusk.png`, `art/source/wallpaper-night.png`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Composition rules: the chameleon in the right third; calm sky on the left
and in the centre for desktop icons; the bottom tenth quiet for the panel;
nothing important outside the central 90% of the width (the 16:10 crop).

## Dusk drafts (1K)

Same prompt for both models, hero as the character reference:

| Model | Settings | Drafts |
|---|---|---|
| `flux-2-pro` | 1K, 16:9, count 2 | A, B |
| `gemini-3.1-flash-image` | 1K, 16:9, count 2 | C, D |

> Wide cosy winter Christmas landscape illustration in soft storybook
> gouache style, for a desktop wallpaper. Dusk in a snowy forest clearing:
> a big warm full moon rising low over soft snow-covered hills, the sky
> fading from deep blue night at the top to icy blue and warm gold near the
> horizon, gentle snowflakes drifting through the air. In the right third of
> the picture, the chameleon character from the reference image, with the
> same green body, red Santa hat with white trim and striped red-and-cream
> knitted scarf, sits on a snow-covered fir branch with its tail curled in a
> spiral, beside glowing paper star lanterns and red baubles hanging from the
> branches. The left two-thirds and the centre are calm open sky and gentle
> snowfall with no detailed objects. The bottom tenth is a quiet, dark,
> simple foreground of snow and fir silhouettes. Calm, friendly, not gaudy.
> No text, no lettering, no watermark, no signature.

| | Notes |
|---|---|
| A | Black letterbox bar across the bottom; otherwise good |
| B | Good: chameleon right, moon low centre-left, calm left, quiet bottom |
| C | Moon too central-right, close to the chameleon; left calm but moon placement off |
| D | Best fit: moon rising over hills at 40–60% width, chameleon at 72–90%, calm left and centre, quiet bottom |

Adversarial review (colours, brief, platform) rejected A (bar defect,
daylight pastel wash), B (acidic yellow halo in the login label zone) and C
(gaudy oversaturated glows, moon placement) and passed D with conditions:
the half-cut horizon moon needs lifting for the login label band and the
height crops, and the keep box needs tightening (right-edge baubles are
expendable decor).

## Night drafts (1K), from dusk D

| Model | Settings | References | Drafts |
|---|---|---|---|
| `gemini-3.1-flash-image` | 1K, 16:9, count 2 | dusk D, hero | E, F |

> Edit image 1 into the very same scene at night. [Same composition
> lock as the Halloween night prompt.] Change only the time of day: deep,
> calm moonlit night, deep blue-black sky fading to dusky blue, faint stars,
> glowing cream-gold moon with halo, silvery snowfall, star lanterns glowing
> with warm golden light and warm rim light on the chameleon. Left
> two-thirds calm, bottom tenth dark and quiet. Friendly, not gaudy. No text,
> no lettering, no watermark, no signature.

| | Notes |
|---|---|
| E | Same composition, glowing lanterns; moon slightly higher than D |
| F | Closest to D, warm lantern light on the face; moon still half-cut by hills |

Chosen at draft stage: **D** (dusk) and **F** (night).

## Moon lift (1K), from dusk D

The login label band (x 0.34–0.66, y 0.75–0.83 of the login background)
sits on the moon in D/F (1.49:1), and the half-cut horizon moon turns into
a sliver in the 21:9 and 32:9 crops. Same edit prompt as the night drafts,
plus: the moon is smaller and higher, a full disc clear of the hills around
47% of the width and 40% of the height, halo not spilling onto the hills,
lower third dark and quiet.

| | Notes |
|---|---|
| G | Moon at ~42%/28%, small; composition otherwise matches D |
| H | Moon at ~42%/35%, larger disc, tighter halo; closest to the spec |

Chosen: **H** as the night base.

## 4K finals

| Model | Settings | References |
|---|---|---|
| `gemini-3.1-flash-image` | 4K (5504x3072), 16:9, count 2 | dusk D, hero |
| `gemini-3.1-flash-image` | 4K (5504x3072), 16:9, count 2 | night H, hero |

Dusk prompt: re-create image 1 exactly, only finer detail (same wording
as the Halloween 4K prompt). Night prompt: re-create image 1 (night H)
exactly, only finer detail.

Dusk finals: #1 moved the chameleon larger and the moon higher than D;
**#2** stays closest to D. Night finals: #1 has a wide halo spilling onto
the hills; **#2** has the tighter halo.

Chosen: dusk **#2** as `art/source/wallpaper-dusk.png`, night **#2** as
`art/source/wallpaper-night.png`. Both 5504x3072.

## Crops and login scrim

`art/crops.toml`: keep tightened to `[0.60, 0.18, 0.95, 0.85]` (the
right-edge baubles past 0.95 are expendable decor; the central-90% rule),
focus `[0.79, 0.50]`. `check_resolutions` passes on all 16 screens (was 98%
on 3:2, 83% on portrait).

`tools/imaging.py` `login_background()`: scrim raised to height 0.42,
strength 0.65. The night snow in the power-action band is brighter than
Halloween's dark foreground: labels went 1.49 → 3.20 (moon lift) → 4.06 →
4.5+ with the scrim tune, measured by the check, no check relaxed.
