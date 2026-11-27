# 01 Character concept

- Masters: `art/source/hero.png`, `art/source/concept-sheet.png`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Sets the hero: a friendly chameleon in a Santa hat and striped scarf, the
character every later render (wallpapers, splash, launcher) must match. The
turnaround sheet is the style reference for the wallpaper drafts; the cut-out
is `ctx.hero` for the build.

| Model | Settings |
|---|---|
| `flux-2-pro` | 1:1, 1K, count 4 |

> Friendly cartoon chameleon character turnaround, leaf-green body with pale
> yellow-green chin, big round turret eye, wearing a fluffy red Santa hat
> with white trim and pom-pom and a striped knitted scarf in red and cream,
> sitting with tail curled in a spiral, three-quarter view. Soft storybook
> illustration with clean simple shapes, smooth gradients, gentle rim light.
> Centred on a solid magenta background (#FF00FF), full body visible with
> even margin. No text, no lettering, no watermark, no signature.

Flux returned a pink-purple background instead of pure magenta, so the
magenta-key cutout the prompt rules assume was not usable directly.

| | Notes |
|---|---|
| 1 | Turnaround sheet, front / both sides / back; front leg odd, sides good |
| 2 | Sitting three-quarter, big eye, hat, scarf, spiral tail, full body with margin |
| 3 | Head close-up; a second eye peeks in on the same side, reads wrong |
| 4 | Sitting side view with dorsal spikes; body good, less close to the brief |

Chosen: **2** as `art/source/hero.png`, **1** as
`art/source/concept-sheet.png`.

Post-processing: `gen-ai remove-bg -m picsart-sod-v8-2` on 2 (4 credits for
the batch including the cutout). Slight pink fringe kept on the pom-pom;
acceptable at wallpaper scale.
