# Google Search Console – Verification & Sitemap Submission

Site: `https://gdokoutlas-boop.github.io/iptvflick/`
Repo: `gdokoutlas-boop/iptvflick` (branch `main`)

> **You must be signed in to your Google account.** The site-side hooks (verification
> meta tag / HTML file) are already prepared in the repo — you only need to paste
> the code Google gives you and I push it live.

---

## Step 1 – Create the property

1. Go to **https://search.google.com/search-console** and sign in with your Google account.
2. Click **Add property** → choose **URL prefix** (not Domain).
3. Paste: `https://gdokoutlas-boop.github.io/iptvflick/`
4. Click **Continue**.

> ⚠️ If you later connect `iptvflick.com`, add a second property at that time
> (URL prefix `https://iptvflick.com/` or a Domain property).

## Step 2 – Verify ownership (choose ONE method)

### Method A – HTML tag (recommended, no file needed)

1. In Search Console choose **"HTML tag"** as the verification method.
2. Copy the `<meta name="google-site-verification" content="...">` tag it shows.
3. **Paste it here in the chat** — I will insert it into `_includes/head.html`
   (a commented placeholder already exists there), push, and confirm it's live.
4. In Search Console click **Verify**.

### Method B – HTML file

1. In Search Console choose **"HTML file"** method → it offers a download like
   `google1234abcd.html`.
2. **Paste the file's contents here in the chat** (or the exact filename).
3. I add it to the repo root, push — it will be served at
   `https://gdokoutlas-boop.github.io/iptvflick/google1234abcd.html`.
4. Click **Verify**.

## Step 3 – Submit the sitemap

1. In Search Console go to **Sitemaps** (left menu).
2. Enter: `sitemap.xml` (full URL: `https://gdokoutlas-boop.github.io/iptvflick/sitemap.xml`)
3. Click **Submit**.

## Step 4 – Request indexing of the pillar (optional, faster)

1. In Search Console open **URL Inspection** (top search bar).
2. Paste the pillar URL: `https://gdokoutlas-boop.github.io/iptvflick/blog/iptv-sverige-komplett-guide/`
3. Click **Request indexing**. Do the same for the homepage and 1–2 other articles.

## Step 5 – Confirm status

- Sitemaps page should show "Success" and an increasing URL count.
- Indexing takes hours to days. Use **URL Inspection** on any article to see
  "URL is on Google" once crawled.

---

## Notes

- `robots.txt` allows all crawlers and points to the sitemap (already live).
- Every page has `index, follow` robots meta, a canonical URL, and the sitemap
  lists all 9 URLs (homepage, blog, 7 articles). No blockers found.
- GitHub Pages site is public, so Google can crawl it immediately.
