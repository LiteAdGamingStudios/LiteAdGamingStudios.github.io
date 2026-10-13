# LiteAd Studios Website & AdMob Verification Guide

## 1. Overview & Live Deployment Details
LiteAd Studios official website is built and deployed as a responsive, zero-cost, zero-framework website on GitHub Pages under the verified account `LiteAdGamingStudios`.

- **Live Homepage URL:** [https://liteadgamingstudios.github.io/](https://liteadgamingstudios.github.io/)
- **Live Root app-ads.txt URL:** [https://liteadgamingstudios.github.io/app-ads.txt](https://liteadgamingstudios.github.io/app-ads.txt)
- **GitHub Repository (Public):** [https://github.com/LiteAdGamingStudios/LiteAdGamingStudios.github.io](https://github.com/LiteAdGamingStudios/LiteAdGamingStudios.github.io)
- **Local Project Path:** `C:\lite_ad_studios\Website`

---

## 2. Verification Evidence (HTTP 200 & Exact Content)

### A. Root `app-ads.txt`
- **HTTP Status:** `200 OK`
- **Content-Type:** `text/plain; charset=utf-8`
- **Exact Byte Length:** `59 bytes`
- **Exact Payload:**
  ```text
  google.com, pub-9023106647301493, DIRECT, f08c47fec0942fa0
  ```

### B. Live Homepage (`index.html`)
- **HTTP Status:** `200 OK`
- **Design Reference Implementation:** Faithfully matches the approved visual reference (`LandingPage.png`) featuring cosmic Eternal/hooded guardian background imagery, vibrant violet/blue/cyan/magenta/gold accents, and glassmorphism cards.
- **Selectable Text & Approved Copy:**
  - **Motto (EXACT):** `"Ads Should Never Get in the Way of Fun."`
  - **Tagline (EXACT):** `"Made for people, not interruptions."`
  - **Philosophy (EXACT):** `"We build games and useful apps with one simple belief: great experiences come first, ads come second."`
  - **Badge:** `"PLAY MORE • INTERRUPT LESS"`
- **Working Verified External Links:**
  - **Tic-Tac-Toe on Google Play:** [https://play.google.com/store/apps/details?id=com.litead.tictactoe](https://play.google.com/store/apps/details?id=com.litead.tictactoe)
  - **YouTube Channel:** [https://www.youtube.com/channel/UCU9h68SPyHJgZMKFbJpS2IQ](https://www.youtube.com/channel/UCU9h68SPyHJgZMKFbJpS2IQ)
  - **Contact Us Email:** `mailto:liteadgamingstudios@gmail.com`
- **Configuration File:** `site-config.json` is provided in root for easy customization of text, colors, and featured apps without framework complexity.
- **Assets Verified Live:**
  - `Assets/hero-bg.webp` (`200 OK`, `299,004 bytes`)
  - `Assets/tictactoe-icon.png` (`200 OK`, `70,310 bytes`)
  - `Assets/logo-icon.png` (`200 OK`, `4,672 bytes`)
  - `style.css` (`200 OK`, `12,360 bytes`)
  - `site-config.json` (`200 OK`, `1,179 bytes`)

---

## 3. Manual Steps for User / Operator

### Step 1: Set Developer Website in Google Play Console
Google AdMob discovers your `app-ads.txt` by reading the developer website URL listed on your Google Play store listing.
1. Log in to [Google Play Console](https://play.google.com/console).
2. Select your published app (e.g., **Tic-Tac-Toe** `com.litead.tictactoe` or **Image to PDF** `com.litead.imagetopdf`).
3. In the left navigation menu, scroll down to **Grow users** &rarr; **Store presence** &rarr; **Store settings**.
4. Under **Store listing contact details**:
   - Set **Website** to: `https://liteadgamingstudios.github.io/`
   - Set **Email address** to: `liteadgamingstudios@gmail.com`
5. Click **Save** in the bottom right corner.
6. Repeat for any other apps published under LiteAd Studios.

### Step 2: Trigger / Verify in Google AdMob Console
1. Log in to [Google AdMob](https://apps.admob.com/).
2. In the sidebar, click **Apps** &rarr; **View all apps**.
3. Select the **app-ads.txt** tab at the top.
4. Verify that Google AdMob displays your domain `liteadgamingstudios.github.io`.
5. If AdMob shows "Not found" or hasn't crawled yet:
   - Click the drop-down arrow next to the app and click **Check for updates**.
   - Note: AdMob crawler may take up to 24 hours to automatically crawl the domain after updating Google Play Console.

---

## 4. Tested Verification Commands
The following automated tests were run and passed:
```powershell
# 1. Verify app-ads.txt exact content and HTTP 200
python -c "import urllib.request; res = urllib.request.urlopen('https://liteadgamingstudios.github.io/app-ads.txt'); data = res.read().decode('utf-8'); assert res.status == 200 and data.strip() == 'google.com, pub-9023106647301493, DIRECT, f08c47fec0942fa0'; print('app-ads.txt OK')"

# 2. Verify homepage HTTP 200 and required elements
python -c "import urllib.request; res = urllib.request.urlopen('https://liteadgamingstudios.github.io/'); html = res.read().decode('utf-8'); assert 'Ads Should Never' in html and 'liteadgamingstudios@gmail.com' in html and 'com.litead.tictactoe' in html and 'UCU9h68SPyHJgZMKFbJpS2IQ' in html; print('Homepage elements OK')"
```

---

## 5. Summary of Actions
- **What was done:**
  - Inspected approved visual reference `Assets/LandingPage.png`.
  - Extracted and optimized required web assets (`hero-bg.webp`, `hero-bg.jpg`, `tictactoe-icon.png`, `logo-icon.png`). Original `LandingPage.png` was strictly preserved.
  - Implemented responsive `index.html` and `style.css` matching color palette (violet `#8b5cf6`, cyan `#38bdf8`, magenta `#ec4899`, gold `#f59e0b`, dark `#05060f`), exact copy, and accessible contrast.
  - Created root `app-ads.txt` containing the exact publisher line.
  - Created `site-config.json` for easy content and color maintenance.
  - Created public GitHub Pages repository `LiteAdGamingStudios/LiteAdGamingStudios.github.io` via GitHub CLI and pushed production code.
  - Successfully verified live deployment over HTTPS on GitHub Pages.
- **What failed:** None.
- **What remains / Next action:**
  - Operator must set developer website in Google Play Console (Step 1 above).
  - Operator triggers AdMob verification check in AdMob dashboard (Step 2 above).
- **Operational Manager Controls:** Not applicable (static public website hosted on GitHub Pages; contains no operational manager controls).
