# Maribo Showcase

A responsive, dark purple script showcase website. No package installation, backend, or build command required.

## Put it on GitHub and Netlify

1. Unzip the download. Upload the **contents** of `maribo-showcase` to the root of your GitHub repository. `index.html` should be at the repository root.
2. In Netlify, import that GitHub repository as a new project.
3. Leave the build command empty. Set the publish directory to `.` (the included `netlify.toml` already sets this).
4. Deploy. Future commits to your connected branch update the website.

## Add your Discord

Open `config.js` and set `discordInvite` to your actual HTTPS Discord invite. All three Discord links update automatically. An empty invite displays an honest coming-soon notice.

## Add videos

Edit the `showcases` array in `config.js`. Each object creates one card. Copy an object to add another showcase; give each a unique `id`.

- `title`: card and player title.
- `category`: generates a filter automatically.
- `description`: short description below the card.
- `video`: a YouTube watch, Shorts, or share URL; a relative MP4 path; or a direct HTTPS MP4 URL.
- `poster`: optional thumbnail image path or HTTPS image URL. Leave empty for the designed abstract placeholder.
- `duration`: visible text such as `02:34` (enter your actual duration).
- `label`: small label over the thumbnail.
- `accent`: `purple`, `blue`, or `pink`.
- `featuredId`: the ID to feature at the top.

Example:

```js
{ id: "my-script", title: "My script", category: "Features",
  description: "A quick look at my latest release.", label: "FULL SHOWCASE",
  duration: "02:34", video: "assets/videos/my-script.mp4",
  poster: "assets/my-thumbnail.jpg", accent: "purple" }
```

Put your MP4 files in `assets/videos/`. For large videos, YouTube or external video hosting keeps your GitHub repository small. Files over GitHub's normal upload limits should use external hosting. Videos must use codecs browsers support (H.264 video with AAC audio is a common choice). Other websites' ordinary page URLs are not direct video files.

This is a public static site: configuration and videos are publicly accessible. It does not include an admin upload dashboard. Add videos by editing `config.js` and committing the changes.

## Preview locally

Open `index.html` directly, or run `python -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Branding

Change `MARIBO` in `index.html`, the page title and description, and the footer to rename the site. Colors and layouts are in `styles.css`. Typography loads Google Fonts with local sans-serif fallbacks. Demo entries are clearly marked as video slots; no footage or live Discord invite is included.
