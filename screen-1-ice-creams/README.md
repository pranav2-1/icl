Deployment instructions — Ice Cream Labs TV pages

This folder contains two public HTML pages for demonstration:

- icecream-slideshow.html  — fullscreen slideshow (served at `/`)
- icecream-menu-v1-saved.html — saved blue-theme page (served at `/saved`)

I added `vercel.json` to route `/` → `icecream-slideshow.html` and `/saved` → `icecream-menu-v1-saved.html`.

Two ways to publish:

1) Push to GitHub and import to Vercel (recommended)

  # initialize git (if not already)
  git init
  git add .
  git commit -m "Add ICL TV pages for Vercel"

  # create a GitHub repo (via website or `gh` CLI)
  # using gh CLI (optional):
  gh repo create my-icl-tv --public --source=. --remote=origin --push

  # then in Vercel dashboard: Import Project → select the GitHub repo → Deploy

2) Deploy directly from your machine with Vercel CLI

  # install (if needed)
  npm i -g vercel
  vercel login
  vercel --prod

Notes:
- The site is static; no build step is required.
- After deployment, `/` will show the slideshow. Visit `/saved` to view the saved backup page.
- If you want me to push to GitHub and trigger the Vercel import, I can do that if you provide repo details or grant access.
