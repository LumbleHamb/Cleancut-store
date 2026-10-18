# Pull request title

Add CleanCut 1.2.0 (profanity filter for Plex)

# Pull request description (copy everything below this line)

## New app: CleanCut 1.2.0

Adds `Apps/cleancut/` (`docker-compose.yml` + `config.json`), `x-casaos.id: com.bigbeartechworld.cleancut`. No other files are changed.

**What it is.** CleanCut is a profanity filter for Plex. It mutes the bad words in the movies and shows in your Plex library (just the word, not the whole line) and stars them out in the subtitles. The picture is never re-encoded and the original audio stays inside each file as a backup track. Cleaned titles get a **Kid Safe** label in Plex so kid profiles only see cleaned titles within the parent's age limit. Everything runs locally; nothing is uploaded.

**Paid after a free trial.** Every feature is free for 3 movies and 10 TV episodes, no card. Then a one-time purchase: CleanCut Cleaner $14.99 or CleanCut Suite $19.99. No subscription. Website: https://shop.harrelsons.org/cleancut/

**Why `NET_ADMIN` and `/dev/net/tun`.** Only for an optional, built-in VPN with a kill switch, inside the container's own network namespace. Off by default; the host network is not touched.

**Multi-arch.** `ghcr.io/lumblehamb/clean-media-stack:1.2.0` is a public multi-arch image (linux/amd64 + linux/arm64), pinned here to its index digest `sha256:640f3c5e...197a`.

**Content sources.** CleanCut works on the user's own media folders and **ships with no download sources**.

**Reviewer key.** Email **ethen@harrelsons.org** for a free full-feature reviewer key (the free trial is also enough for the test below).

**Port.** 8585 is the port used in all CleanCut docs and guides. It is also used by `cantinarr` and `fireshare` in this store; if you prefer a unique port, tell me which one and I will change it.

**Validated with:**
- `.github/scripts/lint-casaos-v2.sh`: `1 migrated app(s) v2-clean`
- `docker compose -f Apps/cleancut/docker-compose.yml config -q`: passed
- `IceWhaleTech/build-appstore-action` build check: passed (amd64 and arm64 composes generated)

**How to test (3 steps):**
1. Install **CleanCut** from the store and open it on port **8585**.
2. In the setup guide, choose a folder with one short movie or episode that has English subtitles, and connect your Plex server.
3. When the title shows **Clean** on the Home page, play it in Plex: the bad words are silent, the subtitles show stars, and the title has the **Kid Safe** label.

Support: https://shop.harrelsons.org/cleancut/help/ or ethen@harrelsons.org
