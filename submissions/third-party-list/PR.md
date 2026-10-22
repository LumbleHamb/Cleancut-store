# Pull request title

docs: add CleanCut Store to the third-party store list

# Pull request description (copy everything below this line)

Docs change only. Adds one `StoreSourceCard` for the **CleanCut Store** to `docs/resources/recommended-third-party-stores.md` (and the matching card to `docs/zh/resources/recommended-third-party-stores.md`), after the existing entries. Nothing else is changed.

**What the store is.** A single-app store for CleanCut Suite, an all-in-one media manager and profanity filter for Plex: it finds and adds new movies and shows from sources the user adds themselves (like Radarr and Sonarr), mutes the bad words in the movies and shows in your Plex library and labels clean titles **Kid Safe** so kid profiles only see cleaned titles. CleanCut is a paid app with a free trial (3 movies + 10 TV episodes), then a one-time purchase (Cleaner $2.99 or Suite $5.99; launch prices that rise for new buyers as features are added, and a bought license never expires). The card's summary says it is paid.

**Store sources.**
- ZimaOS (v2), used in the card: `https://cdn.jsdelivr.net/gh/LumbleHamb/cleancut-store@gh-pages/store.json`
- CasaOS (v1 zip): `https://github.com/LumbleHamb/cleancut-store/archive/refs/heads/main.zip`
- Source repo: https://github.com/LumbleHamb/cleancut-store

The store is built with `IceWhaleTech/build-appstore-action` on every push, and the image (`ghcr.io/lumblehamb/clean-media-stack`) is public and multi-arch (amd64 + arm64). The app ships with no download sources: no sources are included or enabled by default, and the user is responsible for what they download. `NET_ADMIN` and `/dev/net/tun` are used only by an optional VPN inside the container.

**How I checked it.**
1. Both store URLs above return HTTP 200, and `store.json` reports `store_id: org.harrelsons.cleancut-store`.
2. The new card uses the same fields as the existing cards.
3. A reviewer key is available by emailing ethen@harrelsons.org.

Maintainer contact: ethen@harrelsons.org
