<p align="center">
  <img src="images/header.png" alt="StreamFlow TV — IPTV player for Android TV, LG TV and Android phones" width="100%">
</p>

<p align="center">
  <b>An IPTV player for Android TV, LG TV and Android phones.</b><br>
  Bring your own M3U playlist and XMLTV guide; StreamFlow does the rest.
</p>

<p align="center">
  <a href="https://tinyurl.com/5ee4bvwv"><img alt="Download the APK for Android TV" src="https://img.shields.io/badge/Android%20TV-StreamFlow--TV.apk-FFFFFF?style=for-the-badge&logo=android&logoColor=white&labelColor=000000"></a>
  <a href="https://github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-LG.ipk"><img alt="Download the IPK for LG TV" src="https://img.shields.io/badge/LG%20TV-StreamFlow--LG.ipk-FFFFFF?style=for-the-badge&logo=lg&logoColor=white&labelColor=000000"></a>
  <a href="https://github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-Phone.apk"><img alt="Download the APK for Android phones" src="https://img.shields.io/badge/Android%20phone-StreamFlow--Phone.apk-FFFFFF?style=for-the-badge&logo=android&logoColor=white&labelColor=000000"></a>
</p>

<p align="center">
  <img alt="Android TV 5.0+" src="https://img.shields.io/badge/Android%20TV-5.0%2B-262626?style=for-the-badge&logo=android&logoColor=white&labelColor=000000">
  <img alt="LG webOS 22+" src="https://img.shields.io/badge/LG%20webOS-22%2B-262626?style=for-the-badge&logo=lg&logoColor=white&labelColor=000000">
  <img alt="Android 8.0+" src="https://img.shields.io/badge/Android%20phone-8.0%2B-262626?style=for-the-badge&logo=android&logoColor=white&labelColor=000000">
</p>

<p align="center">
  <img src="images/home.jpg" alt="StreamFlow home screen" width="90%">
</p>

**Which one do I need?** An Android TV, Google TV or Android box takes **`StreamFlow-TV.apk`** ([install steps](#%EF%B8%8F-install-on-your-android-tv)). An LG smart TV from 2022 or later takes **`StreamFlow-LG.ipk`** ([install steps](#%EF%B8%8F-install-on-your-lg-tv)). An Android phone takes **`StreamFlow-Phone.apk`** ([install steps](#%EF%B8%8F-install-on-your-android-phone)).

---

## ⬇️ Install on your Android TV

StreamFlow isn't in the Play Store, so it's installed by hand ("sideloaded"). It takes about five minutes the first time.

**1. Get the Downloader app.** On the TV, open the Play Store, search for **Downloader** (by AFTVnews), and install it.

**2. Let Downloader install apps.**
- On **Google TV**, turn on developer mode first: *Settings → System → About*, then click *Android TV OS build* 7 times.
- Then go to *Settings → Apps → Security & restrictions → Unknown sources* and switch **Downloader** on.

The menu names vary a little between TV brands.

**3. Download StreamFlow.** Open Downloader and type this address:

```
tinyurl.com/streamflowapk
```

It leads to the latest `StreamFlow-TV.apk` here; this short link works too: `tinyurl.com/5ee4bvwv`.

Choose **Install** when it finishes. If Play Protect warns about an unknown app, choose to install anyway. You can delete the APK file afterwards to save space.

**4. Set it up from your phone.** Open **StreamFlow**, then scan the QR code on the TV with your phone. Your phone must be on the **same Wi-Fi** as the TV. Enter your **playlist (M3U) URL** and, optionally, your **guide (XMLTV) URL**. The TV loads your channels and you're in.

> **You need your own IPTV subscription.** StreamFlow is a player only; it comes with no channels.
>
> **Prefer a computer?** Download [`StreamFlow-TV.apk`](https://tinyurl.com/5ee4bvwv), then run `adb connect <tv-ip>:5555` and `adb install StreamFlow-TV.apk`.

---

## ⬇️ Install on your Android phone

For phones with **Android 8.0 or newer**. StreamFlow isn't in the Play Store, so it's installed from this page. It takes about two minutes.

**1. Download it on the phone.** In the phone's browser, open `github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-Phone.apk`, or tap the badge at the top of this page. If the browser warns that this type of file can harm your device, choose **Download anyway**.

**2. Open the file and allow the install.** Open the downloaded file (from the browser's downloads, or the notification). The first time, Android says the browser isn't allowed to install apps: tap **Settings**, switch on **Allow from this source**, and go back. (Or: *Settings → Apps → Special app access → Install unknown apps*, then your browser.)

**3. Install.** Tap **Install**. If Play Protect warns about an unknown app, choose to install anyway.

**4. Type your links.** Open **StreamFlow** and enter your **playlist (M3U) link** and, optionally, your **guide (XMLTV) link**. It loads your channels and you're in.

<p align="center">
  <img src="images/phone-live.jpg" alt="Live TV on a phone" width="30%">
  <img src="images/phone-vod.jpg" alt="Movies and series on a phone" width="30%">
  <img src="images/phone-sports.jpg" alt="Live sports on a phone" width="30%"><br>
  <sub>Live TV · Movies &amp; series · Live sports</sub>
</p>

---

## ⬇️ Install on your LG TV

For LG smart TVs with **webOS 22 or newer** (2022 models and later). StreamFlow isn't in the LG Content Store, so it goes on through LG's free **Developer Mode**, from a computer on the same network. It takes about fifteen minutes the first time.

**1. Make an LG developer account** at [webostv.developer.lge.com](https://webostv.developer.lge.com). It's free.

**2. Turn on Developer Mode on the TV.** Install the **Developer Mode** app from the LG Content Store and sign in with that account. Turn on **Dev Mode Status**; the TV restarts. Open the app again and turn on **Key Server**. Keep it open: it shows the TV's **IP address** and a **passphrase**.

**3. Connect your computer to the TV.** Install [Node.js](https://nodejs.org), then LG's tools, and pair with the TV:

```bash
npm install -g @webos-tools/cli
ares-setup-device -a mytv -i "host=<tv-ip>" -i "port=9922" -i "username=prisoner"
ares-novacom -d mytv --getkey
ares-setup-device -m mytv -i "privatekey=mytv_webos" -i "passphrase=<passphrase>"
```

`--getkey` asks for the passphrase shown on the TV.

**4. Install StreamFlow.** Download [`StreamFlow-LG.ipk`](https://github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-LG.ipk) (short link: `tinyurl.com/streamflowlg`), then:

```bash
ares-install -d mytv StreamFlow-LG.ipk
ares-launch -d mytv com.youngertv.streamflow.lgtv
```

**5. Type your links.** Enter your **playlist (M3U) link** and, optionally, your **guide (XMLTV) link**, with the remote or with the **LG ThinQ** app's keyboard on your phone. The TV loads your channels and you're in. From then on StreamFlow is in the TV's app list.

> **Extend Developer Mode every few weeks.** A session lasts 1000 hours (about six weeks). Open the Developer Mode app and extend it before it runs out, or the TV removes StreamFlow along with your saved links.

<p align="center">
  <img src="images/lg-setup.jpg" alt="Typing the playlist link on an LG TV" width="70%"><br>
  <sub>Setup on the LG TV: type your links with the remote or your phone.</sub>
</p>

---

## ✨ What it does

- **Live TV in rows by group,** under a slim rail of icons that opens with labels when you move onto it. **A hero across the top** shows the channel in focus: what's on, its hours and the description, and after 5 seconds **a muted live preview**.
- **One entry per channel.** A channel your playlist lists several times (`Sport 1 (2)`, `Kan 11 FHD` and `Kan 11 SD`) shows once and plays its main stream. **Hold OK** on it, or hold OK while watching, to **select another server**.
- **Tile or list view.** On Android TV, channel cards remember the last picture each channel showed.
- **Movies & series:** series fold into seasons and episodes, and every poster shows its **IMDb rating**. The hero shows the movie or series in focus with its plot, and **after 2 seconds plays its trailer**. **Seek** with LEFT/RIGHT (10 s → 30 s → 1 min → 5 min with quick presses) and **pause** with OK.
- **Hold OK on a movie, series or episode** for **Information** (the plot, year, length and genres) and **Play trailer**, which plays inside StreamFlow.
- **Player overlay:** a channel browser, a forward schedule, a group picker (UP from the first channel, marked "▲ GROUPS"), and CH+/CH− zapping.
- **Live sports:** today's NBA and European football games, each with the channels in your guide that show it, and **goal alerts** while you watch another channel (press OK to switch).
- **Hold OK** on a channel for Play, Select Server, Information or Cancel. In **Information**, LEFT and RIGHT step through the channel's schedule.
- **A guide that keeps itself fresh,** search across everything, and groups you can hide and reorder.
- **Hebrew-friendly:** programme text reads right to left.
- **On a phone:** the same channels, movies and sports in a tab bar; play sideways, swipe through the schedule and the channels, and get goal alerts.

| | |
|:---:|:---:|
| <img src="images/rail.jpg" alt="The rail, open"><br>**The rail**, open | <img src="images/list-view.jpg" alt="List view"><br>**List view** |
| <img src="images/vod.jpg" alt="Movies and series"><br>**Movies & series**, with IMDb ratings | <img src="images/vod-trailer.jpg" alt="A trailer in the hero"><br>**Trailers in the hero**, after 2 seconds |
| <img src="images/vod-info.jpg" alt="Movie information"><br>**Hold OK on a movie** for its information | <img src="images/trailer.jpg" alt="A trailer playing"><br>**Trailers** play full screen too |
| <img src="images/channel-menu.jpg" alt="Channel menu"><br>**Hold OK for the channel menu** | <img src="images/channel-info.jpg" alt="Programme information"><br>**Programme information**, LEFT for what's on later |
| <img src="images/player.jpg" alt="Player overlay"><br>**Player overlay** | <img src="images/vod-seek.jpg" alt="Seeking a movie"><br>**Seeking a movie** |

### ⚽ Live sports and goal alerts

| | |
|:---:|:---:|
| <img src="images/lg-sports.jpg" alt="Live sports on LG TV"><br>**Live sports** — each game with its channels | <img src="images/lg-goal-alert.jpg" alt="Goal alert on LG TV"><br>**Goal alert** — OK switches to the game |
| <img src="images/lg-home.jpg" alt="LG TV home screen"><br>**LG TV home** — with the muted preview | <img src="images/lg-player.jpg" alt="LG TV player"><br>**LG TV player** |

<p align="center">
  <img src="images/phone-player.jpg" alt="The phone's player, sideways" width="70%"><br>
  <sub>The phone's player, sideways</sub>
</p>

<sub>Screenshots use a test playlist: the Android TV and Android phone emulators, and the LG app's desktop build.</sub>

---

## 🎮 Remote at a glance

| On the home screen | While watching |
|---|---|
| **Arrows:** move between channels. LEFT from the first card opens the menu. | **UP / DOWN:** browse channels |
| **OK:** watch | **LEFT / RIGHT:** browse the schedule (live) or seek (movies) |
| **Hold OK:** channel menu (Play, Select Server, Information), or a movie's (Information, Play trailer) | **OK:** play the browsed channel, or pause a movie |
| **LEFT / RIGHT in a channel's Information:** later in its schedule, or back | **Hold OK:** choose another server of the channel |
| **Back:** go to the menu | **Back:** close the overlay, then return home |

On an LG TV the **Magic Remote** works too: point at a channel to focus it and click to press.

---

## ❓ Questions

- **Updating to a new version:** install the new file the same way. It installs over the old one and keeps your settings. On Android TV, **Settings → Check for updates** downloads and installs it for you; on an LG TV it shows what's new and how to install it. On a phone too, **Settings → Check for updates** downloads and installs it.
- **"App not installed" (Android TV or phone):** uninstall any older StreamFlow build first, then install again.
- **The QR page won't open on my phone (Android TV):** make sure the phone and the TV are on the same Wi-Fi network.
- **StreamFlow disappeared from my LG TV:** the Developer Mode session ran out. Turn Developer Mode on again, install the IPK again, and extend the session every few weeks from then on.
- **Typing a long link on the LG TV is slow:** use the LG ThinQ app on your phone as the TV's keyboard.

<sub>This product uses the TMDB API but is not endorsed or certified by TMDB. Ratings: information courtesy of IMDb (imdb.com), used with permission.</sub>

<p align="center">
  <img src="images/tv-banner.png" alt="StreamFlow TV" width="320">
</p>
