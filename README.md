# Portfolio — Setup & Deploy Guide

## What's in here
- `index.html` — the whole site (single scrolling page: Hero, Profile, Projects, Experience, Contact)
- `style.css` — all styling, no build step needed

## 1. Personalize the content
Open `index.html` in any text editor and replace:
- The `#` placeholders in the **LinkedIn** and **GitHub** links (Contact section, and nav if you add it)
- The `href="#"` under the RFM/K-Means project card → your actual GitHub repo URL for that project
- The `k=TBD` chip → the actual number of clusters you settled on
- Add a second, third project card by copying the `<article class="project-card">...</article>` block

## 2. Put your project code on GitHub too
Your portfolio should link OUT to real repos. For the RFM/K-Means project:
1. Create a new repo, e.g. `rfm-kmeans-segmentation`
2. Push your notebook/script + a short `README.md` explaining the dataset, method, and findings
3. Copy that repo's URL into the project card link on your portfolio

## 3. Deploy on GitHub Pages
1. Create a repo named exactly `<your-github-username>.github.io`
2. Upload `index.html` and `style.css` to the root of that repo
   - Web UI: "Add file" → "Upload files" → drag both files in → Commit
   - Or via git: `git add . && git commit -m "portfolio" && git push`
3. Go to repo **Settings → Pages**
4. Under "Build and deployment", set **Source: Deploy from a branch**, **Branch: main / (root)**
5. Wait ~1–2 minutes, then visit `https://<your-github-username>.github.io`

## 4. Keep it current
Every time you finish a new analysis — a SQL project, an A/B test writeup, a second clustering
exercise — duplicate a project card, fill it in, commit, push. This is meant to grow alongside your
Python skills, not be a one-time artifact.

## Design notes
- Fonts: Fraunces (headings), IBM Plex Sans (body), IBM Plex Mono (data/metric labels) — loaded from Google Fonts, no local files needed
- Colors and type scale are set as CSS variables at the top of `style.css` if you want to adjust the palette later
- Fully responsive down to mobile; no JavaScript, so nothing to break
