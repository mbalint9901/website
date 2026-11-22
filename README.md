# balintmazzag.com

Personal site

## Structure

```
├── index.html           Home (bio + links)
├── projects.html        Portfolio of projects
├── publications.html    Publications list (static HTML, edited by hand)
├── sitemap.xml          Submitted to Google Search Console
├── robots.txt
├── cv/                  Balint_Mazzag_CV.tex (source) + .pdf (linked from the home page)
├── assets/
│   ├── css/styles.css
│   └── images/          logo.png, portrait.jpg (also the social preview image)
├── LICENSE
└── .gitignore
```

## CV

Source and published PDF both live in `cv/`. Rebuild with:

```
cd cv && latexmk -pdf Balint_Mazzag_CV.tex && latexmk -c
```

## Publications

The list in `publications.html` is curated by hand, not generated, so it can show author lists
(with my name in bold), sections and DOI links. Add new entries by copying a `pub-row` block;
the formatting rules are in the HTML comment at the top of the list. Update `lastmod` in
`sitemap.xml` when the page changes.

## Design notes

- Typography: **Cardo** (headings) + **Inter** (body) - matches WordPress's Twenty Twenty-Four default theme, for visual consistency with the blog at blog.balintmazzag.com
