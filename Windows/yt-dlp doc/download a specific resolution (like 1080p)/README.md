Perfect ✅ — here’s exactly how you can **download a specific resolution (like 1080p)** using `yt-dlp`.

---

### 🧩 Step 1 — Check available formats

First, run this to **list all available video & audio formats**:

```bash
yt-dlp -F "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

You’ll see output like this:

```
ID     EXT  RESOLUTION FPS  ...  FORMAT NOTE
136    mp4  720p       30   ...  video only
137    mp4  1080p      30   ...  video only
140    m4a  audio only      ...  audio
```

---

### 🎯 Step 2 — Download 1080p video + best audio

Once you find the 1080p format ID (say `137`), combine it with the best audio (say `140`):

```bash
yt-dlp -f 137+140 "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

✅ This will:

* Download the 1080p video (ID 137)
* Download the best audio (ID 140)
* Merge both into a single file (requires **ffmpeg**)

---

### 🧩 Shortcut (auto-pick 1080p if available)

You can also use a **filter**:

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio/best[height=1080]" "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

This tells `yt-dlp`:

* Find the **best video** with **height = 1080**
* Merge it with the **best audio**
* If not available, fall back to best 1080p full video (`best[height=1080]`)

---

### ⚙️ Optional: Save to custom folder or filename

```bash
yt-dlp -f "bestvideo[height=1080]+bestaudio" -o "~/Videos/%(title)s.%(ext)s" URL
```

---

### 🧠 Tips

* If 1080p isn’t available, `yt-dlp` will automatically pick the next best resolution.
* Make sure you have **ffmpeg** installed (for merging).

---

Would you like me to include an example for **downloading 1080p and automatically converting it to MP4** (even if the source is in WebM)?
