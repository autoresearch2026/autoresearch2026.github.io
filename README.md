# AutoResearch 2026 Workshop Website

Source for the **AutoResearch 2026** workshop site: *Workshop on End-to-End Autonomous Scientific Research with Robot and AI Scientists* @ NeurIPS 2026.

It is a plain static site (HTML + CSS + vanilla JS), so GitHub Pages serves it directly with no build step.

## Live site

Because the repository is named `autoresearch2026.github.io`, GitHub Pages publishes it at:

> https://autoresearch2026.github.io/

Enable it once under **Settings -> Pages -> Build and deployment -> Source: Deploy from a branch**, branch `main`, folder `/ (root)`.

## Structure

```
.
├── index.html            # the whole single-page site
├── assets/
│   ├── css/style.css      # all styling (CSS variables at the top)
│   └── js/main.js         # mobile menu + active-section highlight
├── images/
│   ├── speakers/          # speaker headshots (add NAME.jpg here)
│   └── organizers/        # organizer headshots
├── .nojekyll              # tell GitHub Pages to skip Jekyll
└── README.md
```

## How to fill in content

Open `index.html` and search for the section you want to edit. Each section is marked with an HTML comment (for example `<!-- ===== SPEAKERS ===== -->`).

- **Speakers / Organizers / Advisory Board:** each grid currently shows "To be announced" placeholder cards. Inside each grid there is a commented `TEMPLATE` block. Copy it once per real person, then delete the placeholder `person-tba` cards. Put headshots in `images/speakers/` or `images/organizers/` and point the `src` at them.
- **Important dates / Schedule / OpenReview link:** update the text directly; dates are marked *tentative* until the NeurIPS 2026 calendar is fixed.
- **Colors / fonts:** edit the CSS variables in the `:root { ... }` block at the top of `assets/css/style.css`.

## Local preview

Just open `index.html` in a browser, or run a tiny server:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```
