# Vivek Kumar Yadav

Research website source files.

The homepage presents the academic biography, publications, talks and contact details.
The current CV is at `materials/vivek-kumar-yadav-cv.pdf`; replace this file to update it without changing links.

The small homepage footer badge uses Hits (https://hits.sh) to count page views, not unique visitors. It starts when the badge is first loaded and does not reconstruct historical traffic. This external image requires no credentials or JavaScript; blocking the service does not affect site content.

Preview locally with `python3 -m http.server 8000` and open http://localhost:8000.

## Publishing and checks

GitHub Pages publishes the root of `main`. Keep the existing `outputs/` and
`materials/` URLs stable. Commit explicit changed paths, push to `main`, and
confirm the `pages-build-deployment` workflow succeeds before checking the live site.

When changing `styles.css`, update its `?v=` value in all five HTML pages to the
same new version so returning visitors receive the new stylesheet.
Before publishing, check local links and fragments, Tab/Enter skip navigation,
mobile layout, and `git diff --check`. Every page should retain its skip link and
focusable main-content target. Links that open a new tab explicitly use `noopener`.

## CV and image maintenance

Replace `materials/vivek-kumar-yadav-cv.pdf` with the latest approved public CV.
The homepage link should remain Email, Google Scholar, ORCID, GitHub, CV; the top
navigation intentionally omits CV. Check the live PDF after deployment.

Original PNGs remain at the repository root as source assets. The homepage serves
optimized WebP derivatives in `assets/images/`: portrait at 540 px wide and paper
figures at 438 px wide, quality 90. Regenerate them when replacing source images
and compare them at their displayed size before publishing. The portrait remains
180 px wide on desktop and 112 px on mobile; encoding changes must not change this.

The Hits badge is an external image. If it stops loading, check the service and
badge URL; it is not backed by GitHub repository traffic statistics. Do not add
credentials or invent/reset counts as part of routine maintenance.

`.gitignore` covers incidental OS/editor artifacts only. Keep PDFs, figures and
the PICO text script tracked. No build system or runtime dependencies are needed.
