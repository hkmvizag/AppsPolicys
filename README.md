# App policies

Privacy policies for the mobile apps published by Srila Prabhupada's Hare
Krishna Movement, Visakhapatnam. Plain static HTML, served by GitHub Pages —
no build step, no dependencies.

Live at **https://hkmvizag.github.io/AppsPolicys/**

| App | Page |
|---|---|
| HKMV Tasks (`com.hkmv.hkmv_tasks`) | https://hkmvizag.github.io/AppsPolicys/app/hkmv-task/privacy-policy/ |

## Layout

```
index.html                               the list of apps
assets/style.css                         shared styling, light and dark
app/<app-slug>/privacy-policy/index.html one app's policy
templates/privacy-policy.html            starting point for the next app
.nojekyll                                serve the files as they are
```

An app's URL is its folder. `app/hkmv-task/privacy-policy/` is served at
`…/app/hkmv-task/privacy-policy/`, so the path is chosen by where the file
sits — nothing else needs changing.

## Adding an app

1. `cp templates/privacy-policy.html app/<app-slug>/privacy-policy/index.html`
2. Replace everything in CAPITALS, and delete the sections that do not apply.
3. Add the app to the list in `index.html`.
4. Commit and push. Pages redeploys in about a minute.

Write it from the app's own code, not from the template's wording. Play checks
the policy against the Data safety form you fill in, and the two disagreeing is
a common reason for a release being rejected.

## Hosting

GitHub Pages, **Settings → Pages → Deploy from a branch → `main` / `(root)`**.

The repository has to be **public** for the pages to be reachable without a
login, which is one of Google's conditions. Nothing here is a secret — these
pages are written to be read by anyone.
