# ET · The Electronics Engineering Project

An interactive guide for electronics students. It opens on a 3D silicon wafer, zooms into one MOSFET, and the transistor's three terminals open the three tracks: **Source → Analog**, **Gate → Digital**, **Drain → Embedded**.

## What's in this folder

| File | What it is | Do you edit it? |
|---|---|---|
| `content.json` | Every word on the site: home text, primers, career and general guides | Yes, through Pages CMS |
| `.pages.yml` | Tells Pages CMS how to show `content.json` as forms | Only to add new fields |
| `index.html` | The site itself: 3D scenes, layout, styles | Ask Claude for design changes |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are | No |

## Editing content

1. Go to **app.pagescms.org** and sign in with GitHub.
2. Install the Pages CMS GitHub App on your account when asked, and give it access to this repository.
3. Open this repository and choose **ET content**.
4. Open a track (Analog, Digital or Embedded), then its **Primer**, **Career** or **General** list.
5. Edit, then **Save**. Pages CMS commits the change to GitHub and the live site updates within a minute or two.

### Adding a new guide

Open **Career** or **General** in a track and add an entry. Give it:

- a unique **ID** (lowercase, hyphens, no spaces, e.g. `gate-prep`)
- **Status** `ready` once it has content, or `soon` to show it as coming soon

### Primers

Each primer has a **Show the draft note** switch. Turn it off once you've rewritten the primer in your own words.

## Previewing on your computer

Opening `index.html` by double-clicking won't load `content.json`, because browsers block that for local files. From this folder, run:

```
python3 -m http.server 8000
```

Then open http://localhost:8000.
