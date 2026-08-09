# Project Capsule

## Identity
Nashid TV Portal (`nashid-tv-portal`) is a static web portal optimized for downloading Android TV applications.

## Current Outcome
A responsive, visually premium, and remote D-pad friendly landing page to download Nashid TV, LS TV, and Sportzfy APKs.

## Current State
Onboarding completed. The website is functional, supporting desktop, mobile, and TV screen orientations.

## Architecture & Key Decisions
- **Minimalist Google TV Design System**:
  - Pure contrast focus system (focused card expands to `#ffffff` with diffused bloom glow, unselected cards remain subtle dark glass).
  - Solid dark icon badge container (`#141724` unselected, `#0f131c` selected) to preserve 100% contrast and sharpness for white-text and transparent logos.
  - Responsive 2-column TV grid with Outfit typography and ambient radial gradients.
- **Hosted Applications (8 Total)**:
  1. **Nashid TV** (`nashidtv.apk` - 51 MB)
  2. **LS TV** (`ls-tv.apk` - 10 MB)
  3. **Sportzfy** (`Sportzfy_v28.apk` - 15 MB)
  4. **iMPlayer Official** (`implayer_411_official.apk` - 98 MB)
  5. **StreamVault IPTV** (`streamvault.apk` - 17.5 MB)
  6. **Fred TV** (`fred-tv.apk` - 92 MB)
  7. **IPTV Smarters Pro** (`https://www.iptvsmarters.com/iptv-smarters-5.0.apk` - Official APK)
  8. **XCIPTV Player** (`https://play.google.com/store/apps/details?id=com.nathnetwork.xciptv` - Google Play)
- **Authentic Logo Suite (`icons/`)**:
  - High-res launcher icons extracted directly from APKs and official domains (`ottrun.com`, Smarters APK `o-_.png`).
- **GitHub Download Accelerator Engine**:
  - 4 verified mirror endpoints (`ghfast.top`, `gh-proxy.com`, `gh-proxy.org`, `gh.ddlc.top`) + Direct GitHub fallback.
  - Default mirror: `ghfast.top` (bypasses ISP throttling).
  - Selected mirror is stored in `localStorage` for return sessions.
- **Deterministic 2D Zonal D-Pad & Controller Navigation**:
  - Strict 2D navigation map across 4 rows and utility bar.
  - HTML5 Gamepad API loop for Xbox controllers and TV remote controls.
  - Dynamic device detection badge ("TV Remote Active", "Xbox Controller Active", etc.).

## Verification & Active State
- Verified all 8 cards, link rewrites, and D-pad transitions on local test server and GitHub Pages.
- Published directly as the primary homepage `index.html`.

## Active Constraints
- 100% remote D-pad navigation support.
- Zero extra JS frameworks unless requested.
- Fast performance and optimized SEO tags.
- Do NOT use the browser subagent or browser-based tools/testing.

## Immediate Next Action
Verify high-speed download performance on Android TV and mobile devices.

## Retrieval Hints
Project: `nashid-tv-portal`; topics: TV-optimized, static-web, Android-TV, APK-downloads, download-accelerator, gh-proxy; milestone: download-speed-upgrade; artifacts: index.html, index.css.
