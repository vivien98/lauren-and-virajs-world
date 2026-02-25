# 🌍 Lauren & Viraj's World

An interactive 3D globe where we pin our memories, photos, and stories from around the world.

**Live:** `https://<your-username>.github.io/lauren-and-virajs-world/`

## Features

- **Light stylized globe** with real country outlines (Natural Earth data via TopoJSON) and 48+ city labels
- **Right-click anywhere** on the globe to add a Photo Album, Blog Post, or Quick Note at that exact location
- **Left-click** stops the globe spinning
- **Scroll** to zoom in/out, **drag** to rotate
- **Photo galleries** with lightbox viewer
- **Edit & delete** any memory
- Beautiful warm color palette with Playfair Display typography

## Deploy to GitHub Pages (Free Hosting)

### Quick Setup (5 minutes)

1. **Create a GitHub account** (if you don't have one) at [github.com](https://github.com)

2. **Create a new repository:**
   - Go to [github.com/new](https://github.com/new)
   - Name it `lauren-and-virajs-world`
   - Set it to **Public**
   - Click **Create repository**

3. **Upload the files:**
   - On your new repo page, click **"uploading an existing file"**
   - Drag in `index.html` and `README.md`
   - Click **Commit changes**

4. **Enable GitHub Pages:**
   - Go to **Settings** → **Pages** (in the left sidebar)
   - Under "Source", select **Deploy from a branch**
   - Under "Branch", select **main** and **/ (root)**
   - Click **Save**

5. **Wait 1-2 minutes**, then visit:
   ```
   https://<your-username>.github.io/lauren-and-virajs-world/
   ```

### Using Git (Alternative)

```bash
git init
git add .
git commit -m "Our world together 🌍"
git branch -M main
git remote add origin https://github.com/<your-username>/lauren-and-virajs-world.git
git push -u origin main
```

Then enable GitHub Pages in Settings → Pages.

## Customization

### Adding your own memories

Edit the `pins` array in `index.html` to replace the sample data with your real memories. Each pin looks like:

```javascript
{
  id: 1,
  type: 'blog',        // 'blog', 'album', or 'note'
  title: "Our First Trip",
  location: "Paris, France",
  lat: 48.8566,
  lng: 2.3522,
  date: "March 2023",
  emoji: "💕",
  text: "Your story here...",
  images: ["https://your-image-url.jpg"],
  tags: ["love", "travel"],
  color: "#c2536a"
}
```

### Changing colors

Edit the CSS variables at the top of the `<style>` block:
- `--accent` — primary color (terracotta)
- `--accent2` — secondary (rose)
- `--ocean` / `--land` — globe colors

### Globe style

Change these constants in the JavaScript:
- `OCEAN_COLOR` — ocean fill color
- `LAND_COLOR` — land fill color  
- `LAND_STROKE` — country border color

## Tech Stack

- **Three.js** — 3D rendering
- **TopoJSON / world-atlas** — Real country outlines (Natural Earth data, public domain)
- **Google Fonts** — Playfair Display, DM Sans, Caveat
- Zero build step, zero dependencies to install — just one HTML file!

## License

Made with 💕 by Lauren & Viraj
