# Website — context / status

Last updated: 2026-06-13. The "read me first" handoff doc for the Stenumedia site. Shared machine
setup and working rules are in `Projects/ENVIRONMENT.md` and `Projects/CONVENTIONS.md`.

## What this is

The public Stenumedia marketing site — a single static page ("Aim for the Bushes"). Plain
HTML/CSS/JS, no build step, no framework. Hosted on **GitHub Pages** at **stenumedia.com**.

## Repo & branches

- GitHub: `stenumedia/stenumedia.github.io`, checked out at `/Users/asten/Projects/Website`.
- Branch: `main` — this is a user/org Pages repo, so **pushing `main` publishes the live site**. Be deliberate.
- Custom domain pinned by `CNAME` (`stenumedia.com`); don't delete it or Pages drops the domain.

## Current state

Live, single page. Sections: hero (`#work`), expertise (`#expertise`), about/contact (`#about`).

## Architecture / where things live

- `index.html` — the whole page: an editable **`CONTENT` object near the top** (title, nav, hero,
  copy) is rendered into the markup by a small inline script at the bottom (`render CONTENT into the
  page`). Edit copy in `CONTENT`; edit layout in the markup/CSS below it.
- `assets/`, plus `bg.png` and `title.png` — hero/background art (large PNGs).
- `CNAME` — custom domain.

## Build / run / test

No build. Preview locally by opening `index.html`, or `python3 -m http.server` in the folder.

## Deploy / ship

Push to `main` → GitHub Pages publishes to stenumedia.com within a minute. No pipeline.

## Conventions & gotchas

- `main` == production; there's no staging. Preview locally before pushing.
- Keep the `CNAME` file intact.
- Big PNGs are committed directly — keep new art reasonably sized.

## Open items / next

- _(none tracked yet)_
