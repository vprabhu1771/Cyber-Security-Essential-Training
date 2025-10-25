The `yt-dlp` command is a powerful YouTube (and other sites) downloader, and the `-f` option lets you **select the video and audio format** you want to download.

Let’s go step by step 👇

---

### 🧩 Basic Syntax

```bash
yt-dlp -f FORMAT URL
```

**Example:**

```bash
yt-dlp -f best https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

This downloads the **best available quality** (video + audio).

---

### 🎯 Common Format Options

| Option                  | Description                                      |
| ----------------------- | ------------------------------------------------ |
| `best`                  | Best overall quality (default)                   |
| `worst`                 | Lowest quality                                   |
| `bestvideo`             | Best video only (no audio)                       |
| `bestaudio`             | Best audio only                                  |
| `bestvideo+bestaudio`   | Downloads both and merges them (requires ffmpeg) |
| `bv*+ba*`               | Shorthand for best video and best audio          |
| `worstvideo+worstaudio` | Lowest quality version                           |

---

### 📺 Example Usages

#### 1️⃣ Download best video and audio merged

```bash
yt-dlp -f bestvideo+bestaudio https://youtu.be/dQw4w9WgXcQ
```

#### 2️⃣ Download a specific resolution (like 720p)

```bash
yt-dlp -f "bestvideo[height=720]+bestaudio/best[height=720]" https://youtu.be/dQw4w9WgXcQ
```

#### 3️⃣ Download only audio (e.g. for MP3)

```bash
yt-dlp -f bestaudio https://youtu.be/dQw4w9WgXcQ
```

Or extract as MP3:

```bash
yt-dlp -x --audio-format mp3 https://youtu.be/dQw4w9WgXcQ
```

#### 4️⃣ See all available formats before choosing

```bash
yt-dlp -F https://youtu.be/dQw4w9WgXcQ
```

Then pick one from the list (for example `22`):

```bash
yt-dlp -f 22 https://youtu.be/dQw4w9WgXcQ
```

---

### 🧠 Tips

* Combine format filters:

  ```bash
  yt-dlp -f "bv*[ext=mp4]+ba[ext=m4a]" URL
  ```

  → Downloads MP4 video and M4A audio only.

* If you want to **download subtitles**:

  ```bash
  yt-dlp --write-subs --sub-lang en URL
  ```

* To **merge video and audio**, you need **ffmpeg** installed.

---

Would you like me to show you how to **download a specific resolution (like 1080p)** or **convert to MP3 automatically**?
