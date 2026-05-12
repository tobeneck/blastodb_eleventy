# BlastoDB — Static Site Generator

A simple **Markdown-to-HTML** builder for BlastoDB.  
Microbiologists write `.md` files; the builder produces a complete website.

---

## ⚡ Quick Start

This project uses **Eleventy (11ty)** to build the website from Markdown files.

```bash
# Install dependencies
npm install

# Start development server (with live reload)
npm run serve

# Build for production
npm run build
```

The generated website will be in the `output/` folder, ready to deploy to GitHub Pages or any hosting platform.

---

## 📖 Documentation

For complete documentation on editing pages, adding content, and customizing the design, see **[README_11ty.md](README_11ty.md)**.

**Key topics:**
- ✏️ How to create and edit pages
- 📝 Markdown syntax and custom elements (buttons, tags, cards, hero sections, etc.)
- 🎨 Customizing design and colors
- 📦 Deploying to GitHub Pages, Netlify, or other platforms

---

## 📁 Project Structure

```
blastodb/
├── content/                    ← Your pages (one .md file per page)
│   ├── index.md
│   ├── about.md
│   ├── subtypes.md
│   └── ...
├── _includes/
│   └── layouts/
│       └── base.njk            ← Main HTML template
├── assets/
│   ├── style.css               ← Website styling
│   └── main.js                 ← Mobile navigation script
├── lib/
│   └── parser.js               ← Custom markdown parser
├── .eleventy.js                ← 11ty configuration
├── nav.json                    ← Navigation menu configuration
└── output/                     ← Generated website (do not edit)
```

---

## 🎯 For Microbiologists

You **only** need to edit Markdown files in the `content/` folder:

1. Open a `.md` file in any text editor
2. Edit the content using Markdown syntax
3. Save the file
4. The website will automatically rebuild (if using `npm run serve`)

No HTML, no coding required! 🎉

---

## 💡 Example Page Structure

All pages start with **frontmatter** (YAML metadata), followed by your content:

```markdown
---
layout: layouts/base.njk
title: BlastoDB — My Page
description: Short description for search engines.
---

# My Page Title

Your content here using **Markdown** and custom elements like [btn: Click Me -> page.html] or [tag: Important].
```

---

## 🛠️ For Developers

The custom Markdown parser supports:
- ✅ Standard Markdown (headings, paragraphs, links, images, lists, bold, italic, code)
- ✅ Custom syntax for BlastoDB elements:
  - `[btn: Label -> url]` — Primary buttons
  - `[tag: Label]` — Highlighted tags
  - `[nav-box: Label -> url]` — Navigation boxes
  - `[start:hero] ... [end:hero]` — Full-width hero sections
  - `[start:card] ... [end:card]` — Card containers
  - `[start:box] ... [end:box]` — Plain boxes
  - `[start:cols] ... [end:cols]` — Two-column layouts
  - `[start:grid] ... [end:grid]` — Grid layouts

---

## 📦 Deployment

### GitHub Pages

1. Push to GitHub
2. Set up GitHub Actions (see [README_11ty.md](README_11ty.md) for details)
3. Automatic deployment on every push!

### Netlify

1. Connect your GitHub repo to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `output`

### Other Platforms

Run `npm run build` and upload the `output/` folder to your server.

---

## 🔧 Requirements

- **Node.js** (v14 or later)
- **npm** (comes with Node.js)

---

## 📚 Further Reading

- **Eleventy Documentation**: https://www.11ty.dev/
- **Markdown Guide**: https://www.markdownguide.org/
- **Complete Guide**: See [README_11ty.md](README_11ty.md)

---

**Built with ❤️ for microbiologists, by developers.**

This project was migrated from a custom Node.js builder to **Eleventy (11ty)** for better maintainability, easier deployment, and a larger supporting community.
