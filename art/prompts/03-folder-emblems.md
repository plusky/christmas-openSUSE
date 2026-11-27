# 03 Folder and folder emblems

- Masters: `art/source/vectors/folder.svg`, `art/source/vectors/emblem-scroll.svg`,
  `art/source/vectors/emblem-bauble.svg`, `art/source/vectors/emblem-note.svg`,
  `art/source/vectors/emblem-picture.svg`, `art/source/vectors/emblem-reel.svg`,
  `art/source/vectors/emblem-stencil.svg`, `art/source/vectors/emblem-share.svg`,
  `art/source/vectors/emblem-cottage.svg`, `art/source/vectors/emblem-monitor.svg`
- Copyright: 2026 Martin Pluskal <martin@pluskal.org>

Sets the icon family: every folder is the master folder's body (deep
frost-blue back, star-gold front) plus one navy emblem in place of its
snowflake. `tools/vectors.py` holds every colour master to the palette at
build time except the folder body, which ships the master's hues (as does
Halloween's); folder emblems are one-colour glyphs recoloured to the
scheme's night navy, white details to the pocket.

## Master folder icon

The style reference for the whole set.

| Model | Settings |
|---|---|
| `recraftv4_1_utility_pro_vector` (SVG) | 1:1, count 4, ×3 rounds |

> A single file-manager folder icon for a cosy winter Christmas desktop icon
> theme, flat vector design. The folder has a deep frost-blue back panel with
> a rounded tab and a VIVID saturated golden-yellow front pocket, rich
> marigold orange-gold like a Christmas bauble, bold and saturated, never
> pale, beige or pastel, with a slightly lighter gold top edge. Centred on
> the front pocket is a small deep-navy snowflake emblem. Flat shapes with at
> most two subtle tonal steps per colour, a bold, clear silhouette that stays
> readable at 32 pixels, no outlines, no gradients, no texture, no drop
> shadow, no perspective: straight front view. The folder fills the square
> canvas with an even margin of about one eighth on every side, on a plain
> white background. No text, no lettering, no watermark, no signature.

Round 1 asked for a red pocket: vivid red, but the pocket melted into the
ember selection (1.13:1). Round 2 asked for gold and came back pale
parchment. Round 3 added "VIVID ... never pale, beige or pastel" and landed
#FCC220: navy-on-pocket 10.35:1, pocket-on-ember 3.4:1, pocket near the
accent pumpkin. Chosen: round 3 **#3**.

Built pocket #FCC220 vs accent pumpkin #E9A820 is 1.28:1 (same vivid gold
family; Recraft never hits exact hexes, as with Halloween's masters).

Post-processing: none by hand. `tools/vectors.py` changes in this batch:
`split_folder()` accepts a dark emblem on a light pocket (it crashed with
`SystemExit` on the navy flake first — break-first evidence kept in the
commit); folder emblem ink cream → palette night navy; `folder-open`
emitted paperless with a separate papered `folder-drag-accept`; `ALIASES`
gains `folder-image`.

## Emblems

| Model | Settings |
|---|---|
| `recraftv4_1_utility_vector` (SVG), no reference | 1:1, count 2, ×10 |

Every prompt is "A simple bold glyph icon of …, " followed by: Solid black
flat silhouette on a plain white background, with only a few small white
negative-space cut-outs for detail. Single colour, no outlines, no
gradients, no shading, chunky shapes that stay readable at 16 pixels,
centred and filling most of the square. No text, no lettering, no watermark,
no signature.

| Icon | Subject | Chosen |
|---|---|---|
| folder-documents | a rolled parchment scroll, slightly unrolled | v2 #1 (single fat scroll; v1 double scroll died at 16px) |
| folder-download | a round Christmas bauble with a small cap, a short bold down arrow below it | v1 #2 (arrow separate; #1 merged into the bauble) |
| folder-music | a musical eighth note (plain; the star was tried and merged with the stem at 16px) | v2 #2 |
| folder-pictures | a landscape photo: mountains under a starry sun in a rounded-square frame (first round's fir-in-frame read as a tree, not a photo) | v2 #1 (framed; #2 had no frame) |
| folder-videos | an old cinema film reel | v1 #2 (clean symmetric) |
| folder-templates | a document page with folded corner and lines, star cut out (first round's gift box misled: present ≠ template) | v2 #1 (black page; #2 inverted) |
| folder-publicshare | two overlapping solid person busts, no faces (first round's star lantern read as favourites; eyed busts read kitsch) | v2 #2, eyeless round |
| user-home | a snowy cottage: pitched roof, chimney, round window | v1 #1 (simpler window) |
| user-desktop | a monitor with a blank screen (first round's snowflake-on-screen died at 16px) | v2 #2 (bolder stand) |

Post-processing: none by hand. Old `emblem-gift.svg` and `emblem-star.svg`
removed (superseded; unlisted masters fail the provenance check).

## Adversarial review

Four reviewers (icons, colours, brief, platform) on the drafts, then again
on the re-renders. Rejected: red pocket (selection melt), gift box
(misleading), star lantern (reads favourites), framed fir (reads tree),
snowflake monitor and star note (die at 16px), fussy scroll, eyed busts
(kitsch); fixed as above. Declined with reasons in the pull request:
snowflake-default for 8 unmapped `folder-*` names (staged masters, as
Halloween), cream symbolic hardcode and normalise bands (Halloween
precedent), 16px folder variants (Halloween has none; two icons listed as
icon-polish follow-ups), trash/settings glyphs (their own phases).
