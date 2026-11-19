# gforghieri.github.io

Personal site: one static page, no framework, no build step, no JavaScript.

```
index.html                 the whole site (inline CSS)
404.html                   not-found page
assets/profile.webp        photo, 192×192
Giuliano_Forghieri_CV.pdf  public CV (no relocation note, no client-specific security details)
.nojekyll                  tells GitHub Pages to serve files as-is
```

## Deploy

GitHub Pages → **Settings → Pages → Build and deployment → Deploy from a branch → `master` / `(root)`**.
Every push to `master` is live within a minute.

## Update the CV PDF

The PDF comes from the private `gfo-resume` repo:

```bash
cd ../gfo-resume && ./build-public.sh ../gforghieri.github.io/Giuliano_Forghieri_CV.pdf
```

Keep `index.html` in sync with `tailored/Giuliano_Forghieri_CV.yaml` when the CV changes.
