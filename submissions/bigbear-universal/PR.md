Add CleanCut 1.2.0 (media manager and profanity filter for Plex, paid app)

## New app: CleanCut 1.2.0

Adds `apps/cleancut/` (`app.json` + `docker-compose.yml`). No other files are changed.

**What it is.** CleanCut mutes the swearing in the movies and shows on a Plex server: just the bad word in the audio (not the whole line), starred out in the subtitles. The picture is never re-encoded and the original audio stays inside each file as a backup track. Cleaned titles get a **Kid Safe** label in Plex so kid profiles only see cleaned titles within the parent's age limit. CleanCut Suite also includes a built-in media manager (Radarr/Sonarr-style) for sources the user adds; **no sources are included or enabled by default.**

**This is a paid app: please read the licensing fees.** Nothing is hidden behind the install; the fees are also stated in the app's description:
- **Free trial:** every feature for 3 movies and 10 TV episodes, no card, no account.
- **Then a one-time license:** CleanCut Cleaner **$2.99** (language cleaning only) or CleanCut Suite **$5.99** (everything, including the media manager). Cleaner to Suite upgrade: **$3**.
- **No subscription.** A license never expires. These are launch prices; the price for new buyers will rise as major features are added, and existing licenses are kept.
- 30-day money-back guarantee. Prices and terms: https://shop.harrelsons.org/cleancut/

**Why `NET_ADMIN` and `/dev/net/tun`.** Only for the optional built-in VPN with a kill switch, inside the container's own network namespace. Off by default; the host network is not touched.

**Image.** `ghcr.io/lumblehamb/clean-media-stack:1.2.0`, public, multi-arch (amd64 + arm64), pinned to its index digest.

**Validated:** `app.json` passes `schemas/app-schema-v1.json`; `docker compose config` passes.

**How to test:**
1. Install CleanCut and open port **8585**.
2. In the setup guide, pick a folder with one short title that has English subtitles, and connect Plex.
3. When the title shows **Clean**, play it in Plex: the bad words are silent, the subtitles show stars, and the title has the **Kid Safe** label.

A free full-feature reviewer key is available at ethen@harrelsons.org (the trial is enough for the test above). Support: https://shop.harrelsons.org/cleancut/help/
