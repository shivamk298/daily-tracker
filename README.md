# 📅 Shivam's Daily Routine Tracker

A personal interactive daily routine planner with activity tracking, history log, and streak counter — built as a single `index.html` file, powered by `localStorage`.

## ✨ Features

- **Interactive checkboxes** for Exercise, Library I & II, Sports, and Night slot
- **Study / Movie toggle** for the night session — choose each day
- **Optional daily remark** — auto-saved as you type
- **History tab** with a full activity log, study hours bar chart, and remarks
- **Stats** — daily study hours, tasks done, current streak, tonight's plan
- **Best streak** counter across all logged days
- **Persistent storage** via `localStorage` — no backend needed

## 🚀 Deploy to GitHub Pages (3 steps)

### 1. Create a new repository
Go to [github.com/new](https://github.com/new) and create a repo named e.g. `daily-tracker`. Keep it **public**.

### 2. Upload `index.html`
Either:
- Drag and drop `index.html` into the repo on the GitHub website, or
- Clone the repo and push:

```bash
git clone https://github.com/YOUR_USERNAME/daily-tracker.git
cd daily-tracker
cp /path/to/index.html .
git add index.html
git commit -m "Add daily routine tracker"
git push
```

### 3. Enable GitHub Pages
1. Go to **Settings → Pages**
2. Under *Source*, select **Deploy from a branch**
3. Choose **main** branch, **/ (root)** folder
4. Click **Save**

Your tracker will be live at:
```
https://YOUR_USERNAME.github.io/daily-tracker/
```

> **Note:** Data is stored in your browser's `localStorage` — it stays on your device and is not synced across devices or browsers.

## 📁 Structure

```
index.html    ← the entire app (HTML + CSS + JS, no dependencies)
README.md     ← this file
```

## 🗂 Data Format

Each day is stored as a JSON object under the key `shivam_routine_v1`:

```json
{
  "2026-05-28": {
    "date": "2026-05-28",
    "exercise": true,
    "library1": false,
    "library2": true,
    "sports": true,
    "nightMode": "study",
    "nightDone": true,
    "remark": "Great focus day!",
    "savedAt": 1748390400000
  }
}
```

Max study hours per day: **9.5h** (Library I: 3h + Library II: 3h + Night Study: 3.5h)
