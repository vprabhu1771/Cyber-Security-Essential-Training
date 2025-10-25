Excellent choice 🎬 — downloading an entire **YouTube playlist in 1080p MP4** format is easy with `yt-dlp`.
Here’s the complete guide 👇

---

### ✅ Basic Command

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 "https://www.youtube.com/playlist?list=YOUR_PLAYLIST_ID"
```

🧠 Replace `YOUR_PLAYLIST_ID` with your actual YouTube playlist URL, for example:

```
https://www.youtube.com/playlist?list=PL9tY0BWXOZFtFS2KfaYbZp8HPCrOjp1dB
```

---

### 💡 Explanation

| Option                                  | Description                                            |
| --------------------------------------- | ------------------------------------------------------ |
| `-f "bestvideo[height=1080]+bestaudio"` | Selects best 1080p video and best audio for each video |
| `--merge-output-format mp4`             | Ensures final file is MP4                              |
| Playlist URL                            | Automatically processes all videos in the playlist     |

---

### 🗂️ Optional: Save files with organized names

You can include playlist folder and title automatically:

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" \
--merge-output-format mp4 \
-o "~/Videos/%(playlist_title)s/%(playlist_index)s - %(title)s.%(ext)s" \
"https://www.youtube.com/playlist?list=YOUR_PLAYLIST_ID"
```

🗃️ This creates:

```
~/Videos/Your Playlist Name/
  01 - First Video.mp4
  02 - Second Video.mp4
  ...
```

---

### ⚙️ Optional extras

**1️⃣ Limit downloads to first 5 videos:**

```bash
yt-dlp --playlist-items 1-5 -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 URL
```

**2️⃣ Resume partially downloaded playlists:**

```bash
yt-dlp -ic -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 URL
```

> `-i` = ignore errors
> `-c` = continue partially downloaded files

**3️⃣ Show progress and speed clearly:**

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 --progress URL
```

---

### 🧠 Requirements

* Make sure **ffmpeg** is installed (for merging video + audio).
  To check:

  ```bash
  ffmpeg -version
  ```

  If not installed:

  * **Windows:** Install from [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html)
  * **Linux/macOS:**

    ```bash
    sudo apt install ffmpeg
    ```

    or

    ```bash
    brew install ffmpeg
    ```

---

Would you like me to show a version that **automatically skips videos below 1080p** (so it only downloads ones available in 1080p)?
