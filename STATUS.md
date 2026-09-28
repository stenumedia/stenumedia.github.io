# Website — context / status

Last updated: 2026-09-24. Handoff notes for the Stenumedia marketing site.

## What this is

The public Stenumedia marketing site — a single static page ("Aim for the Bushes"). Plain
HTML/CSS/JS, no build step and no framework. Hosted on **GitHub Pages** at **stenumedia.com**.

## Repo & deploy

- GitHub: `stenumedia/stenumedia.github.io`
- Branch: `main` — pushing `main` publishes the live site.
- `CNAME` contains the custom domain. Keep this file intact.

## Main files

- `index.html` — page layout, CSS, editable text in the `CONTENT` object near the top, and the renderer.
- `projects.js` — simple project data file. Add/edit projects here; no HTML changes are needed.
- `assets/projects/` — put project images here.
- `assets/stenumedia-logo.svg` — primary logo used in the header, contact section and footer.
- `assets/stenumedia-logo.png` — PNG copy of the logo.
- `assets/title.png` and `assets/bg.png` — original "Aim for the Bushes" title and hero artwork.
- `CNAME` — custom domain for GitHub Pages.

## Adding a project

1. Put the image in `assets/projects/`.
2. Open `projects.js`.
3. Add one object inside the `PROJECTS` array:

```js
{
  image: "assets/projects/my-project.jpg",
  title: "My Project",
  text: "A short description of the project.",
  category: "games",
  bgColor: "#f57e2e"
},
```

`category` must be one of:

- `games`
- `tech`
- `consumer`
- `solutions`

Projects are automatically grouped underneath the matching business-area card. The text colour is
chosen automatically for readable contrast against the supplied `bgColor`.

## Editing ordinary site copy

The `CONTENT` object is near the top of `index.html`. It contains the hero copy, navigation,
business-area labels, about copy, contact information and footer copy.

## Preview

No build step is required. Either open `index.html` directly or run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy

Preview locally first, then push to `main`. GitHub Pages should update shortly afterwards.
