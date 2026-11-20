# balintmazzag.com

Personal site

## Structure

```
├── index.html           Home (bio + links)
├── projects.html        Portfolio of projects
├── publications.html    Publications list (static HTML, edited by hand)
├── sitemap.xml          Submitted to Google Search Console
├── robots.txt
├── assets/
│   ├── css/styles.css
│   ├── cv/Balint_Mazzag_CV.pdf
│   └── images/          logo.png, portrait.jpg (also the social preview image)
├── LICENSE
└── .gitignore
```

## CV

Source is `cv/Balint_Mazzag_CV.tex`. Rebuild and publish with:

```
cd cv && latexmk -pdf Balint_Mazzag_CV.tex && latexmk -c && mv Balint_Mazzag_CV.pdf ../assets/cv/
```

## Publications

The list in `publications.html` is curated by hand, not generated, so it can show author lists
(with my name in bold), sections and DOI links. Add new entries by copying a `pub-row` block;
the formatting rules are in the HTML comment at the top of the list. Update `lastmod` in
`sitemap.xml` when the page changes.

## Design notes

- Typography: **Cardo** (headings) + **Inter** (body) - matches WordPress's Twenty Twenty-Four default theme, for visual consistency with the blog at blog.balintmazzag.com
