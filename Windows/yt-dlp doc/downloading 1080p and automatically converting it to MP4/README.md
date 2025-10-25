Perfect 👍 — here’s how you can **download 1080p video and automatically convert it to MP4** using `yt-dlp`.

---

### ✅ Step-by-step command

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

---

### 💡 Explanation:

| Option                                  | Meaning                                                 |
| --------------------------------------- | ------------------------------------------------------- |
| `-f "bestvideo[height=1080]+bestaudio"` | Selects the best video with height 1080p and best audio |
| `--merge-output-format mp4`             | Forces the final output to be MP4 after merging         |
| `"URL"`                                 | Replace this with your YouTube link                     |

🧠 Note: You need **ffmpeg** installed — it merges the video and audio into a single MP4 file automatically.

---

### 🧩 Example with custom filename

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 -o "~/Videos/%(title)s.%(ext)s" "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

This saves the file in your `Videos` folder with the video title as the filename.

---

### 🧱 Optional Extras

**1️⃣ If you want to embed metadata:**

```bash
yt-dlp --embed-metadata -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 URL
```

**2️⃣ If you want subtitles too:**

```bash
yt-dlp --write-subs --sub-lang en --embed-subs -f "bestvideo[height=1080]+bestaudio" --merge-output-format mp4 URL
```

---

Would you like me to show you how to **download an entire playlist in 1080p MP4 format** next?
