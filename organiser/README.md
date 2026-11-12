# Podcasts Library Organiser

A standalone, client-side editor for the **Podcasts** Android app.

**Site address (after enabling GitHub Pages):** https://the-bollard.github.io/podcast-library-updates/organiser/

## Enable hosting once

1. Open the public repository's **Settings → Pages**: https://github.com/the-bollard/podcast-library-updates/settings/pages
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select **main**, folder **/(root)** and **Save**.

GitHub Pages can then serve the website from the existing `organiser/index.html`. The site contains no private podcast data. Please don't commit your exported JSON files to this public repository.

## One-time editing workflow

1. Update the Android app to **Podcasts 0.5.7** or newer.
2. In **Settings**, tap **Export library for website** to create `podcasts-organiser.json`.
3. Open the website and choose that file. You can select multiple episodes, search, rename arcs, create new arcs, bulk-move or add assignments, remove wrong assignments and undo edits.
4. Click **Download changes** to save the edited JSON.
5. In the Android app, choose **Settings → Import edited organisation** and pick the downloaded file.

The JSON contains only subscription IDs and titles, hashed episode IDs, episode titles, publish dates, collection names and placements. It does **not** include private subscription addresses, Patreon tokens, audio URLs, downloads or listening progress. File processing happens in your own browser. No external libraries, accounts, tracking, upload or API calls are used by the website.

The app applies these changes transactionally. Once a podcast has been manually edited, automatic arc matching is paused for that podcast so your changes aren't undone. Newly released episodes still appear under **All episodes** until assigned.

You can also download `organiser/index.html` from GitHub and open it locally without any hosting.
