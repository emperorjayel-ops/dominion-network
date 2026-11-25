# CLAUDE.md — Dominion Network

Created by OPS' Broker

## Project

**Dominion Network** — the media and telecommunications network of OMNI-PRESENT SOLUTIONS, INC, built in partnership with the **CEO Network (Bahamas)** and **Hon. Dr. Deborah Bartlett**. Stated reach goal: 134 countries including the U.S. (a launch goal — not live reach; never present it as current reach). Owner: Honorable Jay Ladon Dickey Sr. EL.

Front domain: **dominionnetwork.metaverse**. Google Play package: `com.omnipresentsolutions.dominionnetwork`.

## Tech in this folder

- `index.html` — the entire app: one self-contained HTML file (HTML/CSS/JavaScript inline, no build step, no framework, no server). Edit it directly.
- `privacy.html` — the hosted privacy policy page for the Play Store listing.
- `verification/` — verification screenshots from build checks. Do not ship these as app content.
- `README.md` — project note. Keep it accurate when behavior changes.

There is no backend. Accounts, uploads, approvals, and theater rooms are session-only demos in the browser unless this file says otherwise.

## What the app does (current build)

- Open-source media/telecom feature set: VoIP calling, video chat, voice chat, texting, large-file sharing, screen sharing.
- **Member media uploads** (movies/videos/music) with **administrator approval required before anything appears** — uploads sit in a pending queue; only approved media reaches the library. Large-file handling follows the open-source chunked/resumable pattern (tus/Uppy-style, FFmpeg processing).
- **Watch Together virtual theater:** members in different places watch the same administrator-approved movie in sync and communicate (room chat).
- PlayStation / Xbox game connections are shown as **"Coming Soon"** — neither console account is enrolled and nothing there is live. Keep it that way until enrollment is real and verified.

## Standing rules (apply to every change)

- **Cross-platform, no exceptions:** must work on the owner's Samsung Galaxy S9 (SM-G960U), iPhones (Safari/WebKit), all other phones, and laptops/desktops. Responsive at every width.
- **Adjust to the device:** runtime feature detection and progressive enhancement — WebGL2 → WebGL1 → CSS fallback; camera/microphone features fall back gracefully; auto quality scaling; honor reduced-motion and low-power signals.
- **Lane separation:** Dominion is the media/network lane. No Excalibur train material in here.
- **One-picture rule:** visuals blend into one seamless picture — matched lighting, perspective, color, shadows. Logos merge into the design (the Dominion emblem is blended with feathered edges and the deck's navy/gold glow) with no visible outlines or background-box edges.
- **Cross-app sidebar:** every app in this family (Excalibur Line, FinSwap, HIIYAH, Dominion Network, PMI God's Eye) carries a sidebar linking to all the others. Keep it intact and uniform.
- **Credit:** the line "Created by OPS' Broker" / "Shared by OPS' Broker" stays in the files. Do not remove it, do not add any other creator name.
- **Honesty:** never present a demo, session-only feature, upload, or theater room as live server-backed functionality. The approval gate is real product logic — keep it: nothing member-uploaded appears publicly without administrator approval.

## ⭐ REAL PAYMENTS — scoped to paid member content

Where Dominion charges money — **paid member content, premium media, and paid theater events** — payments must be **real transactions on the real Bitcoin blockchain**, not simulation:

1. Build on the open-source Bitcoin stack: **Bitcoin Core + Counterparty** (the same stack FinSwap uses).
2. Accepted assets: **Bitcoin (BTC), PERFECTCERTS, WEALTHTICKET** (Counterparty assets on the Bitcoin blockchain), and **Alpine Gold-backed currencies**.
3. **End users transact from their own real wallets.** The app builds the payment request / address / QR; the user's wallet signs and broadcasts. Verify payment against the real chain before unlocking paid content.
4. **Never hold, request, receive, store, or transmit a user's seed phrase or private key — server-side or anywhere else.** No custodial key storage, ever.
5. Free features stay free; do not paywall anything the owner has not named as paid. Until a payment path is connected and verified with a real (even tiny) transaction, label it demo.

## Working notes

- Test every change at phone width (Galaxy S9) and desktop width before calling it done, and check Safari/WebKit behavior for anything using newer APIs.
- Report only completed, verified results. An attempt is not a result.
