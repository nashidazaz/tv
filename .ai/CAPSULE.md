# Project Capsule

## Identity
মণ্ডল কেবল নেটওয়ার্ক (`nashid-tv-portal`) is a static web portal optimized for Android TV, PC, and mobile devices to download TV applications with high-speed proxy acceleration.

## Current Outcome
A finalized, responsive, visually stunning, remote D-pad friendly landing page to download TV APKs with silent background speed auto-selection and zero layout overflow.

## Current State
**COMPLETED & FINALIZED (DONE)**. The portal is published live at `https://nashidazaz.github.io/tv/` on branch `main`.

## Architecture & Key Decisions
- **Bengali Header & Modern Google TV Aesthetic**:
  - Rebranded title: **মণ্ডল কেবল নেটওয়ার্ক** using **Hind Siliguri** + **Outfit** typography.
  - Signature Google TV pure contrast focus system (focused card expands to `#ffffff` with diffused bloom glow, unselected cards remain subtle dark glass).
  - Solid dark icon badge container (`#141724` unselected, `#0f131c` selected).
  - Spacious 2-Column responsive TV grid (`max-width: 880px`) with ambient radial glow.
- **Hosted Applications (8 Total)**:
  1. **Nashid TV** (`nashidtv.apk` - 51 MB)
  2. **LS TV** (`ls-tv.apk` - 10 MB)
  3. **Sportzfy** (`Sportzfy_v28.apk` - 15 MB)
  4. **iMPlayer Official** (`implayer_411_official.apk` - 98 MB)
  5. **StreamVault IPTV** (`streamvault.apk` - 17.5 MB)
  6. **Fred TV** (`fred-tv.apk` - 92 MB)
  7. **IPTV Smarters Pro** (`https://www.iptvsmarters.com/iptv-smarters-5.0.apk` - Official APK)
  8. **XCIPTV Player** (`https://play.google.com/store/apps/details?id=com.nathnetwork.xciptv` - Google Play)
- **High-Speed GitHub Proxy Mirror Engine**:
  - 5 active, verified mirror endpoints:
    1. `https://ghfast.top/` (Fast CDN - Default)
    2. `https://gh-proxy.com/` (High-speed proxy)
    3. `https://gh-proxy.org/` (Ultra-low latency proxy)
    4. `https://ghproxy.net/` (Verified CDN proxy)
    5. `https://cf.ghproxy.cc/` (Cloudflare Edge proxy)
  - `🌐 Direct` GitHub endpoint strictly manual-only (excluded from auto-selection pool).
  - Default mirror: `ghfast.top`.
- **Sequential Background Speed Benchmark**:
  - Tests image asset (`icons/sportzfy.png`) sequentially one-by-one to avoid browser download prompt interceptions and eliminate bandwidth splitting.
  - Composite Quality Score: $\text{Score} = \text{Mbps} / \sqrt{\text{Latency (sec)}}$.
  - Auto-selects fastest proxy and updates download URLs in real-time.
- **Responsive & Non-Overflowing Utility Bar**:
  - Compact utility bar with `flex-wrap: wrap` that stays within 880px and never pushes off-screen.
- **Deterministic 2D Zonal D-Pad & Controller Navigation**:
  - Strict 2D navigation map across 4 rows of apps and the utility bar.
  - HTML5 Gamepad API loop for Xbox controllers and TV remote controls.

## Verification & Active State
- Live URL verified and deployed on GitHub Pages: `https://nashidazaz.github.io/tv/`.
- Local verification on `http://localhost:8080/index.html`.

## Retrieval Hints
Project: `nashid-tv-portal`; topics: TV-optimized, static-web, Android-TV, APK-downloads, download-accelerator, gh-proxy, speed-test; milestone: final-release; artifacts: index.html, demo.html.
