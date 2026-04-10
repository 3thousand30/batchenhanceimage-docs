---
layout: default
title: Output Formats
nav_order: 4
---

# Output Formats

BatchEnhance can output in four formats. Here's how to choose.

---

## Same as Input (default)

Keeps each image in its original format. A JPG stays JPG, a PNG stays PNG, a WebP stays WebP.

**Use this when:** You don't need to change formats — you just want to upscale and embed DPI. It's the simplest option and avoids any unnecessary re-encoding.

---

## JPG

JPEG compression — high quality (92%) with a small lossy compression artifact.

**Pros:**
- Smallest file sizes
- Universal compatibility — every printer, photo lab, and editing app accepts JPG
- Ideal for photographs (continuous-tone images without hard edges or text)

**Cons:**
- Lossy — each save introduces a small amount of compression artifact
- No transparency support

**Use JPG when:** You're sending photos to a print lab, printing at home, or uploading to a service that requires JPG. The 92% quality setting used by BatchEnhance is above the threshold where artifacts are visible in print.

---

## PNG

Lossless compression — no quality loss, larger files.

**Pros:**
- No compression artifacts — pixel-perfect output
- Supports transparency (alpha channel)
- Ideal for graphics, illustrations, logos, images with text overlays

**Cons:**
- Larger file sizes than JPG (often 3–5× bigger for photographic content)
- Not all print labs accept PNG directly

**Use PNG when:** Your images have hard edges, text, logos, or transparency — or when you want a lossless archive copy before sending to print.

---

## WebP

A modern format from Google — smaller than JPG at equivalent quality.

**Pros:**
- Excellent compression — smaller than JPG at similar quality
- Supports both lossy and lossless modes
- Supports transparency

**Cons:**
- Not universally supported — some older print software and photo labs don't accept WebP
- Not the standard format for print workflows

**Use WebP when:** You're preparing images for web use alongside print, or archiving with smaller file sizes and you know your downstream tools support it. For sending to a print lab, JPG or PNG is safer.

---

## Format comparison at a glance

| | Same as Input | JPG | PNG | WebP |
|---|---|---|---|---|
| Compression | Original | Lossy | Lossless | Lossy (or lossless) |
| Transparency | Original | No | Yes | Yes |
| File size | Original | Small | Large | Smallest |
| Print lab compatibility | Original | Universal | Good | Limited |
| Best for | General use | Photos | Graphics / logos | Web + archive |

---

## Which format do most print labs want?

Most consumer photo labs (Snapfish, Shutterfly, Walgreens Photo, etc.) prefer **JPG**. Professional fine art and giclée labs typically accept both JPG and PNG, and sometimes TIFF. If you're unsure, ask your lab — or output as JPG and you'll almost always be safe.

---

## A note on TIFF

BatchEnhance reads TIFF files as input but does not output TIFF. If your print lab requires TIFF, output as PNG (lossless, same quality) and convert using a free tool like IrfanView or GIMP.
