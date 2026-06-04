# VijitLabs Blog: How to Publish a Post

## Every time you publish, follow these 4 steps.

---

## Step 1: Create the Post File

Go to:
```
C:\Users\Shaarika\Documents\VijitLabs_Website\_posts\
```

Create a new text file. Name it in this exact format:
```
YYYY-MM-DD-your-post-slug.md
```

Examples:
```
2026-06-15-how-escalationai-reduces-churn.md
2026-06-22-linkedin-prospecting-mistakes.md
```

Rules for the filename:
- Date must match the post date
- Slug is lowercase, words separated by hyphens, no spaces
- Must end in .md

---

## Step 2: Add the Front Matter

Every post starts with this block. Copy it, fill in your details.

```
---
layout: post
title: "Your Full Post Title Here"
subtitle: "One sentence description shown under the title"
date: 2026-06-15
category: Sales Tools
slug: your-post-slug
cta_title: "Try SalesScraper Pro"
cta_text: "One line about what the reader should do next."
cta_url: "https://sspro.vijit.in"
cta_button: "Get SalesScraper Pro"
---
```

Available categories:
- Sales Tools
- Customer Support
- AI Products
- Founder Updates

To skip the CTA box at the bottom, delete the cta lines entirely.

---

## Step 3: Write the Post Content

Write your content below the closing `---`. Use plain text with markdown formatting.

| What you want | What to type |
|---|---|
| Heading | `## Your Heading` |
| Subheading | `### Your Subheading` |
| Bold text | `**bold text**` |
| New paragraph | Leave a blank line between paragraphs |
| Bullet list | Start lines with `- ` |
| Link | `[link text](https://url.com)` |
| Horizontal rule | `---` |

No em dashes. No jargon. Write like you are explaining to a smart colleague.

---

## Step 4: Push to GitHub

Open PowerShell and run these three commands:

```powershell
cd "C:\Users\Shaarika\Documents\VijitLabs_Website"
git add .
git commit -m "New post: your post title here"
git push origin master
```

Vercel auto-deploys in about 30 seconds.

Your post will be live at:
```
https://vijitlabs.com/blog/your-post-slug/
```

---

## Quick Checklist Before Pushing

- [ ] File is in the `_posts` folder
- [ ] Filename format is `YYYY-MM-DD-slug.md`
- [ ] Front matter starts and ends with `---`
- [ ] Date in front matter matches filename date
- [ ] Category is one of the four listed above
- [ ] No em dashes in the content

---

## Full Post Template (Copy This Every Time)

```
---
layout: post
title: "Your Title Here"
subtitle: "Your subtitle here"
date: 2026-06-15
category: Sales Tools
slug: your-post-slug
cta_title: "Try SalesScraper Pro"
cta_text: "Install the extension and run it on a LinkedIn profile."
cta_url: "https://sspro.vijit.in"
cta_button: "Get SalesScraper Pro"
---

Opening paragraph. Start with the reader's problem, not the product.

## First Section Heading

Your content here. Keep paragraphs short. Two to three sentences each.

## Second Section Heading

More content here.

---

Closing paragraph with one specific action for the reader.
```

---

## Blog URL Reference

| Page | URL |
|---|---|
| Blog listing | vijitlabs.com/blog/ |
| Individual post | vijitlabs.com/blog/your-post-slug/ |
| RSS feed | vijitlabs.com/feed.xml |
