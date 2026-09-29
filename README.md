# Blake Wood Ink — Static Site

Fully static, no build needed. Deploy directly to Vercel, GitHub Pages, or any web host.

## Quick start

1. Unzip this folder
2. Add your tattoo photos to `/work/` (JPG or PNG)
3. Update the email in `booking.html` if needed
4. Drag the entire folder into [Vercel](https://vercel.com)

That's it. The site is live.

## Editing copy

- **Home page**: Edit `index.html`
- **Work page**: Edit `work.html` (add photos in `/work/` folder)
- **About page**: Edit `about.html`
- **Booking page**: Edit `booking.html`
- **Blog home**: Edit `blog/index.html`

## Adding blog posts

Create a new `.html` file in the `/blog/` folder. Use one of the existing posts as a template:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Your Title | Blake Wood Ink</title>
  <meta name="description" content="One line about this post." />
  <link rel="icon" href="/_assets/favicon.svg" type="image/svg+xml" />
  <link href="https://fonts.googleapis.com/css2?family=Bodoni+Moda:opsz,wght@6..96,400;6..96,500&family=Hanken+Grotesk:wght@400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="/_assets/style.css" />
</head>
<body>
  <a class="skip" href="#main">Skip to content</a>
  
  <header class="site-header">
    <div class="wrap">
      <a class="wordmark" href="/">Blake Wood Ink</a>
      <nav class="nav" aria-label="Main">
        <a href="/work.html">Work</a>
        <a href="/blog/" aria-current="page">Blog</a>
        <a href="/about.html">About</a>
        <a href="/booking.html">Book</a>
      </nav>
    </div>
  </header>

  <main id="main">
    <article class="article wrap">
      <header>
        <h1>Your Title</h1>
        <p class="meta"><time datetime="2026-09-26">September 26, 2026</time></p>
      </header>
      <div class="body">
        <!-- Your post content here -->
        <p>Start writing...</p>
      </div>
      <a class="back" href="/blog/">Back to the blog</a>
    </article>
  </main>

  <footer class="site-footer">
    <div class="wrap">
      <p>Blake Wood Ink, Toronto. By appointment only.</p>
      <p>
        <a href="https://instagram.com/blakewoodink">Instagram</a>
        &nbsp;&nbsp;<a href="mailto:hello@blakewoodink.com">Email</a>
        &nbsp;&nbsp;© 2026
      </p>
    </div>
  </footer>
</body>
</html>
```

Then add a link to it in `/blog/index.html` at the top of the post list.

## Adding photos to work

1. Save a JPG or PNG to the `/work/` folder
2. Edit `work.html` and `index.html`
3. Replace one of the placeholders with an `<img>` tag:

```html
<figure>
  <img src="/work/my-photo.jpg" alt="Description of the tattoo" />
  <figcaption>Where it goes, style</figcaption>
</figure>
```

## Styling

All styles are in `/_assets/style.css`. The color tokens are at the top:

- `--paper`: Background
- `--ink`: Text
- `--stencil`: Accent (the violet)
- `--muted`: Secondary text

Editing these changes the whole site. Dark mode is built in and respects the system setting.

## Deploy to Vercel

1. Open [vercel.com](https://vercel.com)
2. Click "Add New" → "Project"
3. Upload this folder (or connect a GitHub repo)
4. Vercel will deploy it instantly

No configuration needed. Every time you change a file and re-upload, Vercel updates the site.

## Use your own domain

In Vercel project settings, add your domain under "Domains" and follow the steps to point your DNS there.
