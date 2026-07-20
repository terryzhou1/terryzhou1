# Personal academic website

A minimal, fast-loading personal site (plain HTML/CSS, no build step),
styled after a classic academic-homepage look, with a header nav for
**Home**, **About**, and **Research** (with your CV linked).

## Files

```
.
├── index.html          # Home page — short intro + headshot
├── about.html           # Longer bio
├── research.html        # Publications list + CV link
├── style.css             # Shared styling for all pages
├── images/
│   └── headshot.jpg      # Placeholder — replace with your photo
├── files/
│   ├── cv.pdf            # Placeholder — replace with your real CV
│   ├── wp1.pdf           # Placeholder working paper
│   ├── paper2.pdf        # Placeholder paper draft
│   └── paper2_slides.pdf # Placeholder slides
└── README.md
```

## 1. Customize the content

Everything is plain text/HTML, so you can edit it directly:

- **Name and title**: replace "Jordan Ellis" and the title/affiliation
  text in the `<title>` tags and body of `index.html`, `about.html`,
  and `research.html`.
- **Bio**: edit the paragraphs in `index.html` and `about.html`.
- **Email / Google Scholar link**: update the byline near the top of
  `index.html` and `research.html`.
- **Publications**: each entry in `research.html` is a `<section
  class="pub">` block — copy/paste one, edit the title, venue, and
  links, and delete the ones you don't need.
- **Photo**: replace `images/headshot.jpg` with your own photo (same
  filename, or update the `src` in `index.html`).
- **CV**: replace `files/cv.pdf` with your actual CV, keeping the
  filename `cv.pdf` (or update the links that point to it).
- **Footer year/name**: update the copyright line at the bottom of
  each page.

## 2. Put it on GitHub Pages

1. Create a new GitHub repository named `<your-username>.github.io`
   (this exact naming makes GitHub serve it at the root domain).
2. Upload all the files in this folder to the root of that repository
   (via the GitHub web UI "Add file → Upload files", or with git):
   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**, and under
   **Build and deployment → Source**, choose **Deploy from a branch**,
   then select the `main` branch and `/ (root)` folder. Save.
4. After a minute or two, your site will be live at
   `https://<your-username>.github.io`.

If you'd rather host it as a project page instead of your main user
page (e.g. `https://<your-username>.github.io/my-site/`), you can use
any repository name — GitHub Pages will just serve it from a
subpath instead of the root.

## 3. Local preview (optional)

Since there's no build step, you can just open `index.html` in a
browser. For a closer-to-production preview with relative links
working from a local server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
