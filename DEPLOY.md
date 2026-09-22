# Deploying your portfolio

You have two versions:
- `index.html` — clean version
- `animated.html` — same site with a boot-sequence intro, scroll-reveal animations, animated stat counters, a pulsing circuit background, and cursor-glow on project cards

Pick one as your live site (rename it to `index.html` if you go with the animated version — hosts serve `index.html` by default).

---

## Option A — GitHub Pages (free, recommended)

1. Create a new repo on GitHub, e.g. `aman-portfolio`.
2. On your machine, in the folder with your file(s):

```bash
git init
git add index.html
git commit -m "Add portfolio site"
git branch -M main
git remote add origin https://github.com/ga2495/aman-portfolio.git
git push -u origin main
```

3. On GitHub: go to your repo → **Settings** → **Pages** → under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)` → **Save**.
4. Your site goes live in a minute or two at:
   `https://ga2495.github.io/aman-portfolio/`

To update later: edit the file, then

```bash
git add index.html
git commit -m "Update site"
git push
```

---

## Option B — Netlify (free, drag-and-drop, no git needed)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag your `index.html` file (or a folder containing it) onto the page.
3. Netlify gives you a live URL instantly (e.g. `random-name-123.netlify.app`).
4. Optional: in **Site settings → Domain management**, add a custom domain or change the subdomain to something like `aman-gupta.netlify.app`.

---

## Option C — Vercel

```bash
npm install -g vercel
cd path/to/your/site
vercel
```

Follow the prompts (link/create a project, accept defaults). Vercel prints a live URL when it's done. Run `vercel --prod` to push to your production URL.

---

## Using a custom domain (any option above)

If you buy a domain (e.g. from Namecheap or Google Domains):
- **GitHub Pages**: add a `CNAME` file to the repo containing just your domain name, then point your domain's DNS `A` records to GitHub's IPs (185.199.108.153, .109.153, .110.153, .111.153), or a `CNAME` record to `ga2495.github.io` for a subdomain.
- **Netlify/Vercel**: add the domain in the dashboard under Domain settings — they'll give you the exact DNS records to add.

---

## Before you deploy — quick checklist

- [ ] Double-check the email, phone, and LinkedIn/GitHub links in the contact section are correct
- [ ] If your individual projects have separate GitHub repos, send me the links and I'll wire up "View code" buttons on each project card
- [ ] Test on your phone once it's live — resize your browser first to catch any layout issues
