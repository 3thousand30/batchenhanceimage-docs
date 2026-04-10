---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started

This guide walks you through enhancing your first batch of images for print.

---

## 1. Install the app

Download and install **BatchEnhance Image for printing** from the Microsoft Store. Once installed, launch it from the Start menu.

---

## 2. Select your input folder

Click **Browse** next to **Input Folder** and pick a folder containing your images.

Supported formats: **JPG, PNG, WebP, TIFF**

The app immediately counts how many supported images it found and automatically sets the output folder to an `Enhanced` subfolder inside your input folder. You can change the output folder by clicking its **Browse** button.

---

## 3. Choose your scale

The **Scale** setting controls how much the pixel dimensions are multiplied.

| Option | What it does |
|---|---|
| **1× (DPI only)** | No upscaling — just embeds the DPI metadata and applies sharpening |
| **2×** | Doubles width and height (4× total pixel count) |
| **3×** | Triples width and height |
| **4×** | 4× upscale (two 2× passes for best quality) |
| **6×** | 6× upscale (2× then 3× passes) |
| **8×** | 8× upscale (three 2× passes) |

**Multi-pass upscaling**: Large scale factors (4×, 6×, 8×) are done in multiple smaller passes rather than one big jump. This produces smoother, sharper results than a single-step upscale.

**Which scale should I use?** Start with the pixel dimensions of your source image and divide by your target DPI to see what print size you'll get. See [Understanding DPI](understanding-dpi) for the full calculation.

---

## 4. Choose your DPI

The **DPI** setting (dots per inch) controls how densely the pixels are packed when the image is printed. Higher DPI means finer detail — but also requires more pixels to cover the same physical size.

| DPI | Best for |
|---|---|
| **150** | Large format prints, posters, banners — viewed from a distance |
| **300** | Standard print quality — photo labs, inkjet printers, most use cases |
| **600** | Fine art, archival prints, ultra-sharp detail |

See [Understanding DPI](understanding-dpi) for a deeper explanation and worked examples.

---

## 5. Choose your output format

| Format | Best for |
|---|---|
| **Same as Input** | Simplest — keeps the original format, no conversion |
| **JPG** | Photographs going to print — smallest files |
| **PNG** | Graphics, logos, images with text or transparency |
| **WebP** | Modern web use — not ideal for print labs |

See [Output Formats](output-formats) for full details on quality tradeoffs.

---

## 6. Enhance

Click **Enhance Images**. The button shows the exact count of images that will be processed.

While running:
- A progress bar shows overall completion
- The current filename scrolls through below the bar
- A spinner indicates active processing

When done, a **Open Output Folder** button appears. Click it to see the results in Windows Explorer.

---

## 7. Check the output

Enhanced files are named with the scale and DPI embedded, for example:

```
photo_4x_300dpi.jpg
```

This makes it easy to keep multiple versions side by side.

To verify the DPI was correctly embedded: right-click the output file in Windows Explorer → **Properties** → **Details** tab → look for **Horizontal resolution** and **Vertical resolution**.

---

## Tips

- **Skip existing files** is on by default — you can re-run with different settings without reprocessing everything. Turn it off if you want to overwrite previous outputs.
- Check the **Logs** panel (clipboard icon in the header) for error details if any files failed.
- Use the **1× (DPI only)** option when your images are already high enough resolution and you just need to embed the correct print DPI.
