# chainesh.github.io

My academic website, built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll template (MIT licence).
Most of the setup is already done. You only need the steps below.

## Where everything lives

| What                     | File                                                     |
| ------------------------ | -------------------------------------------------------- |
| Bio on the home page     | `_pages/about.md`                                        |
| Photo                    | `assets/img/prof_pic.jpg`                                |
| Publications             | `_bibliography/papers.bib`                               |
| News items               | `_news/announcement_*.md` (one file per item)            |
| Projects                 | `_projects/*.md`                                         |
| CV page                  | `_data/cv.yml`, plus your PDF at `assets/pdf/cv.pdf`     |
| Email / GitHub / Scholar | `_data/socials.yml`                                      |
| Site name, URL, settings | `_config.yml`                                            |

## Fill in before publishing

Everything comes from your CV, apart from these:

1. **`assets/img/prof_pic.jpg`**: replace it with your photo (square, about 600×600). It's a "CG" placeholder for now.
2. **`_data/socials.yml`**: uncomment `scholar_userid` and add your Google Scholar ID.
3. **`_news/`**: the months are approximate for the NeurIPS, RLC, AAMAS, RLDM and IBM items. Correct them if you know the exact dates.
4. **`assets/pdf/cv.pdf`**: whenever you update your CV, replace this file too.

## Publish on GitHub Pages (free, at https://chainesh.github.io)

1. On GitHub, create a new **public** repository named exactly `Chainesh.github.io`. Leave it empty, with no README.
2. Run these commands in Terminal:

   ```bash
   cd ~/Desktop/chainesh_website
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/Chainesh/Chainesh.github.io.git
   git push -u origin main
   ```

3. In the repo, go to **Settings → Actions → General → Workflow permissions**. Choose **Read and write permissions** and save.
4. Go to the **Actions** tab. The "Deploy site" workflow builds the site in about 3–5 minutes and pushes the result to a `gh-pages` branch. If it ran before you changed the permission in step 3, re-run it.
5. Go to **Settings → Pages → Build and deployment**. Set the source to **Deploy from a branch**, choose `gh-pages` and `/ (root)`, then save.

The site will be live at https://chainesh.github.io a minute later. After that, every `git push` rebuilds it automatically.

## Preview on your Mac (optional)

This needs Ruby 3.3 or newer. You can install it with `brew install ruby`.

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
