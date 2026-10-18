# Daniel Salkinder's website

A plain static website with no build step, dependencies, or hosting-specific code. You can move these same files to any static web host or attach a custom domain later.

## Add PDFs

PDFs live under `pdfs/Math 1200/`. The pages currently use these files:

| Website link | File |
| --- | --- |
| Partial Derivatives and Optimization | `Coaching/Problems - Math 1200 Coaching Session 1.pdf` |
| Preview Session 1: Trigonometry | `Review Sessions/Review Session 1.pdf` |
| Preview Session 2: Parametric Equations | `Review Sessions/Review Session 2.pdf` |
| Preview Session 3: Optimization | `Review Sessions/Review Session 3.pdf` |
| Exam 1 Study Guide | `Study Guides/Exam 1 Recall.pdf` |

Solutions is plain, disabled text until its file is available. To enable one, replace its `<span>` with an `<a href="...">` pointing to the new PDF. Paths are relative to the HTML file; encode spaces as `%20` in links. You can keep your own filenames and folder structure.

## Edit content

- `index.html`: homepage, email, and office hours.
- `math1200.html`: calculus coaching materials.
- `study-guides.html`: study guide materials.
- `style.css`: shared minimal styling.

All local links are relative so the site also works under a GitHub Pages repository subpath.

## Host on GitHub Pages

1. Create a GitHub repository. For a main personal site, name it `YOUR-USERNAME.github.io`; another repository name also works.
2. Upload this folder's contents to the repository root, including the `pdfs/` folder and `.nojekyll`.
3. In the repository's **Settings → Pages**, select **Deploy from a branch**, then select your branch (usually `main`) and **/ (root)**, and save.
4. After deployment completes, GitHub shows the site address. A personal-site repository uses `https://YOUR-USERNAME.github.io/`; other repositories use `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

To publish later changes or PDFs, upload or commit them to the same branch.

## Preview locally

Open `index.html` in your browser, or run `python3 -m http.server 8000` from this folder and visit `http://localhost:8000`.
