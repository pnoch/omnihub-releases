# OmniHub releases

Binaries only. The application source lives in a private repository.

Each release here carries the Linux AppImage and .deb, plus the update feed
electron-updater reads (`latest-linux.yml`). Android builds live under the
rolling `android-latest` prerelease, with `android-latest.json` beside the APK.

## Website

The landing page is in `docs/` and is served by GitHub Pages:
<https://pnoch.github.io/omnihub-releases/>.

- **Turning the store on:** paste the checkout link into `CHECKOUT_URL` in
  `docs/index.html`. The Buy button appears and the "opening soon" line hides.
- **Legal pages:** `privacy.html`, `refunds.html` and `terms.html` are drafts.
  Have them reviewed before taking money; they describe what the app actually
  does today.
- **Android download:** the page reads `android-latest.json` at load time, so it
  always links to the current APK without an edit.
