# yigitalpunal.com

Personal site of **Yigit Alp Unal** — Senior Backend Engineer & Project Lead.
Nine years building production banking systems: SWIFT and SEPA payments, daily
reconciliation, Oracle PL/SQL, Kafka. Author of
[rawthink-mcp](https://github.com/ygtalp/rawthink-mcp), an open-source MCP server.

Live at **[yigitalpunal.com](https://yigitalpunal.com)** · Hosted on GitHub Pages.

---

## Stack

Single static `index.html`. No framework, no build step, no dependencies.
Fonts load from Google Fonts; everything else is inline.

- **Sans:** [Inter](https://rsms.me/inter/) (400/500/600/700)
- **Mono:** [JetBrains Mono](https://www.jetbrains.com/lp/mono/) (400/500/600)
- **Icons:** inline SVG (no icon library)

---

## Repository layout

Every file below lives at the repository root, alongside `index.html`.

```
index.html              the entire site (HTML + CSS + SVG icons)
avatar.jpg              profile photo, square crop
og-image.png            1200x630 link preview card
favicon.ico             legacy browsers
favicon.svg             modern browsers, scalable
favicon-16x16.png
favicon-32x32.png
apple-touch-icon.png    180x180, iOS home screen
CNAME                   custom domain for GitHub Pages
README.md
```

---

## Deploying

GitHub Pages serves the root of the `main` branch. Commit and push; the site
updates within a minute or two.

```bash
git add .
git commit -m "Update site"
git push
```

`CNAME` must stay at the root or the custom domain breaks.

### After deploying

| What | Where | Why |
| --- | --- | --- |
| Link preview card | [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/) | LinkedIn caches preview images. Run the inspector to refresh it. |
| Structured data | [Google Rich Results Test](https://search.google.com/test/rich-results) | Validates the `schema.org/Person` JSON-LD. |
| Favicon | Browser tab | Hard refresh (`Ctrl+Shift+R`) if the old icon persists. |

---

## What's in the `<head>`

- **Open Graph + Twitter Card** — controls the preview card when the link is
  shared on LinkedIn, Slack, WhatsApp, or X. Points at `og-image.png`.
- **`schema.org/Person` JSON-LD** — tells search engines that the GitHub,
  LinkedIn, dev.to, X, and PyPI profiles all belong to the same person, and
  what that person works on (payments, ISO 20022, Kafka, MCP, and so on).
- **Canonical URL** — `https://yigitalpunal.com/`
- **Favicon set** — one file per platform convention.

Regenerating `og-image.png`: it is a plain 1200×630 PNG. Keep those dimensions.
`og:image:alt` in `index.html` should match whatever the card says.

---

## Editing notes

A few things that are easy to get wrong:

- **`.hero` needs `flex-direction:row`.** Without it, the later
  `section{ flex-direction:column }` rule applies and the avatar drops below
  the text.
- **Avatar shape** is one line: `border-radius` in `.avatar`.
  `50%` = circle, `12px` = rounded square (current), `0` = square.
- **Type scale** is driven by `html{ font-size }`. Every size is in `rem`, so
  changing that one value scales the whole page.
- **`mailto:` links deliberately have no `target="_blank"`** — it opens an empty
  tab in most browsers. External links all carry `rel="noopener"`.

---

## Credits

The layout is based on **[dillionverma/portfolio](https://github.com/dillionverma/portfolio)**
by Dillion Verma ([Magic UI](https://magicui.design/)), released under the MIT
License. This version is a hand-written static rewrite: no Next.js, no Tailwind,
no shadcn/ui — just the structure and the restraint.

Fonts are licensed under the SIL Open Font License:
[Inter](https://github.com/rsms/inter) (Rasmus Andersson),
[JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) (JetBrains).

---

## License

Code: MIT. Content, copy, and photography: © Yigit Alp Unal, all rights reserved.
