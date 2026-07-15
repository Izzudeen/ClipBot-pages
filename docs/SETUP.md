# Getting these pages live on GitHub Pages

You need a public URL for the Privacy Policy and Terms of Service (and this
same site can double as your OAuth redirect landing page). Here's the
fastest path:

## 1. Create a repo

- Go to github.com → New repository
- Name it whatever you like, e.g. `clipbot-pages`
- Public repo (GitHub Pages on the free tier requires public, unless you
  have GitHub Pro/Team)

## 2. Upload the files

Easiest way without touching git commands:
- On the repo page, click **Add file → Upload files**
- Drag in `index.html`, `privacy.html`, and `terms.html`
- Commit directly to `main`

(Or if you're comfortable with git: `git add . && git commit -m "site" && git push`)

## 3. Turn on Pages

- Repo → **Settings → Pages**
- Under **Build and deployment → Source**, choose **Deploy from a branch**
- Branch: `main`, folder: `/ (root)`
- Save

GitHub will give you a URL like:

```
https://yourusername.github.io/clipbot-pages/
```

It usually takes 1–2 minutes to go live the first time.

## 4. Your three URLs for TikTok's form

```
Privacy Policy:    https://yourusername.github.io/clipbot-pages/privacy.html
Terms of Service:  https://yourusername.github.io/clipbot-pages/terms.html
```

## 5. Using this same site as your OAuth redirect URI

You can also point your TikTok app's **Redirect URI** at this same domain,
e.g.:

```
https://yourusername.github.io/clipbot-pages/index.html
```

When TikTok redirects back here after you approve the OAuth consent screen,
the page will just show your normal landing page — but the `code=...` value
you need will still be sitting right there in the browser's address bar for
you to copy. That's all you need it for.
