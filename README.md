# Personal website

This site uses plain HTML and CSS. Edit the files directly; no framework or build step is needed.

## Update the homepage

Edit `index.html` to update the profile, concise technical focus terms and CV link. Detailed experience and education live in `assets/resume.pdf`.

The Projects, Blog and Papers sections and their matching homepage navigation links are commented out separately. When a section has content, remove its empty-state paragraph and uncomment both the section and its navigation link. Keep HTML comments at a single level; never nest `<!-- ... -->` comments.

- **Projects:** Add an `<article>` with an `<h3>` title linking to the project and a short `<p>` description.
- **Blog:** Add an `<article>` with a linked title, a publication date in `<time datetime="YYYY-MM-DD">` and a short description. For a full post, create `posts/<slug>.html` and include a return link to `../index.html#blog`.
- **Papers:** Add only real papers, with a linked title, authors and publication details. Include PDF or code links when available.

`projects.html` and `photography.html` remain placeholders for direct URLs and are unlinked from live navigation. The Photography link opens Instagram. Add content to a standalone page before restoring its navigation link.

Example blog entry (replace the placeholders before publishing):

```html
<article>
  <h3><a href="posts/your-post-slug.html">Your post title</a></h3>
  <time datetime="YYYY-MM-DD">Publication date</time>
  <p>A short description of the post.</p>
</article>
```

## Contact form emails

`contact.html` POSTs to `https://formsubmit.co/sunnyjoshi1401@gmail.com`, routing submissions to **sunnyjoshi1401@gmail.com** through [FormSubmit](https://formsubmit.co/). No account registration is required, but first use requires email activation.

1. Open the published contact page, or start the local server below and open <http://localhost:8000/contact.html>. Submit the form once and complete the provider's CAPTCHA.
2. Find FormSubmit's activation email in **sunnyjoshi1401@gmail.com** (check spam too) and click its confirmation link.
3. Submit a second test through the contact page and confirm that the message reaches the inbox. The HTML configuration alone does not verify activation or delivery.

The hidden `_subject` field sets **New message from sunny1401.github.io**. The visitor's `email` field supplies Reply-To. FormSubmit's default CAPTCHA and thank-you page remain enabled.

## Preview locally

From the repository directory, run:

```sh
python3 -m http.server 8000
```

Open <http://localhost:8000> in your browser. Check the page at desktop and mobile widths and follow any new links. Stop the server with `Ctrl+C`.
