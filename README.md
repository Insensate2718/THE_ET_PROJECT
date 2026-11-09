# ET · The Electronics Engineering Project

An interactive guide for electronics students. It opens on a 3D silicon wafer, zooms into one MOSFET, and the transistor's three terminals open the three tracks: **Source → Analog**, **Gate → Digital**, **Drain → Embedded**.

## What's in this folder

| File | What it is | Do you edit it? |
|---|---|---|
| `content.json` | Every word on the site: home text and each track's sections | Yes, through Pages CMS |
| `.pages.yml` | Tells Pages CMS how to show `content.json` as forms | Only to add new fields |
| `index.html` | The site itself: 3D scenes, layout, styles | Ask Claude for design changes |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are | No |

## Editing content

1. Go to **app.pagescms.org** and sign in with GitHub.
2. Open this repository and choose **ET content**.
3. Open a track (Analog, Digital or Embedded), then **Sections**.
4. Each section (Philosophy, Learning route, Careers) is one page. Write its text in the **Page text** box.
5. **Save**. Pages CMS commits to GitHub and the live site updates within a minute or two.

### Writing page text

The page text uses simple Markdown:

```
## A heading (also appears in the page's side menu)
A normal paragraph.

- a bullet
1. a numbered step
**bold**, *italic*, [link text](https://example.com)
```

### Adding a section

In a track's **Sections**, click **Add**, give it a unique **ID** (lowercase, hyphens, e.g. `projects`), a title and a one-line summary. Sections appear in the order listed. Drag to reorder.

Turn off **Show the draft note** once you've rewritten a section in your own words.

## Previewing on your computer

Opening `index.html` by double-clicking won't load `content.json`, because browsers block that for local files. From this folder, run:

```
python3 -m http.server 8000
```

Then open http://localhost:8000.
