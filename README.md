# PDF Editor — kayralrics.net

Single-file, offline, browser-based PDF editing workspace. No installation, package manager, server, CDN, or API is required. Open `index.html` in a modern browser that permits local HTML files.

## Main features

- Open a PDF or a saved `.kpdf` editable project.
- **Inspect PDF**: highlight supported original PDF text runs, embedded images, and basic vector paths. Click an outlined item (or a detected item in the Properties sidebar) to select it. Double-click detected text to make a replacement text layer.
- **Edit area**: drag over any rectangular region, including a scan, when automatic detection cannot identify an element.
- Replace selected text with editable text, replace selected regions with an uploaded image, or cover them visually.
- Adjust movable/resizable overlay layers, fonts, strokes, images, shapes, and page order.
- Undo/redo, save the editable `.kpdf` project, and export a standard PDF.
- Responsive mobile controls: use `⋯` for document commands and the gear icon for the Properties panel.
- All work is local. No code uses network requests or remote services.

## Editing behavior and limits

This version uses **visual PDF overlays**, not guaranteed native editing of every PDF object. Replacing existing text or images covers the original region and adds a new layer. The underlying original content **remains in the exported PDF**, including potentially searchable text. **Do not use Cover/Replace to redact sensitive data.**

Automatic element detection is best-effort for common PDF drawing/content streams, standard text and embedded images. It may not detect content in complex forms, unusual PDF font encodings, scanned pages, encrypted PDFs or unsupported compression/rendering structures. The manual **Edit area** tool is the visual fallback. Original PDF preview may differ for certain complex documents. Digital signatures may be invalidated upon exporting an edited copy.

Browser compatibility depends on features including Canvas, Blob URL, File API, Web Streams, and (for many source PDFs) `DecompressionStream`. Modern Chromium-based browsers work in tested flows. Other browsers, operating systems and local file restrictions have not all been independently verified.

## Quick start

1. Open `index.html` in a browser.
2. Click **Open PDF**, choose a PDF and pick **Inspect PDF** (automatic after import).
3. Select an outlined original item, or choose **Edit area** and drag a rectangle.
4. Use the **Properties** panel to replace with text/image or cover the region.
5. Click **Export PDF**. Also save a `.kpdf` project if you want to edit newly added layers later.

## Verification performed

Browser interaction tests: new and imported documents, detected text/image/vector regions, replace source text, image replacement, manual area selection, undo/redo, project save/reopen, PDF export, mobile properties panel and mobile document menu. Tested PDFs opened in an independent renderer, with no runtime JavaScript exceptions or HTTP requests in those test flows. Coverage is not a guarantee of compatibility with every PDF or browser.

© kayralrics.net
