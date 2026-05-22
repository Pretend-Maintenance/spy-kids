# 🕵️ SPY ACADEMY — QR Activity Site

## File Structure

```
spy-kids/
├── index.html          ← The entire site (single file)
└── videos/
    ├── activity1.mp4   ← Mission 1 video
    ├── activity2.mp4   ← Mission 2 video
    ├── activity3.mp4   ← Mission 3 video
    ├── activity4.mp4   ← Mission 4 video
    ├── activity5.mp4   ← Mission 5 video
    └── activity6.mp4   ← Mission 6 video
```

## Setup

### 1. Add your videos
Drop your 6 video files into the `videos/` folder named exactly `activity1.mp4` through `activity6.mp4`.

### 2. Deploy to GitHub Pages
1. Create a new GitHub repo (e.g. `spy-academy`)
2. Upload both `index.html` and the `videos/` folder
3. Go to **Settings → Pages → Source → main branch → / (root)**
4. Your site will be live at `https://yourusername.github.io/spy-academy/`

---

## Admin Panel

- Visit the site and click **⚙ ADMIN** in the bottom right
- Default password: **`spy123`** — change this immediately in the admin panel
- Add operatives (spy kids) and their code names
- Generate and download individual QR codes for each kid
- Download the 6 activity station QR codes to print and place around your venue
- Reset individual or all progress before/between events

---

## How It Works

### On the day:
1. Open the site on a shared tablet/screen at a central scanning station
2. Each kid scans **their personal QR code** first — the site identifies them
3. They visit activity stations around the venue and scan the **station QR code**
4. A mission briefing video plays automatically
5. Their progress is tracked — completed missions are shown with ✓
6. After all 6 missions: 🏆 banner appears

### QR Code types:
| Type | Scanned by | Effect |
|------|-----------|--------|
| **Operative card** (kid's personal QR) | Kid, at start or scanner | Identifies the active spy |
| **Activity station** (1–6) | Kid, at each station | Plays the mission video |

### Data storage:
All data (kids, progress, settings) is stored in browser `localStorage` — no server needed. Data persists between sessions on the same device/browser. Clear browser data to full reset.

---

## Tips

- **Print QR codes large** — at least 8×8cm for reliable scanning
- **Laminate activity station codes** to survive the event
- Use the **CLEAR OPERATIVE** button between kids if using a shared scanner
- The scanner works best in **good lighting** — avoid backlighting the QR code
- Video files over ~100MB may be slow to load on GitHub Pages — consider compressing to H.264

## Troubleshooting

| Issue | Fix |
|-------|-----|
| Camera won't start | Check browser has camera permission; use HTTPS (GitHub Pages is HTTPS by default) |
| Videos won't play | Ensure files are named `activity1.mp4` exactly; check they're uploaded to `videos/` |
| QR not scanning | More light; hold steady; ensure full code is in frame |
| Lost admin password | Open browser DevTools → Application → Local Storage → delete `spyAcademy` key |
