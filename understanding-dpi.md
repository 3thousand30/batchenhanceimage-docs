---
layout: default
title: Understanding DPI
nav_order: 3
---

# Understanding DPI

DPI (dots per inch) is the most misunderstood setting in image preparation for print. This page explains what it actually means and how to choose the right value.

---

## What DPI really means

DPI tells a printer how many pixels to fit into each inch of paper. It is a relationship between pixel count and physical size — not a measure of quality on its own.

The formula is simple:

```
print size (inches) = pixel dimension ÷ DPI
```

So a 3000-pixel-wide image printed at 300 DPI produces a **10-inch wide print**.
The same 3000-pixel image at 150 DPI produces a **20-inch wide print** — at lower density.

**The quality of a print depends on how many pixels you have, not just the DPI number.** Changing DPI metadata without upscaling the image does not add detail — it just changes what size the printer renders it at.

---

## DPI on screen vs. DPI for print

Your screen typically shows images at 72–96 PPI (pixels per inch). This is why images look large on screen but print small at 300 DPI — the printer is packing those same pixels in much more tightly.

When you "enhance" an image with BatchEnhance, the upscaling step **creates new pixels** via Lanczos3 resampling. More pixels at the target DPI = more inches of print coverage at full quality.

---

## Worked examples

### Starting image: 1200 × 900 px

| Scale | Output size | At 150 DPI | At 300 DPI | At 600 DPI |
|---|---|---|---|---|
| 1× (DPI only) | 1200 × 900 px | 8 × 6 in | 4 × 3 in | 2 × 1.5 in |
| 2× | 2400 × 1800 px | 16 × 12 in | 8 × 6 in | 4 × 3 in |
| 4× | 4800 × 3600 px | 32 × 24 in | 16 × 12 in | 8 × 6 in |
| 8× | 9600 × 7200 px | 64 × 48 in | 32 × 24 in | 16 × 12 in |

---

## Which DPI should I choose?

### 150 DPI — Large format and posters

Use 150 DPI for:
- Posters and banners
- Large-format prints (24 inches and above)
- Prints viewed from more than an arm's length away

At viewing distances of several feet, 150 DPI is indistinguishable from 300 DPI. Using 150 DPI allows you to cover twice the physical area with the same number of pixels.

### 300 DPI — Standard print quality

Use 300 DPI for:
- Photo prints (6×4, 8×10, A4, A3)
- Photo lab uploads
- Desktop inkjet prints
- Most general printing

300 DPI is the industry standard for photographic print quality. Most photo labs require it. This is the right choice when you are unsure.

### 600 DPI — Fine art and archival

Use 600 DPI for:
- Fine art giclée prints
- Archival reproduction work
- Prints with fine line detail (illustrations, maps, text)
- When printing to a high-end inkjet capable of 1200+ DPI nozzle resolution

Note: 600 DPI requires 4× as many pixels as 300 DPI to cover the same physical area. Combine with a high scale factor (4× or 8×) for large fine-art output.

---

## The 1× (DPI only) option

Sometimes your images are already high enough resolution — they just have the wrong DPI metadata embedded (often 72 or 96 from a camera or phone).

In this case, select **1× (DPI only)**. The app will:
- Leave the pixel dimensions unchanged
- Apply a light sharpening pass
- Embed the correct DPI value in the file metadata

The image file will be the same number of pixels but the printer will now know the intended print density.

---

## How to verify DPI after enhancing

1. Right-click the output file in Windows Explorer
2. Select **Properties**
3. Click the **Details** tab
4. Look for **Horizontal resolution** and **Vertical resolution**

Both should show your chosen DPI value (150, 300, or 600).

---

## A note on laser printers and photo printing

Laser printers print using a halftone screen — a grid of tiny dots that simulate continuous tone. Most laser photo printers use a 150–200 line-per-inch halftone screen. Sending a 600 DPI source file to a laser printer provides no visible improvement over 300 DPI, because the halftone bottleneck sits between the source and the paper.

For laser-printed photos, **300 DPI is the sweet spot** — enough detail to saturate the halftone, without unnecessarily large files.

Inkjet and giclée printers work differently (they spray continuous ink), so higher source DPI can genuinely improve output quality up to the printer's native resolution.
