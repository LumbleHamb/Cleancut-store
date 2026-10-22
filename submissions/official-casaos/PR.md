# Pull request title

feat(appstore): add CleanCut 1.2.0

# Pull request description (copy everything below this line)

## New app: CleanCut 1.2.0

This PR adds a **new app**, `Apps/CleanCut/` (`x-casaos.id: org.harrelsons.cleancut`). No other files are changed.

### What it is

CleanCut Suite is an all-in-one media manager and profanity filter for Plex. It finds and adds new movies and shows (like Radarr, Sonarr and a download client in one app, from sources the user adds themselves), and it mutes the bad words in the movies and shows in your Plex library (just the word, not the whole line) and stars them out in the subtitles. The picture is never re-encoded, and the original audio stays inside each file as a backup track, so any mute can be undone. Cleaned titles get a **Kid Safe** label in Plex, so kid profiles only see titles that are cleaned and within the age limit the parent picks. Everything runs on the user's own server; nothing is uploaded. CleanCut Cleaner, the smaller edition, is just the cleaning, for media the user already has.

- One container, one web page (port 8585).
- Image: `ghcr.io/lumblehamb/clean-media-stack:1.2.0` (public, pinned to the release tag).

### Paid app with a free trial

CleanCut is commercial software. Every feature is free for **3 movies and 10 TV episodes**, no card needed. After that it is a one-time purchase: **CleanCut Cleaner $2.99** or **CleanCut Suite $5.99** (upgrade from Cleaner: $3). These are launch prices; the price rises for new buyers as features are added, and a bought license never expires. No subscription. The listing says this in the description.
Website: https://shop.harrelsons.org/cleancut/

### Why `NET_ADMIN` and `/dev/net/tun`

Both are used **only** by an optional, built-in VPN with a kill switch, which runs inside the container's own network namespace. It is off by default. The container does not change the host's network settings. The before-install tip says so too.

### Multi-arch

The image is a multi-arch manifest for **linux/amd64** and **linux/arm64** (64-bit Intel/AMD PCs and ARM boards such as the Raspberry Pi 5). `architectures` lists both.

### Content sources

CleanCut works on the user's own media folders. It **ships with no download sources** of any kind: the optional media manager works only with sources the user adds themselves, no sources are included or enabled by default, and the user is responsible for what they download.

### Reviewer license key

A free full-feature reviewer key is available. Email **ethen@harrelsons.org** and I will send one right away. The free trial is also enough for the tests below.

### How I validated it

- `.github/actions/validate-compose/scripts/validate_compose.py`: passed, 0 errors, 0 warnings.
- `docker compose -f Apps/CleanCut/docker-compose.yml config -q`: passed.
- `IceWhaleTech/build-appstore-action` (`scripts/build_appstore.py`, v1.1.2, the version `scripts/build_dist.sh` uses): builds `dist/apps/org.harrelsons.cleancut/` with `docker-compose.amd64.yml` and `docker-compose.arm64.yml`, both pinned to digests.

### How to test (3 steps)

1. Install **CleanCut** from the store (Media category), then open it on port **8585**.
2. In the setup guide, choose a folder with one short movie or episode that has English subtitles, and connect your Plex server.
3. Wait until the title shows **Clean** on the Home page. Play it in Plex: the bad words are silent, the subtitles show stars, and the title has the **Kid Safe** label.

### Checklist

- [x] New app (not an update)
- [x] Top-level `name` and reverse-domain `x-casaos.id`
- [x] Image pinned to a version tag (`1.2.0`), no `latest`
- [x] `icon.svg`, `thumbnail.png` (784x442) and 4 screenshots (1280x720) included
- [x] Support: https://shop.harrelsons.org/cleancut/help/ and ethen@harrelsons.org
