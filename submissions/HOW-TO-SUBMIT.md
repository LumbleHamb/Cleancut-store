# How to submit CleanCut to the app stores

Everything is already written for you. You only copy, paste and click on the GitHub website.
There are three separate submissions. Do them in any order, one at a time.

**Before you start**

- Sign in at https://github.com.
- The files you will copy are in your own repo: https://github.com/LumbleHamb/cleancut-store/tree/main/submissions
- To copy a text file: open it on GitHub and click the **Copy raw file** button (two overlapping squares, top right of the file).
- To get a picture: open it on GitHub and click **Download raw file** (the arrow pointing down, top right of the file).
- Every folder has a **PR.md**. Its first part is the pull request **title**; everything under "copy everything below this line" is the **description**.

---

## 1. Official ZimaOS / CasaOS App Store

Files: `submissions/official-casaos/`

1. Download the 6 pictures from `submissions/official-casaos/Apps/CleanCut/` to your computer:
   `icon.svg`, `thumbnail.png`, `screenshot-1.png`, `screenshot-2.png`, `screenshot-3.png`, `screenshot-4.png`.
2. Go to https://github.com/IceWhaleTech/CasaOS-AppStore and click **Fork**, then **Create fork**.
3. In your fork, click the **Apps** folder, then **Add file → Create new file**.
4. In the name box type exactly `CleanCut/docker-compose.yml` (the `/` makes the folder).
   Paste the contents of `submissions/official-casaos/Apps/CleanCut/docker-compose.yml`.
5. Click **Commit changes…**, choose **Create a new branch for this commit**, name it `add-cleancut`, then click **Commit changes** (or **Propose changes**). If GitHub opens a pull-request page now, close that tab.
6. Go back to your fork, switch the branch menu (top left, says `main`) to **add-cleancut**, and open **Apps → CleanCut**.
7. Click **Add file → Upload files**, drag in the 6 pictures, keep **Commit directly to the add-cleancut branch**, and click **Commit changes**.
8. Click **Contribute → Open pull request**. Check that the top says **base repository: IceWhaleTech/CasaOS-AppStore** and **compare: add-cleancut**.
9. Paste the title and description from `submissions/official-casaos/PR.md`, then click **Create pull request**.
10. Wait for the automatic checks (green tick). If a reviewer asks for a key, email them one from ethen@harrelsons.org.

---

## 2. Big Bear CasaOS store

Files: `submissions/bigbear/`

1. Go to https://github.com/bigbeartechworld/big-bear-casaos and click **Fork**, then **Create fork**.
2. In your fork, click the **Apps** folder, then **Add file → Create new file**.
3. Type exactly `cleancut/docker-compose.yml` (all lower case) and paste the contents of `submissions/bigbear/Apps/cleancut/docker-compose.yml`.
4. Click **Commit changes…**, choose **Create a new branch for this commit**, name it `add-cleancut`, and commit. Close any pull-request tab that opens.
5. Switch the branch menu to **add-cleancut**, open **Apps → cleancut**, click **Add file → Create new file**, type `config.json`, paste the contents of `submissions/bigbear/Apps/cleancut/config.json`, and commit directly to **add-cleancut**.
6. Click **Contribute → Open pull request**. Check **base repository: bigbeartechworld/big-bear-casaos**, **base: master**, **compare: add-cleancut**.
7. Paste the title and description from `submissions/bigbear/PR.md` and click **Create pull request**.

Note: Big Bear now generates this repo's apps from a second repo (`bigbeartechworld/big-bear-universal-apps`). If they ask you to send the app there instead, reply asking them to move it over for you, or ask me to prepare that version.

---

## 3. Third-party store list (the "Awesome Third-party Stores" page)

Files: `submissions/third-party-list/`

1. Open https://github.com/IceWhaleTech/CasaOS-AppStore/blob/main/docs/resources/recommended-third-party-stores.md
2. Click the **pencil** (Edit this file). If you already forked in step 1, GitHub edits your fork; otherwise it offers to fork it for you. Say yes.
3. Find the line `## About this list`. Just above it, paste the block from
   `submissions/third-party-list/docs/resources/recommended-third-party-stores.ENTRY-ONLY.txt`
   (leave one empty line before and after it). The finished file should look like
   `submissions/third-party-list/docs/resources/recommended-third-party-stores.md`.
4. Click **Commit changes…**, choose **Create a new branch for this commit**, name it `add-cleancut-store-list`, and click **Propose changes**.
5. Optional (Chinese page): switch your fork to the **add-cleancut-store-list** branch, open `docs/zh/resources/recommended-third-party-stores.md`, click the pencil, paste the block from `submissions/third-party-list/docs/zh/resources/recommended-third-party-stores.ENTRY-ONLY.txt` just above `## 页面说明`, and commit directly to **add-cleancut-store-list**.
6. Click **Contribute → Open pull request** (base repository **IceWhaleTech/CasaOS-AppStore**, compare **add-cleancut-store-list**).
7. Paste the title and description from `submissions/third-party-list/PR.md` and click **Create pull request**.

Keep each submission on its own branch, so the three pull requests do not get mixed together.
