# Website Workshop
## 🍴 Step 1 — Fork This Repo

Forking creates your own personal copy of this template under your GitHub account.

1. Click the **Fork** button at the top-right of this page
2. Leave all settings as-is and click **Create fork**
3. You now have your own copy at `github.com/YOUR-USERNAME/REPO-NAME` 🎉

---

## ⚙️ Step 2 — Enable GitHub Pages

This makes your site live on the internet.

1. In **your forked repo**, click the **Settings** tab
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Set the branch to **main** and the folder to **/docs**
5. Click **Save**

> ⏱️ Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/` within a minute or two. It won't look like much yet — that's what the rest of the workshop is for!

---

## 💻 Step 3 — Clone Your Repo Locally

Cloning downloads your repo to your computer so you can edit it.

### Option A: VS Code

1. In your forked repo, click the green **Code** button
2. Copy the HTTPS link
3. Open a terminal and run:

```bash
git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
cd REPO-NAME
```

4. Open the folder in VS Code:

```bash
code .
```

### Option B: RStudio

1. In your forked repo, click the green **Code** button and copy the HTTPS link
2. Open RStudio and go to **File → New Project → Version Control → Git**
3. Paste the HTTPS URL into the **Repository URL** field
4. Choose where to save it locally, then click **Create Project**

RStudio will clone the repo and open it as a project automatically.

---

## 👀 Step 4 — Preview Your Site Locally

Before pushing changes to GitHub, preview them instantly on your computer.

### Option A: VS Code

Open a terminal and run:

```bash
quarto preview
```

### Option B: RStudio

Run the same command from RStudio's built-in **Terminal** tab (bottom pane):

```bash
quarto preview
```

Alternatively, if you have the **Quarto** extension installed in RStudio, you can click the **Render** button at the top of any `.qmd` file to preview that page directly.

---

Both options open a live preview in your browser at `http://localhost:XXXX` that auto-refreshes every time you save a file. Press `Ctrl+C` in the terminal to stop the preview.

---

## ✏️ Step 5 — Make It Yours

Open each file and replace the `✏️` placeholders with your real content:

| File | What to update |
|------|---------------|
| `_quarto.yml` | Your name, GitHub username, repo name |
| `index.qmd` | Your name, headline, intro paragraph |
| `aboutme.qmd` | Your photo, bio, resume PDF, contact links |
| `proj.qmd` | Your project titles, descriptions, PDF files |
| `styles.css` | Optional: tweak colors, fonts, spacing |

> 💡 **Tip:** Replace `headshot.jpg` with your own photo — just make sure your file is also named `headshot.jpg`, or update the filename in `index.qmd` and `aboutme.qmd` to match.

---

## 🚀 Step 6 — Build and Deploy

When you're happy with your changes, build the site and push it to GitHub.

### Option A: VS Code

```bash
# 1. Build the site into the docs/ folder
quarto render

# 2. Stage all changed files
git add .

# 3. Commit with a message describing your changes
git commit -m "Update personal info and projects"

# 4. Push to GitHub
git push
```

### Option B: RStudio

1. Run `quarto render` in RStudio's **Terminal** tab to build the `docs/` folder
2. In the **Git pane** (top-right), check the boxes next to all changed files to stage them
3. Click **Commit**, write your commit message, and click **Commit**
4. Click the **Push** (↑) button to push to GitHub

---

GitHub Pages will automatically pick up the new `docs/` folder and update your live site within a minute.

---

## 🐛 Common Issues

**My site isn't showing up on GitHub Pages**
- Make sure you set the source to the `/docs` folder in Settings → Pages (Step 2)
- Make sure you ran `quarto render` before pushing — GitHub Pages serves the built files in `docs/`, not the `.qmd` source files

**My photo / PDF isn't showing up**
- File names are case-sensitive on GitHub. `Headshot.jpg` and `headshot.jpg` are different files. Check that the filename in your `.qmd` exactly matches the actual file.
- Make sure the file is in the same folder as your `.qmd` file (the root of the repo)

**Changes I pushed aren't showing on my live site**
- Make sure you ran `quarto render` to rebuild the `docs/` folder before pushing
- GitHub Pages can take 1–2 minutes to update — try a hard refresh (`Ctrl+Shift+R`)

**`quarto preview` throws an error**
- Make sure Quarto is installed: run `quarto --version` in your terminal
- Make sure you're in the right folder (the one containing `_quarto.yml`)

---

## 📁 File Structure

```
/
├── _quarto.yml         # Site-wide settings and navigation
├── index.qmd           # Homepage
├── aboutme.qmd         # About Me page
├── proj.qmd            # Projects page
├── styles.css          # Custom CSS styles
├── headshot.jpg        # ✏️ Replace with your photo
├── example_resume.pdf  # ✏️ Replace with your resume
├── example_report.pdf  # ✏️ Replace with your project files
└── docs/               # Auto-generated by "quarto render" — don't edit manually
```

---

## 🙋 Help

Stuck? Ask during the workshop, or open an [Issue](../../issues) on this repo.
