# SpeakUp Updates Site — CCB Vantage Institute

This folder is the complete update server for the SpeakUp app. Host it at:

**https://kingofpakistan11223344.github.io/speakup-updates**

## One-time setup (5 minutes, only you can do this)

1. Sign in to your GitHub account (the one for husnainmunawar62@gmail.com) at github.com.
2. Create a new **public** repository named exactly **speakup-updates**.
3. Upload everything in this folder to the repository (drag & drop on github.com works).
4. In the repo: Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
5. Wait ~2 minutes, then open https://kingofpakistan11223344.github.io/speakup-updates/version.json — if you see the JSON, updates are live.

> If you use a different GitHub username, tell Claude the URL so the app
> constant (`kUpdateBaseUrl` in `update_service.dart`) is updated before building.

## Publishing updates afterwards

- **New app version:** upload the new APK here, edit `version.json`
  (raise `versionCode`, set `versionName`, point `apkUrl` at the new file).
  Phones show the update banner automatically.
- **Changed content:** upload changed bank JSON files into `content/`,
  list them in `content_manifest.json`, and raise `contentVersion`.
  Phones download them silently — no install.
- **Theme change:** edit `theme.json`. Applied on next app start.

Full format reference: `docs/UPDATES_HOSTING.md` in the project.
