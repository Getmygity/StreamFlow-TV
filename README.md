<p align="center">
  <img src="images/header.png" alt="StreamFlow TV — IPTV player for Android TV" width="100%">
</p>

<p align="center">
  <b>An IPTV player for Android TV, made for the remote.</b><br>
  Bring your own M3U playlist and XMLTV guide; StreamFlow does the rest.
</p>

<p align="center">
  <a href="https://github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-TV.apk"><img alt="Download the APK" src="https://img.shields.io/badge/Download-StreamFlow--TV.apk-A78BFA?style=for-the-badge&logo=android&logoColor=white"></a>
  <img alt="Android TV 5.0+" src="https://img.shields.io/badge/Android%20TV-5.0%2B-2B1850?style=for-the-badge&logo=android&logoColor=white">
</p>

<p align="center">
  <img src="images/focused-card.jpg" alt="StreamFlow home screen" width="90%">
</p>

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
github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-TV.apk
```

Choose **Install** when it finishes. If Play Protect warns about an unknown app, choose to install anyway. You can delete the APK file afterwards to save space.

**4. Set it up from your phone.** Open **StreamFlow**, then scan the QR code on the TV with your phone. Your phone must be on the **same Wi-Fi** as the TV. Enter your **playlist (M3U) URL** and, optionally, your **guide (XMLTV) URL**. The TV loads your channels and you're in.

> **You need your own IPTV subscription.** StreamFlow is a player only; it comes with no channels.
>
> **Prefer a computer?** Download [`StreamFlow-TV.apk`](https://github.com/Getmygity/StreamFlow-TV/releases/latest/download/StreamFlow-TV.apk), then run `adb connect <tv-ip>:5555` and `adb install StreamFlow-TV.apk`.

---

## ✨ What it does

- **Live TV in rows by group.** The focused channel expands to show what's on, its time slot and the description, then **starts a muted live preview** in the tile.
- **Tile or list view.** Channel cards remember the last picture each channel showed.
- **Movies & series:** series fold into seasons and episodes. **Seek** with LEFT/RIGHT (10 s → 30 s → 1 min → 5 min with quick presses) and **pause** with OK.
- **Player overlay:** a channel browser, a forward schedule, a group picker, and CH+/CH− zapping.
- **Hold OK** on a channel for Play, Information or Cancel.
- **A guide that keeps itself fresh,** search across everything, and groups you can hide and reorder.
- **Hebrew-friendly:** programme text reads right to left.

| | |
|:---:|:---:|
| <img src="images/list-view.jpg" alt="List view"><br>**List view** | <img src="images/vod.jpg" alt="Movies and series"><br>**Movies & series** |
| <img src="images/channel-menu.jpg" alt="Channel menu"><br>**Hold OK for the channel menu** | <img src="images/channel-info.jpg" alt="Programme information"><br>**Full programme information** |
| <img src="images/player.jpg" alt="Player overlay"><br>**Player overlay** | <img src="images/vod-seek.jpg" alt="Seeking a movie"><br>**Seeking a movie** |

<sub>Screenshots use a test playlist.</sub>

---

## 🎮 Remote at a glance

| On the home screen | While watching |
|---|---|
| **D-pad:** move between channels. LEFT from the first card opens the menu. | **UP / DOWN:** browse channels |
| **OK:** watch | **LEFT / RIGHT:** browse the schedule (live) or seek (movies) |
| **Hold OK:** channel menu | **OK:** play the browsed channel, or pause a movie |
| **Back:** go to the menu | **Back:** close the overlay, then return home |

---

## ❓ Questions

- **Updating to a new version:** install the new APK the same way. It installs over the old one and keeps your settings.
- **"App not installed":** uninstall any older StreamFlow build first, then install again.
- **The QR page won't open on my phone:** make sure the phone and the TV are on the same Wi-Fi network.

<p align="center">
  <img src="images/tv-banner.png" alt="StreamFlow TV" width="320">
</p>
