# Vijit Labs Blog Setup (Jekyll)

## What This Does
Adds a Jekyll-powered blog to vijitlabs.com. Posts are written in markdown. GitHub builds and deploys automatically on every push.

---

## One-Time Setup (Do This Once)

### Step 1: Copy these files into your repo

Add all files from this package into your `vijitlabs-website` repo root, maintaining the folder structure:

```
_layouts/
  post.html
_includes/
  head.html
  nav.html
  footer.html
_posts/
  2026-06-04-salescraperpro-chrome-extension.md
blog/
  index.html
.github/
  workflows/
    jekyll.yml
_config.yml
Gemfile
```

Your existing `index.html`, `logo-icon.png`, `logo-full.png`, `robots.txt`, and `sitemap.xml` stay exactly where they are. Do not move or rename them.

---

### Step 2: Update index.html to add Blog to the nav

Find this line in your existing `index.html`:

```html
<a href="/#about">About</a>
```

Add a Blog link before it:

```html
<a href="/blog/">Blog</a>
<a href="/#about">About</a>
```

---

### Step 3: Enable GitHub Pages with GitHub Actions

1. Go to your repo on GitHub
2. Click **Settings** tab
3. Click **Pages** in the left sidebar
4. Under "Source", select **GitHub Actions**
5. Save

---

### Step 4: Push to master

Commit and push all the new files. GitHub Actions will run the Jekyll build automatically. Your blog will be live at:

```
https://vijitlabs.com/blog/
```

---

## Writing a New Blog Post

Every post is a markdown file in the `_posts/` folder.

**File naming format (required):**
```
YYYY-MM-DD-post-slug.md
```

Example: `2026-06-15-how-escalationai-reduces-churn.md`

**Post front matter (copy this template):**

```markdown
---
layout: post
title: "Your Post Title Here"
subtitle: "Optional one-line description shown under title"
date: 2026-06-15
category: Customer Support
slug: your-post-slug
cta_title: "Try EscalationAI"
cta_text: "See how EscalationAI scores escalation risk inside Zendesk."
cta_url: "https://escalationai.vijit.in"
cta_button: "View EscalationAI"
---

Your post content starts here in markdown...
```

**Available categories:**
- Sales Tools
- Customer Support
- AI Products
- Founder Updates

If you omit `cta_title`, `cta_text`, `cta_url`, the CTA box at the bottom of the post will not appear.

---

## Cross-Publishing to pm.vijit.in (Blogger)

Manual process for now (takes 5 minutes per post):

1. Copy the markdown content of the post
2. Log into Blogger
3. Create a new post, paste content
4. Add a line at the top: *Originally published at [vijitlabs.com/blog](https://vijitlabs.com/blog/)*
5. Publish

Once you are publishing consistently (say, 6 or more posts), set up Zapier to watch the RSS feed at `https://vijitlabs.com/feed.xml` and auto-create Blogger drafts.

---

## File Structure Reference

```
vijitlabs-website/
├── index.html              (your existing homepage, unchanged)
├── logo-icon.png           (unchanged)
├── logo-full.png           (unchanged)
├── robots.txt              (unchanged)
├── sitemap.xml             (unchanged)
├── _config.yml             (NEW - Jekyll config)
├── Gemfile                 (NEW - Ruby dependencies)
├── _layouts/
│   └── post.html           (NEW - blog post template)
├── _includes/
│   ├── head.html           (NEW - shared head/styles)
│   ├── nav.html            (NEW - shared navigation)
│   └── footer.html         (NEW - shared footer)
├── _posts/
│   └── 2026-06-04-salescraperpro-chrome-extension.md  (NEW - first post)
├── blog/
│   └── index.html          (NEW - blog listing page)
└── .github/
    └── workflows/
        └── jekyll.yml      (NEW - auto build and deploy)
```
