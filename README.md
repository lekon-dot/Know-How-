# Know How

Learn it. Fix it. Master it. A step-by-step guide app for IT devices, built as an installable web app (PWA).

## Features
- Search guides by device, problem or error keyword
- Learn / Fix / Discover filters and a device browser
- Step checklists with saved progress and a Resume button
- Favourites (a guide you keep open for 3 minutes saves itself)
- Repair journal, parts and tools list, and a Create-a-guide button
- Detects your device type and shows live battery, network, memory and screen info where the browser allows it
- Works offline after the first visit and can be installed to your home screen
- Free guides vs Plus guides (demo switch in Settings, no real payments)

All data is stored on the device with localStorage. There is no server or login.

## Run it on your computer
Open a terminal in this folder and run `python3 -m http.server 8000`, then visit http://localhost:8000.
(Opening index.html directly works too, but offline mode and installing need http://localhost or https.)

## Put it on GitHub and use it as an app
1. Create a free account at github.com.
2. Click **+** (top right) > **New repository**. Name it `know-how`, set it to **Public**, and click **Create repository**.
3. Upload the files:
   - **Easiest:** on the new repo page click **uploading an existing file**, drag in every file from this folder (index.html, sw.js, manifest.webmanifest, the icons, README.md), then click **Commit changes**.
   - **Or with Git:**
     ```
     git init
     git add .
     git commit -m "Know How app"
     git branch -M main
     git remote add origin https://github.com/YOUR-USERNAME/know-how.git
     git push -u origin main
     ```
4. Turn on GitHub Pages: repo **Settings** > **Pages** > under **Build and deployment** choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. Wait about a minute, then open `https://YOUR-USERNAME.github.io/know-how/`.
6. Install it:
   - **Android (Chrome):** menu > **Install app** / **Add to Home screen**
   - **iPhone/iPad (Safari):** Share > **Add to Home Screen**
   - **Windows/Mac (Chrome or Edge):** click the install icon in the address bar

To update the app later, edit index.html on GitHub (pencil icon), commit, and refresh after a minute. If you still see the old version, change `knowhow-v1` to `knowhow-v2` in sw.js so devices fetch the new files.
