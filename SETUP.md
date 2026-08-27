# Getting your site live on GitHub Pages

Browser only — no git, no terminal, no installs. About 10 minutes.

---

## 1. Create the repository

1. Sign in at [github.com](https://github.com). If you don't have an account, make one — **choose your username carefully**, it becomes part of your web address. Something like `bassemsourour` is ideal.
2. Click the **+** in the top right → **New repository**.
3. Name it exactly: **`YOUR-USERNAME.github.io`**

   This exact name is what makes GitHub host it as your main site. If your username is `bassemsourour`, the repo must be named `bassemsourour.github.io`.
4. Set it to **Public**. (Required for free GitHub Pages, and you want it public anyway — the guide says no login can be required to read your report.)
5. Leave "Add a README" **unchecked**.
6. Click **Create repository**.

## 2. Upload the files

1. On the empty repo page, click **uploading an existing file**.
2. Drag in these three files:
   - `index.html`
   - `work-term-1.html`
   - `styles.css`
3. Scroll down, click **Commit changes**.

## 3. Turn on Pages

1. Go to the repo's **Settings** tab → **Pages** in the left sidebar.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set the branch to **`main`** and the folder to **`/ (root)`**. Click **Save**.
4. Wait 1–2 minutes. Your site is live at:

   **`https://YOUR-USERNAME.github.io`**

First deploy sometimes takes a few minutes. If you get a 404, wait and refresh.

---

## 4. Editing your text

You do not need to download anything. To change any text:

1. Click the file in your repo (e.g. `work-term-1.html`).
2. Click the **pencil icon** (top right of the file view).
3. Edit directly in the browser. Everything you need to change is marked
   `[in square brackets]`, with an `<!-- EDIT ME -->` comment above it
   explaining what belongs there.
4. Scroll down → **Commit changes**.
5. Your live site updates in about a minute.

**Tip:** search the page with Ctrl+F / Cmd+F for `[` to jump between the
spots that still need filling in. When there are no square brackets left,
you're done.

---

## 5. Adding your photos

The rubric specifically rewards **original images** — photos you took
yourself. This is one of the clearest differences between the top grade
and the one below it, and it costs you nothing but a few minutes with
your phone.

1. In your repo, click **Add file** → **Create new file**.
2. Type `images/.gitkeep` as the filename and commit. That creates the folder.
3. Now click **Add file** → **Upload files** and drag your photos into it.
4. In the HTML, find an image placeholder block. It looks like this:

   ```html
   <figure class="reveal">
     <div class="img-placeholder">Replace with your own photo…</div>
     <!-- <img src="images/workplace.jpg" alt="Describe the image"> -->
     <figcaption>[Caption]</figcaption>
   </figure>
   ```

5. Delete the `<div class="img-placeholder">…</div>` line, and uncomment
   the `<img>` line by removing `<!--` and `-->`. Point `src` at your
   actual filename.

**Before uploading:** shrink your photos. A raw phone photo is 3–5 MB and
will make your page slow to load. Resize to about 1600px wide and save as
JPEG — it'll look identical and be ~300 KB. [Squoosh](https://squoosh.app)
does this in the browser for free.

**Always fill in the `alt` text.** It describes the image for anyone using
a screen reader, and it's the kind of detail that quietly signals you know
what you're doing.

---

## 6. Before you submit — checklist

- [ ] No `[square brackets]` left anywhere in either file
- [ ] Opened the live URL in a **private/incognito window** to confirm it loads without a login (the guide requires this)
- [ ] Checked it on your phone — the layout should adapt on its own
- [ ] At least 2–3 original photos in place, each with a caption and `alt` text
- [ ] Nothing confidential: no internal URLs, customer data, unreleased products, or credentials visible in screenshots. If unsure, ask your supervisor.
- [ ] Every goal in the Goals section has an honest status, including any you didn't meet
- [ ] Sent the link to Greg

---

## Optional: using your own domain later

If you register `bassemsourour.com`, pointing it here is free:

1. In your repo: **Settings → Pages → Custom domain**, enter the domain, save.
2. At your registrar, add the DNS records GitHub shows you.
3. Tick **Enforce HTTPS** once it's available.

Your GitHub URL keeps working, so nothing breaks.

---

## If something goes wrong

- **404 after enabling Pages** — repo must be Public, and named exactly `YOUR-USERNAME.github.io`. Give it 2–3 minutes.
- **Site loads but looks unstyled** — `styles.css` must sit in the same folder as the HTML files, spelled exactly.
- **Image doesn't show** — filenames are case-sensitive. `Photo.JPG` and `photo.jpg` are different files.
