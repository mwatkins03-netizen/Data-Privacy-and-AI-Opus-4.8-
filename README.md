# AI & Your Privacy — Interactive Classroom Resources

Two self-contained, interactive web activities that help students understand what happens to their
data when they use AI tools — and how to keep control of it. Created by **Marc Watkins** for classroom use.

| File | What it is |
|------|------------|
| `index.html` | Landing page that lets visitors choose between the two versions |
| `ai-and-privacy.html` | **The Interactive Guide** — a clean, scrollable walkthrough with an animated data-flow diagram |
| `shadow-play.html` | **The Shadow Play** — a rotating lantern carousel students can spin between four themes |

Both activities cover: enterprise-protected accounts (Microsoft Copilot, Google Gemini), turning off
ChatGPT's data harvesting, a "what does the AI know about you?" awareness assignment, and the reframe
dialogue about consent. Students can **save their responses as HTML, PDF, or print** — nothing leaves
the browser until they choose to export it.

---

## Host it on GitHub Pages (free)

### Option A — upload in the browser (no command line)

1. Go to <https://github.com/new> and create a repository, e.g. **`ai-and-privacy`**. Make it **Public**.
2. On the new repo page, click **uploading an existing file**.
3. Drag in **all the files in this folder** — `index.html`, `ai-and-privacy.html`, `shadow-play.html`,
   `.nojekyll`, and this `README.md`. Click **Commit changes**.
4. Go to **Settings → Pages**.
5. Under **Build and deployment → Source**, choose **Deploy from a branch**. Set **Branch** to
   `main` and folder to `/ (root)`. Click **Save**.
6. Wait ~1 minute. Your site appears at:

   ```
   https://<your-username>.github.io/ai-and-privacy/
   ```

   The landing page (`index.html`) loads automatically.

> **Tip:** If the `.nojekyll` file doesn't appear in the upload (browsers sometimes hide dotfiles),
> create it manually: in the repo click **Add file → Create new file**, name it `.nojekyll`, leave it
> empty, and commit. It tells GitHub Pages to serve the files as-is.

### Option B — command line (git)

```bash
cd ai-and-privacy-site
git init
git add .
git commit -m "AI & Your Privacy interactive resources"
git branch -M main
git remote add origin https://github.com/<your-username>/ai-and-privacy.git
git push -u origin main
```

Then enable Pages under **Settings → Pages** as in steps 4–6 above.

---

## Direct links once it's live

- Landing page: `https://<your-username>.github.io/ai-and-privacy/`
- The guide: `…/ai-and-privacy.html`
- The shadow play: `…/shadow-play.html`

You can hand students a direct link to either version, or the landing page so they can pick.

---

## Editing the activities

Each `.html` file is **one standalone file** — open it in any text editor to change wording, links,
or colors. The content lives in clearly labeled data arrays near the top of the `<script>` block
(e.g. `ENTERPRISE`, `OPTOUT`, `READINGS`, `ADVICE`, `THEMES`). No build step or installation needed.

To preview a change locally, just double-click the file to open it in a browser, or run a tiny server
from this folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## A few notes

- **Internet on first open:** the activities load React from a CDN, so the first open needs a
  connection. After that, browsers usually cache it.
- **Privacy:** student responses are stored only in their own browser's local storage until they
  export. Nothing is sent anywhere.
- **Verify your specifics:** statements about enterprise data protection and opt-out steps reflect the
  author's framing for a teaching context. Confirm the details for your institution with your IT/help
  desk, and check the primary sources linked inside each activity, as product menus and agreements change.

---

## Attribution & reuse

Created by **Marc Watkins**, built with the help of an AI assistant (Claude). You're welcome to use and
adapt these resources for educational purposes **with attribution**. A Creative Commons
**CC BY 4.0** license is a good fit if you want to make reuse terms explicit — add a `LICENSE` file if so.
