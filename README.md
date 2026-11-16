# OmniHub releases

Binaries only. The application source lives in a private repository.

Each release here carries the Linux AppImage and .deb, plus the update feed
electron-updater reads (`latest-linux.yml`). Android builds live under the
rolling `android-latest` prerelease, with `android-latest.json` beside the APK.

## Website

The landing page is in `docs/` and is served by GitHub Pages at
<https://omnihub.siamcreations.app/> (custom domain) and
<https://pnoch.github.io/omnihub-releases/> (project URL until the CNAME is
live).

- **Custom domain:** `docs/CNAME` must contain `omnihub.siamcreations.app` and
  DNS must point the subdomain at `pnoch.github.io` (CNAME, replacing any A
  record). Set the domain in the Pages settings once DNS resolves, then enforce
  HTTPS. Do not add `CNAME` before DNS is switched: Pages redirects the project
  URL to the custom domain, so the site would be unreachable at both.
- **App links:** `docs/.well-known/assetlinks.json` associates
  `app.siamcreations.omnihub` with the release signing certificate. Android
  release builds set `EXPO_PUBLIC_SHARE_DOMAIN=omnihub.siamcreations.app`, and
  the release script refuses to publish if the file is not reachable.
  `docs/404.html` is the fallback for a shared `/course/...` link when the app
  is not installed.
- **Turning the store on:** paste the two Paddle checkout links into
  `CHECKOUT_URL_STANDARD` and `CHECKOUT_URL_PRO` in `docs/index.html`. Each
  plan button appears independently, and the "opening soon" line hides once
  either link is set.
- **Support:** the footer and legal pages point at
  `support@siamcreations.app`; the mailbox is live.
- **Legal pages:** `privacy.html`, `refunds.html` and `terms.html` are drafts.
  Have them reviewed before taking money; they describe what the app actually
  does today.
- **Android download:** the page reads `android-latest.json` at load time, so it
  always links to the current APK without an edit.
