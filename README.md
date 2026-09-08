# Personal website

This site uses plain HTML and CSS. Edit the files directly; no framework or build step is needed.

## Update the homepage

Edit `index.html` to update the profile, CV download, experience and education. Add new work to the sections with IDs `projects`, `blog` and `papers`. Remove a section's empty-state paragraph when you add its first item.

- **Projects:** Add an `<article>` with an `<h3>` title linking to the project and a short `<p>` description. `projects.html` currently shows `[under dev]`; update that page too when you want a separate project listing.
- **Blog:** Add an `<article>` with a linked title, a publication date in `<time datetime="YYYY-MM-DD">` and a short description. For a full post, create `posts/<slug>.html` and include a return link to `../index.html#blog`.
- **Papers:** Add only real papers, with a linked title, authors and publication details. Include PDF or code links when available.

Example blog entry (replace the placeholders before publishing):

```html
<article>
  <h3><a href="posts/your-post-slug.html">Your post title</a></h3>
  <time datetime="YYYY-MM-DD">Publication date</time>
  <p>A short description of the post.</p>
</article>
```

## Preview locally

From the repository directory, run:

```sh
python3 -m http.server 8000
```

Open <http://localhost:8000> in your browser. Check the page at desktop and mobile widths and follow any new links. Stop the server with `Ctrl+C`.
