# Release checklist — pending metadata updates

App Store Connect metadata URLs (Support URL, Privacy Policy URL) can only be edited
when submitting a **new app version**. These updates are deferred to the next release
of each app. Nothing is broken in the meantime:
- WindRunner's old `/privacy/` path still works — it 301/redirects to `/windrunner/privacy/`.
- Old `wildboar-studio.github.io/...` URLs auto-redirect to the custom domain.

## Do on the next WindRunner version
- [ ] Support URL → `https://wildboarstudios.io/support/`
- [ ] Privacy Policy URL → `https://wildboarstudios.io/windrunner/privacy/`
- [ ] Marketing URL → `https://wildboarstudios.io`  (this is what AdMob's crawler reads
      to verify app-ads.txt — there is NO developer-URL field inside AdMob itself)

## Do on the next Selah version
- [ ] Support URL → `https://wildboarstudios.io/support/`
- [ ] Privacy Policy URL → `https://wildboarstudios.io/selah/privacy/`
- [ ] Marketing URL → `https://wildboarstudios.io`

## Before Flip Fall / YapIt first release
- [ ] Finalize the draft privacy policies (`/flipfall/privacy/`, `/yapit/privacy/`)
      — remove the "Draft — pending release" note once reviewed.
- [ ] Flip Fall: create an app icon (AppIcon.appiconset is currently empty) and swap
      the placeholder on the website's app card.
- [ ] Set Support URL `https://wildboarstudios.io/support/` and the matching Privacy
      URL for each new app.
- [ ] Add the new app's App Store link to the website app card (replace "Coming soon").

## Other (whenever convenient)
- [ ] AdMob: after the marketing URLs above are live on a new version, open AdMob →
      Apps → View all apps → app-ads.txt → expand the app → "Check for updates" to
      force a re-crawl (it verifies against the store's marketing URL; no URL field
      exists inside AdMob).
- [ ] Google Search Console: add property + submit `sitemap.xml`.
- [ ] Optionally tighten DMARC from `p=none` once reports confirm mail passes.
