# SBD API - Trimble Connect API test console

Four files, kept in the main folder of the GitHub repository `sbd-scantrack` (next to the SBD ScanTrack files):

| File | Purpose |
|---|---|
| sbd-api.html | The test console (Workspace API cards, REST request builder, test summary, reference) |
| sbd-api-manifest.json | Tells Trimble Connect the console's name, address, icon and type |
| sbd-api-icon.svg | Icon shown in the Trimble Connect left menu |
| sbd-api-README.md | This guide |

## 1. Deploy
1. Upload the four files to the main folder of the repository (Add file > Upload files > Commit).
2. Wait 1-2 minutes, then open each address in a browser. All must load (no 404):
   - https://majeedjawhar-gif.github.io/sbd-scantrack/sbd-api.html
   - https://majeedjawhar-gif.github.io/sbd-scantrack/sbd-api-manifest.json
   - https://majeedjawhar-gif.github.io/sbd-scantrack/sbd-api-icon.svg

## 2. Register in Trimble Connect (project administrator)
Project Settings > Apps & Capabilities > Add Custom, paste ONLY:

    https://majeedjawhar-gif.github.io/sbd-scantrack/sbd-api-manifest.json

## 3. Use
1. Open "SBD API" from the Trimble Connect left menu (not directly in a browser tab).
2. Workspace API tab: read the Connection checklist; each line shows a tick or a cross with the reason.
3. Click "Request access token" and approve the consent message. The console then looks up your region automatically.
4. Test summary tab: click "Run all tests". It runs every read-only request and reports pass or fail with timing.
5. REST API tab: run single requests, edit the path, or fill the "Create folder" request (asks for confirmation first).

## Troubleshooting
| Symptom | Fix |
|---|---|
| 404 for a file | The file is not in the repository's main folder or is named differently |
| "URL not found" in Trimble Connect | Paste the manifest link, not the page link; the link must load in a browser |
| Checklist cross on "Opened inside Trimble Connect" | Open the console from the Trimble Connect menu |
| "Failed to fetch" | Browser blocked the call (CORS) or wrong region: choose another Base URL |
| 401 results | No access token: click "Request access token" first |
| 403 results | The signed-in user lacks permission for that request |
