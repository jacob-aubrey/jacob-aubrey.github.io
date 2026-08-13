# Jacob D. Aubrey - personal academic website

This is a lightweight, one-page academic website designed to publish free through GitHub Pages. It contains no analytics, cookies, trackers, external fonts, or framework dependencies.

## Before changing the public site

1. Check all publication links, affiliation text, and email address one last time.
2. Never add unpublished manuscripts, raw imaging data, review correspondence, code, or third-party literature PDFs to this public repository.
3. Keep the downloadable CV privacy-reviewed before replacing it.

## Routine edits

All visible page content is in `index.html` and visual styling is in `assets/styles.css`.

- **Identity, biography, email, and profiles:** edit the hero and contact sections in `index.html`.
- **Research themes:** edit the three `research-card` articles in `index.html`.
- **Selected publications:** edit the `publication-list` section in `index.html`; use persistent DOI links where possible.
- **CV:** replace `assets/files/jacob-aubrey-cv.pdf`; the page already links to that path.
- **Portrait:** replace `assets/images/jacob-aubrey-profile.png`; keep the descriptive `alt` text.

## Updating research cards in GitHub

You can update the page entirely in your web browser. Open the [repository](https://github.com/jdaub00/jdaub00.github.io), open `index.html`, choose the pencil icon (**Edit this file**), then select **Commit changesâ€¦**. GitHub Pages normally reflects a saved change within a few minutes.

### Change a title or description

1. In `index.html`, press `Ctrl+F` (or `Cmd+F` on Mac) and search for the exact current title, for example `Photon-counting CT protocol optimization`.
2. Change the title between `<h3>` and `</h3>`, or the paragraph immediately underneath it between `<p>` and `</p>`.
3. Leave the surrounding `<article>` and `<div>` lines in place, then commit the change.

### Replace a research visual with a figure or image

The three current research visuals are intentionally styled illustrations made in CSS rather than image files. To use your own figure, diagram, or photo instead:

1. Prepare a landscape JPG or PNG (about 1600 pixels wide is ideal). Use only material you can publish publicly: no raw DICOM, patient-identifying content, confidential review material, or unapproved third-party figures.
2. In the repository, open `assets/images`, choose **Add file â†’ Upload files**, and upload it with a clear name such as `research-01-2026.jpg`.
3. In `index.html`, find the matching visual block: `ct-visual` for card 01, `spectrum-visual` for card 02, or `data-visual` for card 03. Replace that entire visual block with this template, changing the filename and plain-language alt text:

```html
<div class="research-visual">
  <img class="research-image" src="assets/images/research-01-2026.jpg" alt="Brief description of what the figure shows.">
</div>
```

4. Commit the update and check the live page. The image will crop automatically to the card shape. Once a card uses an image, later updates are as easy as uploading a new image and changing that filename.

## GitHub Pages publishing

1. Create a public repository named `jdaub00.github.io` under the `jdaub00` account.
2. Place the contents of this `site` folder at the repository root.
3. In the repository's **Settings -> Pages**, set the publishing source to **Deploy from a branch**, then select `main` and `/ (root)`.
4. Once GitHub reports a successful Pages deployment, the site URL will be `https://jdaub00.github.io/`.
5. Open that root URL on a phone before using it in a QR code. Test every email, profile, lab, publication, and CV link.

## Design notes

The page is deliberately independent of institutional branding. It uses semantic HTML, keyboard-visible focus styles, a skip link, responsive layouts, text labels instead of icon-only links, and respects reduced-motion preferences.

