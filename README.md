# IPTV Sverige – Complete Jekyll Site (GitHub Pages Ready)

SEO content cluster + full blog site for **https://iptvflick.com/** targeting **"IPTV Sverige"** (Swedish) / **"IPTV Sweden"** (international variant).

This folder **is the site** – a complete Jekyll project. Copy its contents into a GitHub repo, push, and GitHub Pages builds it automatically.

## 📁 Site structure

```
.
├── _config.yml          # Site config (title, SEO, plugins, permalinks)
├── Gemfile              # Local build deps (github-pages gem)
├── index.html           # Homepage: hero + pillar + satellite cards
├── blog/index.html      # Blog listing page
├── _posts/              # 7 articles (pillar + 6 satellites)
│   ├── 2026-08-01-iptv-sverige-komplett-guide.md       ← PILLAR
│   ├── 2026-08-01-ar-iptv-lagligt-i-sverige.md
│   ├── 2026-08-01-basta-iptv-leverantorer-sverige.md
│   ├── 2026-08-01-installera-iptv-smart-tv-fire-tv.md
│   ├── 2026-08-01-iptv-svenska-kanaler.md
│   ├── 2026-08-01-vanliga-iptv-problem-losningar.md
│   └── 2026-08-01-iptv-gratis-test-billigt.md
├── _layouts/            # default, post, page
├── _includes/           # head (SEO), header, footer
├── assets/css/style.css # Styling
├── 404.html
├── robots.txt
├── sitemap.xml          # Generated automatically by jekyll-sitemap
├── feed.xml             # Generated automatically by jekyll-feed
├── cluster-plan.md      # (documentation – excluded from build)
└── README.md            # (this file – excluded from build)
```

## 🚀 Publish in 3 steps

### 1. Create the repo

- **Option A – user site:** repo named `<your-username>.github.io` → URL: `https://<your-username>.github.io/`
- **Option B – project site:** any repo name → URL: `https://<your-username>.github.io/<repo-name>/` → set `baseurl: "/<repo-name>"` in `_config.yml`

### 2. Copy files & push

```bash
git init
git add .
git commit -m "Add IPTV Sverige SEO blog"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

### 3. Enable Pages

**Repo → Settings → Pages** → *Source: Deploy from a branch* → `main` / `/ (root)` → Save.

Done. Your site is live at the URL above within ~1–2 minutes. The `sitemap.xml` and RSS `feed.xml` are generated automatically by the Jekyll plugins in `_config.yml`.

## 🌐 Pointing to your own domain

In `_config.yml` set:
- `url: "https://iptvflick.com"` (your real domain)
- `baseurl: ""` (empty for root/custom domain)

Then in your domain DNS provider, add a `CNAME` record pointing `www` → `<your-username>.github.io` and a root redirect, and add a `CNAME` file with your domain in the repo root. The canonical/OG/sitemap URLs will use your domain automatically.

## 💻 Local preview (optional, needs Ruby)

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000
```

## 🔗 Internal linking (already wired)

| Link | Count |
|---|---|
| Satellites → pillar | 6 (all satellites link to `/blog/iptv-sverige-komplett-guide/`) |
| Pillar → satellites | 6 (all) |
| iptvflick.com recommendations | 2–4× per article |
| Broken links | 0 (validated) |

> ⚠️ Internal links are written as `{{ site.baseurl }}/blog/<slug>/` (Liquid), so they automatically adapt to the site's base URL. If you later change the `baseurl` in `_config.yml`, links keep working with no edits needed.

## ✅ SEO checklist (already applied to every article)

- Keyword in H1 + first 100 words
- Meta title/description in frontmatter (30–60 / 120–160 chars)
- FAQ block with People-Also-Ask questions
- E-E-A-T signals (author, dates, transparent legality section)
- Citability blocks (`<!-- citability-block -->`) for AI search engines
- Open Graph + Twitter meta tags via `_includes/head.html`
- Automatic XML sitemap + RSS feed
