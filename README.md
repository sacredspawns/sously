# sously — public documentation site

This repo hosts the public-facing documentation for the
[Sously](https://play.google.com/store/apps/details?id=com.sacredspawns.sously)
Android app — a privacy policy and account deletion page that Google Play
Console and end users link to.

The site is served by **GitHub Pages** straight from `main` branch root,
no build step required.

## Live URLs

Once deployed:

- `https://sacredspawns.github.io/sously/` — landing page
- `https://sacredspawns.github.io/sously/privacy/` — privacy policy
- `https://sacredspawns.github.io/sously/delete-account/` — account deletion instructions

These exact URLs are referenced from:
- The in-app `marketing/privacy-policy.md` cross-link in the Sously app source
- Play Console → Data safety → Account deletion URL field
- Play Console → Store listing → Privacy policy URL field

If the URLs change (rename the repo, switch to a custom domain), update
those three references too.

## One-time setup

Push this folder to a new GitHub repo named `sously` under the
`sacredspawns` org/user account, then enable Pages:

```bash
cd /path/to/sously-public-docs
git init
git remote add origin git@github.com:sacredspawns/sously.git
git add -A
git commit -m "Initial public docs site"
git branch -M main
git push -u origin main
```

Then in the GitHub repo:

1. **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main` / `/ (root)`
4. **Save**

Pages takes ~60 seconds to publish. You'll see the live URL in the same
Pages settings panel once it's ready.

## Updating docs

Edit the markdown files, commit, push. Pages re-deploys automatically
within a minute. The "Last updated" line in `privacy.md` should be bumped
manually whenever the policy materially changes — Google Play and users
look at it.

## Files

- `index.md` — landing page
- `privacy.md` — privacy policy (mirrors `marketing/privacy-policy.md` in
  the app repo; keep them in sync if you edit either)
- `delete-account.md` — account deletion explainer + email fallback
- `_config.yml` — Jekyll/Pages config (theme, title)
