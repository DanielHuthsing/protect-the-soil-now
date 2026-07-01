# Images

This folder is where the site's hero photo goes. **Right now no photo is included** —
the hero section (the large banner at the top of the page) shows a terracotta gradient
by default. The site works perfectly without a photo; adding one is optional.

## How to make a photo appear

1. Choose a photo you have the right to use (you own it, or it's properly licensed).
2. Save it as a **JPG** named **exactly** `hero.jpg` (all lowercase).
3. Put it in this folder — `assets/images/`.

That's the whole process — **no code to change.** The site looks for
`assets/images/hero.jpg` and uses it automatically the next time the page loads. To go
back to the gradient, just delete the file again.

## What size and type of image

| | Recommendation |
|---|---|
| **Format** | JPG, named exactly `hero.jpg` |
| **Orientation** | Landscape (wider than tall) |
| **Dimensions** | At least **2000 px wide**; **≈ 2400 × 1600 px** is ideal so it stays sharp on large monitors |
| **File size** | Keep under ~**500 KB** so the page loads fast — compress at [TinyPNG](https://tinypng.com) or [Squoosh](https://squoosh.app) |
| **Composition** | The headline and button sit over the **center** of the image, so keep important detail away from the middle |

**You do not need to darken the photo yourself.** The site automatically lays a dark
terracotta overlay over it so the white headline stays readable on any image.

## A photo somewhere else on the site?

Only the hero currently supports a photo. To place an image elsewhere (between
sections, inside a card, etc.), an `<img>` tag has to be added to `index.html` — see
[`../docs/EDITING.md`](../docs/EDITING.md) or ask whoever maintains the site.
