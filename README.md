# Yigit Alpunal - Developer Portfolio

Personal portfolio website showcasing projects in AI, fintech, and blockchain.

## Live Site
🌐 [yigitalpunal.com](https://yigitalpunal.com)

## Features
- **Projects Timeline**: Chronological showcase of personal development projects
- **Coding Books Library**: Technical books that have influenced my growth
- **Tools & Applications**: Development tools and frameworks I use
- **Markdown Blog**: Thoughts and tutorials with client-side rendering
- **SEO Optimized**: Complete meta tags, structured data, and social media cards
- **Responsive Design**: Optimized for mobile, tablet, and desktop

## Technology Stack
- HTML5, CSS3, JavaScript (ES6+)
- marked.js (Markdown parsing)
- Prism.js (Syntax highlighting)
- GitHub Pages (Hosting)
- JSON (Blog data structure)

## Local Development

Simply open `index.html` in your browser. No build process required.

## Project Structure

```
├── index.html              # Main portfolio page
├── blog/
│   ├── posts/              # Markdown blog posts
│   └── blog-index.json     # Blog post catalog
├── assets/                 # Images and static assets
├── CNAME                   # Custom domain configuration
├── robots.txt              # SEO crawler instructions
├── sitemap.xml             # Site structure for search engines
├── claude.md               # Project documentation
└── session_log/            # Development session logs
```

## Adding Blog Posts

### 1. Create Markdown File

Create a new file in `blog/posts/` with the format `YYYY-MM-DD-slug.md`:

```markdown
---
title: "Your Post Title"
date: 2026-01-28
author: "Yigit Alpunal"
tags: ["tag1", "tag2"]
excerpt: "Brief description"
slug: "your-slug"
---

# Content here...
```

### 2. Update Blog Index

Add an entry to `blog/blog-index.json`:

```json
{
  "slug": "your-slug",
  "title": "Your Post Title",
  "date": "2026-01-28",
  "author": "Yigit Alpunal",
  "tags": ["tag1", "tag2"],
  "excerpt": "Brief description",
  "file": "blog/posts/2026-01-28-your-slug.md"
}
```

### 3. Commit and Push

```bash
git add blog/posts/2026-01-28-your-slug.md blog/blog-index.json
git commit -m "Add blog post: Your Post Title"
git push origin main
```

GitHub Pages will automatically deploy your changes in 1-2 minutes.

## SEO Features

- **Meta Tags**: Title, description, keywords, canonical URL
- **Open Graph**: Social media previews for LinkedIn/Facebook
- **Twitter Cards**: Enhanced Twitter link previews
- **Structured Data**: JSON-LD schema for search engines
- **Google Analytics**: Visitor tracking (configure with your ID)
- **Sitemap & Robots**: Search engine optimization

## GitHub Pages Setup

1. Go to repository Settings → Pages
2. Source: Deploy from branch `main` / `root`
3. Custom domain: `yigitalpunal.com`
4. Enforce HTTPS: ✓

## Custom Domain Configuration

### DNS Settings

At your domain registrar:

```
Type: A
Host: @
Values:
  185.199.108.153
  185.199.109.153
  185.199.110.153
  185.199.111.153

Type: CNAME
Host: www
Value: yourusername.github.io
```

DNS propagation takes 24-48 hours.

## Updating Google Analytics

Replace `G-XXXXXXXXXX` in `index.html` with your Google Analytics 4 Measurement ID.

## Contact

- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [yourprofile](https://linkedin.com/in/yourprofile)

## License

© 2026 Yigit Alpunal. All rights reserved.
