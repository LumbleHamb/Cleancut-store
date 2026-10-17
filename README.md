# CleanCut Store

The app store for **CleanCut Suite** on CasaOS and ZimaOS.

CleanCut Suite is a profanity filter for Plex. It mutes the swearing in the movies and shows on
your Plex before your kids press play: just the word, not the whole line, and it stars the word
out in the subtitles too. The original audio stays inside each file as a backup track. Clean
titles get a Kid Safe label in Plex, so kid profiles only see clean titles within the age limit
you choose. If you like, CleanCut can also find and download new movies and shows and clean them
as they arrive (optional, with an optional VPN to keep your home address private). Try it free on
3 movies and 10 TV episodes, with every feature and no card. Then it's $19.99 once - launch price.
The price goes up after launch; buy now and it's yours for life, with free updates. There is no
CleanCut subscription. 30-day money-back guarantee: if CleanCut won't run on your server, or
doesn't do what its page says, email ethen@harrelsons.org within 30 days and we'll refund you in
full.

More about CleanCut: https://shop.harrelsons.org/cleancut/

## Add this store

Add the store once. After that, CleanCut shows up in your App Store like any other app, and
its updates show up there too.

### CasaOS

1. Open **App Store**.
2. At the top right, click the button that shows how many apps there are (for example
   **"120 apps"**), then choose **More apps**. (If you have never added a store, it's a single
   **More apps** button with a **+** sign.)
3. Paste this address and click **Add**:

   ```
   https://github.com/LumbleHamb/cleancut-store/archive/refs/heads/main.zip
   ```

4. Search for **CleanCut** and click **Install**.

### ZimaOS

1. Open **App Store** and find the option to add a store source (on most ZimaOS versions it's a
   button at the top right of the App Store).
2. Paste this address and add it:

   ```
   https://cdn.jsdelivr.net/gh/LumbleHamb/cleancut-store@gh-pages/store.json
   ```

3. Search for **CleanCut** and click **Install**. If it doesn't show up straight away, refresh
   the page.

ZimaOS menu names change between versions. If yours look different, look for the option to add
an app store source inside the App Store.

### After installing

Open CleanCut (port 8585) and follow the setup guide. It takes about ten minutes. The first
question is what you'd like CleanCut to do: clean the movies and shows already on your Plex, or
also find and download new ones.

CleanCut sees your movies and shows under `/media` (your `/DATA/Media` folder). If they're on
another drive, change the `/media` folder under **Volumes** before you install. CleanCut adds a
clean audio track to each file, so **back up anything irreplaceable first**.

Full install guide: https://shop.harrelsons.org/cleancut/install/

## Moving from a Custom Install

Did you install CleanCut by pasting its compose file (Custom Install)? You can switch to the
store in three steps. Your settings, word list and history carry over, because the app name
(`clean-media`) and its settings folder (`/DATA/AppData/clean-media/config`) are the same.

1. Uninstall CleanCut and **keep its data**: leave **Delete userdata ( config folder )**
   unticked.
2. Add this store (see above).
3. Install CleanCut from the store. Open it on port 8585 and it picks up where you left off.

## Help

Questions or problems: https://shop.harrelsons.org/cleancut/help/

## License

The files in this repository (the store listing, pictures and build workflow) are under the MIT
License. See [LICENSE](LICENSE).

CleanCut Suite itself is commercial software with a free trial. The MIT License does not cover
it; it has its own license (EULA).
