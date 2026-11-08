# Anvil: download site

This repository holds the public download page for **Anvil**, a Windows program for Oracle E-Business Suite R12.2 custom code. It is a single static page (`index.html`, with its images and video in `assets/`) served by GitHub Pages at:

https://ahmed-hamouda-code.github.io/anvil/

The program's source lives in a private repository; nothing from it is here except the screenshots, the promo video and the logo.

## Publish the site

Settings > Pages > Deploy from a branch > `main` / root. The `.nojekyll` file tells Pages to serve the files as they are.

## Publish a new release

The page's Download button always points to:

`https://github.com/ahmed-hamouda-code/anvil/releases/latest/download/Anvil-windows-x64.zip`

so the asset name must never change. For each release:

1. Create a GitHub release in this repository (tag `v<version>`) and attach the customer zip `Anvil-<version>-windows-x64.zip`.
2. Attach the **same zip a second time, renamed to `Anvil-windows-x64.zip`**. This copy is what the button downloads.
3. Mark the release **Latest**: not a draft and not a pre-release (the `latest` link ignores both).
4. Put the checksums and the release notes in the release description.
5. Update the version text in `index.html` (the logo's "v1.2", the hero's "NEW Version 1.2" pill, "Version 1.2.0" under the Download button, and the "What's new" list) and commit.

## Notes

- Pro requests, problems and ideas go through one Google Form (its first answer pre-filled by each link). The site promises a reply within 1 working day and the first 3 months of Pro free; change both places in `index.html` (How to get Pro and the Support card) if that changes.
- `assets/og-card.png` (1200x630) is the preview image shown when the link is shared; the page's Open Graph tags use absolute URLs, so keep the site address in them in step with the repository name.
