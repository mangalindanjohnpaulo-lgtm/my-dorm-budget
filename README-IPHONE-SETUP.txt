# My Dorm Budget — iPhone offline web app

## Files
- `index.html`: your original budget tracker, with PWA metadata and service-worker registration added.
- `manifest.webmanifest`: app name, display mode, colors, and icons.
- `sw.js`: caches the app shell so it can reopen offline after its first successful online load.
- `icons/`: app icons.

## Publish with GitHub Pages
1. Create a GitHub account if needed.
2. Create a **public** repository, for example `my-dorm-budget`.
3. Upload the contents of this folder (not the folder itself) so `index.html` is at the repository root.
4. In the repository, open **Settings → Pages**.
5. Under Build and deployment, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
6. Wait for the published HTTPS URL shown in Pages.
7. On the iPhone, open that URL in Safari while online and wait for the page to finish loading once.
8. Tap **Share → Add to Home Screen**, enable **Open as Web App** if offered, then tap **Add**.
9. Open the new Home Screen icon once while online, then test offline by enabling Airplane Mode and reopening the app.

## Privacy and backups
- GitHub Pages makes the app code publicly reachable. Do not put transaction records, passwords, or other private data into the repository.
- Your transactions and budget settings are stored in browser/app storage on the device; this project does not send them to a server.
- Keep using **Export backup** and store the JSON backup somewhere safe. Use **Restore backup** if needed.
- Opening the app as a Home Screen web app may use a different storage context from a Safari tab. After installing, make a small test entry and export a backup so you know where it is saved.
- Clearing website data, removing the web app, or browser storage eviction can put local entries at risk. Export backups regularly.
- Offline support starts working only after the app shell has been loaded successfully online at least once. Service-worker updates may require opening the app online again.
