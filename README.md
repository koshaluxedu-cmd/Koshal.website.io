# Your Portfolio — Quick Guide

## Files

- `index.html` — your main portfolio (the homepage)
- `work-helio.html` — case study template (duplicate this for each project)

## How to customize

### Change text content
Open the HTML files in any code editor (VS Code, Sublime, even Notepad). All text is plain — search for "Your name", "hello@yourname.com", project titles, etc. Replace and save.

### Change colors
Open `index.html`. Near the top of `<style>` you'll see `:root { --bg: #ede5d3; ... }`. Change the values:
- `--bg` — page background (cream)
- `--ink` — main text color (near-black)
- `--accent` — terracotta highlight color
- `--bg-soft` — slightly darker section background

### Change fonts
Replace the Google Fonts `<link>` at the top with whatever fonts you prefer. Then update `--serif` and `--sans` in the CSS variables.

### Add real project images
The project images are CSS gradients right now (placeholders). To use real images:

1. Create a folder called `images/` in the same directory as your HTML
2. Drop your images in there
3. Find the `.work__slide--01 .work__slide-img-inner` rule in CSS and replace the `background:` line with:
   ```
   background: url('images/your-image.jpg') center/cover no-repeat;
   ```
4. Repeat for `--02`, `--03`, `--04`

Same approach for the hero portrait — find `.hero__visual-img` and replace the gradient.

### Add another case study page
1. Copy `work-helio.html` and rename it (e.g. `work-ember.html`)
2. Open the new file and update the title, project name, content, metrics
3. In `index.html`, find the project that should link to it and update `href="work-helio.html"` to `href="work-ember.html"`

## How to deploy (free)

1. Sign up at **netlify.com** (or vercel.com, or cloudflare pages)
2. Drag the entire folder containing your HTML files into the deploy zone
3. You get a live URL like `your-name.netlify.app` in 30 seconds
4. Optional: buy a custom domain (~$10/year) and point it at your site

## Preview limitation

When viewing this in the chat artifact preview, only the homepage will render. Project links won't navigate (they need a real server). Once you deploy, all links work.
