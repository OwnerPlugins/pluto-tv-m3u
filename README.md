![](https://komarev.com/ghpvc/?username=Belfagor2005)

# 📺 Pluto TV M3U Playlists

![Screenshot](giphy.gif)


This repository contains **automatically updated M3U playlists** for Pluto TV, including both **live channels** and **on‑demand movies**.  
Playlists are generated every 6 hours and are organised by **region**.

> **Note**: These playlists are unofficial and provided for personal use only. All content remains the property of Pluto TV.

---

## 🌍 Regions

All official Pluto TV regions are supported.  
Each region has its own files:

| File                       | Content               |
|----------------------------|-----------------------|
| `pluto-live-XX.m3u`        | Live TV channels      |
| `pluto-vod-XX.m3u`         | Movies (on‑demand)    |

where `XX` is the two‑letter country code (e.g. `US`, `GB`, `IT`, `DE`, …).

---

## 📺 How to Use

1. **Download** the playlist file(s) you want.
2. **Open** with any IPTV‑compatible player, such as:
   - [VLC Media Player](https://www.videolan.org/vlc/)
   - [Kodi](https://kodi.tv/)
   - [TiviMate](https://tivimate.com/) (Android)
   - [IPTVnator](https://github.com/4gray/iptvnator) (desktop)
3. **Enjoy** Pluto TV channels and movies without official restrictions.

### ▶️ Viewing Categories (Groups) in VLC

- Right‑click the playlist → **View** → **Playlist** → enable **Show groups**.  
  Then you will see category groups (e.g. *Entertainment*, *Kids*, *News*) on the left.

---

## 🛠️ Automatic Updates

The playlists are automatically regenerated **every 6 hours** via a GitHub Actions workflow.  
No manual intervention is required – the files in this repository are always up‑to‑date.

---

## 🧪 Playlist Format

All playlists use the standard M3U format with extended attributes:

- `group-title` – for category grouping (supported by many players, including VLC)
- `tvg-id` / `tvg-name` / `tvg-logo` – for EPG and channel logos

Example entry:
```
#EXTINF:-1 group-title="Animals + Nature" tvg-id="51c75f7bb6f26ba1cd00002f" tvg-name="Little Stars Universe" tvg-logo="https://images.pluto.tv/...",Little Stars Universe
https://cfd-v4-service-channel-stitcher-use1-1.prd.pluto.tv/.../master.m3u8?jwt=...
```

---

## ⚠️ Important Notes

- **Streams require a valid JWT token**. The token is automatically included in each URL and refreshed at generation time.  
- If a channel does not work, try downloading the playlist again – the token may have expired.
- Due to regional restrictions, some channels may not play outside the intended region.
- This is an **unofficial** project; Pluto TV may change its API at any time.

---

## 📝 License
```
Mit
```
---

## 🔗 Links

- [Pluto TV Official Website](https://pluto.tv)
---

*Last updated automatically – see the commit history for timestamps.*
