---
layout: default
title: Troubleshooting
nav_order: 5
---

# Troubleshooting

---

## "No supported images found"

The app only processes **JPG, PNG, WebP, and TIFF** files. If your folder contains other formats (BMP, GIF, HEIC, RAW), they will be skipped.

HEIC (iPhone photos) must be converted before enhancing. Use the built-in Windows **Photos** app to export as JPG, or a free tool like [CopyTrans HEIC for Windows](https://www.copytrans.net/copytransheic/).

---

## The Enhance button stays disabled

The button is disabled until:

- An input folder with at least one supported image is selected
- An output folder is set

Both conditions must be met. Check that the image count below the input folder shows a number greater than 0.

---

## Nothing happened — the progress bar showed 0 of X

This usually means the output folder could not be created. Common causes:

- **OneDrive or network folders** — enhanced images are saved locally first. If the output path is on a synced drive with access issues, folder creation can fail silently.
- **Read-only or permission-restricted folders** — try changing the output folder to a local path like `C:\Users\YourName\Documents\Enhanced`

Check the **Logs panel** (clipboard icon in the header) for a "Failed —" entry that shows the exact error.

---

## Some images failed, others succeeded

Partial failures are shown in the **Logs panel** with the filename and error message. Common causes:

| Error | Fix |
|---|---|
| `Input file is missing` | The source file was moved or deleted while processing was running |
| `Input buffer contains unsupported image format` | The file has a supported extension but is corrupt or not a real image |
| `Unable to write to output` | Output folder became unavailable mid-run (synced drive disconnected, full disk) |

---

## The output DPI doesn't match what I selected

Verify DPI in Windows Explorer: right-click the file → **Properties** → **Details** tab → **Horizontal resolution** / **Vertical resolution**.

If the value shows 72 or 96 instead of your chosen DPI, the file format may not support embedded DPI metadata. This can happen with certain WebP files. Try outputting as JPG or PNG instead.

---

## Output images look blurry or over-sharpened

- **Blurry**: A very large scale factor (8×) on a low-resolution source will show interpolation artifacts. The Lanczos3 algorithm used is high quality, but no upscaler can invent detail that isn't there. Start with the highest-resolution source available.
- **Over-sharpened**: The app applies a light sharpening pass (sigma 1.0) after upscaling. This is intentional and calibrated for print output. It is not adjustable in the current version.

---

## The app won't start or crashes on launch

- Ensure you're running Windows 10 or later
- Try reinstalling from the Microsoft Store
- Check for a pending Windows update

If the issue persists, [open an issue](https://github.com/3thousand30/batchenhanceimage-docs/issues) with a description of what happens.

---

## Output folder won't open

The **Open Output Folder** button uses Windows Explorer. If it doesn't open, navigate manually to your configured output folder.

---

## Still stuck?

Email [hello@3thousand30.com](mailto:hello@3thousand30.com) or [open an issue](https://github.com/3thousand30/batchenhanceimage-docs/issues) on GitHub.
